---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE1 -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1-Struktur zu ermöglichen.
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4570629b810fb7a088c7cfd88e3626412d5580beb1891a1a30daf9ffabede5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733992"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1.

</dd> <dt>

**explicit CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1(const D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 ROOT DESCRIPTOR TABLE1, initialisiert mit dem Inhalt einer anderen \_ \_ \_ [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)

</dd> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1 und initialisiert die folgenden Parameter:

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**inline Init(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**static inline Init(D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1 &**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) rootDescriptorTable

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





