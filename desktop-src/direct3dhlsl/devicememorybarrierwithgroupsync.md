---
title: Devicememorybarrierwithgroupsync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Gerätespeicher Zugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Befehl erreicht haben.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- Devicememorybarrierwithgroupsync-Funktion HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312833"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>Devicememorybarrierwithgroupsync-Funktion

Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Gerätespeicher Zugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Befehl erreicht haben.

## <a name="syntax"></a>Syntax

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
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

 

 




