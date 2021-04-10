---
description: Der Member der Vertex-decl, an dem die Software angezeigt werden soll. Dies wird mit der ID3DX10SkinInfo::D osoftwareskinning-API verwendet.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: D3DX10_SKINNING_CHANNEL-Struktur (d3dx10. h)
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
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219574"
---
# <a name="d3dx10_skinning_channel-structure"></a>D3dx10 \_ Skinning \_ Channel-Struktur

Der Member der Vertex-decl, an dem die Software angezeigt werden soll. Dies wird mit der [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) -API verwendet.

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

**SrcOffset**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang jedes Quell Scheitel Punkts.

</dd> <dt>

**Destoffset**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang jedes Ziel Scheitel Punkts.

</dd> <dt>

**IsNormal**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Bestimmt, welches Array von Matrizen in der [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) -API verwendet werden soll. Wenn dieser Wert true ist, wird *pinverpinversiot bonematrices* verwendet; andernfalls werden *pbonematrices* verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
