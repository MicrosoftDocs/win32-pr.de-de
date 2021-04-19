---
description: Lädt ein Mesh aus dem Arbeitsspeicher.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: D3DXLoadMeshFromXInMemory-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373511"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a>D3DXLoadMeshFromXInMemory-Funktion

Lädt ein Mesh aus dem Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
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

Arbeits *Speicher* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf den Arbeitsspeicher Puffer, der die Mesh-Daten enthält.

</dd> <dt>

*Sizeofmemory* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe der Datei im Arbeitsspeicher in Bytes.

</dd> <dt>

*Optionen* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angibt.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.

</dd> <dt>

*ppency* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle. Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.

</dd> <dt>

*ppmaterials* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle. Wenn diese Methode zurückgegeben wird, wird dieser Parameter mit einem Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen gefüllt, das Informationen enthält, die in der DirectX-Datei gespeichert sind.

</dd> <dt>

*ppeer-ectinhaltungen* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der ein Array von Effekt Instanzen enthält, eine pro Attribut Gruppe im zurückgegebenen Mesh. Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pnummaterials* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *ppmaterials* -Array, wenn die Methode zurückgibt.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geladene Mesh darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Alle Netzen in der Datei werden in einem Ausgabe Mesh reduziert. Wenn die Datei eine Frame Hierarchie enthält, werden alle Transformationen auf das Mesh angewendet.

Bei Mesh-Dateien, die keine Effekts-Instanzinformationen enthalten, werden Standardeffekt Instanzen aus den Material Informationen in der x-Datei generiert. Eine Instanz des Standard Effekts verfügt über Standardwerte, die den Membern der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur entsprechen.

Der Standard Textur Name wird ebenfalls ausgefüllt, wird jedoch unterschiedlich behandelt. Der Name ist. dies Texture0@Name entspricht einer Effekt Variablen mit dem Namen "Texture0" mit einer Anmerkung namens "Name". Diese enthält den Namen der Zeichen folgen Datei für die Textur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
