---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY Struktur
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
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353343"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>CD3DX12 \_ - \_ \_ Struktur der \_ primitiven \_ Topologie des Pipeline Zustands Stroms

Eine hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

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

**CD3DX12 \_ \_ \_ \_ primitive Topologie des Pipeline Zustands Stroms \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ primitive \_ Topologie.

</dd> <dt>

**CD3DX12 \_ \_ \_ primitive Topologie des Pipeline Zustands Stroms \_ \_ (D3D12 \_ primitiver \_ \_ Topologietyp Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz einer primitiven CD3DX12 \_ Pipeline \_ State \_ Stream \_ \_ -Topologie, die mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ primitive \_ Topologie** und aus *i* kopierten untergeordneten Daten in einer primitiven [**\_ \_ topologietypstruktur \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) initialisiert wird.

</dd> <dt>

**Operator = (D3D12 \_ primitiver \_ \_ Topologietyp Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ primitiver \_ \_ Topologietyp () konstant**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ primitive \_ \_ Topologietyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ \_ \_ \_ \_ die primitive Topologie des Pipeline Zustands Stroms ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

