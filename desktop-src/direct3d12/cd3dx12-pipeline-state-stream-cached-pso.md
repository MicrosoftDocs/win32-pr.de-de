---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um eine zwischengespeicherte PSO als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11cb4e7a784b89a825f1e1b64083c50cc77731bbadf84d248106d69da9cf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751920"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ CACHED \_ PSO-Struktur

Eine Hilfsstruktur, die verwendet wird, um eine zwischengespeicherte PSO als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CACHED \_ PSO**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ CACHED \_ PSO.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ CACHED \_ PSO(D3D12 \_ CACHED PIPELINE STATE \_ \_ const &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ CACHED \_ PSO, initialisiert mit dem Unterobjekttyp **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE \_ \_ CACHED \_ PSO** und den aus *i* kopierten Unterobjektdaten, einer [**D3D12 \_ CACHED \_ PIPELINE \_ STATE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> <dt>

**operator=(D3D12 \_ CACHED \_ PIPELINE STATE \_ const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator D3D12 \_ CACHED \_ PIPELINE \_ STATE() const**
</dt> <dd>

Implizite Konvertierung in eine [**D3D12 \_ CACHED \_ PIPELINE \_ STATE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ CACHED \_ PSO ist eine Typedef-Spezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

