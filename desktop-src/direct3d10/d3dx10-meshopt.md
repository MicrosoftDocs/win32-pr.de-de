---
description: 'D3DX10_MESHOPT Enumeration: Gibt den Typ der durchzuführenden Gitternetzoptimierung an.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT -Enumeration (D3DX10Mesh.h)
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
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105448"
---
# <a name="d3dx10_meshopt-enumeration"></a>D3DX10 \_ MESHOPT-Enumeration

Gibt den Typ der durchzuführenden Gitternetzoptimierung an.

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

Ordnet Gesichter neu an, um nicht verwendete Scheitelungen und Gesichter zu entfernen.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**
</dt> <dd>

Ordnet Gesichter neu an, um für weniger Attributbündelzustandsänderungen und verbesserte DrawSubset-Leistung zu optimieren.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ VERTEX \_ CACHE**
</dt> <dd>

Ordnet Gesichter neu an, um die Cachetrefferrate von Scheitelpunktcaches zu erhöhen.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ STRIP \_ REORDER**
</dt> <dd>

Ordnet Gesichter neu an, um die Länge benachbarter Dreiecke zu maximieren.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ \_ VERTS IGNORIEREN**
</dt> <dd>

Nur die Gesichter optimieren; optimieren Sie die Scheitelungen nicht.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ NICHT \_ \_ TEILEN**
</dt> <dd>

Teilen Sie bei der Attributsortierung keine Scheitelungen auf, die von Attributgruppen gemeinsam genutzt werden.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**
</dt> <dd>

Wirkt sich auf die Größe des Scheitelpunktcaches aus. Mit diesem Flag wird eine Standardgröße für den Scheitelpunktcache angegeben, die auf Legacyhardware gut funktioniert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die D3DXMESHOPT \_ STRIPREORDER- und D3DXMESHOPT \_ VERTEXCACHE-Optimierungsflags schließen sich gegenseitig aus.

Das D3DXMESHOPT \_ SHAREVB-Flag wurde aus dieser Enumeration entfernt. Verwenden Sie stattdessen D3DXMESH \_ VB \_ SHARE in D3DXMESH.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




