---
description: Der Member der Scheitelpunkt-Decl, auf dem die Softwares skinning wird. Dies wird mit der ID3DX10SkinInfo::D oSoftwareSkinning-API verwendet.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: D3DX10_SKINNING_CHANNEL -Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b8e976ba1aecdeb792ba45fc4f60f25e7feb5a7dde3f7fc845a22962e441bf2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753530"
---
# <a name="d3dx10_skinning_channel-structure"></a>D3DX10 \_ SKINNING \_ CHANNEL-Struktur

Der Member der Scheitelpunkt-Decl, auf dem die Softwares skinning wird. Dies wird mit der [**ID3DX10SkinInfo::D oSoftwareSkinning-API**](id3dx10skininfo-dosoftwareskinning.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Member

<dl> <dt>

**Srcoffset**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang jedes Quellvertex.

</dd> <dt>

**DestOffset**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang jedes Ziel-Scheitelpunkts.

</dd> <dt>

**IsNormal**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Bestimmt, welches Array von Matrizen in der [**ID3DX10SkinInfo::D oSoftwareSkinning-API verwendet werden**](id3dx10skininfo-dosoftwareskinning.md) soll. Wenn dies zutrifft, wird *pInverseTransposeBoneMatrices* verwendet, *andernfalls pBoneMatrices.*

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
