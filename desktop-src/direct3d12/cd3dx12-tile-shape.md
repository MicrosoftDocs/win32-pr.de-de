---
title: CD3DX12_TILE_SHAPE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Kachel \_ Form Struktur zu ermöglichen.
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE Struktur
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
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365288"
---
# <a name="cd3dx12_tile_shape-structure"></a>CD3DX12 \_ Tile- \_ Shape-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) Struktur zu ermöglichen.

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

**CD3DX12- \_ Kachel \_ Form ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Kachel \_ Form.

</dd> <dt>

**explizite CD3DX12- \_ Kachel \_ Form (konstant D3D12 \_ Kachel \_ Form &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Form, die mit dem Inhalt einer anderen [**D3D12- \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Tile- \_ Form (uint widthintexels, uint heightintexels, uint depthintexels)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Form und initialisiert die folgenden Parameter:

Uint widthintexels

Uint-heightintexels

Uint depthintexels

</dd> <dt>

**Operator Konstanten D3D12 \_ Kachel \_ Form& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





