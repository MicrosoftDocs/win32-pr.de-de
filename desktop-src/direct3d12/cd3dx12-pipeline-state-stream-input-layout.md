---
title: CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um ein Eingabe Layout als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366622"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Eingabe \_ Layout-Struktur

Eine hilfsstruktur, die verwendet wird, um ein Eingabe Layout als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ - \_ \_ \_ Eingabe \_ Layout des Pipeline Zustandsdaten Stroms**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Pipeline- \_ Zustandsdaten Strom- \_ \_ Eingabe \_ Layouts.

</dd> <dt>

**CD3DX12 \_ - \_ Eingabe Layout für Pipeline Zustandsdaten \_ Strom \_ \_ (D3D12 \_ input \_ Layout \_ DESC Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline- \_ Zustands \_ Datenstrom- \_ Eingabe \_ Layouts, initialisiert mit einem untergeordneten Typ **des \_ \_ \_ \_ \_ Eingabe \_ Layouts von D3D12-Pipeline** Zuständen und untergeordneten Objekten, die aus *i* kopiert wurden, einer [**D3D12- \_ Eingabe Layout- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) -Struktur.

</dd> <dt>

**Operator = (D3D12 \_ input \_ Layout \_ resc Konstante& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ Eingabe \_ Layout \_ () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ - \_ Eingabe \_ Layout**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ \_ \_ \_ -Eingabe Layout des Pipeline Zustandsdaten Stroms \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

