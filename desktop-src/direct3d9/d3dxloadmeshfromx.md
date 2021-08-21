---
description: Lädt ein Gitter aus einer DirectX-X-Datei.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: D3DXLoadMeshFromX-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3c8c824c994cf852bc1d18eec33c4ce169b2c0ac824fc954f7207476b6a87ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044978"
---
# <a name="d3dxloadmeshfromx-function"></a>D3DXLoadMeshFromX-Funktion

Lädt ein Gitter aus einer DirectX-X-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFilename* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination eines oder mehrerer Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angibt.

</dd> <dt>

*pD3DDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das dem Gittermodell zugeordnete Geräteobjekt.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der Adjacency-Daten enthält. Die Adjacency-Daten enthalten ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppMaterials* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der Materialdaten enthält. Der Puffer enthält ein Array von [**D3DXMATERIAL-Strukturen,**](d3dxmaterial.md) das Informationen aus der DirectX-Datei enthält. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der ein Array von Effektinstanzen enthält, eine pro Attributgruppe im zurückgegebenen Netz. Eine Effect-Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet wird. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ out\]
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

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXLoadMeshFromXW auflösen. Andernfalls wird der Funktionsaufruf in D3DXLoadMeshFromXA auflösen, da ANSI-Zeichenfolgen verwendet werden.

Alle Gitternetze in der Datei werden zu einem Ausgabegitternetz reduziert. Wenn die Datei eine Rahmenhierarchie enthält, werden alle Transformationen auf das Gitternetz angewendet.

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

 

 
