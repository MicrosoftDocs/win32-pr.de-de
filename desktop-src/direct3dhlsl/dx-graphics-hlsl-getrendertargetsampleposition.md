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
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120575"
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

## <a name="remarks"></a>Bemerkungen

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

 

 





