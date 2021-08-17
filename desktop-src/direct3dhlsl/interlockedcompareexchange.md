---
title: InterlockedCompareExchange-Funktion (HLSL-Referenz)
description: Vergleicht das Ziel atomisch mit dem Vergleichswert. Wenn sie identisch sind, wird das Ziel mit dem Eingabewert überschrieben. Der ursprüngliche Wert wird auf den ursprünglichen Wert des Ziels festgelegt.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- InterlockedCompareExchange-Funktion HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46cf8c3fb0e3bc0b21c5bf8bc3d946851ce213b765731518d252495250071228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119254"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>InterlockedCompareExchange-Funktion (HLSL-Referenz)

Vergleicht das Ziel atomisch mit dem Vergleichswert. Wenn sie identisch sind, wird das Ziel mit dem Eingabewert überschrieben. Der ursprüngliche Wert wird auf den ursprünglichen Wert des Ziels festgelegt.

## <a name="syntax"></a>Syntax

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*dest* \[ In\]
</dt> <dd>

Typ: **R**

Die Zieladresse.

</dd> <dt>

*\_ Vergleichswert* \[ in\]
</dt> <dd>

Typ: **T**

Der Vergleichswert.

</dd> <dt>

*wert* \[ In\]
</dt> <dd>

Typ: **T**

Der Eingabewert.

</dd> <dt>

*Ursprünglicher \_ Wert* \[ out\]
</dt> <dd>

Typ: **T**

Der ursprüngliche Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Vergleicht atomisch den Wert, auf den vom *dest* verwiesen wird, mit *dem \_ Vergleichswert,* speichert *den Wert* an der Position, auf die vom *dest* verwiesen wird, wenn die Werte übereinstimmen, und gibt den ursprünglichen Wert von *dest* im *ursprünglichen \_ Wert* zurück. Dieser Vorgang kann nur für **int-** oder **uint-typisierte** Ressourcen und Freigegebene Speichervariablen ausgeführt werden. Es gibt zwei mögliche Verwendungsmöglichkeiten für diese Funktion. Die erste ist, wenn R ein Variablentyp für gemeinsam genutzten Arbeitsspeicher ist. In diesem Fall führt die Funktion den Vorgang für das Shared Memory-Register aus, auf das durch *dest* verwiesen wird. Das zweite Szenario ist, wenn R ein Ressourcenvariablentyp ist. In diesem Szenario führt die Funktion den Vorgang für den Ressourcenspeicherort aus, auf den vom *Dest* verwiesen wird. Dieser Vorgang ist nur verfügbar, wenn R lesbar und schreibbar ist.

> [!Note]  
> Wenn Sie **InterlockedCompareExchange** in einer [**for-**](dx-graphics-hlsl-for.md) oder while-Compute-Shaderschleife aufrufen, müssen Sie zur ordnungsgemäßen Kompilierung das [](dx-graphics-hlsl-while.md) **\[ \_ \_ uav-Bedingungsattribut \] allow für** diese Schleife verwenden.

 

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




