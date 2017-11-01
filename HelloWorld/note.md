## react.js
React核心逻辑，且与具体的渲染引擎无关，从而可以跨平台公用。如果应用迁移到React Native，这一部分的逻辑不变

## react-dom.js
具体的DOM渲染更新逻辑，以及服务端渲染的逻辑

```
  class ComponentName extends React.Component {
    constructor(props) {
      super(props)
      this.state = {...}
      //  bind(this)
      this.handleClick = this.handleClick.bind(this)
    }
    handleClick(e) {
      this.setState({key : value})
    }
    //  or
    //  handleClick = () => {
    //    this.setState({key : value})
    //  }
    /*
      life circle
    */
    componentWillMount() {
      ....
      //  component准备渲染,只执行一次
    }
    componentDidMount() {
      ....
      //  component渲染完毕，只执行一次
    }
    componentWillRecevieProps() {
      ....
      //  component 将要接受新的props执行
    }
    shouldComponentUpdate(nextProps, nextState) {
      ....
      //  判断组件是否渲染，default true
    }
    componentWillUpdate() {
      ....
      // component 准备重新渲染
    }
    componentDidUpdate() {
      ....
      //  component 重新渲染完成
    }
    componentWillUnmount() {
      ....
      //  component 卸载
    }
  } 
```
## React.createClass(v16弃用)
## class ComponentName extends React.Component {
  ....
}
注册一个组件类
  tips:
    1.ComponentName,组件名书写

## jsx
1.可以使用表达式

## state
