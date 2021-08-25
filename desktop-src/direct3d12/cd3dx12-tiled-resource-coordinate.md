---
title: CD3DX12_TILED_RESOURCE_COORDINATE -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ TILED \_ RESOURCE \_ COORDINATE-Struktur zu ermöglichen.
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784955545fe8e71227ffae6c5eec54acfd65b4a0ab0867f5c7de99a148976861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987850"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE.

</dd> <dt>

**explicit CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE(const D3D12 \_ TILED \_ RESOURCE COORDINATE \_ &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 TILED RESOURCE COORDINATE, initialisiert mit dem Inhalt einer anderen \_ \_ \_ [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)

</dd> <dt>

**CD3DX12 \_ TILED \_ RESOURCE \_ COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ TILED \_ RESOURCE COORDINATE und \_ initialisiert die folgenden Parameter:

UINT x

UINT y

UINT z

UINT-Unterressource

</dd> <dt>

**operator const D3D12 \_ TILED \_ RESOURCE COORDINATE \_&() const**
</dt> <dd>

Definiert den & pass-by-reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





