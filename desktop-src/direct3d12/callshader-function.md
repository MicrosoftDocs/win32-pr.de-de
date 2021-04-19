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
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342754"
---
# <a name="callshader-function"></a>CallShader-Funktion

Ruft einen anderen Shader innerhalb eines Shaders auf.

## <a name="syntax"></a>Syntax
Diese intrinsische Funktionsdefinition entspricht der folgenden Funktions Vorlage:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parameter

`ShaderIndex`

Eine ganze Zahl ohne Vorzeichen, die den Index in die Aufruf [Bare shadertabelle](callable-shader.md) darstellt, die im Aufruf von [**dispatchrays**] angegeben ist (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Die benutzerdefinierten Parameter, die an den Aufruf baren Shader übergeben werden.  Diese Parameter Struktur muss der Parameter Struktur entsprechen, die in dem Aufruf baren Shader verwendet wird, auf den in der Shader-Tabelle verwiesen wird.


## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




