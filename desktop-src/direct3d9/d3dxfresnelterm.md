---
description: Berechnen Sie den Fresnel-Begriff.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: D3DXFresnelTerm-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6c6dd19dd6b7b70c5eeb08051f9799756b0782
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354846"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>D3DXFresnelTerm-Funktion (D3dx9math. h)

Berechnen Sie den Fresnel-Begriff.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kostheta* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Wert muss zwischen 0 und 1 liegen.

</dd> <dt>

" *Refractionindex* \[ " in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der abbrechungs Index eines Materials. Der Wert muss größer als 1 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Diese Funktion gibt den Fresnel-Begriff für nicht polarisiertes Licht zurück. Costheta ist der Kosinus des Vorfall Winkels.

## <a name="remarks"></a>Bemerkungen

So finden Sie den Fresnel-Begriff (F):

Wenn ein der Winkel des Auftretens und B der Winkel der abbrechungs Angabe ist, dann


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Wenn Sie die drei-und Vereinfachung verwenden, erhalten Sie Folgendes:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
