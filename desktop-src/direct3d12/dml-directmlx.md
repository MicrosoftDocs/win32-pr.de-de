---
title: DirectMLX
description: DirectMLX ist eine C++-Hilfsbibliothek für Header für DirectML, die das Zusammenstellen einzelner Operatoren in Diagrammen vereinfacht.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: ba7eca27a39b690f678bdac1ea0feba1991e8b40
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521187"
---
# <a name="directmlx"></a><span data-ttu-id="7f00e-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="7f00e-103">DirectMLX</span></span>

<span data-ttu-id="7f00e-104">DirectMLX ist eine C++-Hilfsbibliothek für Header für DirectML, die das Zusammenstellen einzelner Operatoren in Diagrammen vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="7f00e-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="7f00e-105">DirectMLX bietet praktische Wrapper für alle DirectML-Operatortypen (DML) sowie intuitive Operatorüberladungen, wodurch es einfacher wird, DML-Operatoren zu instanziieren und in komplexe Diagramme zu verketten.</span><span class="sxs-lookup"><span data-stu-id="7f00e-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="7f00e-106">Wo sie zu finden sind `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="7f00e-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="7f00e-107">`DirectMLX.h` wird als Open-Source-Software unter der MIT-Lizenz verteilt.</span><span class="sxs-lookup"><span data-stu-id="7f00e-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="7f00e-108">Die neueste Version finden Sie auf [DirectML GitHub.](https://github.com/microsoft/DirectML/tree/master/Libraries)</span><span class="sxs-lookup"><span data-stu-id="7f00e-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7f00e-109">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7f00e-109">Tensor constraints</span></span>

<span data-ttu-id="7f00e-110">DirectMLX erfordert DirectML Version 1.4.0 oder eine neuere Version (siehe [DirectML-Versionsverlauf).](dml-version-history.md#version-table)</span><span class="sxs-lookup"><span data-stu-id="7f00e-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="7f00e-111">Ältere Versionen von DirectML werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f00e-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="7f00e-112">DirectMLX.h erfordert einen C++11-fähigen Compiler, einschließlich (aber nicht beschränkt auf):</span><span class="sxs-lookup"><span data-stu-id="7f00e-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="7f00e-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="7f00e-113">Visual Studio 2017</span></span>
* <span data-ttu-id="7f00e-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="7f00e-114">Visual Studio 2019</span></span>
* <span data-ttu-id="7f00e-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="7f00e-115">Clang 10</span></span>

<span data-ttu-id="7f00e-116">Beachten Sie, dass ein C++17-Compiler (oder neuer) die option ist, die wir empfehlen.</span><span class="sxs-lookup"><span data-stu-id="7f00e-116">Note that a C++17 (or newer) compiler is the option that we recommend.</span></span> <span data-ttu-id="7f00e-117">Das Kompilieren für C++11 ist möglich, erfordert jedoch die Verwendung von Bibliotheken von Drittanbietern (z. B. [GSL](https://github.com/microsoft/GSL) und [Abzwing),](https://github.com/abseil/abseil-cpp)um fehlende Standardbibliotheksfunktionen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7f00e-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="7f00e-118">Wenn Sie über eine Konfiguration verfügen, die nicht kompiliert werden kann, melden Sie `DirectMLX.h` [auf GitHub ein Problem.](https://github.com/microsoft/DirectML/issues)</span><span class="sxs-lookup"><span data-stu-id="7f00e-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="7f00e-119">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="7f00e-119">Basic usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="7f00e-120">Hier ist ein weiteres Beispiel, das einen DirectML-Graphen erstellt, der die [quadratische Formel berechnen kann.](https://en.wikipedia.org/wiki/Quadratic_formula)</span><span class="sxs-lookup"><span data-stu-id="7f00e-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="7f00e-121">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f00e-121">More examples</span></span>

<span data-ttu-id="7f00e-122">Vollständige Beispiele mit DirectMLX finden Sie im [DirectML-GitHub-Repository.](https://github.com/microsoft/DirectML/tree/master/Samples)</span><span class="sxs-lookup"><span data-stu-id="7f00e-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="7f00e-123">Kompilierzeitoptionen</span><span class="sxs-lookup"><span data-stu-id="7f00e-123">Compile-time options</span></span>

<span data-ttu-id="7f00e-124">DirectMLX unterstützt kompilierzeitbasierte #define, um verschiedene Teile des Headers anzupassen.</span><span class="sxs-lookup"><span data-stu-id="7f00e-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="7f00e-125">Option</span><span class="sxs-lookup"><span data-stu-id="7f00e-125">Option</span></span>|<span data-ttu-id="7f00e-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f00e-126">Description</span></span>|
|-|-|
|<span data-ttu-id="7f00e-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="7f00e-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="7f00e-128">Wenn #define, führt dies dazu, dass Fehler zu einem Aufruf von `std::abort` führen, anstatt eine Ausnahme zu auslösen.</span><span class="sxs-lookup"><span data-stu-id="7f00e-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="7f00e-129">Dies wird standardmäßig definiert, wenn Ausnahmen nicht verfügbar sind (z. B. wenn Ausnahmen in den Compileroptionen deaktiviert wurden).</span><span class="sxs-lookup"><span data-stu-id="7f00e-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="7f00e-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="7f00e-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="7f00e-131">Wenn #define, werden Ausnahmen mit ausnahmetypen der [Windows-Implementierungsbibliothek](https://github.com/microsoft/wil) ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7f00e-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="7f00e-132">Andernfalls werden stattdessen `std::runtime_error` Standardausnahmetypen (z. B. ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f00e-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="7f00e-133">Diese Option hat keine Auswirkungen, wenn **DMLX_NO_EXCEPTIONS** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7f00e-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="7f00e-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="7f00e-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="7f00e-135">Wenn #define ist, verwendet [Absturz](https://github.com/abseil/abseil-cpp) als Drop-In-Ersatz für Standardbibliothekstypen, die in C++11 nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f00e-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="7f00e-136">Zu diesen Typen `absl::optional` gehören (statt `std::optional` ), `absl::Span` (statt ) und `std::span` `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="7f00e-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="7f00e-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="7f00e-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="7f00e-138">Steuert, ob [GSL als](https://github.com/microsoft/GSL) Ersatz für verwendet werden `std::span` soll.</span><span class="sxs-lookup"><span data-stu-id="7f00e-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="7f00e-139">Wenn #define, werden Verwendungen von durch für Compiler `std::span` `gsl::span` ohne native `std::span` Implementierungen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7f00e-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="7f00e-140">Andernfalls wird stattdessen eine Inline-Drop-In-Implementierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7f00e-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="7f00e-141">Beachten Sie, dass diese Option nur beim Kompilieren in einem Vor-C++20-Compiler ohne Unterstützung für verwendet wird und keine andere Ersatzlösung der Standardbibliothek (z. B. `std::span` Abkron) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f00e-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="7f00e-142">Steuern des Tensorlayouts</span><span class="sxs-lookup"><span data-stu-id="7f00e-142">Controlling tensor layout</span></span>

