---
title: CD3DX12_SUBRESOURCE_RANGE_UINT64-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64-Struktur zu ermöglichen.
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- CD3DX12_SUBRESOURCE_RANGE_UINT64-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df38d5b2e7a4230d023aeba6c8c3517fbd2b9f4e35a09b5e4439269b228eb82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987990"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64.

</dd> <dt>

**explicit CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64(const D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64, initialisiert mit Werten, die aus einer [**D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) kopiert wurden.

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64(UINT subresource, const D3D12 \_ RANGE \_ UINT64& range)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1, initialisiert mit den werten, die in der Parameterliste übergeben werden.

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64(UINT subresource, UINT64 begin, UINT64 end)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1, initialisiert mit den werten, die in der Parameterliste übergeben werden.

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64&() const**
</dt> <dd>

Implizite Konvertierung in eine D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64-Struktur. Da D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64 der zugrunde liegende Typ von CD3DX12 \_ SUBRESOURCE \_ RANGE \_ UINT64 ist, wird das Objekt einfach als const D3D12 \_ DEPTH \_ STENCIL \_ DESC1-Verweis auf sich selbst zurückgegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ SUBRESOURCE \_ RANGE \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





