---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um Pipelinezustandsflags als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS-Struktur
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
ms.openlocfilehash: 2d8789fb8c393ecaf83e0295654092b22aba7f497abf909c46bac422d442c6fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530709"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ FLAGS-Struktur

Eine Hilfsstruktur, die verwendet wird, um Pipelinezustandsflags als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ FLAGS**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ FLAGS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ FLAGS(D3D12 \_ PIPELINE STATE \_ \_ FLAGS const &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ FLAGS, initialisiert mit einem Unterobjekttyp von **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE \_ \_ FLAGS** und unterobjektdaten, die aus *i*, einer [**D3D12 \_ PIPELINE STATE \_ \_ FLAGS-Struktur,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) kopiert wurden.

</dd> <dt>

**operator=(D3D12 \_ PIPELINE \_ STATE \_ FLAGS const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator D3D12 \_ PIPELINE \_ STATE \_ FLAGS() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ PIPELINE \_ STATE \_ FLAGS-Struktur.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ FLAGS ist eine Typedef-Spezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

