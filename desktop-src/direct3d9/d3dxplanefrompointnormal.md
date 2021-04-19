---
description: Erstellt eine Ebene von einem Punkt und einem normalen.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: D3DXPlaneFromPointNormal-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364343"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a>D3DXPlaneFromPointNormal-Funktion (D3dx9math. h)

Erstellt eine Ebene von einem Punkt und einem normalen.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*PPoint* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den zum Erstellen der Ebene verwendeten Punkt definiert.

</dd> <dt>

*pnormal* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das normale definiert, das zum Erstellen der Ebene verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die aus dem Punkt und der normalen erstellt wurde.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXPlaneFromPointNormal** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneFromPoints**](d3dxplanefrompoints.md)
</dt> </dl>

 

 




