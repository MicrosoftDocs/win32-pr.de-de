---
description: Gibt den Typ der auszuführenden Mesh-Optimierung an.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: D3DXMESHOPT-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361202"
---
# <a name="d3dxmeshopt-enumeration"></a>D3DXMESHOPT-Enumeration

Gibt den Typ der auszuführenden Mesh-Optimierung an.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**
</dt> <dd>

Ordnet Gesichter neu an, um nicht verwendete Vertices und Gesichter zu entfernen.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ attrsort**
</dt> <dd>

Ordnet Gesichter neu an, um weniger Attribut Bündel Statusänderungen und erweiterte [**ID3DXBaseMesh zu optimieren::D rawsubset**](id3dxbasemesh--drawsubset.md) Performance.

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ vertexcache**
</dt> <dd>

Ordnet Gesichter neu an, um die Cache Treffer Rate von Vertex-Caches zu erhöhen.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ stripreorder**
</dt> <dd>

Ordnet Flächen neu an, um die Länge der angrenzenden Dreiecke zu maximieren

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ ignoreverts**
</dt> <dd>

Nur Gesichter optimieren; Optimieren Sie die Vertices nicht.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ donotsplit**
</dt> <dd>

Bei der Attribut Sortierung werden Vertices, die von Attribut Gruppen gemeinsam verwendet werden, nicht aufgeteilt.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT-Geräte \_ abhängige Geräte**
</dt> <dd>

Wirkt sich auf die Scheitelpunkt Cache Größe aus. Die Verwendung dieses Flags gibt eine Standard Cache Größe an, die auf Legacy Hardware gut funktioniert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die \_ Optimierungs Flags "D3DXMESHOPT stripreorder" und "D3DXMESHOPT \_ vertexcache" schließen sich gegenseitig aus.

Das \_ Flag D3DXMESHOPT sharevb wurde aus dieser Enumeration entfernt. Verwenden Sie \_ stattdessen die D3DXMESH vb- \_ Freigabe in [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
