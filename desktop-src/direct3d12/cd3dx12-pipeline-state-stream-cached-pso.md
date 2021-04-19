---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um ein zwischengespeichertes PSO als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung
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
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355786"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>CD3DX12 \_ - \_ \_ \_ PSO-Struktur zwischengespeicherten Pipeline Zustandsdaten Strom \_

Eine hilfsstruktur, die verwendet wird, um ein zwischengespeichertes PSO als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung

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

**CD3DX12 \_ - \_ \_ \_ PSO zwischen gespeicherter Pipeline Zustandsdaten Strom \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Pipeline-Statusdaten Stroms, der \_ \_ \_ \_ zwischengespeichert wird \_ .

</dd> <dt>

**CD3DX12- \_ Pipeline- \_ \_ \_ \_ StatusStream zwischengespeichert PSO (D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status konstant &i)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ -Pipeline- \_ Statusdaten \_ Stroms \_ zwischengespeicherten \_ PSO, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Cache \_ PSO** und unter unter Objekt-Daten, die aus *i* kopiert wurden, einer [**D3D12 \_ zwischengespeicherten \_ Pipeline \_ Zustands**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) Struktur.

</dd> <dt>

**Operator = (D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status konstant& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Zustand () konstant**
</dt> <dd>

Implizite Konvertierung in eine [**\_ zwischengespeicherte D3D12- \_ Pipeline \_ Zustands**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ \_ -Pipeline \_ -StatusStream \_ , der zwischengespeichert \_ ist, ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

