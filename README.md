# Bench Test Speed Apache Vs NGINX

The results of a series of [ApacheBench](https://httpd.apache.org/docs/2.4/programs/ab.html) tests comparing request speeds of Apache to NGINX.

## Technologies Used:

- [ApacheBench](https://httpd.apache.org/docs/2.4/programs/ab.html)
- Debian 9
- Apache 2.4
- Nginx 1.10.3

## Method:

Used [ApacheBench](https://httpd.apache.org/docs/2.4/programs/ab.html) to run 3 iterations each of 100 concurrent requests repeated 10 times, on 3 different resources (small HTML file, medium JavaScript file, large CSS file). Example of command used:

`ab -c 100 -n 10 http://IP_ADDRESS:80/css/full_sparkle.css;`

## Results:

On average, across all requests types (small/medium/large), **NGINX is 11.3% faster than Apache.**

## Tests:

### Resource 1: /login (2.12 kb)

<br/>

**Apache** (avg time per request 228.405 ms):

Requests per second: 337.28 [#/sec] (mean)
Time per request: 296.486 [ms] (mean)

Requests per second: 499.86 [#/sec] (mean)
Time per request: 200.058 [ms] (mean)

Requests per second: 530.02 [#/sec] (mean)
Time per request: 188.671 [ms] (mean)

<br/>

**NGINX** (avg time per request 198.6 ms) (29.8 ms faster, 13.0%):

Requests per second: 452.56 [#/sec] (mean)
Time per request: 220.967 [ms] (mean)

Requests per second: 471.53 [#/sec] (mean)
Time per request: 212.076 [ms] (mean)

Requests per second: 614.47 [#/sec] (mean)
Time per request: 162.743 [ms] (mean)

<br/>

### Resource 2: /js/full_sparkle.js (210 kb)

<br/>

**Apache** (avg time per request 710.7 ms):

Requests per second: 122.77 [#/sec] (mean)
Time per request: 814.515 [ms] (mean)

Requests per second: 158.48 [#/sec] (mean)
Time per request: 630.987 [ms] (mean)

Requests per second: 145.65 [#/sec] (mean)
Time per request: 686.554 [ms] (mean)

<br/>

**NGINX** (avg time per request 661.1 ms) (49.6 ms faster, 7.0%):

Requests per second: 145.03 [#/sec] (mean)
Time per request: 689.503 [ms] (mean)

Requests per second: 144.57 [#/sec] (mean)
Time per request: 691.688 [ms] (mean)

Requests per second: 166.11 [#/sec] (mean)
Time per request: 602.028 [ms] (mean)

<br/>

### Resource 3: /css/full_sparkle.css (707 kb)

<br/>

**Apache** (avg time per request 2537.1 ms):

Requests per second: 32.15 [#/sec] (mean)
Time per request: 3110.595 [ms] (mean)

Requests per second: 43.43 [#/sec] (mean)
Time per request: 2302.707 [ms] (mean)

Requests per second: 45.50 [#/sec] (mean)
Time per request: 2197.987 [ms] (mean)

<br/>

**NGINX** (avg time per request 2186.7 ms) (350.4 ms faster, 13.8%):

Requests per second: 40.17 [#/sec] (mean)
Time per request: 2489.555 [ms] (mean)

Requests per second: 48.17 [#/sec] (mean)
Time per request: 2075.969 [ms] (mean)

Requests per second: 50.14 [#/sec] (mean)
Time per request: 1994.575 [ms] (mean)

<br />

**Total average**: (13.0% + 7.0% + 13.8%) / 3 = 11.3%

### NGINX is on average 11.3% faster than Apache.
