---
title: GetRenderTargetSamplePosition
description: Ruft die Samplingposition (x,y) für einen angegebenen Beispielindex ab.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a406fcbd023d0688baf51cabbfea53438f3d58a6fba4d1fc7d1bf8d33077262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514334"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Ruft die Samplingposition (x,y) für einen angegebenen Beispielindex ab.

float<2> GetRenderTargetSamplePosition( in int<1> Index<br/>);



 

## <a name="parameters"></a>Parameter



| Element                                                                                       | Beschreibung                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*<br/> | \[in \] einem nullbasierten Beispielindex.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die Position (x,y) des angegebenen Beispiels.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion und [**GetRenderTargetSampleCount,**](dx-graphics-hlsl-getrendertargetsamplecount.md) um die Anzahl und Position der Samplingspeicherorte für ein Renderziel zu ermitteln.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Nein        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





