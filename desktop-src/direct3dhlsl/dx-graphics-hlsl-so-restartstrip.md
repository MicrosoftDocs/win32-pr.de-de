---
title: Restartstrip (DirectX HLSL Stream-Output-Objekt)
description: Beendet den aktuellen primitiven Strip und startet einen neuen Strip. Wenn für den aktuellen Strip nicht genügend Scheitel Punkte ausgegeben werden, um die primitive Topologie auszufüllen, wird der unvollständige primitive am Ende verworfen.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993423"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>Restartstrip (DirectX HLSL Stream-Output-Objekt)

Beendet den aktuellen primitiven Strip und startet einen neuen Strip. Wenn für den aktuellen Strip nicht genügend Scheitel Punkte ausgegeben werden, um die primitive Topologie auszufüllen, wird der unvollständige primitive am Ende verworfen.



|                 |
|-----------------|
| Restartstrip (); |



 

## <a name="parameters"></a>Parameter



| Element                                                                                     | BESCHREIBUNG |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**Gar**<br/> |             |



 

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

Ein Strip-Cut bewirkt, dass der aktuelle Bereich endet und ein neuer Bereich gestartet wird. Ein Bereichs Ausschnitt kann durch explizites Aufrufen dieser Methode oder durch Rendering bis zum maximalen Indexwert (1, 0xFFFFFFFF für 32-Bit-Indizes oder 0xFFFF für 16-Bit-Indizes) durchgeführt werden. Jede Instanz einer indizierten, instanzierten Zeichnung generiert automatisch einen Bereichs Ausschnitt. Dies gilt auch dann, wenn es sich bei der Topologie nicht um einen Dreiecks Streifen handelt.

> [!Note]  
> Die Unterstützung für den Neustart und der 1 "Magic Value" for a Cut sind nur auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 oder höher verfügbar.

 

Es wird immer angenommen, dass es sich um einen Dreiecks Streifen handelt. Um die Ausgabe zu einer Dreiecks Liste zu machen, müssen Sie restartstrip zwischen jedem Dreieck aufrufen. Dreiecks Lüfter werden nicht unterstützt.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stream-Output-Objekt](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

