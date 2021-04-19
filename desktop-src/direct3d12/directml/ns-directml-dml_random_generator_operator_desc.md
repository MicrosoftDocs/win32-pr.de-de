---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Füllt einen Ausgabe Mandanten mit deterministisch generierten, pseudo zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generator Status ausgeben, der während der nachfolgenden Ausführungen des Operators verwendet werden kann.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106353243"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="7611e-104">DML_RANDOM_GENERATOR_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="7611e-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="7611e-105">Füllt einen Ausgabe Mandanten mit deterministisch generierten, pseudo zufälligen, gleichmäßig verteilten Bits.</span><span class="sxs-lookup"><span data-stu-id="7611e-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="7611e-106">Dieser Operator kann optional auch einen aktualisierten internen Generator Status ausgeben, der während der nachfolgenden Ausführungen des Operators verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7611e-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="7611e-107">Dieser Operator ist deterministisch und verhält sich so, als ob es sich um eine reine Funktion &mdash; handelt, deren Ausführung keine Nebeneffekte erzeugt und keinen globalen Zustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="7611e-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="7611e-108">Die von diesem Operator erzeugte pseudo zufällige Ausgabe ist ausschließlich von den Werten abhängig, die in *inputstatetensor* bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7611e-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="7611e-109">Die von diesem Operator implementierten Generatoren sind nicht kryptografisch sicher. Daher sollte dieser Operator nicht für die Verschlüsselung, die Schlüsselgenerierung oder andere Anwendungen verwendet werden, die eine kryptografisch sichere Zufallszahlengenerierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="7611e-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7611e-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="7611e-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="7611e-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7611e-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7611e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="7611e-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="7611e-113">Member</span><span class="sxs-lookup"><span data-stu-id="7611e-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="7611e-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7611e-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7611e-115">Ein eingabetensor, der den internen Generator Zustand enthält.</span><span class="sxs-lookup"><span data-stu-id="7611e-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="7611e-116">Die Größe und das Format dieses Eingabe Mandanten hängt von der [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)ab.</span><span class="sxs-lookup"><span data-stu-id="7611e-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="7611e-117">Bei **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** muss dieser tensorflow den Typ **UInt32** aufweisen und Übergrößen verfügen `{1,1,1,6}` .</span><span class="sxs-lookup"><span data-stu-id="7611e-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="7611e-118">Die ersten 4 32-Bit-Werte enthalten einen monoton steigenden 128-Bit-Zählers.</span><span class="sxs-lookup"><span data-stu-id="7611e-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="7611e-119">Die letzten 2 32-Bit-Werte enthalten den 64-Bit-Schlüsselwert für den Generator.</span><span class="sxs-lookup"><span data-stu-id="7611e-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="7611e-120">Wenn Sie den Eingabe Zustand des Generators zum ersten Mal initialisieren, sollte der 128-bit-Counter (die ersten 4 32-Bit-UInt32-Werte) in der Regel mit 0 initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7611e-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="7611e-121">Der Schlüssel kann willkürlich ausgewählt werden. unterschiedliche Schlüsselwerte führen zu unterschiedlichen Zahlen Sequenzen.</span><span class="sxs-lookup"><span data-stu-id="7611e-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="7611e-122">Der Wert für den Schlüssel wird normalerweise mit einem vom *Benutzer bereitgestellten* Startwert generiert.</span><span class="sxs-lookup"><span data-stu-id="7611e-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="7611e-123">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7611e-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7611e-124">Ein Ausgabe-tensorflow, der die resultierenden Pseudo Zufallswerte enthält.</span><span class="sxs-lookup"><span data-stu-id="7611e-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="7611e-125">Dieser Mandanten kann eine beliebige Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7611e-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="7611e-126">Type: \_ maybenull \_ **Konstanten [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7611e-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7611e-127">Ein optionaler Ausgabe Mandanten, der den aktualisierten internen Generator Zustand enthält.</span><span class="sxs-lookup"><span data-stu-id="7611e-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="7611e-128">Wenn angegeben, verwendet dieser Operator den *inputstatetensor* , um einen geeigneten aktualisierten Generator Zustand zu berechnen, und schreibt das Ergebnis in den *outputstatetensor*.</span><span class="sxs-lookup"><span data-stu-id="7611e-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="7611e-129">In der Regel wird dieses Ergebnis von Aufrufern gespeichert und als Eingabe Zustand bei einer nachfolgenden Ausführung dieses Operators bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7611e-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="7611e-130">Typ: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="7611e-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="7611e-131">Einer der Werte aus der [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) Enumeration, die den Typ des zu verwendenden Generators angibt.</span><span class="sxs-lookup"><span data-stu-id="7611e-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="7611e-132">Zurzeit ist der einzige gültige Wert **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, der nach dem " [philox 4x32-10"-Algorithmus](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)Pseudozufallszahlen generiert.</span><span class="sxs-lookup"><span data-stu-id="7611e-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="7611e-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7611e-133">Remarks</span></span>
<span data-ttu-id="7611e-134">Bei jeder Ausführung dieses Operators sollte der 128-Bit-Wert inkrementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7611e-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="7611e-135">Wenn *outputstatetensor* bereitgestellt wird, erhöht dieser Operator den Wert des Zählers mit dem korrekten Wert in Ihrem Namen und schreibt das Ergebnis in den *outputstatetensor*.</span><span class="sxs-lookup"><span data-stu-id="7611e-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="7611e-136">Der Betrag, um den der Wert erhöht werden soll, hängt von der Anzahl der generierten 32-Bit-Ausgabe Elemente und vom Typ des Generators ab.</span><span class="sxs-lookup"><span data-stu-id="7611e-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="7611e-137">Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** sollte der 128-Bit-Wert bei jeder Ausführung um inkrementiert werden `ceil(outputSize / 4)` , wobei `outputSize` die Anzahl der Elemente in *outputtensor* ist.</span><span class="sxs-lookup"><span data-stu-id="7611e-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="7611e-138">Sehen Sie sich ein Beispiel an, in dem der Wert des 128-Bit-Leistungs Zählers aktuell ist `0x48656c6c'6f46726f'6d536561'74746c65` , und die Größe von outputtensor ist `{3,3,20,7219}` .</span><span class="sxs-lookup"><span data-stu-id="7611e-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="7611e-139">Nach dem einmaligen ausführen dieses Operators sollte der Leistungswert um 324.855 erhöht werden (die Anzahl der Ausgabe Elemente, dividiert durch 4, aufgerundet). Dies führt zu einem Leistungs Zählers `0x48656c6c'6f46726f'6d536561'746f776e` .</span><span class="sxs-lookup"><span data-stu-id="7611e-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="7611e-140">Dieser aktualisierte Wert sollte dann als Eingabe für die nächste Ausführung dieses Operators angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7611e-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="7611e-141">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="7611e-141">Availability</span></span>
<span data-ttu-id="7611e-142">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="7611e-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7611e-143">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7611e-143">Tensor constraints</span></span>
<span data-ttu-id="7611e-144">`InputStateTensor` und `OutputStateTensor` müssen über die gleichen *Größen* verfügen.</span><span class="sxs-lookup"><span data-stu-id="7611e-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="7611e-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7611e-145">Tensor support</span></span>
| <span data-ttu-id="7611e-146">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="7611e-146">Tensor</span></span> | <span data-ttu-id="7611e-147">Typ</span><span class="sxs-lookup"><span data-stu-id="7611e-147">Kind</span></span> | <span data-ttu-id="7611e-148">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="7611e-148">Dimensions</span></span> | <span data-ttu-id="7611e-149">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="7611e-149">Supported dimension counts</span></span> | <span data-ttu-id="7611e-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="7611e-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="7611e-151">Inputstatetensor</span><span class="sxs-lookup"><span data-stu-id="7611e-151">InputStateTensor</span></span> | <span data-ttu-id="7611e-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7611e-152">Input</span></span> | <span data-ttu-id="7611e-153">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="7611e-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="7611e-154">4</span><span class="sxs-lookup"><span data-stu-id="7611e-154">4</span></span> | <span data-ttu-id="7611e-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="7611e-155">UINT32</span></span> |
| <span data-ttu-id="7611e-156">Outputtensor</span><span class="sxs-lookup"><span data-stu-id="7611e-156">OutputTensor</span></span> | <span data-ttu-id="7611e-157">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7611e-157">Output</span></span> | <span data-ttu-id="7611e-158">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="7611e-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="7611e-159">4</span><span class="sxs-lookup"><span data-stu-id="7611e-159">4</span></span> | <span data-ttu-id="7611e-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="7611e-160">UINT32</span></span> |
| <span data-ttu-id="7611e-161">Outputstatetensor</span><span class="sxs-lookup"><span data-stu-id="7611e-161">OutputStateTensor</span></span> | <span data-ttu-id="7611e-162">Optionale Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7611e-162">Optional output</span></span> | <span data-ttu-id="7611e-163">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="7611e-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="7611e-164">4</span><span class="sxs-lookup"><span data-stu-id="7611e-164">4</span></span> | <span data-ttu-id="7611e-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="7611e-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="7611e-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7611e-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7611e-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="7611e-167">**Header**</span></span> | <span data-ttu-id="7611e-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="7611e-168">directml.h</span></span> |