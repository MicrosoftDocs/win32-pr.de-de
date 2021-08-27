---
title: CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um eine Knotenmaske als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4850ff986f2006c506d79a8ece1ced873529c2a4939869cd704a4b7c3c4b03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119680"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK-Struktur

Eine Hilfsstruktur, die verwendet wird, um eine Knotenmaske als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**KNOTENMASKE DES \_ CD3DX12-PIPELINESTATUSSTREAMS \_ \_ \_ \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK(UINT const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK, initialisiert mit einem Unterobjekttyp von **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE NODE \_ \_ \_ MASK** und unterobjektdaten, die aus *i*, einer **UINT-Knotenmaske,** kopiert wurden.

</dd> <dt>

**operator=(UINT const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator UINT() const**
</dt> <dd>

Implizite Konvertierung in eine **UINT-Knotenmaske.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM NODE MASK ist eine \_ \_ \_ \_ Typedef-Spezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

