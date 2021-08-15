---
title: WaveActiveBitXor-Funktion
description: Gibt den bitweise XOR aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert ihn zurück an alle aktiven Lanes.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- WaveActiveBitXor-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 733ab8c40a59b784af8a7d50c4f8e1e543f344ee2d75ed9b6896992e6176ff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504880"
---
# <a name="waveactivebitxor-function"></a>WaveActiveBitXor-Funktion

Gibt den bitweise XOR aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert ihn zurück an alle aktiven Lanes.

## <a name="syntax"></a>Syntax

``` syntax
<int_type> WaveActiveBitXor(
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

Der bitweise XOR-Wert.

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




