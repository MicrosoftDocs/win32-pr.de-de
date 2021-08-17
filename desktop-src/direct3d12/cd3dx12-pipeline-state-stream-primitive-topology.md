---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a828ef50956d9ab5336dfe88fa12bed9f7541633ec4589a9c556511e8487a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734262"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>PRIMITIVE TOPOLOGIESTRUKTUR DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMS \_ \_ \_ \_

Eine Hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**PRIMITIVE TOPOLOGIE DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMS \_ \_ \_ \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer PRIMITIVEN TOPOLOGIE DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMs. \_ \_ \_ \_

</dd> <dt>

**PRIMITIVE TOPOLOGIE DES CD3DX12 \_ PIPELINE \_ STATE \_ \_ \_ STREAM(D3D12 \_ PRIMITIVE \_ TOPOLOGY TYPE \_ const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer PRIMITIVEN TOPOLOGIE DES \_ CD3DX12-PIPELINEZUSTANDSDATENSTROMs, \_ \_ \_ \_ initialisiert mit dem Unterobjekttyp **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE PRIMITIVE \_ \_ \_ TOPOLOGY** und den unterobjektdaten, die aus *der* [**Struktur D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) kopiert wurden.

</dd> <dt>

**operator=(D3D12 \_ PRIMITIVE \_ TOPOLOGY TYPE \_ const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE-Struktur.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM PRIMITIVE \_ \_ \_ \_ TOPOLOGY ist eine Typdefinitionsspezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

