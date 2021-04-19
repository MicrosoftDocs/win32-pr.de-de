---
title: D2DSampleInputAtPosition-Funktion (D2d1effecthelpers. h)
description: Gibt eine Stichproben Eingabe N an der absoluten Szenen Position statt an eine Eingabe relative Position aus. Nur für komplexe Eingaben verfügbar.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- D2DSampleInputAtPosition-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354794"
---
# <a name="d2dsampleinputatposition-function"></a>D2DSampleInputAtPosition-Funktion

Gibt eine Stichproben Eingabe N an der absoluten Szenen Position statt an eine Eingabe relative Position aus. Nur für komplexe Eingaben verfügbar.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Die Eingabe Nummer.

</dd> <dt>

*UV* \[ in\]
</dt> <dd>

Die UV-Position.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein **float4** im Format texcoordn zurück.

## <a name="remarks"></a>Bemerkungen

Das folgende Beispiel zeigt die-Funktion, die in einem Zirkel Umbruch verwendet wird.

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
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

 

 





