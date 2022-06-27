构造函数
```
GrGLProgramBuilder::GrGLProgramBuilder(GrGLGpu* gpu,
                                       const GrProgramDesc& desc,
                                       const GrProgramInfo& programInfo)
        : INHERITED(desc, programInfo)
        , fGpu(gpu)
        , fVaryingHandler(this)
        , fUniformHandler(this)
        , fVertexAttributeCnt(0)
        , fInstanceAttributeCnt(0)
        , fVertexStride(0)
        , fInstanceStride(0) {}
```

fVaryingHandler 用来处理varying变量
fUniformHandler 用来处理uniform变量

GrGLProgramBuilder继承自GrGLSLProgramBuilder
GrGLProgramBuilder的大部分方法，属性都在GrGLSLProgramBuilder中，其中fVS和fFS用来构造  
顶点着色器和片段着色器