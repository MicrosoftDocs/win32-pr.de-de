---
title: CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Knoten Maske als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK Struktur
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
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366621"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Knoten \_ Masken Struktur

Eine hilfsstruktur, die verwendet wird, um eine Knoten Maske als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

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

**CD3DX12- \_ Pipeline-Statusdaten Strom- \_ \_ \_ Knoten \_ Maske**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ Pipeline \_ State Stream- \_ \_ Knoten \_ Maske.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Knoten \_ Maske (uint-Konstante &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline- \_ Status \_ \_ Datenstrom \_ -Knoten Maske, die mit einem untergeordneten Typ der **Knoten Maske des D3D12-Pipeline Status-untergeordneten \_ \_ \_ \_ Typs \_ \_** und untergeordneten Daten, die aus *i* kopiert werden,, einer **uint** -Knoten Maske, initialisiert wird.

</dd> <dt>

**Operator = (uint Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator uint () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine **uint** -Knoten Maske.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Node \_ Mask ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
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

 

