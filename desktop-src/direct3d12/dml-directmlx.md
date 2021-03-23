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
# <a name="directmlx"></a>Directmlx

Directmlx ist eine Hilfsbibliothek für C++-Header für directml, die das Verfassen einzelner Operatoren in Graphen erleichtern soll.

Directmlx bietet bequeme Wrapper für alle directml (DML)-Operator Typen sowie intuitive Operator Überladungen, die die Instanziieren von DML-Operatoren vereinfachen und Sie in komplexe Diagramme verketten.

## <a name="where-to-find-directmlxh"></a>Speicherort `DirectMLX.h`

`DirectMLX.h` wird als Open-Source-Software unter der mit-Lizenz verteilt. Die neueste Version finden Sie auf der [directml-GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)-Version.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen

Directmlx erfordert directml-Version 1.4.0 oder höher (siehe [directml-Versionsverlauf](dml-version-history.md#version-table)). Ältere Versionen von directml werden nicht unterstützt.

Directmlx. h erfordert einen C + +11-fähigen Compiler, einschließlich (aber nicht beschränkt auf):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Beachten Sie, dass es sich bei einem c++ 17 (oder neueren) Compiler um Optionen handelt, die wir empfehlen. Die Kompilierung für c++ 11 ist möglich, erfordert jedoch die Verwendung von Drittanbieterbibliotheken (z. b. [gsl](https://github.com/microsoft/GSL) und [Abseil](https://github.com/abseil/abseil-cpp)), um fehlende Standard Bibliotheksfunktionen zu ersetzen.

Wenn Sie über eine Konfiguration verfügen, die nicht kompiliert `DirectMLX.h` werden kann, melden Sie [ein Problem auf unserem GitHub](https://github.com/microsoft/DirectML/issues).

## <a name="basic-usage"></a>Grundlegende Verwendung

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

Im folgenden finden Sie ein weiteres Beispiel, in dem ein directml-Diagramm erstellt wird, das die [quadratische Formel](https://en.wikipedia.org/wiki/Quadratic_formula)berechnen kann.

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

## <a name="more-examples"></a>Weitere Beispiele

Vollständige Beispiele für die Verwendung von directmlx finden Sie im [directml-GitHub](https://github.com/microsoft/DirectML/tree/master/Samples)-Repository.

## <a name="compile-time-options"></a>Compile-Time Optionen

Directmlx unterstützt Kompilierzeit #define zum Anpassen verschiedener Teile des Headers.

|Option|Beschreibung|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Wenn #define würde, führt dies dazu, dass Fehler zu einem-aufrufwurf führen, `std::abort` anstatt eine Ausnahme auszulösen. Dies wird standardmäßig definiert, wenn Ausnahmen nicht verfügbar sind (z. b. wenn Ausnahmen in den Compileroptionen deaktiviert wurden).|
|**DMLX_USE_WIL**|Wenn #define 'd, werden Ausnahmen mit Ausnahme Typen der [Windows-Implementierungs Bibliothek](https://github.com/microsoft/wil) ausgelöst. Andernfalls werden stattdessen Standard Ausnahme Typen (z `std::runtime_error` . b.) verwendet. Diese Option hat keine Auswirkung, wenn **DMLX_NO_EXCEPTIONS** definiert ist.|
|**DMLX_USE_ABSEIL**|Wenn #define 'd, verwendet [Abseilen](https://github.com/abseil/abseil-cpp) als Dropdown Ersatz für Standard Bibliothekstypen, die in c++ 11 nicht verfügbar sind. Zu diesen Typen gehören `absl::optional` (anstelle von `std::optional` ), `absl::Span` (anstelle von `std::span` ) und `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Steuert, ob [gsl](https://github.com/microsoft/GSL) als Ersatz für verwendet werden soll `std::span` . Wenn #define 'd, wird die Verwendung von `std::span` durch `gsl::span` für Compiler ohne Native `std::span` Implementierungen ersetzt. Andernfalls wird stattdessen eine Inline-Dropdown-Implementierung bereitgestellt. Beachten Sie, dass diese Option nur beim Kompilieren von einem Pre-C + + 20-Compiler ohne Unterstützung von verwendet wird `std::span` , und wenn kein anderer Standard Bibliotheks Austausch (z. b. Abseil) verwendet wird.|

## <a name="controlling-tensor-layout"></a>Steuern des Tensor-Layouts

Für die meisten Operatoren berechnet directmlx die Eigenschaften der Ausgabe Mandanten des Operators in Ihrem Namen. Wenn Sie z. b. eine `dml::Reduce` über Achsen `{ 0, 2, 3 }` mit einem Eingabe Mandanten von Größen ausführen `{ 3, 4, 5, 6 }` , berechnet directmlx automatisch die Eigenschaften des Ausgabe Mandanten, einschließlich der korrekten Form von `{ 1, 4, 1, 1 }` .

Die anderen Eigenschaften eines Ausgabe Mandanten umfassen jedoch die *Schritte "Fortschritte*", " *totaltensorsizeinbytes*" und " *GuaranteedBaseOffsetAlignment*". Standardmäßig legt directmlx diese Eigenschaften so fest, dass der tensorflow über kein Striding, keine garantierte Basis Offset Ausrichtung und eine Gesamt-tensorflow-Größe in Bytes verfügt, wie von [dmlcalcbuffertensorsize](./dml-helper-functions.md#dmlcalcbuffertensorsize)berechnet.

Directmlx unterstützt die Möglichkeit zur Anpassung dieser Ausgabe Mandanten Eigenschaften mithilfe von Objekten, die als *tensorflow-Richtlinien* bezeichnet werden. Eine **tensorpolicy** ist ein anpassbarer Rückruf, der von directmlx aufgerufen wird, und gibt die Ausgabe Mandanten Eigenschaften zurück, wenn der berechnete Datentyp, die Flags und die Größe eines Mandanten angegeben sind.

Tensor-Richtlinien können für das **DML:: Scope** -Objekt festgelegt werden und werden für alle nachfolgenden Operatoren in diesem Diagramm verwendet. Tensor-Richtlinien können auch direkt festgelegt werden, wenn ein **tensordebug**-erstellt wird.

Das Layout der von directmlx erzeugten Tensoren kann daher durch Festlegen einer **tensorpolicy** gesteuert werden, die die entsprechenden Schritte auf den Tensoren festlegt.

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

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>Beispiel 2

Directmlx bietet auch einige alternative tensorflow-Richtlinien, die integriert sind. Die **interleavedchannel** -Richtlinie wird z. b. als praktische Bereitstellung bereitgestellt und kann verwendet werden, um Tensoren mit Schritten zu entwickeln, die in der nhwc-Reihenfolge geschrieben werden.

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Siehe auch

* [Directml-GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Directmlx yolov4 Beispiel](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Verwenden von Schritten zum Ausdrücken von Auffüll-und Speicher Layout](./dml-strides.md)
* [DML_GRAPH_DESC Struktur](./directml/ns-directml-dml_graph_desc.md)