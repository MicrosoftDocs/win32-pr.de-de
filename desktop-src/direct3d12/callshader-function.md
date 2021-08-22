---
description: Ruft einen anderen Shader innerhalb eines Shaders auf.
ms.assetid: ''
title: CallShader-Funktion
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280350"
---
# <a name="callshader-function"></a>CallShader-Funktion

Ruft einen anderen Shader innerhalb eines Shaders auf.

## <a name="syntax"></a>Syntax
Diese systeminterne Funktionsdefinition entspricht der folgenden Funktionsvorlage:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parameter

`ShaderIndex`

Eine ganze Zahl ohne Vorzeichen, die den Index in der aufrufbaren [Shadertabelle](callable-shader.md) darstellt, die im Aufruf von [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) angegeben ist.

`Parameter`

Die benutzerdefinierten Parameter, die an den aufrufbaren Shader übergeben werden.  Diese Parameterstruktur muss mit der Parameterstruktur übereinstimmen, die im aufrufbaren Shader verwendet wird, auf den in der Shadertabelle verwiesen wird.


## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Hinweise

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




