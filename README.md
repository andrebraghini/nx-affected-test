# nx-affected-test

This is an example that simulates the case bwlow:

[nx affected:apps fails with error fatal: Not a valid object name master](https://github.com/nrwl/nx/issues/2170)

## Steps

1. This project was generated using [Nx](https://nx.dev) cli: `npx create-nx-workspace@latest myworkspace`

2. After that I created the [./github/workflows/nodejs.yml](./github/workflows/nodejs.yml#L21) file for Github Actions with the command `npm run affected:apps` that calls `nx affected:apps`.

3. Then I created a new branch `new-branch-example` and push to the server.

* The [master action](https://github.com/DedoxBR/nx-affected-test/runs/467941766?check_suite_focus=true) worked normally but the [branch action](https://github.com/DedoxBR/nx-affected-test/runs/467947195?check_suite_focus=true) doesn't.

* It fails with error: `fatal: Not a valid object name master`
