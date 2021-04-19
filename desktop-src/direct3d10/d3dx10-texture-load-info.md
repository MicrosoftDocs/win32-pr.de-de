---
description: Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: D3DX10_TEXTURE_LOAD_INFO-Struktur (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355206"
---
# <a name="d3dx10_texture_load_info-structure"></a>D3dx10 \_ Textur \_ Lade- \_ Informationsstruktur

Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**psrcbox**
</dt> <dd>

Typ: **[ **d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Quell Textur Feld (siehe [**d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pdstbox**
</dt> <dd>

Typ: **[ **d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Ziel Textur Feld (siehe [**d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**Srcfirstmip**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

MipMap-Ebene der Quell Textur. Weitere Informationen finden Sie unter [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .

</dd> <dt>

**Dstfirstmip**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die MipMap-Ebene der Ziel Textur. weitere Details finden Sie unter [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .

</dd> <dt>

**Nummips**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von MipMap-Ebenen in der Quell Textur.

</dd> <dt>

**Srcfirstelement**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Erstes Element der Quell Textur.

</dd> <dt>

**Dstfirstelement**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Erstes Element der Ziel Textur.

</dd> <dt>

**NumElements**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der zu ladenden Elemente.

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filteroptionen während der erneuten Stichprobenentnahme (siehe [**d3dx10 \_ Filter \_ Flag**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filteroptionen beim Erzeugen von Mip-Ebenen (siehe [**d3dx10 \_ Filter \_ Flag**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in einem [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md)-aufrufswert verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
