---
description: Erstellt ein Mesh-Objekt mit einem Deklarator.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: D3DX10CreateMesh-Funktion (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354399"
---
# <a name="d3dx10createmesh-function"></a>D3DX10CreateMesh-Funktion

Erstellt ein Mesh-Objekt mit einem Deklarator.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), das Geräte Objekt, das dem Mesh zugeordnet werden soll.

</dd> <dt>

*pdeclaration* \[ in\]
</dt> <dd>

Type: **Konstanten [**d3d10 \_ input- \_ Element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Array von [**d3d10 \_ input \_ Element \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) -Elementen, das das Vertex-Format für das zurückgegebene Mesh beschreibt. Dieser Parameter muss einem flexiblen Scheitelpunkt Format (FVF) direkt zugeordnet werden.

</dd> <dt>

*Declcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente in der pdeclaration.

</dd> <dt>

*ppositionsemantic* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Semantik, die den Teil der Vertexdeklaration identifiziert, der Positionsinformationen enthält.

</dd> <dt>

*VertexCount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte für das Mesh. Dieser Parameter muss größer als 0 (null) sein.

</dd> <dt>

*FaceCount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Flächen für das Mesh. Der gültige Bereich für diese Zahl ist größer als 0 und ein kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus dem [**d3dx10 \_ Mesh**](d3dx10-mesh.md), das Optionen für das Mesh angibt.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Adresse eines Zeigers auf eine [**ID3DX10Mesh-Schnittstelle**](id3dx10mesh.md), die das erstellte Mesh-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX-Funktionen](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
