---
title: Waveisfirstlane-Funktion
description: Gibt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index true zurück.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Waveisfirstlane-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316778"
---
# <a name="waveisfirstlane-function"></a>Waveisfirstlane-Funktion

Gibt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index true zurück.

## <a name="syntax"></a>Syntax


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

True gilt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index.

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann verwendet werden, um Vorgänge zu identifizieren, die nur einmal pro Wave ausgeführt werden sollen.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




