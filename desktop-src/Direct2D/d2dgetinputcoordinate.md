---
title: D2DGetInputCoordinate-Funktion (D2d1effecthelpers. h)
description: Gibt den Wert des eingegebenen texcoordn zurück. Nur für komplexe Eingaben verfügbar.
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
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361465"
---
# <a name="d2dgetinputcoordinate-function"></a>D2DGetInputCoordinate-Funktion

Gibt den Wert des eingegebenen texcoordn zurück. Nur für komplexe Eingaben verfügbar.

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

Die Eingabe Nummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein **float4** im Format texcoordn zurück.

## <a name="remarks"></a>Bemerkungen

Die von dieser Funktion zurückgegebene Koordinate ist in textraum. Ein Shader sollte keinerlei Abhängigkeiten davon annehmen, wie dieser Wert berechnet wird. Es sollte nur verwendet werden, um eine Stichprobe der Ausgabe des Pixelshaders zu verwenden. Weitere Informationen finden Sie unter [Hinzufügen eines Pixelshaders zu einer benutzerdefinierten Transformation](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).

Das folgende Beispiel zeigt die-Funktion, die für einen Verschiebungs Zuordnungs Effekt verwendet wird.

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
| Header<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> <dt>

[HLSL-Hilfsprogramme](hlsl-helpers.md)
</dt> </dl>

 

