---
title: CD3DX12_HEAP_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Heap- \_ DESC-Struktur zu ermöglichen.
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- CD3DX12_HEAP_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355787"
---
# <a name="cd3dx12_heap_desc-structure"></a>CD3DX12- \_ Heap- \_ Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Heap- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Heap- \_ Debugheap ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Heaps \_ \_ .

</dd> <dt>

**expliziter CD3DX12 \_ Heap- \_ Debugheap (konstant D3D12 \_ Heap- \_ &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ decoens, der mit dem Inhalt einer anderen [**D3D12 \_ Heap- \_ debugerenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Heap Debug \_ (UINT64 Size, D3D12 \_ Heap \_ Properties Properties, UINT64 Alignment = 0, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:

UINT64-Größe

[**D3D12 \_ Eigenschaften von Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

Opt UINT64 Alignment = 0

Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None

</dd> <dt>

**CD3DX12 \_ Heap \_ DESC (UINT64 Size, D3D12 \_ Heap \_ Type type, UINT64 Alignment = 0, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:

UINT64-Größe

[**D3D12 \_ Typ des Heap \_ Typs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

Opt UINT64 Alignment = 0

Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None

</dd> <dt>

**CD3DX12 \_ Heap \_ DESC (UINT64 Size, D3D12 \_ CPU \_ Page \_ Property cpupageproperty, D3D12 \_ Speicher \_ Pool memorypoolpreference, UINT64 Alignment = 0, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:

UINT64-Größe

[**D3D12 \_ CPU \_ - \_ Seiteneigenschaft**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpupageproperty

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) Memorypoolpreference für Speicher Pool

Opt UINT64 Alignment = 0

Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None

</dd> <dt>

**CD3DX12 \_ Heap \_ DESC (Zuordnungs \_ Informationen für Ressourcen \_ Zuordnungen \_& resallocinfo, D3D12 \_ Heap \_ Eigenschaften Eigenschaften, D3D12 Heap Kennzeichen \_ \_ Flags = D3D12 \_ Heap \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo

[**D3D12 \_ Eigenschaften von Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None

</dd> <dt>

**CD3DX12 \_ Heap \_ DESC (Informationen zur Ressourcenzuweisung für "" \_ \_ \_ )& resallocinfo, D3D12 \_ Heap \_ Type type, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo

[**D3D12 \_ Typ des Heap \_ Typs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None

</dd> <dt>

**CD3DX12 \_ Heap \_ DESC (konstant D3D12 \_ Ressourcen \_ Zuordnungs \_ Info& resallocinfo, D3D12 \_ CPU \_ Page \_ Property cpupageproperty, D3D12 \_ Memory \_ Pool memorypoolpreference, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo

[**D3D12 \_ CPU \_ - \_ Seiteneigenschaft**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpupageproperty

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) Memorypoolpreference für Speicher Pool

Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None

</dd> <dt>

**Operator Konstanten D3D12 \_ Heap- \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den CD3DX12 \_ Heap \_ DESC-Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Heap- \_ Debugheap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





