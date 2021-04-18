---
title: CD3DX12_VIEWPORT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Viewport-Struktur zu ermöglichen.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- CD3DX12_VIEWPORT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354409"
---
# <a name="cd3dx12_viewport-structure"></a>CD3DX12 \_ Viewport-Struktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Viewport**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Viewport ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Viewports.

</dd> <dt>

**expliziter CD3DX12 \_ Viewport (konstant D3D12 \_ Viewport& o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Viewports und initialisiert die folgenden Parameter:

Konstanten D3D12 \_ Viewport& o

</dd> <dt>

**expliziter CD3DX12 \_ Viewport (float-topleftx, float-toplefty, float-Breite, float-Höhe, float mintiefe = D3D12 \_ minimale \_ Tiefe, float maxtiefe = D3D12 \_ Max. \_ Tiefe)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Viewports und initialisiert die folgenden Parameter:

FLOAT-topleftx

FLOAT-toplefty

Gleit Komma Breite

FLOAT-Höhe

FLOAT mintiefe = D3D12 \_ minimale \_ Tiefe

FLOAT maxtiefe = D3D12 \_ Maximale \_ Tiefe

</dd> <dt>

**expliziter CD3DX12 \_ Viewport (ID3D12Resource \* presource, uint mipslice = 0, float topleftx = 0,0 f, float toplefty = 0,0 f, float mintiefe = D3D12 \_ minimale \_ Tiefe, float maxtiefe = D3D12 \_ Maximale \_ Tiefe)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Viewports und initialisiert die folgenden Parameter:

ID3D12Resource- \* präsource

Uint mipslice = 0

FLOAT topleftx = 0,0 f

FLOAT toplefty = 0,0 f

FLOAT mintiefe = D3D12 \_ minimale \_ Tiefe

FLOAT maxtiefe = D3D12 \_ Maximale \_ Tiefe

</dd> <dt>

**~ CD3DX12 \_ Viewport ()**
</dt> <dd>

Zerstört eine Instanz eines D3DX12 \_ Viewports.

</dd> <dt>

**Operator Konstanten D3D12 \_ Viewport& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Viewport**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





