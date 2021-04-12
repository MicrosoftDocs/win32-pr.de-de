---
description: Mosaik einen rechteckigen Patch für eine höhere Ordnung in einem Dreiecks Gitter.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: D3DXTessellateRectPatch-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219493"
---
# <a name="d3dxtessellaterectpatch-function"></a>D3DXTessellateRectPatch-Funktion

Mosaik einen rechteckigen Patch für eine höhere Ordnung in einem Dreiecks Gitter.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
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

Ein Zeiger auf ein Array von vier Gleit Komma Werten, die die Anzahl der Segmente angeben, in die die einzelnen Kanten des Rechteck Patches bei einem Mosaik Prozess aufgeteilt werden sollen. Siehe [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md).

</dd> <dt>

*pindecl* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Vertex-Deklarations Struktur, die die Scheitelpunkt Daten definiert. Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*prectpatchinfo* \[ in\]
</dt> <dd>

Type: **[**D3DRECTPATCH \_ Info**](d3drectpatch-info.md) \***

Beschreibt einen rechteckigen Patch. Siehe [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md).

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

Verwenden Sie [**D3DXRectPatchSize**](d3dxrectpatchsize.md) , um die Anzahl der Ausgabe Scheitel Punkte und Indizes zu erhalten, die von der Mosaik Funktion benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
