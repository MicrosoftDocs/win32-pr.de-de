---
title: WaveActiveAllTrue-Funktion
description: Gibt TRUE zurück, wenn der Ausdruck in allen aktiven Lanes in der aktuellen Welle true ist.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- WaveActiveAllTrue-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f80c9af3bb9a1be47a3d64f31f0b3c3c610022d3a017a13053c0e4fc7db3a82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504870"
---
# <a name="waveactivealltrue-function"></a>WaveActiveAllTrue-Funktion

Gibt TRUE zurück, wenn der Ausdruck in allen aktiven Lanes in der aktuellen Welle true ist.

## <a name="syntax"></a>Syntax

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende boolesche Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

True, wenn der Ausdruck in allen Lanes true ist.

## <a name="remarks"></a>Hinweise

Diese Funktion wird vom Shadermodell 6.0 in allen Shaderstufen unterstützt. 



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 6](shader-model-6-0.md)
</dt> </dl>

 

 




