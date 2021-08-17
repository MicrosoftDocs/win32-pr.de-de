---
description: Mosaikt einen dreieckigen Oberflächenpatch höherer Ordnung in ein Dreiecksgitternetz.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: D3DXTessellateTriPatch-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1cae3ff9709cb74e15c176abc0e738e4f12d1417eec1d040b90269b7e3cbc6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122712"
---
# <a name="d3dxtessellatetripatch-function"></a>D3DXTessellateTriPatch-Funktion

Mosaikt einen dreieckigen Oberflächenpatch höherer Ordnung in ein Dreiecksgitternetz.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVB* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Vertexpuffer, der die Patchdaten enthält.

</dd> <dt>

*pNumSegs* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei Gleitkommawerten, die die Anzahl der Segmente identifizieren, in die jeder Rand des Dreieckspatches geteilt werden soll, wenn ein Mosaik verwendet wird. Siehe [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Vertexdeklarationsstruktur, die die Scheitelpunktdaten definiert. Siehe [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> <dt>

*pTriPatchInfo* \[ In\]
</dt> <dd>

Typ: **const [**D3TRIPATCH \_ INFO**](d3dtripatch-info.md) \***

Beschreibt einen Dreieckspatch. Siehe [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

</dd> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf das erstellte Gitternetz. Siehe [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**D3DXTriPatchSize,**](d3dxtripatchsize.md) um die Anzahl der Ausgabevertices und Indizes abzurufen, die die Mosaikfunktion benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
