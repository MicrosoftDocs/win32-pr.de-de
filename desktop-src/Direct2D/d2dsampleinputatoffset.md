---
title: D2DSampleInputAtOffset-Funktion (D2d1effecthelpers. h)
description: Stichproben Eingabe N bei einem Offset des Offsets von der eingabekoordinate. Nur für komplexe Eingaben verfügbar.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- D2DSampleInputAtOffset-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354795"
---
# <a name="d2dsampleinputatoffset-function"></a>D2DSampleInputAtOffset-Funktion

Stichproben Eingabe N bei einem Offset des Offsets von der eingabekoordinate. Nur für komplexe Eingaben verfügbar.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Die Eingabe Nummer.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Der UV-Offset.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein **float4** im Format texcoordn zurück.

## <a name="remarks"></a>Bemerkungen

Im folgenden Beispiel wird die Funktion gezeigt, die als Teil einer Hervorhebungs-und Schatten Farbverlaufs Maske verwendet wird.

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
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

 

 





