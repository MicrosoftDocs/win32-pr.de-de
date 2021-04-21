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
# <a name="using-fused-operators-to-improve-performance"></a>Verwendung von Fused-Operatoren zur Leistungssteigerung

Einige DirectML-Operatoren unterstützen ein Konzept, das als *Fusion bezeichnet wird.* Operator fusion ist eine Möglichkeit, die Leistung zu verbessern, indem ein Operator (in der Regel eine Aktivierungsfunktion) mit einem anderen Operator zusammengeführt wird, sodass sie zusammen ausgeführt werden, ohne dass ein Roundtrip zum Arbeitsspeicher erforderlich ist.

## <a name="when-to-fuse-activations"></a>Wann werden Aktivierungen aktiviert?

Fused-Aktivierungen sind eine Leistungsoptimierung. Ein sehr häufiges Szenario in vielen Machine Learning-Modellen (ML) besteht in der Anwendung einer Nichtlinearität (einer Aktivierungsfunktion) auf die Ausgabe jeder Ebene im Modell.

Normalerweise erfordert dies einen Roundtrip zum Grafikspeicher. Wenn beispielsweise auf eine Konvolution eine nicht fused Relu-Aktivierung folgt, muss die GPU warten, bis die Ergebnisse der Convolution in den GPU-Arbeitsspeicher geschrieben werden, bevor sie mit der Berechnung der Relu-Aktivierungsebene beginnen kann. Da die Computeworkload der meisten Aktivierungsfunktionen tendenziell klein ist, kann dieser Roundtrip zum Grafikspeicher ein großer Leistungsengpass sein.

Operator fusion ermöglicht die Aktivierungsfunktion (im obigen Beispiel Relu) als Teil des vorherigen Operators (z. B. Convolution). Dadurch kann die GPU die Aktivierungsfunktion berechnen, ohne darauf zu warten, dass die Ergebnisse des vorherigen Operators in den Arbeitsspeicher geschrieben werden, was &mdash; die Leistung verbessert.

Da fused-Aktivierungen das gleiche Ergebnis erzeugen, aber in vielen Fällen schneller sind, empfehlen wir Ihnen, Aktivierungsebenen zu beseitigen, indem Sie sie nach Möglichkeit in ihren vorherigen Operator einfingen.

## <a name="how-to-fuse-activations"></a>How to fuse activations (Zusammensnieren von Aktivierungen)

Operatoren, die fused-Aktivierungen unterstützen, verfügen über einen zusätzlichen optionalen Parameter in ihrer Operatorstruktur, `const DML_OPERATOR_DESC* FusedActivation` . Convolution unterstützt z.B. die Fused-Aktivierung und verfügt über eine entsprechende *FusedActivation* in der Operatorbeschreibung (siehe [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Erstellen Sie zum Fuseieren einer Aktivierung eine [DML_OPERATOR_DESC,](/windows/win32/api/directml/ns-directml-dml_operator_desc) die den Typ der Zusicherung beschreibt. Um z. B. eine Relu-Funktion zu fusionieren, wäre der richtige Operatortyp [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Beim Erstellen der Operatorbeschreibung für die Aktivierungsfunktion müssen Sie die *Parameter InputTensor* und *OutputTensor* für die Aktivierungsfunktion auf **NULL** festlegen.

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

Für ein vollständiges Beispiel verwendet das [DirectMLSuperResolution-Beispiel](https://github.com/microsoft/DirectML/tree/master/Samples) fused-Aktivierungen, um die Leistung zu verbessern.

## <a name="operators-that-support-fused-activation"></a>Operatoren, die die fused-Aktivierung unterstützen

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

Operatoren, die nicht in dieser Liste enthalten sind, werden für die Fused-Aktivierung nicht unterstützt.

## <a name="see-also"></a>Siehe auch

* [DirectMLSuperResolution-Beispiel](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
