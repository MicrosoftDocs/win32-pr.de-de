---
title: WavePrefixSum-Funktion
description: Gibt die Summe aller Werte in den aktiven Bereichen mit kleineren Indizes als dieser zurück.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Waveprefixsum-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2021
ms.locfileid: "104980984"
---
# <a name="waveprefixsum-function"></a>WavePrefixSum-Funktion

Gibt die Summe aller Werte in den aktiven Bereichen mit kleineren Indizes als dieser zurück.

## <a name="syntax"></a>Syntax

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parameter

*value* 

Der Wert, der addiert werden soll.

## <a name="return-value"></a>Rückgabewert

Die Summe der Werte.

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Vorgänge in dieser Routine kann nicht garantiert werden. Daher \[ wird das genaue Flag darin \] ignoriert.

Sie können eine postfix Summe berechnen, indem Sie das Präfix Sum dem Wert der aktuellen Lane hinzufügen.

Beachten Sie, dass die aktive Spur mit dem niedrigsten Index immer 0 für die Präfix Summe erhält.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 

## <a name="examples"></a>Beispiele

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

Auf einem Computer mit einer Wellengröße von 8 und allen aktiven Bereichen außer den Bereichen 0 und 4 werden die folgenden Werte von waveprefixsum zurückgegeben.

| Lane-Index | status   | prefixsum     | 
|------------|----------|---------------|
| 0          | inactive | –           |
| 1          | aktiv   | = 0           |
| 2          | aktiv   | = 0 + 2         |
| 3          | aktiv   | = 0 + 2 + 2       |
| 4          | inactive | –           |
| 5          | aktiv   | = 0 + 2 + 2 + 2     |
| 6          | aktiv   | = 0 + 2 + 2 + 2 + 2   |
| 7          | aktiv   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>Weitere Informationen

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shader-Modell 6](shader-model-6-0.md)
