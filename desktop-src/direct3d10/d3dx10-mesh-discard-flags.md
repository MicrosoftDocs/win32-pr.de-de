---
description: Gibt an, welche Teile von Mesh-Daten vom Gerät verworfen werden sollen. Wird mit ID3DX10Mesh::D iscard verwendet.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: D3DX10_MESH_DISCARD_FLAGS-Enumeration (D3DX10Mesh. h)
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
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961710"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>D3dx10 \_ Mesh \_ Verwerfungs \_ Flags-Enumeration

Gibt an, welche Teile von Mesh-Daten vom Gerät verworfen werden sollen. Wird mit [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md)verwendet.

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

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3dx10 \_ Mesh \_ - \_ Attribut \_ Puffer verwerfen**
</dt> <dd>

Verwerfen Sie den Attribut Puffer.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3dx10 \_ Mesh \_ - \_ Attribut \_ Tabelle verwerfen**
</dt> <dd>

Verwerfen Sie die Attribut Tabelle.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3dx10- \_ Mesh- \_ \_ pointreps verwerfen**
</dt> <dd>

Verwerfen Sie den Zeiger Mitarbeiter-Puffer.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3dx10 \_ Mesh- \_ Verwerfungs \_ Fähigkeit**
</dt> <dd>

Verwerfen Sie den annähernden Puffer.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3dx10 \_ Mesh \_ - \_ Geräte \_ Puffer verwerfen**
</dt> <dd>

Verwerfen Sie die Puffer, die an das Gerät übertragen wurden (mit [**ID3DX10Mesh:: commitcomdevice**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




