---
description: Erstellt ein leeres Skin-Mesh-Objekt mit einem Deklarator.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: D3DXCreateSkinInfo-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83ee214eb997414e113256060dbe59d3cd47d1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870111"
---
# <a name="d3dxcreateskininfo-function"></a>D3DXCreateSkinInfo-Funktion

Erstellt ein leeres Skin-Mesh-Objekt mit einem Deklarator.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte für das Skin-Mesh.

</dd> <dt>

*pdeclaration* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format für das zurückgegebene Mesh beschreibt.

</dd> <dt>

*Numbones* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Knochen für das Skin-Mesh.

</dd> <dt>

*ppskininfo* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse eines Zeigers auf eine [**ID3DXSkinInfo**](id3dxskininfo.md) -Schnittstelle, die das erstellte Skin-Mesh-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**setboneinfluence**](id3dxskininfo--setboneinfluence.md) , um das leere Skin-Mesh-Objekt aufzufüllen, das von dieser Methode zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**Setboneingefluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
