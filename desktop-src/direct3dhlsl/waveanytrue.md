---
title: Waveactiveanytrue-Funktion
description: Gibt "true" zurück, wenn der Ausdruck in einer der aktiven Bereiche in der aktuellen Wave "true" ist.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Waveactiveanytrue-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993614"
---
# <a name="waveactiveanytrue-function"></a>Waveactiveanytrue-Funktion

Gibt "true" zurück, wenn der Ausdruck in einer der aktiven Bereiche in der aktuellen Wave "true" ist.

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

Der auszuwertende boolesche Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

True, wenn der Ausdruck in einer beliebigen Spur true ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird vom Shader-Modell 6,0 in allen shaderphasen unterstützt. 



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




