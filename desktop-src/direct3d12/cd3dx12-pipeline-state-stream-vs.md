---
title: CD3DX12_PIPELINE_STATE_STREAM_VS -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um einen Vertex-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VS-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4361cf50a97cd3d7bf2abc6995182e9ca24bad6b824505408aca98bd4b3ead42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045728"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ VS-Struktur

Eine Hilfsstruktur, die verwendet wird, um einen Vertex-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ VS**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ VS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ VS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 PIPELINE STATE STREAM VS, initialisiert mit dem Unterobjekttyp D3D12 PIPELINE STATE SUBOBJECT TYPE VS und unterobjektdaten, die aus \_ \_ i , einer \_ \_ [**D3D12 \_ SHADER \_ BYTECODE-Struktur,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) **\_ \_ \_ \_ \_** kopiert wurden.

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12-SHADER-BYTECODE-Struktur. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 PIPELINE STATE STREAM VS ist eine TypeDef-Spezialisierung der \_ \_ VORLAGE \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
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

 

