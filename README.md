# Ideas

- [ ] Have suede support symlinks, which are resolved in the `release` branch
- [ ] Customize suede to be able to support branches other than `release` 
  - Helpful for monorepo to support several languages, but have a single test bed environment
- [ ] Markdown inclusion parser that uses `template` tag with `data` attributes:
  - unexpanded
```md
# Title

Check this out:

<template data-src="./example.md" />
```
  - expanded
```md
# Title

Check this out:

<template data-src="./example.md">
 
## Some title

Hi!!

</template>
```
