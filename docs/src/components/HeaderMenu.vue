<template lang="pug">
div
  q-btn-dropdown.text-bold(:align="align", flat, no-caps, stretch, :label="`v${$q.version}`", auto-close)
    q-list(dense padding)
      q-item-label(header) Older docs
      q-item(
        v-for="version in ['17', '16', '15', '14', '13']"
        :key="version"
        clickable
        tag="a"
        :href="`https://v0-${version}.quasar-framework.org/`"
        target="_blank"
      )
        q-item-section {{ `v0.${version}` }}

  q-btn-dropdown.text-bold(:align="align", flat, no-caps, stretch, label="Links", auto-close)
    q-list(dense padding)
      q-item(clickable, tag="a", href="https://github.com/quasarframework/quasar-awesome", target="_blank")
        q-item-section.text-yellow-9(avatar)
          q-icon(name="flare")
        q-item-section Awesome Quasar

      q-item(clickable, tag="a", href="https://blog.quasar.dev", target="_blank")
        q-item-section.text-primary(avatar)
          q-icon(name="fab fa-medium")
        q-item-section Quasar Blog

      q-item(clickable, tag="a", href="https://github.com/quasarframework/quasar", target="_blank")
        q-item-section(avatar)
          q-icon(name="fab fa-github")
        q-item-section GitHub

      q-item-label.q-mt-md(header) Quick Tools

      q-item(clickable, to="/style/theme-builder")
        q-item-section.text-teal(avatar)
          q-icon(name="style")
        q-item-section Theme Builder

      q-item(clickable, tag="a", href="/layout-builder", target="_blank")
        q-item-section.text-primary(avatar)
          q-icon(name="dashboard")
        q-item-section Layout Builder

      q-item-label.q-mt-md(header) Playground

      q-item(clickable, tag="a", href="https://codepen.quasar.dev", target="_blank")
        q-item-section.text-brown-5(avatar)
          q-icon(name="fab fa-codepen")
        q-item-section Codepen

      q-item(clickable, tag="a", href="https://jsfiddle.quasar.dev", target="_blank")
        q-item-section.text-primary(avatar)
          q-icon(name="fab fa-jsfiddle")
        q-item-section jsFiddle

      q-item(clickable, tag="a", href="https://codesandbox.quasar.dev", target="_blank")
        q-item-section.text-black(avatar)
          q-icon(name="fas fa-cubes")
        q-item-section Codesandbox

      q-item-label.q-mt-md(header) Social

      q-item(clickable, tag="a", href="https://forum.quasar.dev/category/1/announcements", target="_blank")
        q-item-section.text-purple(avatar)
          q-icon(name="announcement")
        q-item-section Announcements

      q-item(clickable, tag="a", href="https://twitter.com/quasarframework", target="_blank")
        q-item-section.text-blue(avatar)
          q-icon(name="fab fa-twitter")
        q-item-section Twitter

  q-btn-dropdown.text-bold(:align="align", flat, no-caps, stretch, label="Support", auto-close)
    q-list(dense padding)

      q-item(clickable, tag="a", href="https://chat.quasar.dev", target="_blank")
        q-item-section.text-primary(avatar)
          q-icon(name="fab fa-discord")
        q-item-section Chat

      q-item(clickable, tag="a", href="https://forum.quasar.dev/", target="_blank")
        q-item-section.text-secondary(avatar)
          q-icon(name="fas fa-comments")
        q-item-section Forum

      q-item(clickable, tag="a", href="https://stackoverflow.com/search?q=quasarframework", target="_blank")
        q-item-section.text-red(avatar)
          q-icon(name="fab fa-stack-overflow")
        q-item-section Stack Overflow

      q-separator.q-my-sm

      q-item(clickable, tag="a", href="https://github.com/users/rstoenescu/sponsorship", target="_blank")
        q-item-section(avatar)
          q-icon(name="fab fa-github")
        q-item-section Github Sponsorship
</template>

<script>
export default {
  props: {
    align: String
  }
}
</script>
