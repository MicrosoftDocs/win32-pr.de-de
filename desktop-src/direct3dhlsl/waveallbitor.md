---
title: WaveActiveBitOr-Funktion
description: Gibt das bitweise OR aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert es zurück an alle aktiven Lanes.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- WaveActiveBitOr-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7efe678093fca38940e0a98a31d4c39065bcf172d04aa5eb0932467fc716457b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504890"
---
# <a name="waveactivebitor-function"></a>WaveActiveBitOr-Funktion

Gibt das bitweise OR aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert es zurück an alle aktiven Lanes.

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

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




