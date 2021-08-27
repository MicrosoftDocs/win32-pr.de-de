---
title: CD3DX12_TILE_REGION_SIZE -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ TILE \_ REGION \_ SIZE-Struktur zu ermöglichen.
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
ms.openlocfilehash: 9cc1b96ae4d7d33101068a1ba08f0314b99950146e91a352ab49fea714376471
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119610"
---
# <a name="cd3dx12_tile_region_size-structure"></a>STRUKTUR DER GRÖßE DER CD3DX12-KACHELREGION \_ \_ \_

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ TILE \_ REGION \_ SIZE-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) ermöglichen.

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

**CD3DX12 \_ TILE \_ REGION \_ SIZE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ TILE \_ REGION \_ SIZE.

</dd> <dt>

**explizite CD3DX12 \_ TILE \_ REGION \_ SIZE(const D3D12 \_ TILE REGION SIZE &\_ \_ o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 TILE REGION SIZE, initialisiert mit dem Inhalt einer anderen \_ \_ \_ [**D3D12 \_ TILE \_ REGION \_ SIZE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

</dd> <dt>

**CD3DX12 \_ TILE \_ REGION \_ SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ TILE REGION SIZE und \_ \_ initialisiert die folgenden Parameter:

UINT numTiles

BOOL useBox

UINT-Breite

UINT16-Höhe

UINT16-Tiefe

</dd> <dt>

**operator const D3D12 \_ TILE \_ REGION SIZE \_&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GRÖßE DES \_ D3D12-KACHELBEREICHS \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