<span data-ttu-id="7f00e-143">Für die meisten Operatoren berechnet DirectMLX die Eigenschaften der Ausgabetensoren des Operators in Ihrem Namen.</span><span class="sxs-lookup"><span data-stu-id="7f00e-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="7f00e-144">Wenn Sie z. B. eine achsenübergreifend mit einem Eingabetensor von Größen ausführen, berechnet DirectMLX automatisch die Eigenschaften des Ausgabetensors einschließlich der richtigen `dml::Reduce` `{ 0, 2, 3 }` Form von `{ 3, 4, 5, 6 }` `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="7f00e-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="7f00e-145">Die anderen Eigenschaften eines Ausgabetensors umfassen jedoch *strides*, *TotalTensorSizeInBytes* und *GuaranteedBaseOffsetAlignment*.</span><span class="sxs-lookup"><span data-stu-id="7f00e-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="7f00e-146">Standardmäßig legt DirectMLX diese Eigenschaften so fest, dass der Tensor keine striding-Eigenschaft, keine garantierte Ausrichtung des Basisoffsets und eine Gesamtgröße des Tensors in Bytes aufweist, wie von [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize)berechnet.</span><span class="sxs-lookup"><span data-stu-id="7f00e-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="7f00e-147">DirectMLX unterstützt die Möglichkeit, diese Ausgabetensoreigenschaften mithilfe von Objekten anzupassen, die als *Tensorrichtlinien bezeichnet werden.*</span><span class="sxs-lookup"><span data-stu-id="7f00e-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="7f00e-148">**Ein TensorPolicy-Objekt** ist ein anpassbarer Rückruf, der von DirectMLX aufgerufen wird und Ausgabetensoreigenschaften zurückgibt, wenn der berechnete Datentyp, die Flags und die Größen eines Tensors angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f00e-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="7f00e-149">Tensor-Richtlinien können für das **dml::Graph-Objekt festgelegt** werden und werden für alle nachfolgenden Operatoren in diesem Diagramm verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f00e-149">Tensor policies can be set on the **dml::Graph** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="7f00e-150">Tensor-Richtlinien können auch direkt festgelegt werden, wenn ein **TensorDesc erstellt wird.**</span><span class="sxs-lookup"><span data-stu-id="7f00e-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="7f00e-151">Das Layout der von DirectMLX erzeugten Tensoren kann daher durch Festlegen einer **TensorPolicy** gesteuert werden, die die entsprechenden Schritte auf ihren Tensoren legt.</span><span class="sxs-lookup"><span data-stu-id="7f00e-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="7f00e-152">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f00e-152">Example 1</span></span>

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="7f00e-153">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f00e-153">Example 2</span></span>

<span data-ttu-id="7f00e-154">DirectMLX bietet auch einige integrierte alternative Tensorrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="7f00e-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="7f00e-155">Die **InterleavedChannel-Richtlinie** wird beispielsweise zur Vereinfachung bereitgestellt und kann verwendet werden, um Tensoren mit Strides so zu erzeugen, dass sie in NHWC-Reihenfolge geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7f00e-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="7f00e-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f00e-156">See also</span></span>

* [<span data-ttu-id="7f00e-157">DirectML GitHub</span><span class="sxs-lookup"><span data-stu-id="7f00e-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="7f00e-158">DirectMLX yolov4-Beispiel</span><span class="sxs-lookup"><span data-stu-id="7f00e-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="7f00e-159">Verwenden von Strides zum Ausdrücken von Auf padding und Speicherlayout</span><span class="sxs-lookup"><span data-stu-id="7f00e-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="7f00e-160">DML_GRAPH_DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="7f00e-160">DML_GRAPH_DESC structure</span></span>](/windows/win32/api/directml/ns-directml-dml_graph_desc)