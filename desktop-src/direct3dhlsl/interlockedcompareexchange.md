---
title: Interlockedcompareexchange-Funktion (HLSL-Referenz)
description: Vergleicht atomisch das Ziel mit dem Vergleichswert. Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben. Der ursprüngliche Wert wird auf den ursprünglichen Wert des Ziels festgelegt.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Interlockedcompareexchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "104993318"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>Interlockedcompareexchange-Funktion (HLSL-Referenz)

Vergleicht atomisch das Ziel mit dem Vergleichswert. Wenn Sie identisch sind, wird das Ziel mit dem Eingabe Wert überschrieben. Der ursprüngliche Wert wird auf den ursprünglichen Wert des Ziels festgelegt.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
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

</dd> <dt>

*ursprünglicher \_ Wert* ausgehend \[\]
</dt> <dd>

Typ: **T**

Der ursprüngliche Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Vergleicht atomarisch den Wert *, auf den* mit dem Wert " *dest* " verwiesen wird, mit einem *Vergleichs \_ Wert*, speichert den *Wert* an dem Speicherort *, auf den " \_* *dest* " verweist, wenn die Werte entsprechen Dieser Vorgang kann nur für typisierte **int** -oder **uint** -Ressourcen und Shared Memory-Variablen ausgeführt werden. Es gibt zwei Verwendungsmöglichkeiten für diese Funktion. Der erste ist, wenn R ein Variablentyp für den gemeinsamen Speicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das von *dest* verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcen Variablentyp ist. In diesem Szenario führt die Funktion den Vorgang an dem Ressourcen Speicherort aus, auf den " *dest*" verweist. Dieser Vorgang ist nur verfügbar, wenn R lesbar und beschreibbar ist.

> [!Note]  
> Wenn Sie in einer [**for**](dx-graphics-hlsl-for.md) -oder [**while**](dx-graphics-hlsl-while.md) -Compute-Shader-Schleife **interlockedcompareexchange** aufrufen, müssen Sie für die ordnungsgemäße Kompilierung das Attribut " **\[ \_ UAV- \_ \] Bedingung zulassen** " in dieser Schleife verwenden.

 

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




