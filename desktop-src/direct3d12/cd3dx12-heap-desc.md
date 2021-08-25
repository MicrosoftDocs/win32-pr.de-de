---
title: CD3DX12_HEAP_DESC-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ HEAP \_ DESC-Struktur zu ermöglichen.
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
ms.openlocfilehash: 347e44a8516b48dcd779d3ac19fbc9b5bbf5d37ad565f36a0b9b10a083d395c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858370"
---
# <a name="cd3dx12_heap_desc-structure"></a>CD3DX12 \_ HEAP \_ DESC-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ HEAP \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) zu ermöglichen.

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

**CD3DX12 \_ HEAP \_ DESC()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ HEAP \_ DESC.

</dd> <dt>

**Explicit CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ HEAP \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ HEAP \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(UINT64 size, D3D12 \_ HEAP \_ PROPERTIES properties, UINT64 alignment = 0, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC und initialisiert die folgenden Parameter:

UINT64-Größe

[**D3D12 \_ HEAP \_ PROPERTIES-Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) UINT64-Ausrichtung = 0

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(UINT64 size, D3D12 \_ HEAP \_ TYPE type, UINT64 alignment = 0, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC und initialisiert die folgenden Parameter:

UINT64-Größe

[**D3D12 \_ \_HEAPTYPTYP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) UINT64-Ausrichtung = 0

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(UINT64 size, D3D12 \_ CPU \_ PAGE \_ PROPERTY cpuPageProperty, D3D12 \_ MEMORY \_ POOL memoryPoolPreference, UINT64 alignment = 0, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC und initialisiert die folgenden Parameter:

UINT64-Größe

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) UINT64-Ausrichtung = 0

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ PROPERTIES properties, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ RESSOURCENZUORDNUNGSINFORMATIONEN**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ HEAP \_ PROPERTIES-Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ TYPE type, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ RESSOURCENZUORDNUNGSINFORMATIONEN**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ \_HEAPTYPTYP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ CPU \_ PAGE \_ PROPERTY cpuPageProperty, D3D12 \_ MEMORY \_ POOL memoryPoolPreference, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ DESC und initialisiert die folgenden Parameter:

[**D3D12 \_ \_ \_ RESSOURCENZUORDNUNGSINFORMATIONEN**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) [**D3D12 \_ HEAP \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**operator const D3D12 \_ HEAP \_ DESC&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den CD3DX12 \_ HEAP \_ DESC-Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





