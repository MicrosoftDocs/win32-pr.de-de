---
title: D2DGetScenePosition-Funktion (D2d1effecthelpers. h)
description: Gibt den Wert der Eingabe Szenen \_ Position zurück. Nur verfügbar, wenn \_ \_ für D2D \_ die Szenen Position in der Quelldatei deklariert ist.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- D2DGetScenePosition-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365642"
---
# <a name="d2dgetsceneposition-function"></a>D2DGetScenePosition-Funktion

Gibt den Wert der Eingabe Szenen \_ Position zurück. Nur verfügbar, wenn \_ \_ für D2D \_ die Szenen Position in der Quelldatei deklariert ist.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein **float4** -Wert in der Format Szenen \_ Position zurück.

## <a name="remarks"></a>Bemerkungen

Im folgenden Beispiel wird die Verwendung der-Funktion zum Erstellen eines Auflösungs Musters veranschaulicht.

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
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

 

 





