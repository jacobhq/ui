[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/supabase/ui)

# Supabase UI

Supabase UI is a React UI library.

🚧  
Supabase UI is still a work-in-progress until a major release is published.

## Roadmap

Some of these are a work in progress - we invite anyone to submit a [feature request](https://github.com/supabase/ui/issues/new?labels=enhancement&template=2.Feature_request.md) if there is something you would like to see.

_General_

- [x] Button
- [x] Typography
- [x] Icon

_Data Input_

- [x] Input
- [ ] InputNumber
- [x] Select
- [x] Checkbox (and Checkbox Groups)
- [x] Radio (and Radio Groups)
- [x] Toggle (work in progress)
- [ ] Upload (work in progress)
- [ ] Slider
- [ ] Date picker
- [ ] Time picker
- [ ] Form

_Layout_

- [ ] Layout
- [ ] Grid (Flex)
- [x] Divider
- [x] Space (Flex)

_Display_

- [x] Card
- [ ] Avatar
- [ ] Alert
- [x] Badge
- [x] Menu
- [ ] Tooltips
- [ ] Tables
- [ ] Code block

_Navigation_

- [ ] Tabs
- [ ] Breadcrumb
- [x] Dropdown
- [ ] Menu
- [ ] Page Header
- [ ] Sidebar
- [ ] Flyout menu
- [ ] Steps

_Overlay_

- [x] Modal
- [ ] Drawer / SidePanel
- [ ] Toast messages / Notifaction
- [ ] Progress
- [ ] Feeds / Timeline

_Utility_

- [x] Loading
- [x] Transition (work in progress)

_Misc_

- [ ] Storybook docs
- [ ] Themeing (in progress)
- [ ] Supabase Auth Elements
- [ ] Documentation website

We would be keen to hear any feedback on this project.

Feel free to [submit a question or idea here](https://github.com/supabase/supabase/discussions/category_choices)

## Install Supabase UI

```cli
npm install @supabase/ui
```

## Using Supabase UI

Example of importing a component

```js
import { Button } from '@supabase/ui'

//...

return <Button>I am a Supabase UI button</Button>
```

It is probably advisable to use [Normalize](https://github.com/sindresorhus/modern-normalize) with Supabase UI for the timebeing.

## Run storybook locally

Supabase UI uses storybook to develop and organise components.
They can be viewed locally in the Storybook docs explorer

make sure you are in the supabase-ui folder

```cli
cd supabase-ui
```

run storybook

```cli
npm run storybook
```

(you may need to run `npm install` first)

Storybook runs by default on `http://localhost:6006/`

## Local Development

If you want to test Supabase UI components locally, in context in another project locally, then you will need to `npm link` the supabase-ui project locally.

Follow these instructions here ->
[NPM Linking and Unlinking instructions](https://dev.to/erinbush/npm-linking-and-unlinking-2h1g)

### Common issues

_A common issue found with local testing is multiple versions of react running._

You may need to npm-link the react node module in the target app you want to locally test the library in. Then use that version of react inside the library, and then npm-link the library so the target app can use the library with just the 1 version of react.

Step by step:

• run npm link in /your-app/node_modules/react. This should make the React's global link.

• run npm link react in /supabase/ui. This should make the library use the application’s React copy.

• run npm link @supabase/ui in /your-app
