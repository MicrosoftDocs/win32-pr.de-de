---
description: Gibt die Typen der Anzeigemodi an, die herausgefiltert werden sollen.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: D3DDISPLAYMODEFILTER-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354466"
---
# <a name="d3ddisplaymodefilter-structure"></a>D3DDISPLAYMODEFILTER-Struktur

Gibt die Typen der Anzeigemodi an, die herausgefiltert werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Größe dieser Struktur. Diese sollte immer auf sizeof (D3DDISPLAYMODEFILTER) festgelegt werden.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Das auszufilternde Anzeigemodus-Format. Siehe [D3DFORMAT](d3dformat.md).

</dd> <dt>

**Scanlineorder**
</dt> <dd>

Typ: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Ob die Scanline-Reihenfolge Zeilen Sprung oder progressiv ist. Siehe [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
