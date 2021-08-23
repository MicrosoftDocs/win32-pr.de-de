---
title: CD3DX12_RESOURCE_ALLOCATION_INFO-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO-Struktur zu ermöglichen.
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO-Struktur
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
ms.openlocfilehash: 63915f2fa05950ad96bc621b9887b1c4fe23149e22ba408767d111f7b74d6927
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729220"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO-Struktur

Eine Hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) zu ermöglichen.

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

**CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ o)**
</dt> <dd>

Erstellt eine neue Instanz von CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ RESOURCE ALLOCATION \_ \_ INFO-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

</dd> <dt>

**CD3DX12 \_ RESOURCE ALLOCATION INFO \_ \_ (UINT64-Größe, UINT64-Ausrichtung)**
</dt> <dd>

Erstellt eine neue Instanz von CD3DX12 \_ RESOURCE ALLOCATION INFO und \_ \_ initialisiert die folgenden Parameter:

UINT64-Größe

UINT64-Ausrichtung

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ ALLOCATION INFO \_&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INFORMATIONEN \_ ZUR D3D12-RESSOURCENZUORDNUNG \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





