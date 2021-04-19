---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um den Wert des Index Puffer Streifens als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357222"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>CD3DX12 \_ Pipeline \_ State Stream-Datenstrom-Wert der IB-Bereichs \_ \_ \_ \_ Kürzung \_

Eine hilfsstruktur, die verwendet wird, um den Wert des Index Puffer Streifens als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12- \_ Pipeline- \_ \_ \_ \_ \_ Ausschneide \_ Wert des Pipeline Zustandsdaten Stroms**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines Datenstrom-Enumerationswerts für den CD3DX12 \_ Pipeline- \_ Statusdaten \_ Strom \_ \_ \_ \_ .

</dd> <dt>

**CD3DX12-Daten \_ Strom des Pipeline- \_ \_ \_ \_ \_ \_ statusausschnitts (D3D12- \_ Index- \_ Puffer Strip- \_ \_ Ausschneide \_ Wert Konstanten Konstante &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline- \_ statusausschneide Werts (Pipeline State) \_ \_ \_ \_ \_ , initialisiert mit einem untergeordneten Typ des **D3D12 \_ Pipeline \_ State \_ unter Objekt- \_ \_ \_ \_ \_ Werts** und aus den aus *i* kopierten Daten, einer [**D3D12 \_ Index \_ Puffer \_ Strip \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) -Struktur

</dd> <dt>

**Operator = (D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert konstant& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 der \_ Index \_ Puffer Strip- \_ \_ Ausschneide \_ Wert () konstant.**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

\_Der CD3DX12 \_ - \_ Pipeline \_ -Status-Stream \_ \_ \_ -Wert des Pipeline-Ausschnitts ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

