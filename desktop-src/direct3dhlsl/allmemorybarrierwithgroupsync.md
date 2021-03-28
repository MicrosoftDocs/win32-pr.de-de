---
title: Allmemorybarrierwithgroupsync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen-Befehl erreicht haben.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- Allmemorybarrierwithgroupsync-Funktion HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038142"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>Allmemorybarrierwithgroupsync-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen-Befehl erreicht haben.

## <a name="syntax"></a>Syntax

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Arbeitsspeicher Barriere gewährleistet, dass ausstehende Speichervorgänge abgeschlossen wurden. Threads werden bei groupsync-Barrieren synchronisiert. Dies kann einen Thread oder Threads blockieren, wenn Arbeitsspeicher Vorgänge ausgeführt werden.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




