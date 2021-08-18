---
title: DeviceMemoryBarrierWithGroupSync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Gerätespeicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Aufruf erreicht haben.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- DeviceMemoryBarrierWithGroupSync-Funktion HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2567a209b86481cd0f25922e8e3b1cf947196a2c799344089591cf70fa3624fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625820"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>DeviceMemoryBarrierWithGroupSync-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Gerätespeicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Aufruf erreicht haben.

## <a name="syntax"></a>Syntax

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

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

 

 




