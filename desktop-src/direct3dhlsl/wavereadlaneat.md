---
title: Wavereadlaneat-Funktion
description: Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Wave zurück.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Wavereadlaneat-Funktion HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2020
ms.locfileid: "104390103"
---
# <a name="wavereadlaneat-function"></a>Wavereadlaneat-Funktion

Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Wave zurück.

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

*laneingedex* 
</dt> <dd>

Der Index der Spur, für die das *expr* -Ergebnis zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der resultierende Wert ist das Ergebnis von *expr*. Er ist einheitlich, wenn *laneingedex* einheitlich ist.

## <a name="remarks"></a>Bemerkungen

Bei dieser Funktion handelt es sich tatsächlich um eine Übertragung des Werts in der laneindexth-Spur.

Diese Funktion wird vom Shader-Modell 6,0 in den folgenden shadertypen unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modell 6](shader-model-6-0.md)
</dt> </dl>

 

 




