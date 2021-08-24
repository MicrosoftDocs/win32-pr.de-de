---
description: 'D3DX10CreateMesh-Funktion: Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.'
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: D3DX10CreateMesh-Funktion (D3DX10Mesh.h)
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
ms.openlocfilehash: a4f044d3337a2da05eb78b027492b870f450e4309c94faa8c72db935437511dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853480"
---
# <a name="d3dx10createmesh-function"></a>D3DX10CreateMesh-Funktion

Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.

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

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), das Geräteobjekt, das dem Gittermodell zugeordnet werden soll.

</dd> <dt>

*pDeclaration* \[ In\]
</dt> <dd>

Typ: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Array von [**D3D10 \_ INPUT ELEMENT \_ \_ DESC-Elementen,**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) das das Scheitelpunktformat für das zurückgegebene Gitternetz beschreibt. Dieser Parameter muss direkt einem flexiblen Vertexformat (FVF) zugeordnet werden.

</dd> <dt>

*DeclCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente in pDeclaration.

</dd> <dt>

*pPositionSemantic* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Semantik, die angibt, welcher Teil der Scheitelpunktdeklaration Positionsinformationen enthält.

</dd> <dt>

*VertexCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte für das Gitternetz. Dieser Parameter muss größer als 0 sein.

</dd> <dt>

*FaceCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Gesichter für das Gitternetz. Der gültige Bereich für diese Zahl ist größer als 0 und einer kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren Flags aus dem [**D3DX10 \_ MESH,**](d3dx10-mesh.md)die Optionen für das Gitternetz angeben.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Adresse eines Zeigers auf eine [**ID3DX10Mesh-Schnittstelle,**](id3dx10mesh.md)die das erstellte Gittermodellobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX-Funktionen](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
