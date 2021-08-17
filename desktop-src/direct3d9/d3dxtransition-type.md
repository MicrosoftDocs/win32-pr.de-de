---
description: Definiert den Übergangsstil zwischen Werten einer Gitternetzanimation.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: D3DXTRANSITION_TYPE -Enumeration (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f451b94fe204a82cd15c65e424cc214025aa670f82af5224897100cbc6f8f6e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730937"
---
# <a name="d3dxtransition_type-enumeration"></a>D3DXTRANSITION \_ TYPE-Enumeration

Definiert den Übergangsstil zwischen Werten einer Gitternetzanimation.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ LINEAR**
</dt> <dd>

Linearer Übergang zwischen Werten.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Einfaches, einfaches Splineübergang zwischen Werten.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Berechnung für die Rampe von "ease in" bis "ease out" wird wie folgt berechnet:

<dl> Q(t) = 2(x - y)t) + 3(y - x)t× + x  
</dl>

Wobei die Rampe eine Funktion Q(t) mit den folgenden Eigenschaften ist:

-   Q(t) ist ein kubischer Spline.
-   Q(t) interpoliert zwischen x und y, da t zwischen 0 und 1 liegt.
-   Q(t) ist horizontal, wenn t = 0 und t = 1.

Mathematischer Natur bedeutet dies:

<dl> Q(t) = At" + "Bt" + "Ct + D" (und daher "Q'(t)" = 3At taste + 2Bt + C)  
2a) Q(0) = x  
2b) Q(1) = y  
3a) Q'(0) = 0  
3b) Q'(1) = 0  
</dl>

Lösung für A, B, C, D:

<dl> D = x (aus 2a)  
C = 0 (von 3a)  
3A + 2B = 0 (von 3b)  
A + B = y - x (von 2b und D = x)  
</dl>

Deshalb gilt Folgendes:

<dl> A = 2(x - y), B = 3(y - x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




