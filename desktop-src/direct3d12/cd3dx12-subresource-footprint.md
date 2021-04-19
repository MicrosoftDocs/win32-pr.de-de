---
title: CD3DX12_SUBRESOURCE_FOOTPRINT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12-unter Ressourcen-Speicherplatz \_ \_ Struktur ermöglicht.
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT Struktur
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
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370402"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>CD3DX12 unter Ressourcen-Speicherplatz \_ \_ Struktur

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) -unter Ressourcen-Speicherplatz Struktur ermöglicht.

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

**CD3DX12 Ressourcen \_ \_ Bedarf ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Ressourcen Speicherplatzes \_ \_ .

</dd> <dt>

**expliziter CD3DX12 Ressourcen \_ \_ Bedarf (konstant D3D12 Ressourcenbedarf bei der unter Quelle \_ \_ &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12-Speicherplatzes \_ \_ , der mit dem Inhalt einer anderen [**D3D12 \_ subresource \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) -Speicherplatz Struktur initialisiert wurde.

</dd> <dt>

**CD3DX12 \_ subresource-Speicher \_ Bedarf (DXGI- \_ Format Format, uint-Breite, uint-Höhe, uint-Tiefe, uint-rowpitch)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12-Speicherplatzes für \_ die unter Quelle \_ und initialisiert die folgenden Parameter:

[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format

Uint-Breite

Uint-Höhe

Uint-Tiefe

Uint-rowpitch

</dd> <dt>

**expliziter CD3DX12- \_ \_ Ressourcenbedarf (konstant D3D12 \_ Ressourcen- \_& resdesc, uint rowpitch)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12-Speicherplatzes für \_ die unter Quelle \_ und initialisiert die folgenden Parameter:

[**D3D12 \_ Ressourcen \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) -& resdesc

Uint-rowpitch

</dd> <dt>

**Operator Konstanten D3D12 Ressourcenbedarf für unter Ressourcen \_ \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 Ressourcen \_ \_ Bedarf**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

