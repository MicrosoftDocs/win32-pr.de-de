---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beschreibung der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1-Struktur (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367348"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1 Struktur

Eine hilfsstruktur, die verwendet wird, um eine Beschreibung der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ Tiefe \_ STENCIL1.

</dd> <dt>

**CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1 (CD3DX12- \_ tiefen \_ Schablone \_ DESC1 Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline \_ State Stream \_ - \_ Tiefe \_ STENCIL1, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Tiefe \_ STENCIL1** und untergeordnete Daten, die aus *i* kopiert werden, einer [**CD3DX12- \_ tiefen \_ Schablone \_ DESC1**](cd3dx12-depth-stencil-desc1.md) -Struktur.

</dd> <dt>

**Operator = (CD3DX12- \_ tiefen \_ Schablone \_ DESC1 Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 () konstant**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12 \_ Tiefe \_ Schablone \_ DESC1**](cd3dx12-depth-stencil-desc1.md) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ Tiefe \_ STENCIL1 ist eine typedef-Spezialisierung der Vorlage " [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ SubObject**](cd3dx12-pipeline-state-stream-subobject.md) " und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

