---
description: Gibt den Typ der auszuführenden Mesh-Optimierung an.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT-Enumeration (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355557"
---
# <a name="d3dx10_meshopt-enumeration"></a>D3dx10 \_ meshopt-Enumeration

Gibt den Typ der auszuführenden Mesh-Optimierung an.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3dx10 \_ meshopt \_ Compact**
</dt> <dd>

Ordnet Gesichter neu an, um nicht verwendete Vertices und Gesichter zu entfernen.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3dx10 \_ meshopt \_ attr \_ Sortieren**
</dt> <dd>

Ordnet Gesichter neu an, um die Leistung zu verbessern und die Leistung des Attribut Bündel Zustands zu optimieren.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3dx10 \_ meshopt- \_ Scheitelpunkt \_ Cache**
</dt> <dd>

Ordnet Gesichter neu an, um die Cache Treffer Rate von Vertex-Caches zu erhöhen.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3dx10 \_ meshopt \_ Strip \_ neu anordnen**
</dt> <dd>

Ordnet Flächen neu an, um die Länge der angrenzenden Dreiecke zu maximieren

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3dx10 \_ meshopt \_ ignoriert \_**
</dt> <dd>

Nur Gesichter optimieren; Optimieren Sie die Vertices nicht.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3dx10 \_ meshopt \_ \_ nicht \_ teilen**
</dt> <dd>

Bei der Attribut Sortierung werden Vertices, die von Attribut Gruppen gemeinsam verwendet werden, nicht aufgeteilt.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3dx10 \_ meshopt- \_ Geräte \_ unabhängig**
</dt> <dd>

Wirkt sich auf die Scheitelpunkt Cache Größe aus. Die Verwendung dieses Flags gibt eine Standard Cache Größe an, die auf Legacy Hardware gut funktioniert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die \_ Optimierungs Flags "D3DXMESHOPT stripreorder" und "D3DXMESHOPT \_ vertexcache" schließen sich gegenseitig aus.

Das \_ Flag D3DXMESHOPT sharevb wurde aus dieser Enumeration entfernt. Verwenden Sie \_ stattdessen die D3DXMESH vb- \_ Freigabe in D3DXMESH.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




