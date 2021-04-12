---
description: Gibt einen FVF-Code (Flexible Vertex-Format) aus einem Deklarator zurück.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: D3DXFVFFromDeclarator-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354837"
---
# <a name="d3dxfvffromdeclarator-function"></a>D3DXFVFFromDeclarator-Funktion

Gibt einen FVF-Code (Flexible Vertex-Format) aus einem Deklarator zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdeclaration* \[ in\]
</dt> <dd>

Typ: **Konstanten [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das den Code für den Code von Code beschreibt.

</dd> <dt>

*pfvf* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf einen DWORD-Wert, der die zurückgegebene Kombination von [D3DFVF](d3dfvf.md) darstellt, die das vom Deklarator zurückgegebene Scheitelpunkt Format beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann für alle Deklaratoren, die nicht direkt einer FVF zugeordnet sind, nicht ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
