---
title: Verwendung von Fused-Operatoren zur Leistungssteigerung
description: Einige DirectML-Operatoren unterstützen ein Konzept, das als *Fusion bezeichnet wird.* Operator fusion ist eine Möglichkeit, die Leistung zu verbessern, indem ein Operator (in der Regel eine Aktivierungsfunktion) mit einem anderen Operator zusammengeführt wird, sodass sie zusammen ausgeführt werden, ohne dass ein Roundtrip zum Arbeitsspeicher erforderlich ist.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: bba4a9d0ef5c69976a5a344432bf82d31b00c0c7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803984"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="dde05-104">Verwendung von Fused-Operatoren zur Leistungssteigerung</span><span class="sxs-lookup"><span data-stu-id="dde05-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="dde05-105">Einige DirectML-Operatoren unterstützen ein Konzept, das als *Fusion bezeichnet wird.*</span><span class="sxs-lookup"><span data-stu-id="dde05-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="dde05-106">Operator fusion ist eine Möglichkeit, die Leistung zu verbessern, indem ein Operator (in der Regel eine Aktivierungsfunktion) mit einem anderen Operator zusammengeführt wird, sodass sie zusammen ausgeführt werden, ohne dass ein Roundtrip zum Arbeitsspeicher erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dde05-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="dde05-107">Wann werden Aktivierungen aktiviert?</span><span class="sxs-lookup"><span data-stu-id="dde05-107">When to fuse activations</span></span>

<span data-ttu-id="dde05-108">Fused-Aktivierungen sind eine Leistungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="dde05-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="dde05-109">Ein sehr häufiges Szenario in vielen Machine Learning-Modellen (ML) besteht in der Anwendung einer Nichtlinearität (einer Aktivierungsfunktion) auf die Ausgabe jeder Ebene im Modell.</span><span class="sxs-lookup"><span data-stu-id="dde05-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="dde05-110">Normalerweise erfordert dies einen Roundtrip zum Grafikspeicher.</span><span class="sxs-lookup"><span data-stu-id="dde05-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="dde05-111">Wenn beispielsweise auf eine Konvolution eine nicht fused Relu-Aktivierung folgt, muss die GPU warten, bis die Ergebnisse der Convolution in den GPU-Arbeitsspeicher geschrieben werden, bevor sie mit der Berechnung der Relu-Aktivierungsebene beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="dde05-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="dde05-112">Da die Computeworkload der meisten Aktivierungsfunktionen tendenziell klein ist, kann dieser Roundtrip zum Grafikspeicher ein großer Leistungsengpass sein.</span><span class="sxs-lookup"><span data-stu-id="dde05-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="dde05-113">Operator fusion ermöglicht die Aktivierungsfunktion (im obigen Beispiel Relu) als Teil des vorherigen Operators (z. B. Convolution).</span><span class="sxs-lookup"><span data-stu-id="dde05-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="dde05-114">Dadurch kann die GPU die Aktivierungsfunktion berechnen, ohne darauf zu warten, dass die Ergebnisse des vorherigen Operators in den Arbeitsspeicher geschrieben werden, was &mdash; die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="dde05-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="dde05-115">Da fused-Aktivierungen das gleiche Ergebnis erzeugen, aber in vielen Fällen schneller sind, empfehlen wir Ihnen, Aktivierungsebenen zu beseitigen, indem Sie sie nach Möglichkeit in ihren vorherigen Operator einfingen.</span><span class="sxs-lookup"><span data-stu-id="dde05-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="dde05-116">How to fuse activations (Zusammensnieren von Aktivierungen)</span><span class="sxs-lookup"><span data-stu-id="dde05-116">How to fuse activations</span></span>

<span data-ttu-id="dde05-117">Operatoren, die fused-Aktivierungen unterstützen, verfügen über einen zusätzlichen optionalen Parameter in ihrer Operatorstruktur, `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="dde05-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="dde05-118">Convolution unterstützt z.B. die Fused-Aktivierung und verfügt über eine entsprechende *FusedActivation* in der Operatorbeschreibung (siehe [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="dde05-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

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

<span data-ttu-id="dde05-119">Erstellen Sie zum Fuseieren einer Aktivierung eine [DML_OPERATOR_DESC,](/windows/win32/api/directml/ns-directml-dml_operator_desc) die den Typ der Zusicherung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dde05-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="dde05-120">Um z. B. eine Relu-Funktion zu fusionieren, wäre der richtige Operatortyp [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="dde05-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="dde05-121">Beim Erstellen der Operatorbeschreibung für die Aktivierungsfunktion müssen Sie die *Parameter InputTensor* und *OutputTensor* für die Aktivierungsfunktion auf **NULL** festlegen.</span><span class="sxs-lookup"><span data-stu-id="dde05-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="dde05-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dde05-122">Example</span></span>

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

<span data-ttu-id="dde05-123">Für ein vollständiges Beispiel verwendet das [DirectMLSuperResolution-Beispiel](https://github.com/microsoft/DirectML/tree/master/Samples) fused-Aktivierungen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="dde05-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="dde05-124">Operatoren, die die fused-Aktivierung unterstützen</span><span class="sxs-lookup"><span data-stu-id="dde05-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="dde05-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="dde05-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="dde05-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="dde05-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="dde05-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="dde05-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="dde05-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** und **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="dde05-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="dde05-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="dde05-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="dde05-130">Aktivierungen, die für Fusion unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="dde05-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="dde05-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="dde05-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="dde05-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="dde05-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="dde05-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="dde05-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="dde05-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="dde05-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="dde05-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="dde05-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="dde05-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="dde05-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="dde05-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="dde05-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="dde05-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="dde05-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="dde05-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="dde05-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="dde05-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="dde05-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="dde05-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="dde05-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="dde05-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="dde05-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="dde05-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="dde05-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="dde05-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="dde05-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="dde05-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="dde05-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="dde05-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="dde05-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="dde05-147">Operatoren, die nicht in dieser Liste enthalten sind, werden für die Fused-Aktivierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dde05-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="dde05-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dde05-148">See also</span></span>

* [<span data-ttu-id="dde05-149">DirectMLSuperResolution-Beispiel</span><span class="sxs-lookup"><span data-stu-id="dde05-149">DirectMLSuperResolution sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [<span data-ttu-id="dde05-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="dde05-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
