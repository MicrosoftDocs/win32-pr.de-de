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
ms.openlocfilehash: cc744536336a4a102bafeaeae3ba87bbad58eb97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113358"
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

Zeiger auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), das Geräteobjekt, das dem Netz zugeordnet werden soll.

</dd> <dt>

*pDeclaration* \[ In\]
</dt> <dd>

Typ: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Array von [**D3D10 \_ INPUT ELEMENT \_ \_ DESC-Elementen,**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) das das Scheitelpunktformat für das zurückgegebene Netz beschreibt. Dieser Parameter muss direkt einem flexiblen Scheitelpunktformat (FVF) zuordnen.

</dd> <dt>

*DeclCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente in pDeclaration.

</dd> <dt>

*pPositionSemantic* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Semantik, die identifiziert, welcher Teil der Scheitelpunktdeklaration Positionsinformationen enthält.

</dd> <dt>

*VertexCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelzeichen für das Gitternetz. Dieser Parameter muss größer als 0 sein.

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



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX-Funktionen](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
