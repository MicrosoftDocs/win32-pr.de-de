---
title: CD3DX12_RANGE_UINT64-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Range \_ UINT64-Struktur zu ermöglichen.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- CD3DX12_RANGE_UINT64 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365344"
---
# <a name="cd3dx12_range_uint64-structure"></a>CD3DX12 \_ Range \_ UINT64-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Range \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Range \_ UINT64 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Range \_ UINT64.

</dd> <dt>

**expliziter CD3DX12 \_ Range \_ UINT64 (konstant D3D12 \_ Bereich \_ UINT64 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Range \_ UINT64, das mit Werten initialisiert wird, die aus einer [**D3D12 \_ Range \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) -Struktur kopiert wurden.

</dd> <dt>

**CD3DX12 \_ Range \_ UINT64 (UINT64 BEGIN, UINT64 End)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.

</dd> <dt>

**Operator konstant D3D12 \_ Range \_ UINT64& () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine D3D12 \_ Range \_ UINT64-Struktur. Da D3D12 \_ Range \_ UINT64 der zugrunde liegende Typ von CD3DX12 \_ Range \_ UINT64 ist, wird das Objekt einfach als konstanter D3D12 \_ Range UINT64- \_ Verweis zurückgegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ Range \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





