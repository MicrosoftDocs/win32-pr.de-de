---
UID: NF:directml.IDMLDevice1.CompileGraph
title: 'IDMLDevice1:: compilegraph'
description: Kompiliert ein Diagramm von directml-Operatoren in ein Objekt, das an die GPU gesendet werden kann.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361741"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="04ff8-103">IDMLDevice1:: compilegraph-Methode (directml. h)</span><span class="sxs-lookup"><span data-stu-id="04ff8-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="04ff8-104">Kompiliert ein Diagramm von directml-Operatoren in ein Objekt, das an die GPU gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="04ff8-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="04ff8-105">Ein kompilierter Operator stellt die effiziente, gebackte Form eines Operators dar, der für die Ausführung auf der GPU geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="04ff8-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="04ff8-106">Ein kompilierter Operator enthält Status (z. b. Shader und andere Objekte), die für die Ausführung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="04ff8-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="04ff8-107">Da ein kompilierter Operator die [idmlpable](/windows/win32/api/directml/nn-directml-idmlpageable) -Schnittstelle implementiert, können Sie bei Bedarf einen aus GPU-Speicher entfernen.</span><span class="sxs-lookup"><span data-stu-id="04ff8-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="04ff8-108">Weitere Informationen finden Sie unter [IDMLDevice1:: evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) und [IDMLDevice1:: makeresident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .</span><span class="sxs-lookup"><span data-stu-id="04ff8-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="04ff8-109">Der kompilierte Operator verwendet weder noch die [idmloperator](/windows/win32/api/directml/nn-directml-idmloperator) -Objekte, die innerhalb der Diagramm Beschreibung bereitgestellt werden, nachdem diese Methode zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="04ff8-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ff8-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="04ff8-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="04ff8-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="04ff8-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04ff8-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="04ff8-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="04ff8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="04ff8-113">Parameters</span></span>

`desc`

<span data-ttu-id="04ff8-114">Typ: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="04ff8-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="04ff8-115">Eine Beschreibung des zu kompilierenden Diagramms.</span><span class="sxs-lookup"><span data-stu-id="04ff8-115">A description of the graph to compile.</span></span> <span data-ttu-id="04ff8-116">Siehe [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="04ff8-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="04ff8-117">Typ: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="04ff8-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="04ff8-118">Alle Flags zum Steuern der Ausführung dieses Operators.</span><span class="sxs-lookup"><span data-stu-id="04ff8-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="04ff8-119">Typ: <b>refID</b></span><span class="sxs-lookup"><span data-stu-id="04ff8-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="04ff8-120">Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in <i>PPV</i>zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="04ff8-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="04ff8-121">Dies wird als GUID von [idmlcompiledoperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)erwartet.</span><span class="sxs-lookup"><span data-stu-id="04ff8-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="04ff8-122">Typ: <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="04ff8-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="04ff8-123">Ein Zeiger auf einen Speicherblock, der einen Zeiger auf den kompilierten Operator empfängt.</span><span class="sxs-lookup"><span data-stu-id="04ff8-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="04ff8-124">Dies ist die Adresse eines Zeigers auf einen [idmlcompiledoperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), der den erstellten kompilierten Operator darstellt.</span><span class="sxs-lookup"><span data-stu-id="04ff8-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="04ff8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04ff8-125">Return value</span></span>

<span data-ttu-id="04ff8-126">Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="04ff8-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="04ff8-127">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="04ff8-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="04ff8-128">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="04ff8-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ff8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04ff8-129">Remarks</span></span>

<span data-ttu-id="04ff8-130">Die Graph-API des directml-Operators bietet eine abstrakte Möglichkeit zur effizienten Verwendung von directml über verschiedene Hardware hinweg.</span><span class="sxs-lookup"><span data-stu-id="04ff8-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="04ff8-131">Directml wendet Optimierungen auf tensorflow-Ebene an, z. b. die Auswahl des effizientesten tensorflow-Layouts basierend auf dem verwendeten Adapter.</span><span class="sxs-lookup"><span data-stu-id="04ff8-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="04ff8-132">Außerdem werden Optimierungen angewendet, z. b. das Entfernen von Join-oder Split-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="04ff8-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="04ff8-133">Es wird empfohlen, dass Sie vor dem Aufbau eines directml-Diagramms auf hoher Ebene Optimierungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="04ff8-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="04ff8-134">Beispielsweise das Zusammenfassen von-Operatoren mit batchnorm, Konstantenfaltung und allgemeiner Teil Ausdrucks Löschung.</span><span class="sxs-lookup"><span data-stu-id="04ff8-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="04ff8-135">Die Optimierungen im Graph-Optimierer von directml dienen dazu, solche geräteunabhängigen Optimierungen zu ergänzen, die in der Regel generisch von Machine Learning-Frameworks verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="04ff8-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ff8-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04ff8-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="04ff8-137">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="04ff8-137">**Target Platform**</span></span> | <span data-ttu-id="04ff8-138">Windows</span><span class="sxs-lookup"><span data-stu-id="04ff8-138">Windows</span></span> |
| <span data-ttu-id="04ff8-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="04ff8-139">**Header**</span></span> | <span data-ttu-id="04ff8-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="04ff8-140">directml.h</span></span> |
| <span data-ttu-id="04ff8-141">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="04ff8-141">**Library**</span></span> | <span data-ttu-id="04ff8-142">Directml. lib</span><span class="sxs-lookup"><span data-stu-id="04ff8-142">DirectML.lib</span></span> |
| <span data-ttu-id="04ff8-143">**DLL**</span><span class="sxs-lookup"><span data-stu-id="04ff8-143">**DLL**</span></span> | <span data-ttu-id="04ff8-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="04ff8-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="04ff8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04ff8-145">See also</span></span>

[<span data-ttu-id="04ff8-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="04ff8-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)