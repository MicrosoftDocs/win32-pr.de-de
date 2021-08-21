---
description: Lädt ein Gittermodell aus einem ID3DXFileData-Objekt.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: D3DXLoadMeshFromXof-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 703ca249fd5ef8011824f9eb7afb5f833a3e4430a71f51c7ca72933a810b51a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044938"
---
# <a name="d3dxloadmeshfromxof-function"></a>D3DXLoadMeshFromXof-Funktion

Lädt ein Gittermodell aus einem [**ID3DXFileData-Objekt.**](id3dxfiledata.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pxofMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Zeiger auf eine [**ID3DXFileData-Schnittstelle,**](id3dxfiledata.md) die das zu ladende Dateidatenobjekt darstellt.

</dd> <dt>

*Optionen* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination eines oder mehrerer Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das dem Gittermodell zugeordnete Geräteobjekt.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der Adjacency-Daten enthält. Die Adjacency-Daten enthalten ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppMaterials* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md) Wenn die Methode zurückgegeben wird, wird dieser Parameter mit einem Array von [**D3DXMATERIAL-Strukturen**](d3dxmaterial.md) gefüllt.

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der ein Array von Effektinstanzen enthält, eine pro Attributgruppe im zurückgegebenen Netz. Eine Effect-Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet wird. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der [**D3DXMATERIAL-Strukturen**](d3dxmaterial.md) im *ppMaterials-Array,* wenn die Methode zurückgegeben wird.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das geladene Gitternetz darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Für Meshdateien, die keine Effektinstanzinformationen enthalten, werden Standardeffektinstanzen aus den Materialinformationen in der X-Datei generiert. Eine Standardeffektinstanz hat Standardwerte, die den Membern der [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) entsprechen.

Der Standardtexturname ist ebenfalls ausgefüllt, wird jedoch anders behandelt. Der Name ist , was einer Effektvariablen mit dem Namen "Texture0" mit einer Anmerkung Texture0@Name namens "Name" entspricht. Dieser enthält den Namen der Zeichenfolgendatei für die Textur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
