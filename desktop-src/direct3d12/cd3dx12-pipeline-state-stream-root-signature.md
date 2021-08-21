---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um die Stammsignatur als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccddd5663b6a079656823efed4cb48b3183d88d0688149c7ae05d96e8dc1cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530700"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM ROOT \_ \_ \_ \_ SIGNATURE-Struktur

Eine Hilfsstruktur, die verwendet wird, um die Stammsignatur als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**STAMMSIGNATUR DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMS \_ \_ \_ \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ PIPELINE STATE STREAM ROOT \_ \_ \_ \_ SIGNATURE.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM ROOT \_ \_ \_ \_ SIGNATURE(ID3D12RootSignature \* const &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ PIPELINE STATE STREAM ROOT \_ \_ \_ \_ SIGNATURE, initialisiert mit dem Unterobjekttyp **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE ROOT \_ \_ \_ SIGNATURE** und unterobjektdaten, die aus *i*, einer [**ID3D12RootSignature-Struktur,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) kopiert wurden.

</dd> <dt>

**operator=(ID3D12RootSignature \* const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**operator ID3D12RootSignature \* () const**
</dt> <dd>

Implizite Konvertierung in einen [**ID3D12RootSignature-Strukturzeiger.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM ROOT SIGNATURE ist eine \_ \_ \_ \_ Typedef-Spezialisierung der [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
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

 

