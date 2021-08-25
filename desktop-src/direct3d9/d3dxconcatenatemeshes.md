---
description: Verkettet eine Gruppe von Gitternetzen zu einem gemeinsamen Gitternetz. Diese Methode kann optional eine Matrixtransformation auf jedes Eingabegitternetz und seine Texturkoordinaten anwenden.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: D3DXConcatenateMeshes-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21801c2f4b8ef8dd2a34c9788b402128da4ce4fed33c3c38a08e61c35a847e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857390"
---
# <a name="d3dxconcatenatemeshes-function"></a>D3DXConcatenateMeshes-Funktion

Verkettet eine Gruppe von Gitternetzen zu einem gemeinsamen Gitternetz. Diese Methode kann optional eine Matrixtransformation auf jedes Eingabegitternetz und seine Texturkoordinaten anwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMeshes* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Array von Eingabegitternetzzeigern (siehe [**ID3DXMesh**](id3dxmesh.md)). Die Anzahl der Elemente im Array ist NumMeshes.

</dd> <dt>

*NumMeshes* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der zu verkettenden Eingabegitternetze.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Optionen für die Mesherstellung; Dies ist eine Kombination aus einem oder mehreren [**D3DXMESH-Flags.**](./d3dxmesh.md) Die Optionen für die Mesherstellung entsprechen dem Optionsparameter, der von [**D3DXCreateMesh**](d3dxcreatemesh.md)benötigt wird.

</dd> <dt>

*pGeomXForms* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Optionales Array von Geometrietransformationen. Die Anzahl der Elemente im Array ist NumMeshes. jedes Element ist eine Transformationsmatrix (siehe [**D3DXMATRIX**](d3dxmatrix.md)). Kann **NULL** sein.

</dd> <dt>

*pTextureXForms* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Optionales Array von Texturtransformationen. Die Anzahl der Elemente im Array ist NumMeshes. jedes Element ist eine Transformationsmatrix (siehe [**D3DXMATRIX**](d3dxmatrix.md)). Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pDecl* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Optionaler Zeiger auf eine Scheitelpunktdeklaration (siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)). Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pD3DDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf ein [**IDirect3DDevice9-Gerät,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das zum Erstellen des neuen Gitternetzes verwendet wird.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf das erstellte Gitternetz (siehe [**ID3DXMesh**](id3dxmesh.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Wenn keine [Scheitelpunktdeklaration](vertex-declaration.md) als Teil des Options mesh creation-Parameters angegeben wird, generiert die Methode eine Vereinigung aller Scheitelpunktdeklarationen der Untermeshes, wobei bei Bedarf Kanäle und Typen heraufstreckt werden. Die -Methode erstellt eine Attributtabelle aus Attributtabellen der Eingabegitternetze. Um die Erstellung einer Attributtabelle sicherzustellen, rufen [**Sie Optimieren**](id3dxmesh--optimize.md) mit Flags auf, die auf D3DXMESHOPT \_ COMPACT und D3DXMESHOPT ATTRSORT festgelegt sind \_ (siehe [**D3DXMESHOPT**](./d3dxmeshopt.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
