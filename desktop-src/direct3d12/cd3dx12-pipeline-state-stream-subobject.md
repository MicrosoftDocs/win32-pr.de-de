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
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="9ce6b-104">CD3DX12 \_ Pipeline \_ State \_ Stream-Struktur des untergeordneten \_ Objekts</span><span class="sxs-lookup"><span data-stu-id="9ce6b-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="9ce6b-105">Eine auf Vorlagen basierende hilfsstruktur, die verwendet wird, um untergeordnete und untergeordnete Datenpaare als ein einzelnes Objekt zu kapseln, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ce6b-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="9ce6b-107">Member</span><span class="sxs-lookup"><span data-stu-id="9ce6b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ce6b-108">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="9ce6b-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State Stream- \_ unter \_ Objekts.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="9ce6b-110">**CD3DX12 \_ Pipeline \_ State \_ Stream-unter \_ Objekt (** innerstructtype \* \* Konstanten &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="9ce6b-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="9ce6b-111">Erstellt eine neue CD3DX12 \_ Pipeline \_ State \_ Stream \_ -untergeordnete Vorlagen Instanz, die mit einem untergeordneten Typ des [**D3D12 \_ Pipeline \_ State \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) -untergeordneten Typs initialisiert wurde, und untergeordnete Daten werden aus *i* kopiert.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="9ce6b-112">Der untergeordnete Typ und der untergeordnete Datentyp werden als Vorlagen Parameter ( **Type** bzw. **innerstructtype**) angegeben.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="9ce6b-113">Weitere Informationen finden Sie weiter unten in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="9ce6b-114">**Operator = (** innerstructtype \* \* Konstanten& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="9ce6b-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="9ce6b-115">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="9ce6b-116">**Operator **innerstructtype**() Konstanten**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="9ce6b-117">Implizite Konvertierung in den untergeordneten Datentyp, der durch den **innerstructtype** -Vorlagen Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ce6b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ce6b-118">Remarks</span></span>

<span data-ttu-id="9ce6b-119">CD3DX12 \_ Pipeline \_ State \_ Stream \_ ist eine Vorlage, die wie folgt definiert ist:</span><span class="sxs-lookup"><span data-stu-id="9ce6b-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


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



<span data-ttu-id="9ce6b-120">Der Vorlagen Parameter **innerstructtype** gibt den untergeordneten Datentyp an. Das heißt, die untergeordneten Details, die in einen Stream codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="9ce6b-121">Der Vorlagen **Parametertyp** gibt den Typ des untergeordneten Objekts an. Das heißt, der Typ der Struktur, die durch den Vorlagen Parameter **innerstructtype** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="9ce6b-122">Der Vorlagen Parameter **defaultArg** gibt einen optionalen Wert an, mit dem die untergeordneten Daten initialisiert werden, wenn eine Instanz der entsprechenden Vorlagen Instanziierung standardmäßig erstellt wird. um beispielsweise Default-Construct a [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) , initialisiert mit Common Blend-State defaults using [**CD3DX12 \_ default**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="9ce6b-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="9ce6b-123">Die folgenden Vorlagen Instanziierungen sind definiert:</span><span class="sxs-lookup"><span data-stu-id="9ce6b-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="9ce6b-124">**CD3DX12 \_ - \_ Flags für Pipeline Zustandsdaten \_ Strom \_**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="9ce6b-125">**CD3DX12- \_ Pipeline-Statusdaten Strom- \_ \_ \_ Knoten \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="9ce6b-126">**CD3DX12 \_ Pipeline-Statusdaten Strom-Stamm \_ \_ \_ \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="9ce6b-127">**CD3DX12 \_ - \_ \_ \_ Eingabe \_ Layout des Pipeline Zustandsdaten Stroms**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="9ce6b-128">**CD3DX12- \_ Pipeline- \_ \_ \_ \_ \_ Ausschneide \_ Wert des Pipeline Zustandsdaten Stroms**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="9ce6b-129">**CD3DX12 \_ \_ \_ \_ primitive Topologie des Pipeline Zustands Stroms \_**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="9ce6b-130">**CD3DX12 \_ Pipeline \_ State \_ Stream im \_ Vergleich zu**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="9ce6b-131">**CD3DX12 \_ Pipeline \_ State- \_ Stream- \_ GS**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="9ce6b-132">**Stream-Ausgabe des CD3DX12- \_ Pipeline \_ Zustandsdaten \_ \_ Stroms \_**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="9ce6b-133">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ HS**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="9ce6b-134">**CD3DX12 \_ Pipeline \_ State- \_ Stream- \_ DS**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="9ce6b-135">**CD3DX12 \_ Pipeline \_ Status- \_ Stream \_ PS**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="9ce6b-136">**CD3DX12- \_ Pipeline- \_ Stream- \_ \_ Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="9ce6b-137">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="9ce6b-138">**CD3DX12 \_ - \_ \_ \_ tiefen \_ Schablone für Pipeline Zustandsdaten Strom**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="9ce6b-139">**CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="9ce6b-140">**CD3DX12 \_ Daten \_ \_ Strom- \_ tiefen \_ Schablone- \_ Format des Pipeline Zustands**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="9ce6b-141">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="9ce6b-142">**CD3DX12 \_ - \_ \_ \_ \_ renderzielformate des Pipeline Zustands Stroms \_**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="9ce6b-143">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="9ce6b-144">**CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Beispiel \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="9ce6b-145">**CD3DX12 \_ - \_ \_ \_ PSO zwischen gespeicherter Pipeline Zustandsdaten Strom \_**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="9ce6b-146">Der [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ tiefen \_ Schablone**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Tiefe \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)und [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer**](cd3dx12-pipeline-state-stream-rasterizer.md) -Strukturen werden definiert, um die untergeordneten Daten mit allgemeinen Standardeinstellungen mithilfe von [**CD3DX12 \_ default**](cd3dx12-default.md)zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="9ce6b-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce6b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ce6b-147">Requirements</span></span>



| <span data-ttu-id="9ce6b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ce6b-148">Requirement</span></span> | <span data-ttu-id="9ce6b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="9ce6b-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce6b-150">Header</span><span class="sxs-lookup"><span data-stu-id="9ce6b-150">Header</span></span><br/> | <dl> <span data-ttu-id="9ce6b-151"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce6b-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce6b-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ce6b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce6b-153">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="9ce6b-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9ce6b-154">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="9ce6b-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

