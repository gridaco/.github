# React coding conventions

## Techniques

**Animations / Motioons**

- [Framer motion](https://framer.com/motion)
- After Effects + BodyMobvin + [Lottie](https://github.com/airbnb/lottie-web) (uses react-lottie as a wrapper)

**Global State Management**

- [RecoilJS](https://recoiljs.org/)

**Reponsive Layout Development**

- [Rebass](https://rebassjs.org/)

**General UI Development**

- [Reflect React](https://reflect-ui.com)
- [Emotion/styled](https://emotion.sh/docs/styled)


## React coding conventions
**for root components**
- use function as component
- don't use const as component
- don't use React.FC as component
- don't export function as default on end of file explicitly.
``` tsx
export default function GeneralComponent(props: {
  title: string
  desc: string
}){
  <div>
    <h1>{props.title}</h1>
    <p>{props.desc}</p>
  </div>
}
```