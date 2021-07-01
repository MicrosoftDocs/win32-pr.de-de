---
title: RestartStrip (DirectX HLSL Stream-Output Object)
description: Beendet den aktuellen primitiven Strip und startet einen neuen Strip. Wenn für den aktuellen Strip nicht genügend Scheitelpunkte ausgegeben werden, um die primitive Topologie zu füllen, wird das unvollständige Primitive am Ende verworfen.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120195"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (DirectX HLSL Stream-Output Object)

Beendet den aktuellen primitiven Strip und startet einen neuen Strip. Wenn für den aktuellen Strip nicht genügend Scheitelpunkte ausgegeben werden, um die primitive Topologie zu füllen, wird das unvollständige Primitive am Ende verworfen.

RestartStrip();



 

## <a name="parameters"></a>Parameter



| Element                                                                                     | Beschreibung |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**nichts**<br/> |             |



 

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

Ein Strip cut bewirkt, dass der aktuelle Strip endet und ein neuer Strip gestartet wird. Ein Strip cut kann durch explizites Aufrufen dieser Methode oder einfach durch Rendern bis zum maximalen Indexwert (1, der für 32-Bit-Indizes 0xffffffff ist, oder 0xffff für 16-Bit-Indizes) erfolgen. Jede Instanz eines indizierten instanziierten Zeichnens generiert automatisch einen Strip cut. Dies gilt auch, wenn die Topologie kein Dreiecksstreifen ist.

> [!Note]  
> Unterstützung für Neustart und 1 "Magischer Wert" für einen Cut ist nur auf Geräten der [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 oder höher verfügbar.

 

Die Ausgabe wird immer als Dreiecksstreifen angenommen. Um die Ausgabe zu einer Dreiecksliste zu machen, müssen Sie RestartStrip zwischen den einzelnen Dreiecken aufrufen. Dreiecksfächer werden nicht unterstützt.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stream-Output-Objekt](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

