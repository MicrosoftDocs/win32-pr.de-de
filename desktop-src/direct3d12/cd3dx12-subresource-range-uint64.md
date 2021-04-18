---
title: CD3DX12_SUBRESOURCE_RANGE_UINT64-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer D3D12-unter \_ \_ Bereichs UINT64-Struktur aktiviert werden kann \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- CD3DX12_SUBRESOURCE_RANGE_UINT64 Struktur
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
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351927"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>CD3DX12 \_ subresource- \_ Bereich \_ UINT64 Struktur

Eine hilfsstruktur, mit der die einfache Initialisierung einer D3D12-unter [**\_ \_ Bereichs \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) -Struktur aktiviert werden kann.

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

**CD3DX12 \_ subresource- \_ Bereich \_ UINT64 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ subresource- \_ Bereichs \_ UINT64.

</dd> <dt>

**expliziter CD3DX12-unter \_ \_ Bereichs Bereich \_ UINT64 (konstant D3D12 unter \_ \_ Bereichs Quelle \_ UINT64 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ subresource- \_ Bereichs \_ UINT64, initialisiert mit Werten, die aus einem D3D12-unter [**\_ \_ Bereich \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) -Struktur kopiert wurden.

</dd> <dt>

**CD3DX12 \_ subresource \_ Range \_ UINT64 (uint subresource, Konstanten D3D12 \_ Range \_ UINT64& Range)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.

</dd> <dt>

**CD3DX12 \_ subresource \_ Range \_ UINT64 (uint subresource, UINT64 BEGIN, UINT64 End)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.

</dd> <dt>

**Operator Konstanten D3D12 \_ subresource- \_ Bereich \_ UINT64& () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine D3D12 \_ subresource \_ Range \_ UINT64-Struktur. Da D3D12 \_ subresource \_ Range \_ UINT64 der zugrunde liegende Typ von CD3DX12 \_ subresource \_ Range \_ UINT64 ist, wird das Objekt einfach als Konstante D3D12-tiefen Schablone zurückgegeben, \_ \_ \_ DESC1 Verweis auf sich selbst.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ subresource- \_ Bereich \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





