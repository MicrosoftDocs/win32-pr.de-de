---
description: 'D3DX10_MESH-Enumeration: Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.'
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH-Enumeration (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105438"
---
# <a name="d3dx10_mesh-enumeration"></a>D3DX10 \_ MESH-Enumeration

Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ 32 \_ BIT**
</dt> <dd>

Das Gitternetz verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes. Siehe Hinweise.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ MESH \_ GS \_ ADJAZ**
</dt> <dd>

Signalisiert, dass das Gitternetz Geometrie-Shader-Adjazenzdaten enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein 32-Bit-Gitternetz (D3DXMESH \_ 32BIT) kann theoretisch (2)-1 Gesichter und Scheitelpunkte unterstützen. Die Zuweisung von Arbeitsspeicher für ein Gitternetz, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




