---
title: Groupmemorybarrierwithgroupsync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle freigegebenen Gruppen Zugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Befehl erreicht haben.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Groupmemorybarrierwithgroupsync-Funktion HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976185"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>Groupmemorybarrierwithgroupsync-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle freigegebenen Gruppen Zugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Befehl erreicht haben.

## <a name="syntax"></a>Syntax

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 




