---
description: 'D3DXVec3UnprojectArray-Funktion (D3dx9math.h): Projiziert ein Array (x, y, z, 0) aus dem Bildschirmbereich in den Objektbereich.'
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: D3DXVec3UnprojectArray-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67e42b30a8f8d44bb9b21668a515a202436b7631
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097718"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a>D3DXVec3UnprojectArray-Funktion (D3dx9math.h)

Projiziert ein Array (x, y, z, 0) aus dem Bildschirmbereich in den Objektbereich.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*OutStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Schreitet zwischen Vektoren im Ausgabedatenstrom.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)

</dd> <dt>

*VStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Schreitet zwischen Vektoren im Eingabedatenstrom.

</dd> <dt>

*pViewport* \[ In\]
</dt> <dd>

Typ: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Zeiger auf eine [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) die den Viewport darstellt.

</dd> <dt>

*pProjection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Projektionsmatrix darstellt.

</dd> <dt>

*pView* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Ansichtsmatrix darstellt.

</dd> <dt>

*pWorld* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Weltmatrix darstellt.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) bei der es sich um das Array handelt, das vom Bildschirmbereich in den Objektraum projiziert wird.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die [**D3DXVec3Unproject-Funktion**](d3dxvec3unproject.md) als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Project**](d3dxvec3project.md)
</dt> </dl>

 

 
