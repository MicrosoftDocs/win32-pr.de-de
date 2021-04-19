---
description: Erstellt eine Links bündige Matrix.
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: D3DXMatrixLookAtLH-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fa7acdf467761bd3b3cfbc023662e9b3368b98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363167"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a>D3DXMatrixLookAtLH-Funktion (D3dx9math. h)

Erstellt eine Links bündige Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Peer* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Augen Punkt definiert. Dieser Wert wird bei der Übersetzung verwendet.

</dd> <dt>

*pAt* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Erscheinungsbild der Kamera definiert.

</dd> <dt>

*PUP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den aktuellen Globus definiert, normalerweise \[ 0, 1, 0 \] .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, bei der es sich um eine Links übergebene Matrix handelt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixLookAtLH** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




