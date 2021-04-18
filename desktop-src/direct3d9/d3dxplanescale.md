---
description: Skalieren Sie die Ebene mit dem angegebenen Skalierungsfaktor.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: D3DXPlaneScale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354980"
---
# <a name="d3dxplanescale-function"></a>D3DXPlaneScale-Funktion

Skalieren Sie die Ebene mit dem angegebenen Skalierungsfaktor.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Skalierungsfaktor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die skalierte Ebene darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Daher kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
