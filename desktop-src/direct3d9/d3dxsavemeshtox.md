---
description: Speichert ein Mesh in einer x-Datei.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: D3DXSaveMeshToX-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361199"
---
# <a name="d3dxsavemeshtox-function"></a>D3DXSaveMeshToX-Funktion

Speichert ein Mesh in einer x-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das Mesh darstellt, das in einer x-Datei gespeichert werden soll.

</dd> <dt>

*padjacency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt. Dieser Parameter kann **null** sein.

</dd> <dt>

*pmaterials* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATERIAL**](d3dxmaterial.md) \***

Ein Zeiger auf ein Array von [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen, die Material Informationen enthalten, die in der x-Datei gespeichert werden sollen.

</dd> <dt>

" *Peer-ectinhaltungen* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Zeiger auf ein Array von Effekt Instanzen, eines pro Attribut Gruppe im Mesh. Dieser Parameter kann **null** sein. Eine Effekt Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet werden. Weitere Informationen finden Sie unter [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*Nummaterial* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der [**D3DXMATERIAL**](d3dxmaterial.md) -Strukturen im *pmaterials* -Array.

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus Dateiformat und Speicheroptionen beim Speichern einer x-Datei. Siehe [D3DX X-Datei Konstanten](dx9-graphics-reference-d3dx-x-file-constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveMeshToXW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXSaveMeshToXA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Das Standarddatei Format ist Binary. Wenn eine Datei jedoch sowohl als binäre als auch als Textdatei angegeben wird, wird Sie als Textdatei gespeichert. Unabhängig vom Dateiformat können Sie auch das komprimierte Format verwenden, um die Dateigröße zu verringern.

Im folgenden finden Sie ein typisches Codebeispiel für die Verwendung dieser Funktion.


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



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

 

 
