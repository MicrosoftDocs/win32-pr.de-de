---
title: CD3DX12_SUBRESOURCE_FOOTPRINT-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ SUBRESOURCE \_ FOOTPRINT-Struktur zu ermöglichen.
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32c3da3e133a5509543ffaa4fbf80b4c565730f13d3b9e92753658c96efcfcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069730"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ \_ SUBRESOURCE-SPEICHERBEDARFs.

</dd> <dt>

**explicit CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ SUBRESOURCE \_ FOOTPRINT &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(DXGI \_ FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT und initialisiert die folgenden Parameter:

[**DXGI \_ FORMAT-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT-Breite

UINT-Höhe

UINT-Tiefe

UINT rowPitch

</dd> <dt>

**explicit CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ RESOURCE \_ DESC& resDesc, UINT rowPitch)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT und initialisiert die folgenden Parameter:

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

UINT rowPitch

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ FOOTPRINT&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

