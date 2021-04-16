---
description: Berechnen Sie den Fresnel-Begriff.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: D3DXFresnelTerm-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531052"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>D3DXFresnelTerm-Funktion (D3DX10Math. h)

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
