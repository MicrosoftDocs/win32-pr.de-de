---
title: WavePrefixProduct-Funktion
description: Gibt das Produkt aller Werte in den aktiven Lanes in dieser Welle mit Indizes zurück, die kleiner als diese Spur sind.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct-Funktion HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8cb780f951433afc480c38d52c8120e086a91d32117fe9bb566657e0fcf9f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948960"
---
# <a name="waveprefixproduct-function"></a>WavePrefixProduct-Funktion

Gibt das Produkt aller Werte in den aktiven Lanes in dieser Welle mit Indizes zurück, die kleiner als diese Spur sind.

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

## <a name="remarks"></a>Hinweise

Die Reihenfolge der Vorgänge für diese Routine kann nicht garantiert werden. Das genaue Flag wird also \[ \] ignoriert.

Ein Postfixprodukt kann berechnet werden, indem das Präfixprodukt mit dem Wert der aktuellen Lane multipliziert wird.

Beachten Sie, dass die aktive Spur mit dem niedrigsten Index immer eine 1 für ihr Präfixprodukt erhält.

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 

## <a name="examples"></a>Beispiele

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

Auf einem Computer mit einer Wellengröße von 8 und allen aktiven Lanes außer den Lanes 0 und 4 werden die folgenden Werte von WavePrefixProduct zurückgegeben.

| lane index | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inactive | –           |
| 1          | aktiv   | = 1           |
| 2          | aktiv   | = 1 \* 2        |
| 3          | aktiv   | = 1 \* 2 \* 2     |
| 4          | inactive | –           |
| 5          | aktiv   | = 1 \* 2 \* 2 \* 2       |
| 6          | aktiv   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | aktiv   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Siehe auch

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shadermodell 6](shader-model-6-0.md)
