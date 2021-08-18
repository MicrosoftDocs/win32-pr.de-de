---
title: WaveGetLaneIndex-Funktion
description: Gibt den Index der aktuellen Spur innerhalb der aktuellen Welle zurück.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- WaveGetLaneIndex-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb6b0290b46727cdf0d9ce705d2910df003cbc114638a0135be2023bb836202a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721720"
---
# <a name="wavegetlaneindex-function"></a>WaveGetLaneIndex-Funktion

Gibt den Index der aktuellen Spur innerhalb der aktuellen Welle zurück.

## <a name="syntax"></a>Syntax

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der aktuelle Lane-Index. Das Ergebnis liegt zwischen 0 und dem von [**WaveGetLaneCount zurückgegebenen Ergebnis.**](wavegetlanecount.md)

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




