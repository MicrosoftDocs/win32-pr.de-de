---
description: Speichert ein Gitternetz in einer X-Datei.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: D3DXSaveMeshToX-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 668131237def6078d775d0002f624b035ad29e21b9a49399b673933dc63e5b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988437"
---
# <a name="d3dxsavemeshtox-function"></a>D3DXSaveMeshToX-Funktion

Speichert ein Gitternetz in einer X-Datei.

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

*pFilename* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das Gitternetz darstellt, das in einer X-Datei gespeichert werden soll.

</dd> <dt>

*pAdjacency* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben. Dieser Parameter kann NULL **sein.**

</dd> <dt>

*pMaterials* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Zeiger auf ein Array von [**D3DXMATERIAL-Strukturen**](d3dxmaterial.md) mit Materialinformationen, die in der X-Datei gespeichert werden sollen.

</dd> <dt>

*pEffectInstances* \[ In\]
</dt> <dd>

Typ: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Zeiger auf ein Array von Effektinstanzen, eine pro Attributgruppe im Gitternetz. Dieser Parameter kann NULL **sein.** Eine Effect-Instanz ist eine bestimmte Instanz von Zustandsinformationen, die zum Initialisieren eines Effekts verwendet wird. Weitere Informationen finden Sie unter [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der [**D3DXMATERIAL-Strukturen**](d3dxmaterial.md) im *pMaterials-Array.*

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus Dateiformat und Speicheroptionen beim Speichern einer X-Datei. Weitere Informationen [finden Sie unter D3DX X-Dateikonst constants](dx9-graphics-reference-d3dx-x-file-constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXSaveMeshToXW auflösen. Andernfalls wird der Funktionsaufruf in D3DXSaveMeshToXA auflösen, da ANSI-Zeichenfolgen verwendet werden.

Das Standarddateiformat ist binär. Wenn eine Datei jedoch sowohl als Binärdatei als auch als Textdatei angegeben wird, wird sie als Textdatei gespeichert. Unabhängig vom Dateiformat können Sie auch das komprimierte Format verwenden, um die Dateigröße zu reduzieren.

Im Folgenden finden Sie ein typisches Codebeispiel für die Verwendung dieser Funktion.


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

 

 
