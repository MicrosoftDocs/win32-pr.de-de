---
title: WavePrefixProduct-Funktion
description: Gibt das Produkt aller Werte in den aktiven Bereichen in dieser Welle mit Indizes zurück, die kleiner sind als diese Strecke.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Waveprefixproduct-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391226"
---
# <a name="waveprefixproduct-function"></a>WavePrefixProduct-Funktion

Gibt das Produkt aller Werte in den aktiven Bereichen in dieser Welle mit Indizes zurück, die kleiner sind als diese Strecke.

## <a name="syntax"></a>Syntax

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Parameter

*value* 

Der zu multiplizierende Wert.

## <a name="return-value"></a>Rückgabewert

Das Produkt aller Werte.

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Vorgänge in dieser Routine kann nicht garantiert werden. Daher \[ wird das genaue Flag darin \] ignoriert.

Ein postfix-Produkt kann berechnet werden, indem das Präfix Product mit dem Wert der aktuellen Lane multipliziert wird.

Beachten Sie, dass die aktive Spur mit dem niedrigsten Index immer 1 für das Präfix Produkt empfängt.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 

## <a name="examples"></a>Beispiele

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

Auf einem Computer mit einer Wellengröße von 8 und allen aktiven Bereichen außer den Bereichen 0 und 4 werden die folgenden Werte von waveprefixproduct zurückgegeben.

| Lane-Index | status   | prefixproduct | 
|------------|----------|---------------|
| 0          | inactive | –           |
| 1          | aktiv   | = 1           |
| 2          | aktiv   | = 1 \* 2        |
| 3          | aktiv   | = 1 \* 2 \* 2     |
| 4          | inactive | –           |
| 5          | aktiv   | = 1 \* 2 \* 2 2 \*       |
| 6          | aktiv   | = 1 \* 2 \* 2 2 \* 2 2 \*    |
| 7          | aktiv   | = 1 2 2 2 2 2 2 \* \* \* \* \* |

## <a name="see-also"></a>Weitere Informationen

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shader-Modell 6](shader-model-6-0.md)
