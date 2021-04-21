---
title: DirectMLX
description: DirectMLX ist eine C++-Hilfsbibliothek nur für Header für DirectML, die die Erstellung einzelner Operatoren in Diagrammen vereinfachen soll.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 2ddd6d9063002b76449224ebafdb6dd021b27fa0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803369"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX ist eine C++-Hilfsbibliothek nur für Header für DirectML, die die Erstellung einzelner Operatoren in Diagrammen vereinfachen soll.

DirectMLX bietet praktische Wrapper für alle DirectML-Operatortypen (DML) sowie intuitive Operatorüberladungen, wodurch es einfacher ist, DML-Operatoren zu instanziieren und in komplexe Diagramme zu verketten.

## <a name="where-to-find-directmlxh"></a>Wo sie zu finden sind `DirectMLX.h`

`DirectMLX.h` wird als Open-Source-Software unter der MIT-Lizenz verteilt. Die neueste Version finden Sie auf [DirectML GitHub.](https://github.com/microsoft/DirectML/tree/master/Libraries)

## <a name="tensor-constraints"></a>Tensoreinschränkungen

DirectMLX erfordert DirectML Version 1.4.0 oder höher (siehe [DirectML-Versionsverlauf](dml-version-history.md#version-table)). Ältere Versionen von DirectML werden nicht unterstützt.

DirectMLX.h erfordert einen C++11-fähigen Compiler, einschließlich (aber nicht beschränkt auf):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Beachten Sie, dass ein C++17-Compiler (oder ein neuerer) die empfohlene Option ist. Das Kompilieren für C++11 ist möglich, erfordert jedoch die Verwendung von Drittanbieterbibliotheken (z. [B. GSL](https://github.com/microsoft/GSL) und [Abseil),](https://github.com/abseil/abseil-cpp)um fehlende Standardbibliotheksfunktionen zu ersetzen.

Wenn Sie über eine Konfiguration verfügen, die nicht kompiliert werden `DirectMLX.h` kann, melden Sie [ein Problem auf unserem GitHub.](https://github.com/microsoft/DirectML/issues)

## <a name="basic-usage"></a>Grundlegende Verwendung

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

Im Folgenden finden Sie ein weiteres Beispiel, in dem ein DirectML-Graph erstellt wird, der die [quadratische Formel](https://en.wikipedia.org/wiki/Quadratic_formula)berechnen kann.

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

## <a name="more-examples"></a>Weitere Beispiele

Vollständige Beispiele mit DirectMLX finden Sie im [DirectML GitHub-Repository.](https://github.com/microsoft/DirectML/tree/master/Samples)

## <a name="compile-time-options"></a>Optionen zur Kompilierzeit

DirectMLX unterstützt #define zur Kompilierzeit, um verschiedene Teile des Headers anzupassen.

|Option|Beschreibung|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Wenn #define d, verursacht Fehler, die zu einem Aufruf von führen, `std::abort` anstatt eine Ausnahme auszu auslösen. Dies wird standardmäßig definiert, wenn Ausnahmen nicht verfügbar sind (z. B. wenn Ausnahmen in den Compileroptionen deaktiviert wurden).|
|**DMLX_USE_WIL**|Wenn #define, werden Ausnahmen mit ausnahmetypen der [Windows-Implementierungsbibliothek](https://github.com/microsoft/wil) ausgelöst. Andernfalls werden stattdessen `std::runtime_error` Standardausnahmetypen (z. B. ) verwendet. Diese Option hat keine Auswirkungen, wenn **DMLX_NO_EXCEPTIONS** definiert ist.|
|**DMLX_USE_ABSEIL**|Wenn #define ist, verwendet [Absturz](https://github.com/abseil/abseil-cpp) als Drop-In-Ersatz für Standardbibliothekstypen, die in C++11 nicht verfügbar sind. Zu diesen Typen `absl::optional` gehören (statt `std::optional` ), `absl::Span` (statt ) und `std::span` `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Steuert, ob [GSL als](https://github.com/microsoft/GSL) Ersatz für verwendet werden `std::span` soll. Wenn #define, werden Verwendungen von durch für Compiler `std::span` `gsl::span` ohne native `std::span` Implementierungen ersetzt. Andernfalls wird stattdessen eine Inline-Drop-In-Implementierung bereitgestellt. Beachten Sie, dass diese Option nur beim Kompilieren in einem Vor-C++20-Compiler ohne Unterstützung für verwendet wird, und wenn kein anderer Ersatz für die Standardbibliothek (z. B. `std::span` Abinstallieren) verwendet wird.|

## <a name="controlling-tensor-layout"></a>Steuern des Tensorlayouts

Für die meisten Operatoren berechnet DirectMLX die Eigenschaften der Ausgabetensoren des Operators in Ihrem Namen. Wenn Sie z. B. eine achsenübergreifend mit einem Eingabetensor von Größen ausführen, berechnet DirectMLX automatisch die Eigenschaften des Ausgabetensors einschließlich der richtigen `dml::Reduce` `{ 0, 2, 3 }` Form von `{ 3, 4, 5, 6 }` `{ 1, 4, 1, 1 }` .

Die anderen Eigenschaften eines Ausgabetensors umfassen jedoch *strides*, *TotalTensorSizeInBytes* und *GuaranteedBaseOffsetAlignment*. Standardmäßig legt DirectMLX diese Eigenschaften so fest, dass der Tensor keine striding-Eigenschaft, keine garantierte Ausrichtung des Basisoffsets und eine Gesamtgröße des Tensors in Bytes aufweist, wie von [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize)berechnet.

DirectMLX unterstützt die Möglichkeit, diese Ausgabetensoreigenschaften mithilfe von Objekten anzupassen, die als *Tensorrichtlinien bezeichnet werden.* Eine **TensorPolicy** ist ein anpassbarer Rückruf, der von DirectMLX aufgerufen wird und Ausgabe-Tensoreigenschaften zurückgibt, wenn der berechnete Datentyp, die Flags und die Größen eines Tensors angegeben werden.

Tensor-Richtlinien können für das **dml::Graph-Objekt** festgelegt werden und werden für alle nachfolgenden Operatoren in diesem Diagramm verwendet. Tensor-Richtlinien können auch direkt festgelegt werden, wenn ein **TensorDesc** erstellt wird.

Das Layout von Tensoren, die von DirectMLX erzeugt werden, kann daher durch Festlegen einer **TensorPolicy** gesteuert werden, die die entsprechenden Schritte auf ihren Tensoren festlegt.

### <a name="example-1"></a>Beispiel 1

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

### <a name="example-2"></a>Beispiel 2

DirectMLX bietet auch einige integrierte alternative Tensorrichtlinien. Die **InterleavedChannel-Richtlinie** wird beispielsweise zur Vereinfachung bereitgestellt und kann verwendet werden, um Tensoren mit Schritten zu erzeugen, sodass sie in NHWC-Reihenfolge geschrieben werden.

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Siehe auch

* [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [DirectMLX yolov4-Beispiel](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Verwenden von Schritten zum Ausdrücken der Auffüllung und des Speicherlayouts](./dml-strides.md)
* [DML_GRAPH_DESC Struktur](./directml/ns-directml-dml_graph_desc.md)