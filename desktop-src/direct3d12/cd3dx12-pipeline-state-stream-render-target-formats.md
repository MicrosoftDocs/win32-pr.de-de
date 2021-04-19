---
title: CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die renderzielformate als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353340"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>CD3DX12 \_ - \_ Struktur des Pipeline Status-Stream- \_ \_ \_ Renderziels \_

Eine hilfsstruktur, die verwendet wird, um die renderzielformate als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ - \_ \_ \_ \_ renderzielformate des Pipeline Zustands Stroms \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz von \_ \_ \_ \_ \_ renderzielformaten eines CD3DX12 Pipeline-Statusdaten Stroms \_ .

</dd> <dt>

**CD3DX12 \_ - \_ \_ \_ renderzielformate des Pipeline Zustands Stroms \_ \_ (D3D12 \_ RT- \_ Format \_ Array konstant &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State- \_ Stream \_ \_ -renderzielformats \_ , das mit einem untergeordneten Typ von **D3D12 Pipeline State-untergeordneten \_ \_ \_ \_ Typen \_ \_ renderzielformate \_** und aus *i* kopierten untergeordneten Daten, einer Array Struktur im [**D3D12 RT- \_ \_ \_ Format**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) , initialisiert wird.

</dd> <dt>

**Operator = (D3D12 \_ RT- \_ Format \_ Array konstant& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ RT- \_ Format \_ Array () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**Array Struktur im D3D12 \_ RT- \_ Format \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ \_ -renderzielformate \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
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

 

