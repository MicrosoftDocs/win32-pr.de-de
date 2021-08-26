---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um den Indexpufferstrip-Schnittwert als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
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
ms.openlocfilehash: 1e204b4f89cced7cf0bd5cdcb21702c37c241a81abfbc12d8644eafdb3c7c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988410"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT \_ \_ \_ \_ \_ \_ VALUE-Struktur

Eine Hilfsstruktur, die verwendet wird, um den Indexpufferstrip-Schnittwert als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT \_ \_ \_ \_ \_ \_ VALUE.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT VALUE \_ \_ \_ \_ \_ \_ (D3D12 \_ INDEX BUFFER STRIP CUT VALUE \_ \_ \_ \_ const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT \_ \_ \_ \_ \_ \_ VALUE, initialisiert mit einem Unterobjekttyp von **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE IB STRIP \_ \_ CUT \_ \_ \_ VALUE** und Unterobjektdaten, die aus *i*, einer [**D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE-Struktur,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) kopiert wurden.

</dd> <dt>

**operator=(D3D12 \_ INDEX BUFFER STRIP CUT VALUE \_ \_ \_ \_ const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE-Struktur.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT VALUE ist eine \_ \_ \_ \_ \_ \_ Typdefinitionsspezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

