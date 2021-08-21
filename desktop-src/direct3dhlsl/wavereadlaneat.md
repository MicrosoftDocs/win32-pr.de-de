---
title: WaveReadLaneAt-Funktion
description: Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Welle zurück.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08fa669f8c4284c26052dd68bdbe9ab4f5b99b80b8bdf9445aa3375f0a87a9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504620"
---
# <a name="wavereadlaneat-function"></a>WaveReadLaneAt-Funktion

Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Welle zurück.

## <a name="syntax"></a>Syntax

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*expr* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> <dt>

*laneIndex* 
</dt> <dd>

Der Index der Spur, für die *das Expr-Ergebnis* zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der resultierende Wert ist das Ergebnis von *expr*. Sie ist einheitlich, wenn *laneIndex* gleich ist.

## <a name="remarks"></a>Hinweise

Diese Funktion ist effektiv eine Übertragung des Werts in *der laneIndex*-th lane.

Diese Funktion wird von Shadermodell 6.0 in allen Shaderstufen unterstützt.

## <a name="see-also"></a>Siehe auch

* [Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Shadermodell 6](shader-model-6-0.md)
