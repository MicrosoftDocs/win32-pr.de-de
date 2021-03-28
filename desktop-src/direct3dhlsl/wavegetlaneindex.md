---
title: Wavegetlaneingedex-Funktion
description: Gibt den Index der aktuellen Lane innerhalb der aktuellen Wave zurück.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Wavegetlaneingedex-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993615"
---
# <a name="wavegetlaneindex-function"></a>Wavegetlaneingedex-Funktion

Gibt den Index der aktuellen Lane innerhalb der aktuellen Wave zurück.

## <a name="syntax"></a>Syntax

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der aktuelle Bereichs Index. Das Ergebnis liegt zwischen 0 und dem von [**wavegetlanecount**](wavegetlanecount.md)zurückgegebenen Ergebnis.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




