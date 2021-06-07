---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Kompiliert ein Diagramm von DirectML-Operatoren in ein Objekt, das an die GPU gesendet werden kann.
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
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417175"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="00db0-103">IDMLDevice1::CompileGraph-Methode (directml.h)</span><span class="sxs-lookup"><span data-stu-id="00db0-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="00db0-104">Kompiliert ein Diagramm von DirectML-Operatoren in ein Objekt, das an die GPU gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="00db0-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="00db0-105">Ein kompilierter Operator stellt die effiziente, gebackene Form eines Operators dar, der für die Ausführung auf der GPU geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="00db0-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="00db0-106">Ein kompilierter Operator enthält den Zustand (z. B. Shader und andere Objekte), der für die Ausführung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="00db0-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="00db0-107">Da ein kompilierter Operator die [IDMLPageable-Schnittstelle](/windows/win32/api/directml/nn-directml-idmlpageable) implementiert, können Sie eine schnittstelle aus dem GPU-Speicher aus dem GPU-Speicher ausziehen, wenn Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="00db0-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="00db0-108">Weitere Informationen finden Sie unter [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) und [IDMLDevice1::MakeResident.](/windows/win32/api/directml/nf-directml-idmldevice-makeresident)</span><span class="sxs-lookup"><span data-stu-id="00db0-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="00db0-109">Der kompilierte Operator verwendet die [IDMLOperator-Objekte,](/windows/win32/api/directml/nn-directml-idmloperator) die in der Graphbeschreibung angegeben sind, und verweist nicht darauf, nachdem diese Methode zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="00db0-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00db0-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="00db0-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="00db0-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="00db0-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="00db0-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="00db0-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="00db0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="00db0-113">Parameters</span></span>

`desc`

<span data-ttu-id="00db0-114">Typ: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="00db0-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="00db0-115">Eine Beschreibung des zu kompilierenden Diagramms.</span><span class="sxs-lookup"><span data-stu-id="00db0-115">A description of the graph to compile.</span></span> <span data-ttu-id="00db0-116">Weitere Informationen finden Sie [unter DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="00db0-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="00db0-117">Typ: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="00db0-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="00db0-118">Alle Flags zum Steuern der Ausführung dieses Operators.</span><span class="sxs-lookup"><span data-stu-id="00db0-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="00db0-119">Typ: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="00db0-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="00db0-120">Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in <i>ppv</i>zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="00db0-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="00db0-121">Es wird erwartet, dass dies die GUID von [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)ist.</span><span class="sxs-lookup"><span data-stu-id="00db0-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="00db0-122">Typ: <b>void\*\*</b></span><span class="sxs-lookup"><span data-stu-id="00db0-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="00db0-123">Ein Zeiger auf einen Speicherblock, der einen Zeiger auf den kompilierten Operator empfängt.</span><span class="sxs-lookup"><span data-stu-id="00db0-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="00db0-124">Dies ist die Adresse eines Zeigers auf einen [IDMLCompiledOperator,](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)der den erstellten kompilierten Operator darstellt.</span><span class="sxs-lookup"><span data-stu-id="00db0-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="00db0-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00db0-125">Return value</span></span>

<span data-ttu-id="00db0-126">Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="00db0-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="00db0-127">Wenn diese Methode erfolgreich ist, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00db0-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="00db0-128">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00db0-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00db0-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00db0-129">Remarks</span></span>

<span data-ttu-id="00db0-130">Die Graph-API für DirectML-Operatoren bietet eine abstrakte Möglichkeit, DirectML effizient auf verschiedenen Hardwarekomponenten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="00db0-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="00db0-131">DirectML wendet Optimierungen auf Tensorebene an, z. B. die Auswahl des effizientesten Tensorlayouts basierend auf dem verwendeten Adapter.</span><span class="sxs-lookup"><span data-stu-id="00db0-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="00db0-132">Außerdem werden Optimierungen wie das Entfernen von Join- oder Split-Operatoren angewendet.</span><span class="sxs-lookup"><span data-stu-id="00db0-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="00db0-133">Es wird empfohlen, vor dem Erstellen eines DirectML-Graphen optimierungsorientierte Optimierungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="00db0-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="00db0-134">Beispiel: Zusammenführung von Convolution-Operatoren mit BatchNorm, Konstantenfaltung und gängiger Teilausdruckslöschung.</span><span class="sxs-lookup"><span data-stu-id="00db0-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="00db0-135">Die Optimierungen im Graphoptimierer von DirectML sollen solche geräteunabhängigen Optimierungen ergänzen, die in der Regel generisch von Machine Learning-Frameworks verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="00db0-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="00db0-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="00db0-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="00db0-137">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="00db0-137">**Target Platform**</span></span> | <span data-ttu-id="00db0-138">Windows</span><span class="sxs-lookup"><span data-stu-id="00db0-138">Windows</span></span> |
| <span data-ttu-id="00db0-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="00db0-139">**Header**</span></span> | <span data-ttu-id="00db0-140">directml.h</span><span class="sxs-lookup"><span data-stu-id="00db0-140">directml.h</span></span> |
| <span data-ttu-id="00db0-141">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="00db0-141">**Library**</span></span> | <span data-ttu-id="00db0-142">DirectML.lib</span><span class="sxs-lookup"><span data-stu-id="00db0-142">DirectML.lib</span></span> |
| <span data-ttu-id="00db0-143">**Dll**</span><span class="sxs-lookup"><span data-stu-id="00db0-143">**DLL**</span></span> | <span data-ttu-id="00db0-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="00db0-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="00db0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00db0-145">See also</span></span>

[<span data-ttu-id="00db0-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="00db0-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)