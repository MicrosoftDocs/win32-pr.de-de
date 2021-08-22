---
title: D2DGetScenePosition-Funktion (D2d1effecthelpers.h)
description: Gibt den Wert der EingabePOSITION DER SZENE \_ zurück. Nur verfügbar, wenn D2D \_ REQUIRES SCENE POSITION in der \_ \_ Quelldatei deklariert ist.
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
ms.openlocfilehash: fbcd7a1ee987cf64a92aa76b0f8910bee1c9a15465872bbd3ccfe2502629f700
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641640"
---
# <a name="d2dgetsceneposition-function"></a>D2DGetScenePosition-Funktion

Gibt den Wert der EingabePOSITION DER SZENE \_ zurück. Nur verfügbar, wenn D2D \_ REQUIRES SCENE POSITION in der \_ \_ Quelldatei deklariert ist.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **float4 im** Format SCENE \_ POSITION zurück.

## <a name="remarks"></a>Hinweise

Das folgende Beispiel zeigt die Verwendung der -Funktion beim Generieren eines musters.

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
| Header<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> <dt>

[HLSL-Hilfsatoren](hlsl-helpers.md)
</dt> </dl>

 

 





