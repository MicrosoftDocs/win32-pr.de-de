---
description: 'D3DXMESHOPT-Enumeration: Gibt den Typ der durchzuführenden Meshoptimierung an.'
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: D3DXMESHOPT-Enumeration (D3dx9mesh.h)
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
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114348"
---
# <a name="d3dxmeshopt-enumeration"></a>D3DXMESHOPT-Enumeration

Gibt den Typ der durchzuführenden Meshoptimierung an.

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

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**
</dt> <dd>

Ordnet Gesichter neu an, um nicht verwendete Scheitelpunkte und Gesichter zu entfernen.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Ordnet Gesichter neu an, um die Leistung von [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) zu optimieren, um weniger Änderungen am Attributbündelzustand zu erzielen.

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Ordnet Gesichter neu an, um die Cachetrefferrate von Scheitelpunktcaches zu erhöhen.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Ordnet Gesichter neu an, um die Länge benachbarter Dreiecke zu maximieren.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Nur die Gesichter optimieren; optimieren Sie die Scheitelpunkte nicht.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Teilen Sie beim Sortieren von Attributen keine Scheitelpunkte, die von Attributgruppen gemeinsam genutzt werden.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

Wirkt sich auf die Größe des Scheitelpunktcaches aus. Die Verwendung dieses Flags gibt eine Standardgröße des Scheitelpunktcaches an, die auf Legacyhardware gut funktioniert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Optimierungsflags D3DXMESHOPT \_ STRIPREORDER und D3DXMESHOPT \_ VERTEXCACHE schließen sich gegenseitig aus.

Das SHAREVB-Flag D3DXMESHOPT \_ wurde aus dieser Enumeration entfernt. Verwenden Sie stattdessen D3DXMESH \_ VB \_ SHARE in [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
