---
title: CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beschreibung des Rasterizers als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373486"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer Structure

Eine hilfsstruktur, die verwendet wird, um eine Beschreibung des Rasterizers als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State Stream- \_ \_ Rasterizers.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer (CD3DX12 \_ Rasterizer \_ DESC Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ -Rasterizers, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Rasterizer** und unter Objekt Data kopiert aus *i*, einer [**CD3DX12 \_ Rasterizer \_ DESC**](cd3dx12-rasterizer-desc.md) -Struktur.

</dd> <dt>

**Operator = (CD3DX12 \_ Rasterizer \_ resc Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator CD3DX12 \_ Rasterizer \_ Entsc () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12 \_ Rasterizer \_**](cd3dx12-rasterizer-desc.md) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 

