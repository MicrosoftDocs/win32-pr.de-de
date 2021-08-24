---
title: CD3DX12_PACKED_MIP_INFO-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ PACKED \_ MIP \_ INFO-Struktur zu ermöglichen.
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- CD3DX12_PACKED_MIP_INFO Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32a4b0516560ac553b3ce6acb6972def5d0e3f84a2eb84026a0635f779a2c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752160"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>CD3DX12 \_ PACKED \_ MIP \_ INFO-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ PACKED \_ MIP \_ INFO-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PACKED \_ MIP \_ INFO()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PACKED \_ MIP \_ INFO.

</dd> <dt>

**Explicit CD3DX12 \_ PACKED \_ MIP \_ INFO(const D3D12 \_ PACKED \_ MIP \_ INFO &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ PACKED \_ MIP \_ INFO, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ PACKED \_ MIP \_ INFO-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)

</dd> <dt>

**CD3DX12 \_ PACKED \_ MIP \_ INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ PACKED \_ MIP \_ INFO und initialisiert die folgenden Parameter:

UINT8 numStandardMips

UINT8 numPackedMips

UINT numTilesForPackedMips

UINT startTileIndexInOverallResource

</dd> <dt>

**operator const D3D12 \_ PACKED \_ MIP \_ INFO&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ PACKED \_ MIP \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





