---
title: WaveGetLaneCount-Funktion
description: Gibt die Anzahl der Lanes in einer Welle in dieser Architektur zurück.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504738"
---
# <a name="wavegetlanecount-function"></a>WaveGetLaneCount-Funktion

Gibt die Anzahl der Lanes in einer Welle in dieser Architektur zurück.

## <a name="syntax"></a>Syntax

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Das Ergebnis liegt zwischen 4 und 128 und umfasst alle Wellen: aktive, inaktive und/oder Hilfsspuren. Das von dieser Funktion zurückgegebene Ergebnis kann je nach Treiberimplementierung erheblich variieren.

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




