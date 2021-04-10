---
description: Definiert den Übergangsstil zwischen den Werten einer Mesh-Animation.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: D3DXTRANSITION_TYPE-Enumeration (D3dx9anim. h)
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
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961590"
---
# <a name="d3dxtransition_type-enumeration"></a>D3DXTRANSITION- \_ Typenumeration

Definiert den Übergangsstil zwischen den Werten einer Mesh-Animation.

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

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ linear**
</dt> <dd>

Linearer Übergang zwischen Werten.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ easeingeeaseout**
</dt> <dd>

Vereinfachen Sie den Spline-Übergang zwischen den Werten.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Berechnung für die Rampe von Easy in zur Erleichterung wird wie folgt berechnet:

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

Dabei ist die-Rampe eine Funktion Q (t) mit den folgenden Eigenschaften:

-   Q (t) ist eine kubische Spline.
-   Q (t) interpoliert zwischen x und y als t zwischen 0 und 1.
-   Q (t) ist horizontal, wenn t = 0 und t = 1.

Mathematisch bedeutet dies Folgendes:

<dl> Q (t) = bei ³ + BT ² + CT + D (und somit q ' (t) = 3AT ² + 2BT + C)  
2a) Q (0) = x  
2B) Q (1) = y  
3a) Q ' (0) = 0  
3B) Q ' (1) = 0  
</dl>

Lösung für A, B, C, D:

<dl> D = x (von 2a)  
C = 0 (von 3a)  
3a + 2B = 0 (aus 3B)  
A + B = y-x (von 2B und D = x)  
</dl>

Deshalb gilt Folgendes:

<dl> A = 2 (x-y), B = 3 (y-x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




