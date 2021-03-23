---
title: Directmlx
description: Directmlx ist eine Hilfsbibliothek für C++-Header für directml, die das Verfassen einzelner Operatoren in Graphen erleichtern soll.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 8388edd51b6ad3ca30fe1c65947167cee7dac5e6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548767"
---
# <a name="directmlx"></a><span data-ttu-id="d344c-103">Directmlx</span><span class="sxs-lookup"><span data-stu-id="d344c-103">DirectMLX</span></span>

<span data-ttu-id="d344c-104">Directmlx ist eine Hilfsbibliothek für C++-Header für directml, die das Verfassen einzelner Operatoren in Graphen erleichtern soll.</span><span class="sxs-lookup"><span data-stu-id="d344c-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="d344c-105">Directmlx bietet bequeme Wrapper für alle directml (DML)-Operator Typen sowie intuitive Operator Überladungen, die die Instanziieren von DML-Operatoren vereinfachen und Sie in komplexe Diagramme verketten.</span><span class="sxs-lookup"><span data-stu-id="d344c-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="d344c-106">Speicherort `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="d344c-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="d344c-107">`DirectMLX.h` wird als Open-Source-Software unter der mit-Lizenz verteilt.</span><span class="sxs-lookup"><span data-stu-id="d344c-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="d344c-108">Die neueste Version finden Sie auf der [directml-GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)-Version.</span><span class="sxs-lookup"><span data-stu-id="d344c-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d344c-109">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d344c-109">Tensor constraints</span></span>

<span data-ttu-id="d344c-110">Directmlx erfordert directml-Version 1.4.0 oder höher (siehe [directml-Versionsverlauf](dml-version-history.md#version-table)).</span><span class="sxs-lookup"><span data-stu-id="d344c-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="d344c-111">Ältere Versionen von directml werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d344c-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="d344c-112">Directmlx. h erfordert einen C + +11-fähigen Compiler, einschließlich (aber nicht beschränkt auf):</span><span class="sxs-lookup"><span data-stu-id="d344c-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="d344c-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="d344c-113">Visual Studio 2017</span></span>
* <span data-ttu-id="d344c-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="d344c-114">Visual Studio 2019</span></span>
* <span data-ttu-id="d344c-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="d344c-115">Clang 10</span></span>

<span data-ttu-id="d344c-116">Beachten Sie, dass es sich bei einem c++ 17 (oder neueren) Compiler um Optionen handelt, die wir empfehlen.</span><span class="sxs-lookup"><span data-stu-id="d344c-116">Note that a C++17 (or newer) compiler is options that we recommend.</span></span> <span data-ttu-id="d344c-117">Die Kompilierung für c++ 11 ist möglich, erfordert jedoch die Verwendung von Drittanbieterbibliotheken (z. b. [gsl](https://github.com/microsoft/GSL) und [Abseil](https://github.com/abseil/abseil-cpp)), um fehlende Standard Bibliotheksfunktionen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d344c-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="d344c-118">Wenn Sie über eine Konfiguration verfügen, die nicht kompiliert `DirectMLX.h` werden kann, melden Sie [ein Problem auf unserem GitHub](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="d344c-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="d344c-119">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="d344c-119">Basic Usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Scope scope(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="d344c-120">Im folgenden finden Sie ein weiteres Beispiel, in dem ein directml-Diagramm erstellt wird, das die [quadratische Formel](https://en.wikipedia.org/wiki/Quadratic_formula)berechnen kann.</span><span class="sxs-lookup"><span data-stu-id="d344c-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

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

dml::Scope scope(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(scope, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(scope, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="d344c-121">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="d344c-121">More examples</span></span>

<span data-ttu-id="d344c-122">Vollständige Beispiele für die Verwendung von directmlx finden Sie im [directml-GitHub](https://github.com/microsoft/DirectML/tree/master/Samples)-Repository.</span><span class="sxs-lookup"><span data-stu-id="d344c-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="d344c-123">Compile-Time Optionen</span><span class="sxs-lookup"><span data-stu-id="d344c-123">Compile-Time Options</span></span>

<span data-ttu-id="d344c-124">Directmlx unterstützt Kompilierzeit #define zum Anpassen verschiedener Teile des Headers.</span><span class="sxs-lookup"><span data-stu-id="d344c-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="d344c-125">Option</span><span class="sxs-lookup"><span data-stu-id="d344c-125">Option</span></span>|<span data-ttu-id="d344c-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d344c-126">Description</span></span>|
|-|-|
|<span data-ttu-id="d344c-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="d344c-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="d344c-128">Wenn #define würde, führt dies dazu, dass Fehler zu einem-aufrufwurf führen, `std::abort` anstatt eine Ausnahme auszulösen.</span><span class="sxs-lookup"><span data-stu-id="d344c-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="d344c-129">Dies wird standardmäßig definiert, wenn Ausnahmen nicht verfügbar sind (z. b. wenn Ausnahmen in den Compileroptionen deaktiviert wurden).</span><span class="sxs-lookup"><span data-stu-id="d344c-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="d344c-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="d344c-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="d344c-131">Wenn #define 'd, werden Ausnahmen mit Ausnahme Typen der [Windows-Implementierungs Bibliothek](https://github.com/microsoft/wil) ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d344c-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="d344c-132">Andernfalls werden stattdessen Standard Ausnahme Typen (z `std::runtime_error` . b.) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d344c-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="d344c-133">Diese Option hat keine Auswirkung, wenn **DMLX_NO_EXCEPTIONS** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d344c-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="d344c-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="d344c-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="d344c-135">Wenn #define 'd, verwendet [Abseilen](https://github.com/abseil/abseil-cpp) als Dropdown Ersatz für Standard Bibliothekstypen, die in c++ 11 nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d344c-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="d344c-136">Zu diesen Typen gehören `absl::optional` (anstelle von `std::optional` ), `absl::Span` (anstelle von `std::span` ) und `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="d344c-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="d344c-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="d344c-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="d344c-138">Steuert, ob [gsl](https://github.com/microsoft/GSL) als Ersatz für verwendet werden soll `std::span` .</span><span class="sxs-lookup"><span data-stu-id="d344c-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="d344c-139">Wenn #define 'd, wird die Verwendung von `std::span` durch `gsl::span` für Compiler ohne Native `std::span` Implementierungen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d344c-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="d344c-140">Andernfalls wird stattdessen eine Inline-Dropdown-Implementierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d344c-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="d344c-141">Beachten Sie, dass diese Option nur beim Kompilieren von einem Pre-C + + 20-Compiler ohne Unterstützung von verwendet wird `std::span` , und wenn kein anderer Standard Bibliotheks Austausch (z. b. Abseil) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d344c-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="d344c-142">Steuern des Tensor-Layouts</span><span class="sxs-lookup"><span data-stu-id="d344c-142">Controlling Tensor Layout</span></span>

