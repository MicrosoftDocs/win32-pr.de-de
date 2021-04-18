---
title: CD3DX12_HEAP_PROPERTIES-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Heap \_ Eigenschaften Struktur zu ermöglichen.
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- CD3DX12_HEAP_PROPERTIES Struktur
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354351"
---
# <a name="cd3dx12_heap_properties-structure"></a>Struktur der CD3DX12- \_ Heap \_ Eigenschaften

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Heap- \_ Eigenschaften ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz von CD3DX12 \_ Heap \_ Eigenschaften.

</dd> <dt>

**explizite CD3DX12 \_ Heap \_ Eigenschaften (Konstanten D3D12 \_ Heap \_ Eigenschaften &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Heap Eigenschaft \_ , die mit dem Inhalt einer anderen [**D3D12 \_ Heap \_ Properties**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Heap- \_ Eigenschaften (D3D12 \_ CPU \_ Page \_ Property cpupageproperty, D3D12 \_ Memory \_ Pool memorypoolpreference, uint anationnodemask = 1, uint nodemask = 1)**
</dt> <dd>

Erstellt eine neue Instanz der CD3DX12- \_ Heap \_ Eigenschaften und initialisiert die folgenden Parameter:

[**D3D12 \_ CPU \_ - \_ Seiteneigenschaft**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpupageproperty

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) Memorypoolpreference für Speicher Pool

Opt Uint-kreationnodemask = 1

Opt Uint nodemask = 1

</dd> <dt>

**explizite CD3DX12 \_ Heap- \_ Eigenschaften (D3D12 \_ Heap \_ Type type, uint kreationnodemask = 1, uint nodemask = 1)**
</dt> <dd>

Erstellt eine neue Instanz der CD3DX12- \_ Heap \_ Eigenschaften und initialisiert die folgenden Parameter:

[**D3D12 \_ Typ des Heap \_ Typs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

Opt Uint-kreationnodemask = 1

Opt Uint nodemask = 1

</dd> <dt>

**Operator Konstanten D3D12 \_ Heap \_ Eigenschaften& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> <dt>

**Inline Operator = = (Konstanten D3D12 \_ Heap \_ Eigenschaften& l, Konstanten D3D12 \_ Heap \_ Eigenschaften& r)**
</dt> <dd>

Testet basierend auf der Gleichheit aller Element Felder auf Gleichheit zwischen den angegebenen D3D12 \_ Heap- \_ Eigenschaften Instanzen.

</dd> <dt>

**Inline Operator! = (Konstanten D3D12 \_ Heap \_ Eigenschaften& l, Konstanten D3D12 \_ Heap \_ Eigenschaften& r)**
</dt> <dd>

Prüft auf Ungleichheit zwischen den angegebenen D3D12 \_ Heap- \_ Eigenschaften Instanzen. Wird durch die Umkehrung des **Operators = =** implementiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





