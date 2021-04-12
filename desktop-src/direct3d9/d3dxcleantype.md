---
description: Definiert Vorgänge, die für Scheitel Punkte zur Vorbereitung der Mesh-Bereinigung durchgeführt werden.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: D3DXCLEANTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219557"
---
# <a name="d3dxcleantype-enumeration"></a>D3DXCLEANTYPE-Enumeration

Definiert Vorgänge, die für Scheitel Punkte zur Vorbereitung der Mesh-Bereinigung durchgeführt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_**
</dt> <dd>

Das Zusammenführen von Dreiecken, die die gleichen Scheitelpunkt Indizes aufweisen, aber über Gesichts normale verfügen, die auf entgegengesetzte Richtungen zeigen Wenn die Dreiecke nicht durch Hinzufügen eines replizierten Scheitel Punkts geteilt werden, können die Gitter einfügdaten der beiden Dreiecke einen Konflikt verursachen.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN- \_ bowties**
</dt> <dd>

Wenn ein Scheitelpunkt die Spitze zweier Dreiecks Lüfter (ein Bowtie) ist und Mesh-Vorgänge einen der Lüfter beeinflussen, teilen Sie den freigegebenen Scheitelpunkt in zwei neue Scheitel Punkte auf. Bowties können Probleme bei Vorgängen verursachen, z. b. bei der Mesh-Vereinfachung, bei der Vertices entfernt werden, da das Entfernen eines Scheitel Punkts zwei unterschiedliche Dreiecke

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN- \_ Skinning**
</dt> <dd>

Verwenden Sie dieses Flag, um unendliche Schleifen während der Einrichtung von settervorgängen zu vermeiden.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN- \_ Optimierung**
</dt> <dd>

Verwenden Sie dieses Flag, um unendliche Schleifen während Gitter Optimierungs Vorgängen zu verhindern.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN- \_ Vereinfachung**
</dt> <dd>

Verwenden Sie dieses Flag, um unendliche Schleifen während Mesh-Vereinfachungs Vorgängen zu verhindern.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




