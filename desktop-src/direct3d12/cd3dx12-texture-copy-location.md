---
title: CD3DX12_TEXTURE_COPY_LOCATION-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer D3D12- \_ Textur \_ Kopie- \_ Speicherort Struktur aktiviert werden kann.
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- CD3DX12_TEXTURE_COPY_LOCATION Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365073"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>\_Struktur des CD3DX12-Textur \_ Kopier \_ Orts

Eine hilfsstruktur, mit der die einfache Initialisierung einer [**D3D12- \_ Textur Kopie- \_ \_ Speicherort**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) Struktur aktiviert werden kann.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>Member

<dl> <dt>

**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts.

</dd> <dt>

**expliziter CD3DX12 \_ Textur \_ Kopier \_ Speicherort (konstant D3D12 \_ Textur \_ Kopier \_ Speicherort &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts, der mit dem Inhalt einer anderen [**D3D12- \_ Textur Kopie- \_ \_ Speicherort**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) Struktur initialisiert wird.

</dd> <dt>

**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ (ID3D12Resource \* pRes)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts und initialisiert die folgenden Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Prä

</dd> <dt>

**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ (ID3D12Resource \* pRes, D3D12 Speicherort der unter \_ \_ Quelle \_& Speicherbedarf)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts und initialisiert die folgenden Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Prä

[**D3D12 \_ Der \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) Speicherplatz der untergeordneten Quelle& Speicherbedarf.

</dd> <dt>

**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ (ID3D12Resource \* pRes, uint Sub)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts und initialisiert die folgenden Parameter:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Prä

Uint Sub

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicherort der D3D12- \_ Textur \_ Kopie \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





