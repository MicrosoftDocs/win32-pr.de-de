---
title: CD3DX12_TILED_RESOURCE_COORDINATE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Kachel \_ Ressourcen \_ Koordinaten Struktur zu ermöglichen.
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE Struktur
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
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354987"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>CD3DX12 \_ Kacheln der \_ Ressourcen \_ Koordinaten Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Kachel \_ Ressourcen \_ Koordinaten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) Struktur zu ermöglichen.

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

**CD3DX12 \_ gekachelte \_ Ressourcen \_ Koordinate ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Kachel \_ Ressourcen \_ Koordinate.

</dd> <dt>

**explizite CD3DX12 \_ gekachelte \_ Ressourcen \_ Koordinate (konstant D3D12 \_ gekachelte \_ Ressourcen \_ Koordinate &o)**
</dt> <dd>

Erstellt eine neue Instanz einer \_ gekachelten \_ Ressourcen \_ Koordinate (CD3DX12), die mit dem Inhalt einer anderen [**D3D12- \_ Kachel \_ Ressourcen \_ Koordinaten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ gekachelte \_ Ressourcen \_ Koordinate (uint x, uint y, uint z, uint subresource)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ gekachelten \_ Ressourcen \_ Koordinate und initialisiert die folgenden Parameter:

Uint x

Uint y

Uint z

Uint-unter Quelle

</dd> <dt>

**Operator Konstanten D3D12 \_ \_ \_& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





