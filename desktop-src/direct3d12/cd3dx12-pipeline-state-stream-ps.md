---
title: CD3DX12_PIPELINE_STATE_STREAM_PS-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um einen Pixel-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: A71E2ABE-5B52-41B4-ACE0-25CA63EF2565
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a3ea2393482f09b233cd7bb8a404cc55ed39588a44ba334fd85e11d3bfb16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734022"
---
# <a name="cd3dx12_pipeline_state_stream_ps-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ PS-Struktur

Eine Hilfsstruktur, die verwendet wird, um einen Pixel-Shader als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PS {
                                   CD3DX12_PIPELINE_STATE_STREAM_PS;
                                   CD3DX12_PIPELINE_STATE_STREAM_PS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ PS**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ PS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ PS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ PS, initialisiert mit einem Unterobjekttyp von **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE \_ \_ PS** und aus *i* kopierten Unterobjektdaten, einer [**D3D12 \_ SHADER \_ BYTECODE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

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

CD3DX12 \_ PIPELINE STATE STREAM PS ist eine \_ \_ \_ Typedef-Spezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PS>
    CD3DX12_PIPELINE_STATE_STREAM_PS;
          
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

 

