---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Blend-Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC Struktur
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
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361843"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend- \_ DESC-Struktur

Eine hilfsstruktur, die verwendet wird, um eine Blend-Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.

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

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC (CD3DX12 \_ Blend \_ DESC Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Blend** -und unter Objekt-Daten, die aus *i* kopiert wurden, einer [**CD3DX12 \_ Blend \_ DESC**](cd3dx12-blend-desc.md) -Struktur.

</dd> <dt>

**Operator = (CD3DX12 \_ Blend \_& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator CD3DX12 \_ Blend-Operator \_ ()**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12 \_ Blend \_**](cd3dx12-blend-desc.md) -Debug-Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

