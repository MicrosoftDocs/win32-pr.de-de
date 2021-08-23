---
title: D2DSampleInput-Funktion (D2d1effecthelpers.h)
description: Beispieleingabe N an Position uv. Nur für komplexe Eingaben verfügbar.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- D2DSampleInput-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c887221ade413b63456ecb3c4a91c7a5b480858b04e1f34e89506fdcf071dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075274"
---
# <a name="d2dsampleinput-function"></a>D2DSampleInput-Funktion

Beispieleingabe N an Position uv. Nur für komplexe Eingaben verfügbar.

## <a name="syntax"></a>Syntax

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Die Eingabenummer.

</dd> <dt>

*uv* \[ In\]
</dt> <dd>

Die UV-Position.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **float4** im Format TEXCOORDN zurück.

## <a name="remarks"></a>Hinweise

Das folgende Beispiel zeigt die Funktion, die zum Berechnen von Oberflächennormbreiten verwendet wird.

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effektshader-Verknüpfung](effect-shader-linking.md)
</dt> <dt>

[HLSL-Hilfshilfen](hlsl-helpers.md)
</dt> </dl>

 

 





