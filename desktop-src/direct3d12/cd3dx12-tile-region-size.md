---
title: CD3DX12_TILE_REGION_SIZE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Tile- \_ Regions \_ Größen Struktur zu ermöglichen.
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353701"
---
# <a name="cd3dx12_tile_region_size-structure"></a>Struktur der CD3DX12- \_ Kachel \_ Regions \_ Größe

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Tile- \_ Regions \_ Größen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Tile- \_ Regions \_ Größe ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Kachel \_ Bereichs \_ Größe.

</dd> <dt>

**explizite CD3DX12- \_ Kachel \_ Regions \_ Größe (konstant D3D12 \_ Kachel \_ Regions \_ Größe &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Regions \_ Größe, die mit dem Inhalt einer anderen [**D3D12 \_ Tile- \_ Regions \_ Größen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Tile \_ Regions \_ size (uint numtiles, bool usebox, uint Width, UInt16 Height, UInt16 Tiefe)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Regions \_ Größe und initialisiert die folgenden Parameter:

Uint-numtiles

Boolesche usebox

Uint-Breite

UInt16-Höhe

UInt16 Tiefe

</dd> <dt>

**Operator Konstanten D3D12 \_ Kachel \_ Regions \_ Größe& () konstant**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Tile- \_ Regions \_ Größe**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





