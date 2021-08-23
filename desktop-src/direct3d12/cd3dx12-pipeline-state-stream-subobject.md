---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT -Struktur (D3dx12.h)
description: Eine Vorlagen-Hilfsstruktur, die zum Kapseln von Unterobjekttyp- und Unterobjektdatenpaaren als einzelnes Objekt verwendet wird, das für eine Streambeschreibung geeignet ist.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT-Struktur
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
ms.openlocfilehash: 5d945296ae4ee09710b74b9fdf2259251632d25fb309ede2983858c0c59be72d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729480"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT-Struktur

Eine Vorlagen-Hilfsstruktur, die zum Kapseln von Unterobjekttyp- und Unterobjektdatenpaaren als einzelnes Objekt verwendet wird, das für eine Streambeschreibung geeignet ist.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ SUBOBJECT.

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT(** InnerStructType** const &i)**
</dt> <dd>

Erstellt eine neue CD3DX12 PIPELINE STATE STREAM SUBOBJECT-Vorlageninstanz, die mit dem Unterobjekttyp \_ \_ \_ \_ [**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) initialisiert wurde, und unterobjektdaten, die aus i kopiert wurden. Sowohl der Unterobjekttyp als auch der Unterobjektdatentyp werden als Vorlagenparameter, **Type** bzw. **InnerStructType,** angegeben. Weitere Informationen finden Sie weiter unten in den Anmerkungen.

</dd> <dt>

**operator=(** InnerStructType** const& i)**
</dt> <dd>

Kopierzuweisungsoperator.

</dd> <dt>

**operator **InnerStructType**() const**
</dt> <dd>

Implizite Konvertierung in den Unterobjektdatentyp, der durch den **InnerStructType-Vorlagenparameter** angegeben wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT ist eine Vorlage, die wie folgt definiert ist:


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



Der Vorlagenparameter **InnerStructType gibt** den Unterobjektdatentyp an. Das heißt, die Details des Unterobjekts, die in einen Stream codiert werden sollen. Der Vorlagenparameter **Type** gibt den Unterobjekttyp an. Das heißt, der Typ der -Struktur, der durch den Vorlagenparameter **InnerStructType angegeben wird.** Der Vorlagenparameter **DefaultArg** gibt einen optionalen Wert an, mit dem die Unterobjektdaten initialisiert werden, wenn eine Instanz der entsprechenden Vorlageninstanziierung standardmäßig erstellt wird. Um z. B. einen [**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) zu erstellen, der mit allgemeinen Blendzustandseinstellungen initialisiert wurde, indem [**CD3DX12 \_ DEFAULT verwendet wird.**](cd3dx12-default.md)

Hier sind die Vorlagen instanziierungen, die definiert sind:

-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ FLAGS**](cd3dx12-pipeline-state-stream-flags.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ NODE \_ MASK**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**STAMMSIGNATUR DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMS \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ INPUT \_ LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**PRIMITIVE TOPOLOGIE DES \_ CD3DX12-PIPELINEZUSTANDSSTREAMS \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ VS**](cd3dx12-pipeline-state-stream-vs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ STREAM \_ OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL \_ FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**RENDERZIELFORMATE FÜR \_ CD3DX12-PIPELINEZUSTANDSSTREAM \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SAMPLE \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SAMPLE \_ MASK**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CACHED \_ PSO**](cd3dx12-pipeline-state-stream-cached-pso.md)

Die [**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC,**](cd3dx12-pipeline-state-stream-blend-desc.md) [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL,**](cd3dx12-pipeline-state-stream-depth-stencil.md) [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)und [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ RASTERIZER-Strukturen**](cd3dx12-pipeline-state-stream-rasterizer.md) werden definiert, um ihre Unterobjektdaten mithilfe von [**CD3DX12 DEFAULT zu \_ initialisieren.**](cd3dx12-default.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

