---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die zum Beschreiben von Pipeline-Statusflags als einzelnes Objekt verwendet wird, das für eine streambeschreibung geeignet ist.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357280"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>CD3DX12 \_ Pipeline \_ - \_ Stream- \_ Flags-Struktur

Eine hilfsstruktur, die zum Beschreiben von Pipeline-Statusflags als einzelnes Objekt verwendet wird, das für eine streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ - \_ Flags für Pipeline Zustandsdaten \_ Strom \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Pipeline- \_ \_ \_ StatusStream- \_ Flags.

</dd> <dt>

**CD3DX12 \_ - \_ Flags für Pipeline Zustandsdaten \_ Strom \_ (D3D12 \_ Pipeline- \_ \_ Statusflags Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz der CD3DX12 \_ Pipeline- \_ \_ \_ Statusflags, die mit einem untergeordneten Typ von **D3D12 Pipeline State-untergeordneten \_ \_ \_ \_ typfjektflags \_** und aus *i* kopierten untergeordneten Daten, einer [**D3D12 \_ Pipeline \_ State \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) -Struktur, initialisiert werden.

</dd> <dt>

**Operator = (D3D12 \_ Pipeline \_ State \_ Flags Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ Pipeline \_ - \_ Statusflags ()**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ Pipeline \_ State \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Flags ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

