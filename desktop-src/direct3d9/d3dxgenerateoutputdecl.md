---
description: Generiert eine Ausgabe-Scheitelpunkt Deklaration aus der Eingabe Deklaration. Die Ausgabe Deklaration ist für die Verwendung durch die Gitter Mosaik Funktionen vorgesehen.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: D3DXGenerateOutputDecl-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355010"
---
# <a name="d3dxgenerateoutputdecl-function"></a>D3DXGenerateOutputDecl-Funktion

Generiert eine Ausgabe-Scheitelpunkt Deklaration aus der Eingabe Deklaration. Die Ausgabe Deklaration ist für die Verwendung durch die Gitter Mosaik Funktionen vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*poutput* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

Zeiger zur Ausgabe Scheitelpunkt Deklaration. Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pinput* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Ein Zeiger auf die Deklaration der Eingabe Vertex. Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




