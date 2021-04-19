---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die Datenstrom-Ausgabe Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367347"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>CD3DX12 \_ Pipeline Status-Stream- \_ \_ \_ \_ Ausgabestruktur

Eine hilfsstruktur, die verwendet wird, um die Datenstrom-Ausgabe Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**Stream-Ausgabe des CD3DX12- \_ Pipeline \_ Zustandsdaten \_ \_ Stroms \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz der Stream-Ausgabe eines CD3DX12 \_ Pipeline-Statusdaten \_ \_ Stroms \_ \_ .

</dd> <dt>

**CD3DX12 Pipeline-Stream-Stream- \_ Ausgabe des Pipeline \_ Status \_ \_ \_ (D3D12 \_ Stream- \_ Ausgabe \_ DESC Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz der Stream- \_ Ausgabe eines CD3DX12 Pipeline \_ \_ -Statusdaten Stroms \_ \_ , initialisiert mit einem untergeordneten Typ von D3D12-Pipeline-statusausgabetyp- **\_ \_ \_ \_ \_ \_ Streamausgabe** und untergeordneten Daten, die aus *i* kopiert werden, einer D3D12- [**Stream- \_ \_ Ausgabe \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) -Struktur.

</dd> <dt>

**Operator = (D3D12 \_ Stream \_ Output \_ DESC& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ Stream \_ Output \_ DESC () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**\_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) -Struktur der D3D12 Stream-Ausgabe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Stream \_ Output ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

