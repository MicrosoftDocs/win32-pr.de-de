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
# <a name="using-fused-operators-to-improve-performance"></a>Verbessern der Leistung mithilfe von Fused-Operatoren

Einige directml-Operatoren unterstützen ein Konzept, das als *Fusion* bezeichnet wird. Die Operator Fusion ist eine Möglichkeit, die Leistung zu verbessern, indem ein Operator (in der Regel eine Aktivierungsfunktion) in einen anderen Operator gemergt wird, sodass Sie zusammen ausgeführt werden, ohne dass ein Roundtrip zum Arbeitsspeicher erforderlich ist.

## <a name="when-to-fuse-activations"></a>Zeitpunkt der Aktivierung von Aktivierungen

Die Aktivierung von aktivierten Aktivierungen ist eine Leistungsoptimierung. Ein sehr gängiges Szenario in vielen Machine Learning-Modellen (ml) ist das Anwenden einer nicht Linearität (eine Aktivierungsfunktion) auf die Ausgabe jeder Ebene im Modell.

Normalerweise ist hierfür ein Roundtrip zum Grafikspeicher erforderlich. Wenn z. b. auf eine Zusammenstellung von einer nicht gecluchten relu-Aktivierung folgt, muss die GPU warten, bis die Ergebnisse der Übertragung in den GPU-Speicher geschrieben wurden, bevor Sie mit dem Berechnen der relu-Aktivierungs Ebene beginnen kann. Wenn die Compute-Arbeitsauslastung der meisten Aktivierungs Funktionen tendenziell gering ist, kann dieser Roundtrip zum Grafikspeicher zu einem großen Leistungsengpass beitragen.

Die Operator Fusion ermöglicht die Ausführung der Aktivierungsfunktion (relu im obigen Beispiel) als Teil des vorangehenden Operators (z. b.). Dadurch kann die GPU die Aktivierungsfunktion berechnen, ohne darauf zu warten, dass die Ergebnisse des vorangehenden Operators in den Arbeitsspeicher geschrieben werden, &mdash; und die Leistung wird verbessert.

Da die Aktivierung von aktivierten Aktivierungen das gleiche Ergebnis ergibt, aber in vielen Fällen schneller ist, empfiehlt es sich, Aktivierungs Ebenen auszuschließen, indem Sie Sie nach Möglichkeit in den vorangehenden Operator hineinbringen.

## <a name="how-to-fuse-activations"></a>Vorgehensweise beim vereinen von Aktivierungen

Operatoren, die die Aktivierung von Aktivierungen unterstützen, verfügen über einen zusätzlichen optionalen Parameter in der Operator Struktur, `const DML_OPERATOR_DESC* FusedActivation` . Beispielsweise unterstützt die Übertragung die Aktivierung, und Sie verfügt über eine entsprechende *fusedactivation* in der Operator Beschreibung (siehe [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Um eine Aktivierung zu verleihen, erstellen Sie eine [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) , die den Typ der zu verschmelfenden Aktivierung beschreibt. Um z. b. eine relu-Funktion zu vereinen, wäre der richtige Operatortyp [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Beim Erstellen der Operator Beschreibung für die Aktivierungsfunktion müssen die Parameter *inputtensor* und *outputtensor* für die Aktivierungsfunktion auf **null** festgelegt werden.

## <a name="example"></a>Beispiel

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

Ein umfassendes Beispiel verwendet das [directmlsuperresolution](https://github.com/microsoft/DirectML/tree/master/Samples) -Beispiel, um die Leistung zu verbessern.

## <a name="operators-that-support-fused-activation"></a>Operatoren, die die Aktivierung von Fused

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** und **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Aktivierungen, die für Fusion unterstützt werden

* [DML_OPERATOR_ACTIVATION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTIVATION_HARD_SIGMOID**
* **DML_OPERATOR_ACTIVATION_IDENTITY**
* **DML_OPERATOR_ACTIVATION_LEAKY_RELU**
* **DML_OPERATOR_ACTIVATION_LINEAR**
* **DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_RELU**
* **DML_OPERATOR_ACTIVATION_SCALED_ELU**
* **DML_OPERATOR_ACTIVATION_SCALED_TANH**
* **DML_OPERATOR_ACTIVATION_SIGMOID**
* **DML_OPERATOR_ACTIVATION_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_SOFTSIGN**
* **DML_OPERATOR_ACTIVATION_TANH**
* **DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_ACTIVATION_CELU**

Alle Operatoren, die nicht in dieser Liste enthalten sind, werden nicht für die Aktivierung aktiviert.

## <a name="see-also"></a>Siehe auch

[Beispiel für directmlsuperresolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
[DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
