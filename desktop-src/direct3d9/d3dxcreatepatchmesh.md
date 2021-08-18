---
description: Erstellt ein Gitternetz aus einem Steuerpatchgitter.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: D3DXCreatePatchMesh-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa4e1292f4b5c42515351d89dc7fc039f1f6f29201da72a78e07f447818e0f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988640"
---
# <a name="d3dxcreatepatchmesh-function"></a>D3DXCreatePatchMesh-Funktion

Erstellt ein Gitternetz aus einem Steuerpatchgitter.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInfo* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***

Struktur der Patchinformationen. Weitere Informationen finden Sie unter [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> <dt>

*dwNumPatches* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Patches.

</dd> <dt>

*dwNumVertices* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Kontrollvertices im Patch.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nicht verwendet. Für die spätere Verwendung reserviert.

</dd> <dt>

*pDecl* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) das das Scheitelpunktformat für das zurückgegebene Netz beschreibt.

</dd> <dt>

*pD3DDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeigen Sie auf das Gerät, das das Patchgittergerät erstellt. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pPatchMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Zeiger auf das [**erstellte ID3DXPatchMesh-Objekt.**](id3dxpatchmesh.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode verwendet ein Eingabepatchgitter und konvertiert es in ein mosaikiertes Gitter. Patchgitternetze verwenden 16-Bit-Indexpuffer. Daher sind Indizes für [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) 16 Bits.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXPATCHINFO**](d3dxpatchinfo.md)
</dt> </dl>

 

 
