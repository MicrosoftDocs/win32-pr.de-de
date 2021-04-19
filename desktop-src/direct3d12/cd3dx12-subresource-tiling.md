---
title: CD3DX12_SUBRESOURCE_TILING-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-unter Berichts- \_ \_ Tick-Struktur zu ermöglichen.
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- CD3DX12_SUBRESOURCE_TILING Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364346"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>CD3DX12-Struktur für unter \_ geordnete Elemente \_

Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-unter Berichts- [**\_ \_ Tick**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ subresource- \_ tiult ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ subresource- \_ Tick.

</dd> <dt>

**explizite CD3DX12 \_ subresource- \_ tiult (Konstanten D3D12 \_ subresource- \_ tiult &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12-untergeordneten \_ Quelle \_ , die mit dem Inhalt einer anderen [**D3D12 \_ subresource- \_ tilinger**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ subresource \_ tiult (uint widthintiles, UInt16 uptintiles, UInt16 depthintiles, uint starttileindexinoverallresource)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12-Unterteilung \_ \_ , wobei die folgenden Parameter initialisiert werden:

Uint widthintiles

UInt16-Höhen Kacheln

UInt16 depthintiles

Uint starttileingede xinoverallresource

</dd> <dt>

**Operator Konstanten D3D12 Unterteilung \_ \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12-unter \_ geordnete \_ tiult**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





