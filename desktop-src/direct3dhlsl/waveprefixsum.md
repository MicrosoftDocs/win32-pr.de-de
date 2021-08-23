---
title: WavePrefixSum-Funktion
description: Gibt die Summe aller Werte in den aktiven Lanes mit kleineren Indizes als dieser zurück.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbb9ced3fbf7e150cbe3b9bca7eb176e61cf6c8881def22a977ae37a2dbf4b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671090"
---
# <a name="waveprefixsum-function"></a>WavePrefixSum-Funktion

Gibt die Summe aller Werte in den aktiven Lanes mit kleineren Indizes als dieser zurück.

## <a name="syntax"></a>Syntax

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parameter

*value* 

Der wert, der summiert werden soll.

## <a name="return-value"></a>Rückgabewert

Die Summe der Werte.

## <a name="remarks"></a>Hinweise

Die Reihenfolge der Vorgänge für diese Routine kann nicht garantiert werden. Das genaue Flag wird also \[ \] ignoriert.

Eine Postfixsumme kann berechnet werden, indem dem Wert der aktuellen Spur die Präfixsumme hinzugefügt wird.

Beachten Sie, dass die aktive Spur mit dem niedrigsten Index immer 0 für ihre Präfixsumme erhält.

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 

## <a name="examples"></a>Beispiele

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

Auf einem Computer mit einer Wellengröße von 8 und allen aktiven Lanes außer den Lanes 0 und 4 werden die folgenden Werte von WavePrefixSum zurückgegeben.

| Lane-Index | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inactive | –           |
| 1          | aktiv   | = 0           |
| 2          | aktiv   | = 0+2         |
| 3          | aktiv   | = 0+2+2       |
| 4          | inactive | –           |
| 5          | aktiv   | = 0+2+2+2     |
| 6          | aktiv   | = 0+2+2+2+2+2   |
| 7          | aktiv   | = 0+2+2+2+2+2+2 |

## <a name="see-also"></a>Siehe auch

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shadermodell 6](shader-model-6-0.md)
