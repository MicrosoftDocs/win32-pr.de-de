---
title: asuint-Funktion
description: Interpretiert das Bitmuster eines 64-Bit-Werts als zwei Ganzzahlen 32 ohne Vorzeichen zurück.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint-Funktion HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038140"
---
# <a name="asuint-function"></a>asuint-Funktion

Interpretiert das Bitmuster eines 64-Bit-Werts als zwei Ganzzahlen 32 ohne Vorzeichen zurück.

## <a name="syntax"></a>Syntax

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **Double**

Der Eingabewert.

</dd> <dt>

*lowbits* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Das niedrige 32-Bit-Muster des *Werts*.

</dd> <dt>

*highbits* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Das hohe 32-Bit-Muster des *Werts*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist eine Alternative Version von " [**asuint**](dx-graphics-hlsl-asuint.md) ", die in früheren shadermodellen verfügbar war und für Shader Model 5 eingeführt wurde. Die ursprüngliche Funktion (im HLSL-Compiler mit der unterschiedlichen Signatur erkannt) bleibt für Shader Model 5 verfügbar.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




