---
title: WaveIsFirstLane-Funktion
description: Gibt nur true für die aktive Lane in der aktuellen Welle mit dem kleinsten Index zurück.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d909d4269db61980325c48b5858d910955512f701fb09adbcb91f5e078fa3b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852710"
---
# <a name="waveisfirstlane-function"></a>WaveIsFirstLane-Funktion

Gibt nur true für die aktive Lane in der aktuellen Welle mit dem kleinsten Index zurück.

## <a name="syntax"></a>Syntax


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

True nur für die aktive Lane in der aktuellen Welle mit dem kleinsten Index.

## <a name="remarks"></a>Hinweise

Diese Funktion kann verwendet werden, um Vorgänge zu identifizieren, die nur einmal pro Welle ausgeführt werden sollen.

Diese Funktion wird vom Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




