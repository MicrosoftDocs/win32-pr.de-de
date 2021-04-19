---
description: Ein Shader, der von einem anderen Shader mit der systeminternen Funktion callshader aufgerufen wird.
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
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346629"
---
# <a name="callable-shader"></a>Callable-Shader

Ein Shader, der von einem anderen Shader mit der systeminternen Funktion [**callshader**](callshader-function.md) aufgerufen wird.

An der **callshader** -Aufruf Site wird eine Parameter Struktur bereitgestellt, die der in dem Aufruf baren Shader verwendeten Parameter Struktur entsprechen muss, auf die der angeforderte Index in die Aufruf Bare shadertabelle verweist, die durch die [**dispatchrays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) -Methode bereitgestellt wird.  Der Aufruf Bare Shader muss diesen Parameter als *INOUT* deklarieren.  Außerdem kann der Aufruf Bare Shader Start Index und Dimensions Eingaben lesen. Weitere Informationen finden Sie unter [**System eigene System Wert**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md)Funktionen. 


## <a name="shader-type-attribute"></a>Shader Type-Attribut


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

 

 




