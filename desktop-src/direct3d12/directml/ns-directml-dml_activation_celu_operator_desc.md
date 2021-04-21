---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Führt die AKTIVIERUNGsfunktion der kontinuierlich differenzierbaren exponentiellen linearen Einheit (EXPONENTIAL Linear Unit, CELU) für jedes Element in *InputTensor* aus und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*
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
ms.openlocfilehash: b6497e995601d7e9e01696f39920672674be07c4
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803730"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="ccd91-103">DML_ACTIVATION_CELU_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ccd91-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="ccd91-104">Führt die AKTIVIERUNGsfunktion der kontinuierlich differenzierbaren exponentiellen linearen Einheit (EXPONENTIAL Linear Unit, CELU) für jedes Element in *InputTensor* aus und platziert das Ergebnis in das entsprechende Element von *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="ccd91-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="ccd91-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ccd91-105">Where:</span></span>
* <span data-ttu-id="ccd91-106">exp(x) ist die funktion "natural exponentiation"</span><span class="sxs-lookup"><span data-stu-id="ccd91-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="ccd91-107">max(a,b) gibt den größeren der beiden Werte a,b zurück.</span><span class="sxs-lookup"><span data-stu-id="ccd91-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="ccd91-108">min(a,b) gibt den kleineren der beiden Werte a,b zurück.</span><span class="sxs-lookup"><span data-stu-id="ccd91-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="ccd91-109">Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass der Ausgabe-Tensor während der Bindung den Alias *InputTensor* aliasen darf.</span><span class="sxs-lookup"><span data-stu-id="ccd91-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccd91-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="ccd91-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ccd91-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ccd91-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd91-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccd91-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="ccd91-113">Member</span><span class="sxs-lookup"><span data-stu-id="ccd91-113">Members</span></span>

`InputTensor`

<span data-ttu-id="ccd91-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccd91-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccd91-115">Der Eingabe-Tensor, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccd91-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="ccd91-116">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccd91-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccd91-117">Der Ausgabe-Tensor, in den die Ergebnisse geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ccd91-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="ccd91-118">Typ: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="ccd91-118">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="ccd91-119">Der Alphakoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="ccd91-119">The alpha coefficient.</span></span> <span data-ttu-id="ccd91-120">Ein typischer Standardwert für diesen Wert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="ccd91-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="ccd91-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ccd91-121">Availability</span></span>
<span data-ttu-id="ccd91-122">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ccd91-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ccd91-123">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="ccd91-123">Tensor constraints</span></span>
<span data-ttu-id="ccd91-124">*InputTensor* und *OutputTensor* müssen die gleichen *Datentypen*, *DimensionCount* und *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ccd91-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ccd91-125">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ccd91-125">Tensor support</span></span>
| <span data-ttu-id="ccd91-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="ccd91-126">Tensor</span></span> | <span data-ttu-id="ccd91-127">Typ</span><span class="sxs-lookup"><span data-stu-id="ccd91-127">Kind</span></span> | <span data-ttu-id="ccd91-128">Unterstützte Dimensionsanzahl</span><span class="sxs-lookup"><span data-stu-id="ccd91-128">Supported Dimension Counts</span></span> | <span data-ttu-id="ccd91-129">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="ccd91-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ccd91-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="ccd91-130">InputTensor</span></span> | <span data-ttu-id="ccd91-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ccd91-131">Input</span></span> | <span data-ttu-id="ccd91-132">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ccd91-132">1 to 8</span></span> | <span data-ttu-id="ccd91-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ccd91-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ccd91-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ccd91-134">OutputTensor</span></span> | <span data-ttu-id="ccd91-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ccd91-135">Output</span></span> | <span data-ttu-id="ccd91-136">1 bis 8</span><span class="sxs-lookup"><span data-stu-id="ccd91-136">1 to 8</span></span> | <span data-ttu-id="ccd91-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ccd91-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="ccd91-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccd91-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ccd91-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="ccd91-139">**Header**</span></span> | <span data-ttu-id="ccd91-140">directml.h</span><span class="sxs-lookup"><span data-stu-id="ccd91-140">directml.h</span></span> |