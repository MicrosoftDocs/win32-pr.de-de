---
title: AllMemoryBarrierWithGroupSync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Aufruf erreicht haben.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- AllMemoryBarrierWithGroupSync-Funktion HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d3c146ff04597b7eca13dd5cbef93dc1c79f81709353bf5b4fa1a993a8da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626690"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>AllMemoryBarrierWithGroupSync-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Aufruf erreicht haben.

## <a name="syntax"></a>Syntax

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Speicherbarriere garantiert, dass ausstehende Speichervorgänge abgeschlossen wurden. Threads werden über GroupSync-Barrieren synchronisiert. Dies kann einen Thread oder Threads blockieren, wenn Arbeitsspeichervorgänge ausgeführt werden.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




