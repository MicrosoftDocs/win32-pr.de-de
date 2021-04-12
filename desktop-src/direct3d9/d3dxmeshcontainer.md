---
description: Kapselt ein Mesh-Objekt in einer Transformations Frame Hierarchie.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: D3DXMESHCONTAINER-Struktur (D3dx9anim. h)
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
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354177"
---
# <a name="d3dxmeshcontainer-structure"></a>D3DXMESHCONTAINER-Struktur

Kapselt ein Mesh-Objekt in einer Transformations Frame Hierarchie.

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

Netz Name.

</dd> <dt>

**Meshdata**
</dt> <dd>

Typ: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Der Typ der Daten im Mesh. Siehe [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**pmaterials**
</dt> <dd>

Typ: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Array von Mesh-Material. Siehe [**D3DXMATERIAL**](d3dxmaterial.md).

</dd> <dt>

**Peer-ffects**
</dt> <dd>

Typ: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Zeiger auf einen Satz von Standardeffekt Parametern. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**Nummaterial**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Materialien im Mesh.

</dd> <dt>

**padjacency**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Ein Zeiger auf ein Array von drei DWORDs pro Dreieck des Netzes, das Informationen zu Informationen enthält.

</dd> <dt>

**pskininfo**
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Ein Zeiger auf die Skin Information-Schnittstelle. Siehe [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**pnextmeschcontainer**
</dt> <dd>

Typ: * * * * D3DXMESHCONTAINER **\***

</dd> <dd>

Zeiger auf den nächsten Mesh-Container.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann von dieser Struktur abgeleitet werden, um weitere Daten hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
