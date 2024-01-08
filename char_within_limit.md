```mermaid
gantt
title CI
dateFormat  HH:mm:ss
axisFormat  %H:%M:%S
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
section check-dist
Waiting for a runner (6s) :active, job2-0, 00:00:18, 6s
Set up job (2s) :job2-1, after job2-0, 2s
Build k1LoW/octocov-action@v0 (4s) :job2-2, after job2-1, 4s
Run actions/checkout@v4 (1s) :job2-3, after job2-2, 1s
Run /./.github/actions/setup-deno-with-cache (7s) :job2-4, after job2-3, 7s
Rebuild the dist/ directory (7s) :job2-5, after job2-4, 7s
Upload dist for post job (0s) :job2-6, after job2-5, 0s
Create dist/*.js size json (0s) :job2-7, after job2-6, 0s
Create dummy coverage (0s) :job2-8, after job2-7, 0s
Run k1LoW/octocov-action@v0 (5s) :job2-9, after job2-8, 5s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job2-10, after job2-9, 0s
Post Run actions/checkout@v4 (0s) :job2-11, after job2-10, 0s
Complete job (0s) :job2-12, after job2-11, 0s
section run_self
Waiting for a runner (6s) :active, job3-0, 00:00:57, 6s
Set up job (1s) :job3-1, after job3-0, 1s
Download bundled dist (1s) :job3-2, after job3-1, 1s
Run self action (0s) :job3-3, after job3-2, 0s
section test
Waiting for a runner (6s) :active, job0-0, 00:00:18, 6s
Set up job (0s) :job0-1, after job0-0, 0s
Run actions/checkout@v4 (0s) :job0-2, after job0-1, 0s
Run /./.github/actions/setup-deno-with-cache (4s) :job0-3, after job0-2, 4s
Run deno test (10s) :job0-4, after job0-3, 10s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job0-5, after job0-4, 0s
Post Run actions/checkout@v4 (0s) :job0-6, after job0-5, 0s
Complete job (0s) :job0-7, after job0-6, 0s
section check
Waiting for a runner (5s) :active, job1-0, 00:00:18, 5s
Set up job (0s) :job1-1, after job1-0, 0s
Run actions/checkout@v4 (0s) :job1-2, after job1-1, 0s
Run /./.github/actions/setup-deno-with-cache (3s) :job1-3, after job1-2, 3s
Run deno fmt --check (4s) :job1-4, after job1-3, 4s
Run deno lint (0s) :job1-5, after job1-4, 0s
Post Run /./.github/actions/setup-deno-with-cache (0s) :job1-6, after job1-5, 0s
Post Run actions/checkout@v4 (0s) :job1-7, after job1-6, 0s
Complete job (0s) :job1-8, after job1-7, 0s
```
