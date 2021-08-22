---
title: D2DGetInputCoordinate-Funktion (D2d1effecthelpers.h)
description: Gibt den Wert der Eingabe TEXCOORDN zurück. Nur für komplexe Eingaben verfügbar.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- D2DGetInputCoordinate-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3fe0d825dea70c8e5211b8c13f1e850fa513670bbc93de98f1f8e2b87ef046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075294"
---
# <a name="d2dgetinputcoordinate-function"></a>D2DGetInputCoordinate-Funktion

Gibt den Wert der Eingabe TEXCOORDN zurück. Nur für komplexe Eingaben verfügbar.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Die Eingabenummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **float4** im Format TEXCOORDN zurück.

## <a name="remarks"></a>Hinweise

Die von dieser Funktion zurückgegebene Koordinate befindet sich im Texelraum. Ein Shader sollte keine Abhängigkeiten davon annehmen, wie dieser Wert berechnet wird. Es sollte nur verwendet werden, um die Eingabe des Pixelshaders abzutasten. Weitere Informationen finden Sie unter [Hinzufügen eines Pixel-Shaders zu einer benutzerdefinierten Transformation.](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform)

Das folgende Beispiel zeigt die Funktion, die für einen Verschiebungszuordnungseffekt verwendet wird.

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> <dt>

[HLSL-Hilfshilfen](hlsl-helpers.md)
</dt> </dl>

 

