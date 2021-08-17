---
description: Gibt einen flexiblen Vertexformatcode (FVF) von einem Deklarator zurück.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: D3DXFVFFromDeclarator-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 5f9bad9968a52fb6c3b11de96936f48e432bd038e172318cb52f21fad4b08ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525647"
---
# <a name="d3dxfvffromdeclarator-function"></a>D3DXFVFFromDeclarator-Funktion

Gibt einen flexiblen Vertexformatcode (FVF) von einem Deklarator zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDeclaration* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die den FVF-Code beschreiben.

</dd> <dt>

*pFVF* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf einen DWORD-Wert, der die zurückgegebene Kombination von [D3DFVF darstellt,](d3dfvf.md) die das vom Deklarator zurückgegebene Scheitelpunktformat beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Funktion kann nicht für jeden Deklarator verwendet werden, der einer FVF nicht direkt zufällt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
