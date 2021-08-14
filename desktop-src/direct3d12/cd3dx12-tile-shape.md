---
title: CD3DX12_TILE_SHAPE -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ TILE \_ SHAPE-Struktur zu ermöglichen.
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b02f699ab06ef93f3eeace3ce515b0947030e4824e2cb0fa51034c3e33f51dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987870"
---
# <a name="cd3dx12_tile_shape-structure"></a>CD3DX12 \_ TILE \_ SHAPE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ TILE \_ SHAPE-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ TILE \_ SHAPE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ TILE \_ SHAPE-Instanz.

</dd> <dt>

**explicit CD3DX12 \_ TILE \_ SHAPE(const D3D12 \_ TILE SHAPE &\_ o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 TILE SHAPE,initialisiert mit dem Inhalt einer anderen \_ \_ [**D3D12 \_ TILE \_ SHAPE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)

</dd> <dt>

**CD3DX12 \_ TILE \_ SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**
</dt> <dd>

Erstellt eine neue Instanz von CD3DX12 \_ TILE \_ SHAPE und initialisiert die folgenden Parameter:

UINT widthInTexels

UINT heightInTexels

UINT depthInTexels

</dd> <dt>

**operator const D3D12 \_ TILE \_ SHAPE&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ TILE \_ SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





