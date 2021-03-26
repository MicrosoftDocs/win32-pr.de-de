---
title: GetRenderTargetSamplePosition
description: Ruft die samplingposition (x, y) für einen angegebenen Beispiel Index ab.
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
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103717777"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Ruft die samplingposition (x, y) für einen angegebenen Beispiel Index ab.



|                                                                                  |
|----------------------------------------------------------------------------------|
| float<2> GetRenderTargetSamplePosition (in int<1> Index<br/>); |



 

## <a name="parameters"></a>Parameter



| Element                                                                                       | BESCHREIBUNG                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Sin*<br/> | \[in \] einem NULL basierten Beispiel Index.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die Position (x, y) des angegebenen Beispiels.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion und [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) , um die Anzahl und Position der Stichproben Speicherorte für ein Renderziel zu ermitteln.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Nein        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