<span data-ttu-id="d344c-143">Für die meisten Operatoren berechnet directmlx die Eigenschaften der Ausgabe Mandanten des Operators in Ihrem Namen.</span><span class="sxs-lookup"><span data-stu-id="d344c-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="d344c-144">Wenn Sie z. b. eine `dml::Reduce` über Achsen `{ 0, 2, 3 }` mit einem Eingabe Mandanten von Größen ausführen `{ 3, 4, 5, 6 }` , berechnet directmlx automatisch die Eigenschaften des Ausgabe Mandanten, einschließlich der korrekten Form von `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="d344c-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="d344c-145">Die anderen Eigenschaften eines Ausgabe Mandanten umfassen jedoch die *Schritte "Fortschritte*", " *totaltensorsizeinbytes*" und " *GuaranteedBaseOffsetAlignment*".</span><span class="sxs-lookup"><span data-stu-id="d344c-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="d344c-146">Standardmäßig legt directmlx diese Eigenschaften so fest, dass der tensorflow über kein Striding, keine garantierte Basis Offset Ausrichtung und eine Gesamt-tensorflow-Größe in Bytes verfügt, wie von [dmlcalcbuffertensorsize](./dml-helper-functions.md#dmlcalcbuffertensorsize)berechnet.</span><span class="sxs-lookup"><span data-stu-id="d344c-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="d344c-147">Directmlx unterstützt die Möglichkeit zur Anpassung dieser Ausgabe Mandanten Eigenschaften mithilfe von Objekten, die als *tensorflow-Richtlinien* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d344c-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="d344c-148">Eine **tensorpolicy** ist ein anpassbarer Rückruf, der von directmlx aufgerufen wird, und gibt die Ausgabe Mandanten Eigenschaften zurück, wenn der berechnete Datentyp, die Flags und die Größe eines Mandanten angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d344c-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="d344c-149">Tensor-Richtlinien können für das **DML:: Scope** -Objekt festgelegt werden und werden für alle nachfolgenden Operatoren in diesem Diagramm verwendet.</span><span class="sxs-lookup"><span data-stu-id="d344c-149">Tensor policies can be set on the **dml::Scope** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="d344c-150">Tensor-Richtlinien können auch direkt festgelegt werden, wenn ein **tensordebug**-erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d344c-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="d344c-151">Das Layout der von directmlx erzeugten Tensoren kann daher durch Festlegen einer **tensorpolicy** gesteuert werden, die die entsprechenden Schritte auf den Tensoren festlegt.</span><span class="sxs-lookup"><span data-stu-id="d344c-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="d344c-152">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d344c-152">Example 1</span></span>

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

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="d344c-153">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d344c-153">Example 2</span></span>

<span data-ttu-id="d344c-154">Directmlx bietet auch einige alternative tensorflow-Richtlinien, die integriert sind.</span><span class="sxs-lookup"><span data-stu-id="d344c-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="d344c-155">Die **interleavedchannel** -Richtlinie wird z. b. als praktische Bereitstellung bereitgestellt und kann verwendet werden, um Tensoren mit Schritten zu entwickeln, die in der nhwc-Reihenfolge geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d344c-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="d344c-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d344c-156">See also</span></span>

* [<span data-ttu-id="d344c-157">Directml-GitHub</span><span class="sxs-lookup"><span data-stu-id="d344c-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="d344c-158">Directmlx yolov4 Beispiel</span><span class="sxs-lookup"><span data-stu-id="d344c-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="d344c-159">Verwenden von Schritten zum Ausdrücken von Auffüll-und Speicher Layout</span><span class="sxs-lookup"><span data-stu-id="d344c-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="d344c-160">DML_GRAPH_DESC Struktur</span><span class="sxs-lookup"><span data-stu-id="d344c-160">DML_GRAPH_DESC structure</span></span>](./directml/ns-directml-dml_graph_desc.md)