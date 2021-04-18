---
description: Diese Konstante ist die maximale Anzahl von Vertex-Deklaratoren für ein Mesh.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: MAX_FVF_DECL_SIZE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371905"
---
# <a name="max_fvf_decl_size-enumeration"></a>Maximal zulässige Anzahl von \_ f- \_ decl- \_ Größen

Diese Konstante ist die maximale Anzahl von Vertex-Deklaratoren für ein Mesh.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**maximale \_ Größe der f- \_ decl \_**
</dt> <dd>

Die maximale Anzahl von Elementen in der Vertex-Deklaration. Der zusätzliche (+ 1) ist für [**D3DDECL \_ End**](d3ddecl-end.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

MAXD3DDECLLENGTH wird als Maximum von 64 definiert (siehe d3d9types. h). Dies schließt nicht das "End"-markervertex-Element ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**GetDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
