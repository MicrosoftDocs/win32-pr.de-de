---
title: GetRenderTargetSampleCount
description: Ruft die Anzahl der Beispiele für ein Renderziel ab.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54414d7af326c1a069585f9d5deaa3e728d421a65490c5b9f5322b98e06f531e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120134"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Ruft die Anzahl der Beispiele für ein Renderziel ab.



| *UINT* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                 | Beschreibung |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>nichts<br/> |             |



 

## <a name="return-value"></a>Rückgabewert

Die Anzahl der Beispiele.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion und [**GetRenderTargetSamplePosition,**](dx-graphics-hlsl-getrendertargetsampleposition.md) um die Anzahl und Position der Samplingspeicherorte für ein Renderziel zu ermitteln.

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

 

 





