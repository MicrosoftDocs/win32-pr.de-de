---
title: D2DGetInput-Funktion (D2d1effecthelpers. h)
description: Gibt die Farbe der Eingabe N an der eingabekoordinate zurück. Nur für einfache Eingaben verfügbar.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- D2DGetInput-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365600"
---
# <a name="d2dgetinput-function"></a>D2DGetInput-Funktion

Gibt die Farbe der Eingabe N an der eingabekoordinate zurück. Nur für einfache Eingaben verfügbar.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DGetInput(
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

Die-Funktion gibt ein **float4**-Wert zurück, der die RGBA-Farbe im Format inputn enthält.

## <a name="remarks"></a>Bemerkungen

Im folgenden Beispiel wird die Funktion gezeigt, die als Teil eines arithmetischen zusammengesetzten Effekts verwendet wird.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Ein weiteres Beispiel für die Verwendung dieser Funktion finden Sie auch in der Anmerkung zum [ \_ \_ Eintrag D2D PS](d2d-ps-entry.md) .

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

 

 





