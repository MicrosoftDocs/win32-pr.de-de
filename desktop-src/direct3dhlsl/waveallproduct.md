---
title: Waveactiveproduct-Funktion
description: Multipliziert die Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Welle und repliziert Sie zurück in alle aktiven Bereiche.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- Waveactiveproduct-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858550"
---
# <a name="waveactiveproduct-function"></a>Waveactiveproduct-Funktion

Multipliziert die Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Welle und repliziert Sie zurück in alle aktiven Bereiche.

## <a name="syntax"></a>Syntax

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Produktwert.

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Vorgänge ist nicht definiert.

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




