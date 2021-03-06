## rct201 may c2

- Create following custom components in react
- Using typescript is optional, 1 extra point for using typescript.
- For every component test `must` exist
- All tests go in `__tests__` folder. 
- Write tests with jest/rect-testing-library, do NOT use cypress
- Image:
  - is used to show images.
  - accepts following props and changes the underlying image based on props:
  - `src`, `alt`, `borderRadius`, `width`, `height`, `fit`
  - fit is the property that will decide `object-fit` style of the image. eg: `<Image fit="cover" />`
  - `borderRadius` defines the radius of image: `<Image borderRadius={100} />` will make image circle
- Input:
  - Custom wrapper around input box
  - Takes following props:
  - `type`, `size`, `variant`, `rightLogo`, `rightLogoOnClick`, `onChange`,
  - type is type of input box. default type is `text`
  - size will have following values: sm, md, lg, xl. you can decide what these values for sizes going to be
  - default value must be `md` if not given
  - variant has following values: `outline`, `filled`, and `flushed`. reference: [docs](https://chakra-ui.com/docs/components/form/input#changing-the-appearance-of-the-input=)
  - rightLogo is the property that shows a component inside the inputbox.
  - eg: show and hide password `eye` this image is included with boilerplate feel free to use any other if you want
  - You can pass logo like: `import Eye from "./eye.svg"`  and then `<Input rightLogo={Eye}>` then you can use it in an image tag inside this component
  - rightLogoOnClick is a callback
  - onChange is also a callback that directly gives you value. it doesn't give entire event object only the value we are typing
- Pagination:
  - Simple Pagination component that accepts following props:
  - total, selected, onPageChange
  - `total` decides how many pages will be there. eg: `<Pagination total={10}>`
  - `selected` decides which page is currently selected. \
  - `onPageChange` is a call back when user changes page number
  - Take inspiration from [ant design](https://ant.design/components/pagination/)
  - Inside this component theres prev and next buttons as well.
  - eg: `<Pagination total={5} />` creates 7 boxes inside:
    - [<] [1] [2] [3] [4] [5] [>]
  - prev and next are disabled when there's no prev and next page available
  - Selected page must be highlighted with a `blue` border
  - Hint: `Pagination` component will need one more `PageCell` component which represents one single box
- Writting test case has 60% weightage. every components must be checked for all the props.
- Test case like `should exists in dom` or cases that checks only existance of elements have no weightage at all, and are completely discarded
- Test cases are checked based on `coverage` so make sure you write enough test cases for each and every component