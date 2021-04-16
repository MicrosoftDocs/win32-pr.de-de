---
description: Messen Sie die Leistung der Cache-Treffer Rate für Texturen und indizierte Vertices.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530866"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>D3DDEVINFO \_ D3D9CACHEUTILIZATION-Struktur

Messen Sie die Leistung der Cache-Treffer Rate für Texturen und indizierte Vertices.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Texturecachehitrate**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Treffer Rate zum Ermitteln einer Textur im Textur Cache. Dabei wird davon ausgegangen, dass ein Textur Cache vorhanden ist. Das Erhöhen der Detailebene für die Verwendung der detaillierteren Textur mit vielen großen Texturen oder das Erzeugen eines near Random Texture-Zugriffs Musters für große Texturen mit benutzerdefiniertem shadercode kann die Treffer Rate des Textur Caches erheblich beeinträchtigen.

</dd> <dt>

**Posttransformvertexcachehitrate**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Treffer Rate zum Suchen transformier ender Scheitel Punkte im Scheitelpunkt Cache. Die GPU ist so konzipiert, dass Sie indizierte Scheitel Punkte transformiert und Sie möglicherweise in einem Scheitelpunkt Cache speichert. Wenn Sie Meshes verwenden, kann [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) oder [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) zu einer besseren Vertex-Cache Auslastung führen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein effizienter Cache liegt in der Regel bei einer Treffer Rate von 90 Prozent, und ein ineffizienter Cache liegt in der Regel bei einer Trefferquote von 10 Prozent (obwohl ein niedriger Prozentsatz nicht unbedingt ein Problem darstellt).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
