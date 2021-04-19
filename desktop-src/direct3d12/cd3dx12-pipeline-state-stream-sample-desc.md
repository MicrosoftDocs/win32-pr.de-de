---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beispiel Beschreibung als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351988"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample ( \_ DESC-Struktur)

Eine hilfsstruktur, die verwendet wird, um eine Beispiel Beschreibung als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC (DXGI \_ Sample \_ DESC resc &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC, initialisiert with a unter Objekt Type of **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Sample \_ DESC** and unter Objekt Data kopiert from *i*, a [**DXGI \_ Sample \_ DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) Structure.

</dd> <dt>

**Operator = (DXGI \_ Sample \_& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator DXGI \_ Sample Debug \_ () Konstanten**
</dt> <dd>

Implizite Konvertierung in eine [**DXGI \_ - \_ Beispiel**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

