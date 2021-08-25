---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die verwendet wird, um eine Blendbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300506d2c41be5a5380f4f0f64c93779185fd59ced2e0dd613d926f8397ea85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752170"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC-Struktur

Eine Hilfsstruktur, die verwendet wird, um eine Blendbeschreibung als einzelnes Objekt zu beschreiben, das für eine Streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC(CD3DX12 \_ BLEND \_ DESC const &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 PIPELINE STATE STREAM BLEND DESC, initialisiert mit dem Unterobjekttyp D3D12 PIPELINE STATE SUBOBJECT TYPE BLEND und unterobjektdaten, die aus \_ \_ i , einer \_ \_ \_ [**CD3DX12 \_ BLEND \_ DESC-Struktur,**](cd3dx12-blend-desc.md) **\_ \_ \_ \_ \_** kopiert wurden.

</dd> <dt>

**operator=(CD3DX12 \_ BLEND \_ DESC const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**Operator CD3DX12 \_ BLEND \_ DESC() const**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12 \_ BLEND \_ DESC-Struktur.**](cd3dx12-blend-desc.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 PIPELINE STATE STREAM BLEND DESC ist eine Typedef-Spezialisierung der \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Vorlage**](cd3dx12-pipeline-state-stream-subobject.md) und wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

