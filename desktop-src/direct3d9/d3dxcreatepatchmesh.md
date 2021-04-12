---
description: Erstellt ein Mesh aus einem Steuerelement patchmesh.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: D3DXCreatePatchMesh-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355857"
---
# <a name="d3dxcreatepatchmesh-function"></a>D3DXCreatePatchMesh-Funktion

Erstellt ein Mesh aus einem Steuerelement patchmesh.

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

*pinfo* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***

Struktur der Patchinformationen. Weitere Informationen finden Sie unter [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> <dt>

*dwnumpatches* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Patches.

</dd> <dt>

*dwnumvertices* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Steuerungs Scheitel Punkte im Patch.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nicht verwendet. Reserviert für die spätere Verwendung.

</dd> <dt>

*pdecl* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format für das zurückgegebene Mesh beschreibt.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät, das das patchmesh erstellt. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*ppatchmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Zeiger auf das [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Objekt, das erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode nimmt ein eingaberpatchmesh an und konvertiert es in ein Mosaik Gitter. Patchnetze verwenden 16-Bit-Index Puffer. Daher sind Indizes zu [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) 16 Bits.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXPATCHINFO**](d3dxpatchinfo.md)
</dt> </dl>

 

 
