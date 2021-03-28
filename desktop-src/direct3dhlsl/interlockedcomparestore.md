---
title: Interlockedcomparestore-Funktion (HLSL-Referenz)
description: Vergleicht atomisch das Ziel mit dem Vergleichswert. Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Interlockedcomparestore-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104389765"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Interlockedcomparestore-Funktion (HLSL-Referenz)

Vergleicht atomisch das Ziel mit dem Vergleichswert. Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Typ: **R**

Die Zieladresse.

</dd> <dt>

*\_ Wert vergleichen* \[ in\]
</dt> <dd>

Typ: **T**

Der Vergleichswert.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Vergleicht atomarisch den Wert, auf den mit dem " *dest* " *verwiesen wird,* mit dem Wert "Wert vergleichen" und speichert den *Wert* in dem Speicherort, auf den *\_* Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt zwei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest* verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den " *dest*" verweist.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




