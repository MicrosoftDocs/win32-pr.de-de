---
description: Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH-Enumeration (D3DX10Mesh. h)
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
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361890"
---
# <a name="d3dx10_mesh-enumeration"></a>D3dx10 \_ Mesh-Enumeration

Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3dx10 \_ Mesh \_ 32- \_ Bit**
</dt> <dd>

Das Mesh verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes. Siehe Hinweise.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3dx10 \_ Mesh-Sicherheit \_ \_**
</dt> <dd>

Signalisiert, dass das Mesh Geometrie-Shader-Daten enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein 32-Bit-Mesh (D3DXMESH \_ 32 Bit) kann theoretisch (2 ³ ²)-1 Gesichter und Scheitel Punkte unterstützen. Das belegen von Speicher für ein Mesh, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




