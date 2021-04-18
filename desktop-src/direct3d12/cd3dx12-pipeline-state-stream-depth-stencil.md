---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beschreibung der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL-Struktur (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351933"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>CD3DX12 \_ - \_ \_ \_ tiefen Schablone- \_ Struktur der Pipeline Zustandsdaten Strom

Eine hilfsstruktur, die verwendet wird, um eine Beschreibung der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ - \_ \_ \_ tiefen \_ Schablone für Pipeline Zustandsdaten Strom**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz der \_ tiefen Schablone eines CD3DX12 \_ Pipeline \_ Zustands \_ Stroms \_ .

</dd> <dt>

**CD3DX12 \_ - \_ tiefen Schablone für Pipeline Zustandsdaten \_ Strom \_ \_ (CD3DX12 \_ tiefen \_ Schablone \_ DESC Konstanten &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ -tiefen \_ Schablone, initialisiert mit einem untergeordneten Typ der **\_ tiefen Schablone des D3D12-Pipeline \_ Zustands \_ unter Objekt \_ \_ \_** und der von *i* kopierten untergeordneten Daten, einer [**CD3DX12- \_ tiefen \_ Schablone- \_ DESC**](cd3dx12-depth-stencil-desc.md) -Struktur.

</dd> <dt>

**Operator = (CD3DX12 \_ tiefen \_ Schablone \_& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator CD3DX12 \_ tiefen \_ Schablone \_ () Konstanten ()**
</dt> <dd>

Implizite Konvertierung in eine [**CD3DX12- \_ tiefen \_ Schablone \_**](cd3dx12-depth-stencil-desc.md) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

\_Die CD3DX12 \_ \_ \_ -tiefen Schablone des Pipeline Zustands Stroms \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

