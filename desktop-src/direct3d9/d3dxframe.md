---
description: Kapselt einen Transformations Rahmen in einer Transformations Frame Hierarchie.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: D3DXFRAME-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219514"
---
# <a name="d3dxframe-structure"></a>D3DXFRAME-Struktur

Kapselt einen Transformations Rahmen in einer Transformations Frame Hierarchie.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **LPSTR**

</dd> <dd>

Der Name des Frames.

</dd> <dt>

**Transformationmatrix**
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

Transformationsmatrix.

</dd> <dt>

**pmeshcontainer**
</dt> <dd>

Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

Zeiger auf den Mesh-Container.

</dd> <dt>

**pframesierend**
</dt> <dd>

Typ: * * * * D3DXFRAME **\***

</dd> <dd>

Zeiger auf einen gleich geordneten Frame.

</dd> <dt>

**pframefirstchild**
</dt> <dd>

Typ: * * * * D3DXFRAME **\***

</dd> <dd>

Zeiger auf einen untergeordneten Frame.

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

 

 




