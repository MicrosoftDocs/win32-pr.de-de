---
title: CD3DX12_PACKED_MIP_INFO-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ gepackten \_ MIP Info-Struktur zu ermöglichen \_ .
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
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357223"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>CD3DX12- \_ gepackte \_ MIP- \_ Informationsstruktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ gepackten \_ MIP \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) -Struktur zu ermöglichen.

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

**CD3DX12- \_ gepackte \_ MIP- \_ Informationen ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ gepackten \_ MIP- \_ Info.

</dd> <dt>

**explizites CD3DX12 \_ gepackte \_ MIP- \_ Informationen (konstant D3D12 \_ gepackte \_ MIP \_ Info &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ gepackten \_ MIP- \_ Info, die mit dem Inhalt einer anderen [**D3D12- \_ gepackten \_ MIP \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12- \_ gepackte \_ MIP- \_ Informationen (Uint8 numstandardmips, Uint8 numpackedmips, uint numtilesforpackedmips, uint starttileindexinoverallresource)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12- \_ gepackten \_ MIP- \_ Info und initialisiert die folgenden Parameter:

Uint8 numstandardmips

Uint8 numpackedmips

Uint numtilesforpackedmips

Uint starttileingede xinoverallresource

</dd> <dt>

**Operator konstant D3D12 \_ gepackte \_ MIP- \_ Info& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ gepackte \_ MIP- \_ Informationen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





