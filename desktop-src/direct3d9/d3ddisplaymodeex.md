---
description: Informationen zu den Eigenschaften eines Anzeigemodus.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: D3DDISPLAYMODEEX-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373498"
---
# <a name="d3ddisplaymodeex-structure"></a>D3DDISPLAYMODEEX-Struktur

Informationen zu den Eigenschaften eines Anzeigemodus.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Größe dieser Struktur. Diese sollte immer auf sizeof (D3DDISPLAYMODEEX) festgelegt werden.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des Anzeigemodus.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Höhe des Anzeigemodus.

</dd> <dt>

**RefreshRate**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Aktualisierungsrate des Anzeigemodus.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Das Format des Anzeigemodus. Siehe [D3DFORMAT](d3dformat.md).

</dd> <dt>

**Scanlineorder**
</dt> <dd>

Typ: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Gibt an, ob die Scanline-Reihenfolge progressiv oder mit Zeilen Sprung ist. Siehe [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in verschiedenen Methoden verwendet, um Direct3D 9Ex-Geräte ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) und SwapChain ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)) zu erstellen und zu verwalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
