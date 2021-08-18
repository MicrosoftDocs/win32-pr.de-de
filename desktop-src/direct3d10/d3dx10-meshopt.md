---
description: 'D3DX10_MESHOPT Enumeration: Gibt den Typ der durchzuführenden Meshoptimierung an.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT-Enumeration (D3DX10Mesh.h)
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
ms.openlocfilehash: 193bf832f00c9812a515ae9b5c478f6baed637d87605e9f8d04349a12d79aac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989220"
---
# <a name="d3dx10_meshopt-enumeration"></a>D3DX10 \_ MESHOPT-Enumeration

Gibt den Typ der durchzuführenden Meshoptimierung an.

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

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**
</dt> <dd>

Ordnet Gesichter neu an, um nicht verwendete Scheitelpunkte und Gesichter zu entfernen.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**
</dt> <dd>

Ordnet Gesichter neu an, um weniger Änderungen am Attributbündelzustand und eine verbesserte DrawSubset-Leistung zu erzielen.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ VERTEX \_ CACHE**
</dt> <dd>

Ordnet Gesichter neu an, um die Cachetrefferrate von Scheitelpunktcaches zu erhöhen.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ STRIP \_ REORDER**
</dt> <dd>

Ordnet Gesichter neu an, um die Länge benachbarter Dreiecke zu maximieren.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ IGNORE \_ VERTS**
</dt> <dd>

Nur die Gesichter optimieren; optimieren Sie die Scheitelpunkte nicht.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ \_ NICHT \_ TEILEN**
</dt> <dd>

Teilen Sie beim Sortieren von Attributen keine Scheitelpunkte, die von Attributgruppen gemeinsam genutzt werden.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**
</dt> <dd>

Wirkt sich auf die Größe des Scheitelpunktcaches aus. Die Verwendung dieses Flags gibt eine Standardgröße des Scheitelpunktcaches an, die auf Legacyhardware gut funktioniert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Optimierungsflags D3DXMESHOPT \_ STRIPREORDER und D3DXMESHOPT \_ VERTEXCACHE schließen sich gegenseitig aus.

Das D3DXMESHOPT \_ SHAREVB-Flag wurde aus dieser Enumeration entfernt. Verwenden Sie stattdessen D3DXMESH \_ VB \_ SHARE in D3DXMESH.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




