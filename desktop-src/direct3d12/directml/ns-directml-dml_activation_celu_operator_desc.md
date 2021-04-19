---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Führt die fortlaufend differenzierbare Funktion zur Aktivierung der exponentiellen linearen Einheit (CELU) für jedes Element in *inputtensor* aus, wobei das Ergebnis in das entsprechende Element von *outputtensor* platziert wird.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: d474bd44c8a830117bb62927f4bda954a753b612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106369920"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="c0fb3-103">DML_ACTIVATION_CELU_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c0fb3-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c0fb3-104">Führt die fortlaufend differenzierbare Funktion zur Aktivierung der exponentiellen linearen Einheit (CELU) für jedes Element in *inputtensor* aus, wobei das Ergebnis in das entsprechende Element von *outputtensor* platziert wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="c0fb3-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="c0fb3-105">Where:</span></span>
* <span data-ttu-id="c0fb3-106">Exp (x) ist die natürliche exponentiations Funktion</span><span class="sxs-lookup"><span data-stu-id="c0fb3-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="c0fb3-107">Max (a, b) gibt den größeren der beiden Werte a, b</span><span class="sxs-lookup"><span data-stu-id="c0fb3-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="c0fb3-108">min (a, b) gibt den kleineren der beiden Werte a, b zurück.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="c0fb3-109">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass der ausgabetensor während der Bindung den Alias *inputtensor* zulässt.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0fb3-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="c0fb3-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c0fb3-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c0fb3-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0fb3-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0fb3-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="c0fb3-113">Member</span><span class="sxs-lookup"><span data-stu-id="c0fb3-113">Members</span></span>

`InputTensor`

<span data-ttu-id="c0fb3-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c0fb3-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c0fb3-115">Der eingabetensor, aus dem gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="c0fb3-116">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c0fb3-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c0fb3-117">Der Ausgabe Mandanten, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="c0fb3-118">Typ: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="c0fb3-118">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="c0fb3-119">Der Alpha Koeffizient.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-119">The alpha coefficient.</span></span> <span data-ttu-id="c0fb3-120">Ein typischer Standardwert für diesen Wert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="c0fb3-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c0fb3-121">Availability</span></span>
<span data-ttu-id="c0fb3-122">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="c0fb3-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c0fb3-123">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c0fb3-123">Tensor constraints</span></span>
<span data-ttu-id="c0fb3-124">*Inputtensor* und *outputtensor* müssen denselben *Datentyp*, jede *DimensionCount* und jede *Größe* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c0fb3-125">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c0fb3-125">Tensor support</span></span>
| <span data-ttu-id="c0fb3-126">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="c0fb3-126">Tensor</span></span> | <span data-ttu-id="c0fb3-127">Typ</span><span class="sxs-lookup"><span data-stu-id="c0fb3-127">Kind</span></span> | <span data-ttu-id="c0fb3-128">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="c0fb3-128">Supported Dimension Counts</span></span> | <span data-ttu-id="c0fb3-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="c0fb3-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c0fb3-130">Inputtensor</span><span class="sxs-lookup"><span data-stu-id="c0fb3-130">InputTensor</span></span> | <span data-ttu-id="c0fb3-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c0fb3-131">Input</span></span> | <span data-ttu-id="c0fb3-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="c0fb3-132">1 to 8</span></span> | <span data-ttu-id="c0fb3-133">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c0fb3-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c0fb3-134">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="c0fb3-134">OutputTensor</span></span> | <span data-ttu-id="c0fb3-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c0fb3-135">Output</span></span> | <span data-ttu-id="c0fb3-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="c0fb3-136">1 to 8</span></span> | <span data-ttu-id="c0fb3-137">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c0fb3-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="c0fb3-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0fb3-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c0fb3-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="c0fb3-139">**Header**</span></span> | <span data-ttu-id="c0fb3-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="c0fb3-140">directml.h</span></span> |