---
description: Kapselt ein Gittermodellobjekt in einer Transformationsrahmenhierarchie.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: D3DXMESHCONTAINER-Struktur (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 192b60c34c8a15c34a759bda8fd4f3350956003914f40578bd9c5efa54c772df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731666"
---
# <a name="d3dxmeshcontainer-structure"></a>D3DXMESHCONTAINER-Struktur

Kapselt ein Gittermodellobjekt in einer Transformationsrahmenhierarchie.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **LPSTR**

</dd> <dd>

Meshname.

</dd> <dt>

**MeshData**
</dt> <dd>

Typ: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Der Typ der Daten im Gitternetz. Siehe [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**pMaterials**
</dt> <dd>

Typ: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Array von Gitternetzmaterialien. Siehe [**D3DXMATERIAL**](d3dxmaterial.md).

</dd> <dt>

**pEffects**
</dt> <dd>

Typ: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Zeiger auf einen Satz von Standardeffektparametern. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**NumMaterials**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Materialien im Gitter.

</dd> <dt>

**pAdjacency**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Zeiger auf ein Array von drei DWORDs pro Dreieck des Gitters, das Informationen zur Adjacency enthält.

</dd> <dt>

**pSkinInfo**
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Zeiger auf die Skininformationsschnittstelle. Siehe [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**pNextMeshContainer**
</dt> <dd>

Typ: ".D3DXMESHCONTAINER"**\***

</dd> <dd>

Zeiger auf den nächsten Meshcontainer.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Anwendung kann von dieser Struktur ableiten, um weitere Daten hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
