---
title: CD3DX12_RESOURCE_BARRIER-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12- \_ Ressourcen \_ Barriere ermöglicht.
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER Struktur
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
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361900"
---
# <a name="cd3dx12_resource_barrier-structure"></a>CD3DX12 \_ \_ ressourcensperrenstruktur

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12- \_ Ressourcen \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) ermöglicht.

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

**CD3DX12- \_ Ressourcen \_ Barriere ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Ressourcen \_ Barriere.

</dd> <dt>

**explizites CD3DX12 \_ Ressourcen \_ Barriere (konstant D3D12 \_ Ressourcen \_ Barriere &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ Ressourcen \_ Barriere, die mit dem Inhalt einer anderen [**D3D12- \_ Ressourcen \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)initialisiert wird.

</dd> <dt>

**statischer Inline Übergang ("ID3D12Resource \* presource", "D3D12 \_ Resource \_ States statebefore", "D3D12 \_ Resource \_ States stateafter", "uint subresource = D3D12 \_ Resource \_ Barrier \_ All \_ subresources", "D3D12 \_ Resource \_ Barrier \_ Flags Flags = D3D12 \_ Resource \_ Barrier \_ Flag \_ None")**
</dt> <dd>

Übergänge zwischen Ressourcen Zuständen mit den folgenden Parametern:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* vorab Quelle

[**D3D12 \_ Ressourcen \_ Zustände**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) statebefore

[**D3D12 \_ Ressourcen \_ Zustände**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateafter

Opt Uint subresource = [ **D3D12 \_ Ressourcen \_ Barriere \_ alle \_ unter Ressourcen**](constants.md)

Opt [**D3D12 \_ \_ \_ Ressourcensperrungsflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = \_ D3D12 \_ ressourcensperrungsflag " \_ \_ None"

</dd> <dt>

**statisches Inline Aliasing (ID3D12Resource \* presourcebefore, ID3D12Resource \* presourceafter)**
</dt> <dd>

Erstellt Aliase für die Ressource vor und nach dem Sperr Übergang. Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* presourcebefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* presourceafter

</dd> <dt>

**statische Inline-UAV (ID3D12Resource \* presource)**
</dt> <dd>

Erstellt eine ungeordnete Zugriffs Ansicht (UAV) für die Ressource. Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* vorab Quelle

</dd> <dt>

**Operator konstant D3D12 \_ Ressourcen \_ Barriere& () konstant**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Ressourcen \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





