---
title: CD3DX12_HEAP_PROPERTIES-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ HEAP \_ PROPERTIES-Struktur zu ermöglichen.
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- CD3DX12_HEAP_PROPERTIES-Struktur
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
ms.openlocfilehash: 36a4d2241568d98957ecd809f33f27c343bb0e73d0d246284e5635f22a594108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752320"
---
# <a name="cd3dx12_heap_properties-structure"></a>CD3DX12 \_ HEAP \_ PROPERTIES-Struktur

Eine Hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ HEAP \_ PROPERTIES-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) zu ermöglichen.

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

**CD3DX12 \_ HEAP \_ PROPERTIES()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ HEAP \_ PROPERTIES.

</dd> <dt>

**Explicit CD3DX12 \_ HEAP \_ PROPERTIES(const D3D12 \_ HEAP PROPERTIES &\_ o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ HEAP \_ PROPERTIES, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ HEAP \_ PROPERTIES-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

</dd> <dt>

**CD3DX12 \_ HEAP \_ PROPERTIES(D3D12 \_ CPU PAGE PROPERTY \_ \_ cpuPageProperty, D3D12 \_ MEMORY POOL \_ memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**
</dt> <dd>

Erstellt eine neue Instanz von CD3DX12 \_ HEAP \_ PROPERTIES und initialisiert die folgenden Parameter:

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) UINT-ErstellungNodeMask = 1

(opt) UINT nodeMask = 1

</dd> <dt>

**Explicit CD3DX12 \_ HEAP \_ PROPERTIES(D3D12 \_ HEAP TYPE \_ type, UINT creationNodeMask = 1, UINT nodeMask = 1)**
</dt> <dd>

Erstellt eine neue Instanz von CD3DX12 \_ HEAP \_ PROPERTIES und initialisiert die folgenden Parameter:

[**D3D12 \_ \_HEAPTYPTYP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) UINT-ErstellungNodeMask = 1

(opt) UINT nodeMask = 1

</dd> <dt>

**operator const D3D12 \_ HEAP \_ PROPERTIES&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> <dt>

**inline operator==( const D3D12 \_ HEAP \_ PROPERTIES& l, const D3D12 \_ HEAP PROPERTIES& r \_ )**
</dt> <dd>

Testet auf Gleichheit zwischen den angegebenen D3D12 \_ HEAP \_ PROPERTIES-Instanzen basierend auf der Gleichheit aller Elementfelder.

</dd> <dt>

**inline operator!=( const D3D12 \_ HEAP \_ PROPERTIES& l, const D3D12 \_ HEAP PROPERTIES& r \_ )**
</dt> <dd>

Testet auf Ungleichheit zwischen den angegebenen D3D12 \_ HEAP \_ PROPERTIES-Instanzen. Wird implementiert, indem die Umkehrung des **operators==-Werts** angenommen wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_D3D12-HEAPEIGENSCHAFTEN \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





