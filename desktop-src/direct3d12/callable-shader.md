---
description: Ein Shader, der von einem anderen Shader mit der systeminternen CallShader-Eigenschaft aufgerufen wird.
ms.assetid: ''
title: Callable-Shader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: b84ec6ea58fbc456db1747259f687a2fb6c8cb0fe3374b3d32396861dcd2f9b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461070"
---
# <a name="callable-shader"></a>Callable-Shader

Ein Shader, der von einem anderen Shader mit der [**systeminternen CallShader-Eigenschaft**](callshader-function.md) aufgerufen wird.

An der **CallShader-Aufrufwebsite** wird eine Parameterstruktur bereitgestellt, die mit der Parameterstruktur übereinstimmen muss, die im aufrufbaren Shader verwendet wird, auf den der angeforderte Index in der aufrufbaren Shadertabelle verweist, die über die [**DispatchRays-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) bereitgestellt wird.  Der aufrufbare Shader muss diesen Parameter als *inout* deklarieren.  Darüber hinaus kann der aufrufbare Shader Startindex- und Dimensionseingaben lesen. Weitere Informationen finden Sie unter [**System value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md). 


## <a name="shader-type-attribute"></a>Shadertypattribut


```
[shader("callable")]
```



## <a name="example"></a>Beispiel

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




