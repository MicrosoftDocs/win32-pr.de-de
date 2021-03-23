---
title: Verbessern der Leistung mithilfe von Fused-Operatoren
description: Einige directml-Operatoren unterstützen ein Konzept, das als *Fusion* bezeichnet wird. Die Operator Fusion ist eine Möglichkeit, die Leistung zu verbessern, indem ein Operator (in der Regel eine Aktivierungsfunktion) in einen anderen Operator gemergt wird, sodass Sie zusammen ausgeführt werden, ohne dass ein Roundtrip zum Arbeitsspeicher erforderlich ist.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: b692727d52e252bb3752573e692bcf5beda794e2
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548768"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="5c680-104">Verbessern der Leistung mithilfe von Fused-Operatoren</span><span class="sxs-lookup"><span data-stu-id="5c680-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="5c680-105">Einige directml-Operatoren unterstützen ein Konzept, das als *Fusion* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5c680-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="5c680-106">Die Operator Fusion ist eine Möglichkeit, die Leistung zu verbessern, indem ein Operator (in der Regel eine Aktivierungsfunktion) in einen anderen Operator gemergt wird, sodass Sie zusammen ausgeführt werden, ohne dass ein Roundtrip zum Arbeitsspeicher erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5c680-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="5c680-107">Zeitpunkt der Aktivierung von Aktivierungen</span><span class="sxs-lookup"><span data-stu-id="5c680-107">When to fuse activations</span></span>

<span data-ttu-id="5c680-108">Die Aktivierung von aktivierten Aktivierungen ist eine Leistungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="5c680-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="5c680-109">Ein sehr gängiges Szenario in vielen Machine Learning-Modellen (ml) ist das Anwenden einer nicht Linearität (eine Aktivierungsfunktion) auf die Ausgabe jeder Ebene im Modell.</span><span class="sxs-lookup"><span data-stu-id="5c680-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="5c680-110">Normalerweise ist hierfür ein Roundtrip zum Grafikspeicher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5c680-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="5c680-111">Wenn z. b. auf eine Zusammenstellung von einer nicht gecluchten relu-Aktivierung folgt, muss die GPU warten, bis die Ergebnisse der Übertragung in den GPU-Speicher geschrieben wurden, bevor Sie mit dem Berechnen der relu-Aktivierungs Ebene beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="5c680-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="5c680-112">Wenn die Compute-Arbeitsauslastung der meisten Aktivierungs Funktionen tendenziell gering ist, kann dieser Roundtrip zum Grafikspeicher zu einem großen Leistungsengpass beitragen.</span><span class="sxs-lookup"><span data-stu-id="5c680-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="5c680-113">Die Operator Fusion ermöglicht die Ausführung der Aktivierungsfunktion (relu im obigen Beispiel) als Teil des vorangehenden Operators (z. b.).</span><span class="sxs-lookup"><span data-stu-id="5c680-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="5c680-114">Dadurch kann die GPU die Aktivierungsfunktion berechnen, ohne darauf zu warten, dass die Ergebnisse des vorangehenden Operators in den Arbeitsspeicher geschrieben werden, &mdash; und die Leistung wird verbessert.</span><span class="sxs-lookup"><span data-stu-id="5c680-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="5c680-115">Da die Aktivierung von aktivierten Aktivierungen das gleiche Ergebnis ergibt, aber in vielen Fällen schneller ist, empfiehlt es sich, Aktivierungs Ebenen auszuschließen, indem Sie Sie nach Möglichkeit in den vorangehenden Operator hineinbringen.</span><span class="sxs-lookup"><span data-stu-id="5c680-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="5c680-116">Vorgehensweise beim vereinen von Aktivierungen</span><span class="sxs-lookup"><span data-stu-id="5c680-116">How to fuse activations</span></span>

<span data-ttu-id="5c680-117">Operatoren, die die Aktivierung von Aktivierungen unterstützen, verfügen über einen zusätzlichen optionalen Parameter in der Operator Struktur, `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="5c680-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="5c680-118">Beispielsweise unterstützt die Übertragung die Aktivierung, und Sie verfügt über eine entsprechende *fusedactivation* in der Operator Beschreibung (siehe [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="5c680-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

<span data-ttu-id="5c680-119">Um eine Aktivierung zu verleihen, erstellen Sie eine [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) , die den Typ der zu verschmelfenden Aktivierung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5c680-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="5c680-120">Um z. b. eine relu-Funktion zu vereinen, wäre der richtige Operatortyp [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="5c680-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="5c680-121">Beim Erstellen der Operator Beschreibung für die Aktivierungsfunktion müssen die Parameter *inputtensor* und *outputtensor* für die Aktivierungsfunktion auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5c680-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="5c680-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5c680-122">Example</span></span>

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

<span data-ttu-id="5c680-123">Ein umfassendes Beispiel verwendet das [directmlsuperresolution](https://github.com/microsoft/DirectML/tree/master/Samples) -Beispiel, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="5c680-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="5c680-124">Operatoren, die die Aktivierung von Fused</span><span class="sxs-lookup"><span data-stu-id="5c680-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="5c680-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="5c680-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="5c680-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="5c680-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="5c680-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="5c680-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="5c680-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** und **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="5c680-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="5c680-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="5c680-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="5c680-130">Aktivierungen, die für Fusion unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="5c680-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="5c680-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="5c680-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="5c680-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="5c680-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="5c680-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="5c680-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="5c680-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="5c680-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="5c680-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="5c680-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="5c680-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="5c680-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="5c680-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="5c680-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="5c680-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="5c680-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="5c680-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="5c680-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="5c680-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="5c680-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="5c680-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="5c680-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="5c680-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="5c680-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="5c680-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="5c680-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="5c680-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="5c680-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="5c680-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="5c680-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="5c680-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="5c680-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="5c680-147">Alle Operatoren, die nicht in dieser Liste enthalten sind, werden nicht für die Aktivierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5c680-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c680-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c680-148">See also</span></span>

<span data-ttu-id="5c680-149">[Beispiel für directmlsuperresolution](https://github.com/microsoft/DirectML/tree/master/Samples)  </span><span class="sxs-lookup"><span data-stu-id="5c680-149">[DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples)  </span></span>  
[<span data-ttu-id="5c680-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="5c680-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
