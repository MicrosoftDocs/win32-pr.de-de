---
description: Verkettet eine Gruppe von Netzen zu einem gemeinsamen Mesh. Diese Methode kann optional eine Matrix Transformation auf jedes Eingabe Mesh und seine Texturkoordinaten anwenden.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: D3DXConcatenateMeshes-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371924"
---
# <a name="d3dxconcatenatemeshes-function"></a>D3DXConcatenateMeshes-Funktion

Verkettet eine Gruppe von Netzen zu einem gemeinsamen Mesh. Diese Methode kann optional eine Matrix Transformation auf jedes Eingabe Mesh und seine Texturkoordinaten anwenden.

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

*ppmeshes* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Array von Eingabe Gitter Zeigern (siehe [**ID3DXMesh**](id3dxmesh.md)). Die Anzahl der Elemente im Array ist nummeshes.

</dd> <dt>

*Nummeshes* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Eingabe-Netzen, die verkettet werden sollen.

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gitter Erstellungs Optionen; Dies ist eine Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags. Die Gitter Erstellungs Optionen entsprechen dem Optionsparameter, der für [**D3DXCreateMesh**](d3dxcreatemesh.md)erforderlich ist.

</dd> <dt>

*pgeomxforms* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Optionales Array von Geometrie Transformationen. Die Anzahl der Elemente im Array ist nummeshes. jedes Element ist eine Transformationsmatrix (siehe [**D3DXMATRIX**](d3dxmatrix.md)). Kann **null** sein.

</dd> <dt>

*ptexturexforms* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Optionales Array von Textur Transformationen. Die Anzahl der Elemente im Array ist nummeshes. jedes Element ist eine Transformationsmatrix (siehe [**D3DXMATRIX**](d3dxmatrix.md)). Dieser Parameter kann **null** sein.

</dd> <dt>

*pdecl* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Optionaler Zeiger auf eine Scheitelpunkt Deklaration (siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)). Dieser Parameter kann **null** sein.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf ein [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Gerät, das zum Erstellen des neuen Netzes verwendet wird.

</dd> <dt>

*ppmeshout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf das erstellte Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert eines der folgenden Werte sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Wenn keine [Scheitelpunkt Deklaration](vertex-declaration.md) als Teil des Optionen Gitter Erstellungs-Parameters angegeben wird, generiert die Methode eine Vereinigung aller Scheitelpunkt Deklarationen der Subnetze und fördert ggf. Kanäle und Typen. Die-Methode erstellt eine Attribut Tabelle aus Attribut Tabellen der Eingabe-Meshes. Um die Erstellung einer Attribut Tabelle sicherzustellen, führen Sie " [**optimieren**](id3dxmesh--optimize.md) " mit Flags aus, die auf D3DXMESHOPT \_ Compact und D3DXMESHOPT \_ attrsort festgelegt sind (siehe [**D3DXMESHOPT**](./d3dxmeshopt.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
