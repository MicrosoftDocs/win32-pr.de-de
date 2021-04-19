---
title: CD3DX12_RESOURCE_ALLOCATION_INFO-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Ressourcen \_ Zuordnungs Info-Struktur zu ermöglichen \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350662"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>CD3DX12 \_ \_ ressourcenzuordnungs- \_ Informationsstruktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Ressourcen \_ Zuordnungs \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Ressourcen \_ Zuordnungs \_ Informationen ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Ressourcen \_ Zuordnungs \_ Informationen.

</dd> <dt>

**explizite CD3DX12 \_ Ressourcen \_ Zuordnungs \_ Informationen (konstant D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen& o)**
</dt> <dd>

Erstellt eine neue Instanz der CD3DX12- \_ Ressourcen \_ Zuordnungs \_ Informationen, die mit dem Inhalt einer anderen [**D3D12 \_ Resource \_ Allocation \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) -Struktur initialisiert werden.

</dd> <dt>

**CD3DX12 \_ Ressourcen \_ Zuordnungs \_ Informationen (UINT64 Size, UINT64 Alignment)**
</dt> <dd>

Erstellt eine neue Instanz der CD3DX12- \_ Ressourcen \_ Zuordnungs \_ Informationen und initialisiert die folgenden Parameter:

UINT64-Größe

UINT64-Ausrichtung

</dd> <dt>

**Operator Konstanten D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





