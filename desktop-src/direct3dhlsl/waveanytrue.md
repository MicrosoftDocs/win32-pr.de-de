---
title: WaveActiveAnyTrue-Funktion
description: Gibt TRUE zurück, wenn der Ausdruck in einer der aktiven Lanes in der aktuellen Welle true ist.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- WaveActiveAnyTrue-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c49c9727461d316d7d2c9d8f048971384e568476d1ca693aeec49cdf14a4795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721730"
---
# <a name="waveactiveanytrue-function"></a>WaveActiveAnyTrue-Funktion

Gibt TRUE zurück, wenn der Ausdruck in einer der aktiven Lanes in der aktuellen Welle true ist.

## <a name="syntax"></a>Syntax

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auswertende boolesche Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Ausdruck in einer beliebigen Lane true ist.

## <a name="remarks"></a>Hinweise

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




