# Ideas

- [x] ~~Have suede support symlinks, which are resolved in the `release` branch~~ _These actually wouldn't work* since pushes to release would be to the file, and then wouldn't be easily resolvable to their destination file. With some extra work, I guess it would be possible to (1) unsymlink the file, apply the changes, re-follow the symlink, and make the target file look like the state of the release file. Seems like a little too much magic though!_
- [ ] Customize suede to be able to support branches other than `release` 
  - Helpful for monorepo to support several languages, but have a single test bed environment
  - Maybe would work with a `.suede` file at the root of the repo?
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
- inline
- Hello <template data-src="./example.md">**world**</template>
- variables
- ```Hello <template data-var="question" />```

```md
<template id="tutor" data-match="tutor*" data-prefix="Tutor: \n" data-suffix="" />

<template id="user" data-match="user*" data-prefix="User: \n" data-suffix="" />

<template data-delimiter=" " data-src="./user* ./tutor*" data-wrapper="tutor user" data-sort="created" data-order="desc" data-limit="10" />
```
