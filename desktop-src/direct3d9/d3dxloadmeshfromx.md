---
description: Lädt ein Mesh aus einer DirectX. x-Datei.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: D3DXLoadMeshFromX-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354806"
---
# <a name="d3dxloadmeshfromx-function"></a>D3DXLoadMeshFromX-Funktion

Lädt ein Mesh aus einer DirectX. x-Datei.

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

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Optionen* \[ in\]
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

Zeiger auf einen Puffer, der die Daten enthält. Die Daten der Daten enthalten ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Mesh angeben. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppmaterials* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf einen Puffer, der Materialdaten enthält. Der Puffer enthält ein Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen, das Informationen aus der DirectX-Datei enthält. Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).

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

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadMeshFromXW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXLoadMeshFromXA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

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

 

 
