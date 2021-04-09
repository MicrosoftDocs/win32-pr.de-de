---
description: Mosaik Elemente in einem Dreiecks Gitter, das eine eckige Oberfläche für eine höhere Ordnung ist.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: D3DXTessellateTriPatch-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762018"
---
# <a name="d3dxtessellatetripatch-function"></a>D3DXTessellateTriPatch-Funktion

Mosaik Elemente in einem Dreiecks Gitter, das eine eckige Oberfläche für eine höhere Ordnung ist.

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

*PVB* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Vertex-Puffer, der die Patchdaten enthält.

</dd> <dt>

*pnumsek* \[ . in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von drei Gleit Komma Werten, die die Anzahl der Segmente identifizieren, in denen die einzelnen Kanten des Dreiecks Patches bei einem Mosaik Prozess aufgeteilt werden sollen. Siehe [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md).

</dd> <dt>

*pindecl* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Vertex-Deklarations Struktur, die die Scheitelpunkt Daten definiert. Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pzpatchinfo* \[ in\]
</dt> <dd>

Type: **[**D3TRIPATCH \_ Info**](d3dtripatch-info.md) \***

Beschreibt einen Dreiecks Patch. Siehe [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md).

</dd> <dt>

*pmesh* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf das erstellte Mesh. Siehe [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXTriPatchSize**](d3dxtripatchsize.md) , um die Anzahl der Ausgabe Scheitel Punkte und Indizes zu erhalten, die von der Mosaik Funktion benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
