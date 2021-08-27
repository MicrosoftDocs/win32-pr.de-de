---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um die Streamausgabebeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
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
ms.openlocfilehash: 5c0dbaf9952575801846adfbbb825c2ddbdc2e90d9d8d64f60f373ea2bcc1be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119670"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ \_ OUTPUT-Struktur

Eine Hilfsstruktur, die verwendet wird, um die Streamausgabebeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

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

**STREAMAUSGABE DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMS \_ \_ \_ \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE STATE STREAM STREAM \_ \_ \_ \_ OUTPUT.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM STREAM OUTPUT \_ \_ \_ \_ (D3D12 \_ STREAM OUTPUT \_ \_ DESC const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12-PIPELINE \_ \_ STATE STREAM STREAM \_ \_ \_ OUTPUT, initialisiert mit dem Unterobjekttyp **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE STREAM \_ \_ \_ OUTPUT** und von *i* kopierten Unterobjektdaten, einer [**D3D12 \_ STREAM OUTPUT \_ \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)

</dd> <dt>

**operator=(D3D12 \_ STREAM \_ OUTPUT \_ DESC const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator D3D12 \_ STREAM \_ OUTPUT \_ DESC() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ STREAM \_ OUTPUT \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM STREAM OUTPUT ist eine \_ \_ \_ \_ Typedef-Spezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

