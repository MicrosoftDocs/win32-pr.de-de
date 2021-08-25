---
description: Definiert Vorgänge, die für Scheitelungen als Vorbereitung für die Gitternetzbereinigung durchzuführen sind.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: D3DXCLEANTYPE-Enumeration (D3dx9mesh.h)
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
ms.openlocfilehash: 2517c59d5505a8f2892ef0aee1d3884b8d489625637002d6e69a4f86434237fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894110"
---
# <a name="d3dxcleantype-enumeration"></a>D3DXCLEANTYPE-Enumeration

Definiert Vorgänge, die für Scheitelungen als Vorbereitung für die Gitternetzbereinigung durchzuführen sind.

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

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKFACING**
</dt> <dd>

Zusammenführen von Dreiecken, die dieselben Scheitelpunktindizes gemeinsam haben, aber Gesichtsnormwerte haben, die in entgegengesetzte Richtungen zeigen (hintere Dreiecke). Sofern die Dreiecke nicht durch Hinzufügen eines replizierten Scheitelpunkts geteilt werden, können Mesh-Adjakencydaten aus den beiden Dreiecken in Konflikt stehen.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**
</dt> <dd>

Wenn ein Scheitelpunkt der Apex von zwei Dreiecks-Lüftern (eine Bowtie) ist und Gitternetzvorgänge einen der Lüfter betreffen, teilen Sie den gemeinsamen Scheitelpunkt in zwei neue Scheitelpunkte auf. Schleifen können Probleme bei Vorgängen wie Gitternetz-Vereinfachungen verursachen, die Scheitelpunkte entfernen, da das Entfernen eines Scheitelpunkts zwei unterschiedliche Sätze von Dreiecken betrifft.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ SKINNING**
</dt> <dd>

Verwenden Sie dieses Flag, um endlose Schleifen bei Skinningsetup-Gitternetzvorgängen zu verhindern.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN-OPTIMIERUNG \_**
</dt> <dd>

Verwenden Sie dieses Flag, um Endlosschleifen während Gitternetzoptimierungsvorgängen zu verhindern.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN-VEREINFACHUNG \_**
</dt> <dd>

Verwenden Sie dieses Flag, um Endlosschleifen während Vorgängen zur Vereinfachung des Gitters zu verhindern.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




