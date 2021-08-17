---
description: Messen Sie die Leistung der Cachetrefferrate für Texturen und indizierte Scheitelungen.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION -Struktur (D3D9Types.h)
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
ms.openlocfilehash: 01f0521ca7833cd74c3cb45b5a650fbd12aae485e36a153b57e6d9b10b49d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733071"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>D3DDEVINFO \_ D3D9CACHEUTILIZATION-Struktur

Messen Sie die Leistung der Cachetrefferrate für Texturen und indizierte Scheitelungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Member

<dl> <dt>

**TextureCacheHitRate**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Trefferrate zum Suchen einer Textur im Texturcache. Dabei wird davon ausgegangen, dass ein Texturcache vorhanden ist. Die Erhöhung der Detailebenenverzerrung, um die ausführlichste Textur zu verwenden, viele große Texturen zu verwenden oder ein nahezu zufälliges Texturzugriffsmuster für große Texturen mit benutzerdefiniertem Shadercode zu erzeugen, kann sich erheblich auf die Trefferrate des Texturcaches auswirken.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Trefferrate für das Suchen transformierte Scheitelpunkte im Scheitelpunktcache. Die GPU ist für die Transformation indizierter Scheitelpunkte konzipiert und kann sie in einem Scheitelpunktcache speichern. Wenn Sie Gitternetze verwenden, führt [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) oder [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) möglicherweise zu einer besseren Auslastung des Scheitelpunktcaches.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein effizienter Cache liegt in der Regel näher an einer Trefferrate von 90 Prozent, und ein ineffizienter Cache ist in der Regel näher an einer Trefferrate von 10 Prozent (obwohl ein niedriger Prozentsatz nicht unbedingt ein Problem darstellt).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
