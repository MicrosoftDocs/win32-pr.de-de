---
description: Erstellt ein leeres Skin mesh-Objekt mithilfe eines flexiblen Vertexformatcodes (FVF).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: D3DXCreateSkinInfoFVF-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ccf10bad879b51f42c743ddd18112e24d355b366691b7922816164e57ed1b3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495780"
---
# <a name="d3dxcreateskininfofvf-function"></a>D3DXCreateSkinInfoFVF-Funktion

Erstellt ein leeres Skin mesh-Objekt mithilfe eines flexiblen Vertexformatcodes (FVF).

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte für das Skin mesh.

</dd> <dt>

*FVF* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus [D3DFVF,](d3dfvf.md) die das Scheitelpunktformat für das zurückgegebene Skin mesh beschreibt.

</dd> <dt>

*NumBones* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl von Gittern für das Skin mesh.

</dd> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse eines Zeigers auf eine [**ID3DXSkinInfo-Schnittstelle,**](id3dxskininfo.md) die das erstellte Skininformationsobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**SetBoneInfluence,**](id3dxskininfo--setboneinfluence.md) um das leere Skin mesh-Objekt aufzufüllen, das von dieser Methode zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
