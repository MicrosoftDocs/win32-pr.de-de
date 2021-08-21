---
description: Lädt ein Patchgittermodell aus einem ID3DXFileData-Objekt.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: D3DXLoadPatchMeshFromXof-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8bfdf0faf0a9a8d8d32d38899cdd666d7c4a5d3910119ac36cbca2bf8bb33430
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564830"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a>D3DXLoadPatchMeshFromXof-Funktion

Lädt ein Patchgittermodell aus einem [**ID3DXFileData-Objekt.**](id3dxfiledata.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pxofMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Zeiger auf eine [**ID3DXFileData-Schnittstelle,**](id3dxfiledata.md) die das zu ladende Dateidatenobjekt darstellt.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [**D3DXMESH-Flags,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*pD3DDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät, von dem aus das Gitternetz erstellt wird.

</dd> <dt>

*ppMaterials* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Array von Materialien, die im Gitternetz enthalten sind. Jedes Material wird durch eine [**ID3DXBuffer-Schnittstelle**](id3dxbuffer.md) indiziert.

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der ein Array von Effektinstanzen enthält, eine pro Attributgruppe im zurückgegebenen Gitternetz. Eine Effektinstanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Weitere Informationen zum Zugriff auf den Puffer finden Sie unter [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*pNumMaterials* \[ out\]
</dt> <dd>

Typ: **PDWORD**

Zeiger, der die Anzahl der Materialien im Gitternetz enthält.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXPatchMesh-Schnittstelle,**](id3dxpatchmesh.md) die das geladene Gitternetz darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Für Meshdateien, die keine Effektinstanzinformationen enthalten, werden Standardeffektinstanzen aus den Materialinformationen in der X-Datei generiert. Eine Default Effect-Instanz hat Standardwerte, die den Membern der [**D3DMATERIAL9-Struktur**](d3dmaterial9.md) entsprechen.

Der Standardtexturname ist ebenfalls ausgefüllt, wird jedoch anders behandelt. Der Name lautet Texture0@Name , was einer Effektvariablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name" entspricht. Dieser enthält den Namen der Zeichenfolgendatei für die Textur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
