---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT-Struktur (D3dx12. h)
description: Eine auf Vorlagen basierende hilfsstruktur, die verwendet wird, um untergeordnete und untergeordnete Datenpaare als ein einzelnes Objekt zu kapseln, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364394"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream-Struktur des untergeordneten \_ Objekts

Eine auf Vorlagen basierende hilfsstruktur, die verwendet wird, um untergeordnete und untergeordnete Datenpaare als ein einzelnes Objekt zu kapseln, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State Stream- \_ unter \_ Objekts.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream-unter \_ Objekt (** innerstructtype * * Konstanten &i) * *
</dt> <dd>

Erstellt eine neue CD3DX12 \_ Pipeline \_ State \_ Stream \_ -untergeordnete Vorlagen Instanz, die mit einem untergeordneten Typ des [**D3D12 \_ Pipeline \_ State \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) -untergeordneten Typs initialisiert wurde, und untergeordnete Daten werden aus *i* kopiert. Der untergeordnete Typ und der untergeordnete Datentyp werden als Vorlagen Parameter ( **Type** bzw. **innerstructtype**) angegeben. Weitere Informationen finden Sie weiter unten in den hinweisen.

</dd> <dt>

**Operator = (** innerstructtype * * Konstanten& i) * *
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator **innerstructtype**() Konstanten**
</dt> <dd>

Implizite Konvertierung in den untergeordneten Datentyp, der durch den **innerstructtype** -Vorlagen Parameter angegeben wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream \_ ist eine Vorlage, die wie folgt definiert ist:


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



Der Vorlagen Parameter **innerstructtype** gibt den untergeordneten Datentyp an. Das heißt, die untergeordneten Details, die in einen Stream codiert werden sollen. Der Vorlagen **Parametertyp** gibt den Typ des untergeordneten Objekts an. Das heißt, der Typ der Struktur, die durch den Vorlagen Parameter **innerstructtype** angegeben wird. Der Vorlagen Parameter **defaultArg** gibt einen optionalen Wert an, mit dem die untergeordneten Daten initialisiert werden, wenn eine Instanz der entsprechenden Vorlagen Instanziierung standardmäßig erstellt wird. um beispielsweise Default-Construct a [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) , initialisiert mit Common Blend-State defaults using [**CD3DX12 \_ default**](cd3dx12-default.md).

Die folgenden Vorlagen Instanziierungen sind definiert:

-   [**CD3DX12 \_ - \_ Flags für Pipeline Zustandsdaten \_ Strom \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**CD3DX12- \_ Pipeline-Statusdaten Strom- \_ \_ \_ Knoten \_ Maske**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**CD3DX12 \_ Pipeline-Statusdaten Strom-Stamm \_ \_ \_ \_ Signatur**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**CD3DX12 \_ - \_ \_ \_ Eingabe \_ Layout des Pipeline Zustandsdaten Stroms**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12- \_ Pipeline- \_ \_ \_ \_ \_ Ausschneide \_ Wert des Pipeline Zustandsdaten Stroms**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**CD3DX12 \_ \_ \_ \_ primitive Topologie des Pipeline Zustands Stroms \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**CD3DX12 \_ Pipeline \_ State \_ Stream im \_ Vergleich zu**](cd3dx12-pipeline-state-stream-vs.md)
-   [**CD3DX12 \_ Pipeline \_ State- \_ Stream- \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**Stream-Ausgabe des CD3DX12- \_ Pipeline \_ Zustandsdaten \_ \_ Stroms \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**CD3DX12 \_ Pipeline \_ State- \_ Stream- \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ Pipeline \_ Status- \_ Stream \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**CD3DX12- \_ Pipeline- \_ Stream- \_ \_ Datenstrom**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**CD3DX12 \_ - \_ \_ \_ tiefen \_ Schablone für Pipeline Zustandsdaten Strom**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**CD3DX12 \_ Daten \_ \_ Strom- \_ tiefen \_ Schablone- \_ Format des Pipeline Zustands**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**CD3DX12 \_ - \_ \_ \_ \_ renderzielformate des Pipeline Zustands Stroms \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Beispiel \_ Maske**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**CD3DX12 \_ - \_ \_ \_ PSO zwischen gespeicherter Pipeline Zustandsdaten Strom \_**](cd3dx12-pipeline-state-stream-cached-pso.md)

Der [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ tiefen \_ Schablone**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Tiefe \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)und [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer**](cd3dx12-pipeline-state-stream-rasterizer.md) -Strukturen werden definiert, um die untergeordneten Daten mit allgemeinen Standardeinstellungen mithilfe von [**CD3DX12 \_ default**](cd3dx12-default.md)zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

