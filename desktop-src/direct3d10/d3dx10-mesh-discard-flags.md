---
description: Gibt an, welche Teile der Gitternetzdaten vom Gerät verworfen werden. Wird mit ID3DX10Mesh::D iscard verwendet.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: D3DX10_MESH_DISCARD_FLAGS -Enumeration (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: d4b98550a2f3a896ed7b99f3e16f33a399a58035497e44420709ee8a0726901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989470"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>D3DX10 \_ MESH \_ DISCARD \_ FLAGS-Enumeration

Gibt an, welche Teile der Gitternetzdaten vom Gerät verworfen werden. Wird mit [**ID3DX10Mesh::D iscard verwendet.**](id3dx10mesh-discard.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10 \_ MESH \_ DISCARD \_ ATTRIBUTE \_ BUFFER**
</dt> <dd>

Verwerfen Sie den Attributpuffer.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10 \_ MESH \_ DISCARD \_ ATTRIBUTE \_ TABLE**
</dt> <dd>

Verwerfen Sie die Attributtabelle.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ MESH \_ DISCARD \_ POINTREPS**
</dt> <dd>

Verwerfen Sie den Puffer der Zeiger-Reps.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ MESH \_ DISCARD \_ ADJACENCY**
</dt> <dd>

Verwerfen Sie den Adjacency-Puffer.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10 \_ MESH \_ VERWERFEN VON \_ \_ GERÄTEPUFFERN**
</dt> <dd>

Verwerfen Sie die Puffer, die auf das Gerät übertragen wurden (mit [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




