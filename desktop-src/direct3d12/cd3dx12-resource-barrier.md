---
title: CD3DX12_RESOURCE_BARRIER -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ RESOURCE \_ BARRIER-Struktur zu ermöglichen.
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3490f48e04c97c845264f514e65db390a01e115ebff7c53aca792d29f0c522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098453"
---
# <a name="cd3dx12_resource_barrier-structure"></a>CD3DX12 \_ RESOURCE \_ BARRIER-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ RESOURCE \_ BARRIER-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ RESOURCE \_ BARRIER()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ RESOURCE \_ BARRIER.

</dd> <dt>

**explizites CD3DX12 \_ RESOURCE \_ BARRIER(const D3D12 \_ RESOURCE BARRIER &\_ o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 RESOURCE BARRIER, die mit dem Inhalt einer anderen \_ \_ [**D3D12 \_ RESOURCE \_ BARRIER initialisiert wird.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

</dd> <dt>

**Statischer Inlineübergang (ID3D12Resource \* pResource, D3D12 \_ RESOURCE \_ STATES stateBefore, D3D12 \_ RESOURCE STATES \_ stateAfter, UINT subresource = D3D12 \_ RESOURCE BARRIER ALL \_ \_ \_ SUBRESOURCES, D3D12 \_ RESOURCE BARRIER \_ \_ FLAGS flags = D3D12 \_ RESOURCE BARRIER FLAG \_ \_ \_ NONE)**
</dt> <dd>

Übergänge zwischen Ressourcenzuständen mithilfe der folgenden Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

[**D3D12 \_ RESOURCE \_ STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_ RESOURCE \_ STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter

(opt) UINT-Unterressource = [ **D3D12 \_ RESOURCE \_ BARRIER ALL \_ \_ SUBRESOURCES**](constants.md)

(opt) [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS-Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = D3D12 \_ RESOURCE BARRIER FLAG \_ \_ \_ NONE

</dd> <dt>

**static inline Aliasing(ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Erstellt Aliase für die Ressource vor und nach dem Übergang der Barriere. Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**static inline UAV(ID3D12Resource \* pResource)**
</dt> <dd>

Erstellt eine ungeordnete Zugriffsansicht (UAV) für die Ressource. Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ BARRIER&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ RESOURCE \_ BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





