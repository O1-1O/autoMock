# autoMock
采用javaparser等语法分析工具，自动生成基于test-ng+Mockito框架的单元测试类

## 目标
生成的单测覆盖率达到80%以上

## 理论基础
### AST 抽象语法树
分析源代码，得到语法树

### Mockito单元测试框架
1. 基本Mock
2. 打桩和连续打桩
3. PowerMockito的使用，抽象方法、静态类等

## 核心逻辑
结合类语法树和Mockito的规则，自动生成单测

**问题**
1. 语法树和Mockito规则的结合点
2. 分支覆盖（if-else、for、while、switch、try-catch）
2. 方法体中的参数可能是从外界直接传入的也可能是经过处理的，难以区分
