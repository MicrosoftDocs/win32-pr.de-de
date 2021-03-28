---
title: Waveactivebitor-Funktion
description: Gibt das bitweise OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- Waveactivebitor-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039841"
---
# <a name="waveactivebitor-function"></a>Waveactivebitor-Funktion

Gibt das bitweise OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche.

## <a name="syntax"></a>Syntax

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der bitweise OR-Wert.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




