# Repro for issue 6828

## Steps to reproduce

1. Create a branch `some-changes`
2. Create PR
   - GitHub actions will automatically create a preview site
3. Open preview site
4. Click "Click me" button
5. An error is raised

```
Firebase: Error (auth/unauthorized-domain).
```

6. Switch to `main` branch
7. Update `firebase-hosting-pull-request.yml` to use `firebase-tools` v13.3.1
8. Commit changes and push to `main`
9. Create a new branch `some-changes-2`
10. Create PR
    - GitHub actions will automatically create a preview site
11. Open preview site
12. Click "Click me" button
13. Sign in with Google working as expected

## Notes

See the ff PRs:<br>
https://github.com/aalej/issues-6828/pull/2<br>
https://github.com/aalej/issues-6828/pull/1
