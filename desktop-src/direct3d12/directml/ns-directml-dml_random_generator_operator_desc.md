---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Füllt einen Ausgabe-Tensor mit deterministisch generierten, pseudo-zufälligen, gleichmäßig verteilten Bits. Dieser Operator kann optional auch einen aktualisierten internen Generatorzustand ausgeben, der bei nachfolgenden Ausführungen des Operators verwendet werden kann.
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
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804066"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="100dd-104">DML_RANDOM_GENERATOR_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="100dd-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="100dd-105">Füllt einen Ausgabe-Tensor mit deterministisch generierten, pseudo-zufälligen, gleichmäßig verteilten Bits.</span><span class="sxs-lookup"><span data-stu-id="100dd-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="100dd-106">Dieser Operator kann optional auch einen aktualisierten internen Generatorzustand ausgeben, der bei nachfolgenden Ausführungen des Operators verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="100dd-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="100dd-107">Dieser Operator ist deterministisch und verhält sich so, als wäre er eine reine &mdash; Funktion, d. h., seine Ausführung erzeugt keine Nebeneffekte und verwendet keinen globalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="100dd-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="100dd-108">Die von diesem Operator erzeugte Pseudozufallsausgabe hängt ausschließlich von den Werten ab, die im *InputStateTensor* bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="100dd-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="100dd-109">Die von diesem Operator implementierten Generatoren sind nicht kryptografisch sicher. daher sollte dieser Operator nicht für Verschlüsselung, Schlüsselgenerierung oder andere Anwendungen verwendet werden, die eine kryptografisch sichere Zufallszahlengenerierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="100dd-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="100dd-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="100dd-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="100dd-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="100dd-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="100dd-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="100dd-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="100dd-113">Member</span><span class="sxs-lookup"><span data-stu-id="100dd-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="100dd-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="100dd-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="100dd-115">Ein Eingabe-Tensor, der den internen Generatorzustand enthält.</span><span class="sxs-lookup"><span data-stu-id="100dd-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="100dd-116">Die Größe und das Format dieses Eingabe-Tensors hängen vom [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)ab.</span><span class="sxs-lookup"><span data-stu-id="100dd-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="100dd-117">Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** muss dieser Tensor vom Typ **UINT32** sein und die Größe `{1,1,1,6}` aufweisen.</span><span class="sxs-lookup"><span data-stu-id="100dd-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="100dd-118">Die ersten vier 32-Bit-Werte enthalten einen monoton ansteigenden 128-Bit-Indikator.</span><span class="sxs-lookup"><span data-stu-id="100dd-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="100dd-119">Die letzten beiden 32-Bit-Werte enthalten den 64-Bit-Schlüsselwert für den Generator.</span><span class="sxs-lookup"><span data-stu-id="100dd-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="100dd-120">Beim erstmaligen Initialisieren des Eingabezustands des Generators sollte in der Regel der 128-Bit-Zähler (die ersten vier UINT32-Werte mit 32 Bit) mit 0 initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="100dd-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="100dd-121">Der Schlüssel kann beliebig ausgewählt werden. unterschiedliche Schlüsselwerte erzeugen unterschiedliche Sequenzen von Zahlen.</span><span class="sxs-lookup"><span data-stu-id="100dd-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="100dd-122">Der Wert für den Schlüssel wird in der Regel mithilfe eines vom Benutzer bereitgestellten *Startwerts generiert.*</span><span class="sxs-lookup"><span data-stu-id="100dd-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="100dd-123">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="100dd-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="100dd-124">Ein Ausgabe tensor, der die resultierenden Pseudozufallswerte enthält.</span><span class="sxs-lookup"><span data-stu-id="100dd-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="100dd-125">Dieser Tensor kann eine beliebige Größe haben.</span><span class="sxs-lookup"><span data-stu-id="100dd-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="100dd-126">Typ: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="100dd-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="100dd-127">Ein optionaler Ausgabe tensor, der den aktualisierten internen Generatorzustand enthält.</span><span class="sxs-lookup"><span data-stu-id="100dd-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="100dd-128">Wenn angegeben, verwendet dieser Operator den *InputStateTensor,* um einen entsprechenden aktualisierten Generatorzustand zu berechnen, und schreibt das Ergebnis in *den OutputStateTensor.*</span><span class="sxs-lookup"><span data-stu-id="100dd-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="100dd-129">In der Regel speichern Aufrufer dieses Ergebnis und geben es als Eingabezustand bei einer nachfolgenden Ausführung dieses Operators an.</span><span class="sxs-lookup"><span data-stu-id="100dd-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="100dd-130">Typ: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="100dd-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="100dd-131">Einer der Werte [](./ne-directml-dml_random_generator_type.md) aus der DML_RANDOM_GENERATOR_TYPE-Enum, der den Typ des zu verwendenden Generators angibt.</span><span class="sxs-lookup"><span data-stu-id="100dd-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="100dd-132">Derzeit ist der einzige gültige Wert **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, der pseudozufälligkeitsbasierte Zahlen gemäß dem [Algorithmus Desox 4x32-10 generiert.](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)</span><span class="sxs-lookup"><span data-stu-id="100dd-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="100dd-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="100dd-133">Remarks</span></span>
<span data-ttu-id="100dd-134">Bei jeder Ausführung dieses Operators sollte der 128-Bit-Zähler erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="100dd-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="100dd-135">Wenn *outputStateTensor* angegeben wird, erhöht dieser Operator den Zähler mit dem richtigen Wert in Ihrem Namen und schreibt das Ergebnis in *den OutputStateTensor.*</span><span class="sxs-lookup"><span data-stu-id="100dd-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="100dd-136">Der Betrag, um den sie erhöht werden soll, hängt von der Anzahl der generierten 32-Bit-Ausgabeelemente und dem Typ des Generators ab.</span><span class="sxs-lookup"><span data-stu-id="100dd-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="100dd-137">Für **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** sollte der 128-Bit-Leistungsindikator bei jeder Ausführung um erhöht werden, wobei die Anzahl der Elemente `ceil(outputSize / 4)` im `outputSize` *OutputTensor ist.*</span><span class="sxs-lookup"><span data-stu-id="100dd-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="100dd-138">Stellen Sie sich ein Beispiel vor, bei dem der Wert des 128-Bit-Leistungsindikators derzeit ist und die Größe des `0x48656c6c'6f46726f'6d536561'74746c65` OutputTensors `{3,3,20,7219}` ist.</span><span class="sxs-lookup"><span data-stu-id="100dd-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="100dd-139">Nachdem dieser Operator einmal ausgeführt wurde, sollte der Zähler um 324.855 erhöht werden (die Anzahl der generierten Ausgabeelemente dividiert durch 4, aufgerundet), was zu einem Zählerwert von `0x48656c6c'6f46726f'6d536561'746f776e` führt.</span><span class="sxs-lookup"><span data-stu-id="100dd-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="100dd-140">Dieser aktualisierte Wert sollte dann als Eingabe für die nächste Ausführung dieses Operators angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="100dd-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="100dd-141">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="100dd-141">Availability</span></span>
<span data-ttu-id="100dd-142">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="100dd-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="100dd-143">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="100dd-143">Tensor constraints</span></span>
<span data-ttu-id="100dd-144">`InputStateTensor`und `OutputStateTensor` müssen die gleichen Größen *aufweisen.*</span><span class="sxs-lookup"><span data-stu-id="100dd-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="100dd-145">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="100dd-145">Tensor support</span></span>
| <span data-ttu-id="100dd-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="100dd-146">Tensor</span></span> | <span data-ttu-id="100dd-147">Typ</span><span class="sxs-lookup"><span data-stu-id="100dd-147">Kind</span></span> | <span data-ttu-id="100dd-148">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="100dd-148">Dimensions</span></span> | <span data-ttu-id="100dd-149">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="100dd-149">Supported dimension counts</span></span> | <span data-ttu-id="100dd-150">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="100dd-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="100dd-151">InputStateTensor</span><span class="sxs-lookup"><span data-stu-id="100dd-151">InputStateTensor</span></span> | <span data-ttu-id="100dd-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="100dd-152">Input</span></span> | <span data-ttu-id="100dd-153">{ 1, 1, 1, 6 }</span><span class="sxs-lookup"><span data-stu-id="100dd-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="100dd-154">4</span><span class="sxs-lookup"><span data-stu-id="100dd-154">4</span></span> | <span data-ttu-id="100dd-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="100dd-155">UINT32</span></span> |
| <span data-ttu-id="100dd-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="100dd-156">OutputTensor</span></span> | <span data-ttu-id="100dd-157">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="100dd-157">Output</span></span> | <span data-ttu-id="100dd-158">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="100dd-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="100dd-159">4</span><span class="sxs-lookup"><span data-stu-id="100dd-159">4</span></span> | <span data-ttu-id="100dd-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="100dd-160">UINT32</span></span> |
| <span data-ttu-id="100dd-161">OutputStateTensor</span><span class="sxs-lookup"><span data-stu-id="100dd-161">OutputStateTensor</span></span> | <span data-ttu-id="100dd-162">Optionale Ausgabe</span><span class="sxs-lookup"><span data-stu-id="100dd-162">Optional output</span></span> | <span data-ttu-id="100dd-163">{ 1, 1, 1, 6 }</span><span class="sxs-lookup"><span data-stu-id="100dd-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="100dd-164">4</span><span class="sxs-lookup"><span data-stu-id="100dd-164">4</span></span> | <span data-ttu-id="100dd-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="100dd-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="100dd-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="100dd-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="100dd-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="100dd-167">**Header**</span></span> | <span data-ttu-id="100dd-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="100dd-168">directml.h</span></span> |