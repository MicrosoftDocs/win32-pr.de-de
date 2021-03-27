---
title: Wavegetlanecount-Funktion
description: Gibt die Anzahl der Bereiche in einer Welle für diese Architektur zurück.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Wavegetlanecount-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391227"
---
# <a name="wavegetlanecount-function"></a>Wavegetlanecount-Funktion

Gibt die Anzahl der Bereiche in einer Welle für diese Architektur zurück.

## <a name="syntax"></a>Syntax

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Das Ergebnis ist zwischen 4 und 128 und umfasst alle Wellen: aktive, inaktive und/oder hilfsbereiche. Das Ergebnis, das von dieser Funktion zurückgegeben wird, kann sich abhängig von der Treiber Implementierung erheblich unterscheiden.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="examples"></a>Beispiele

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




