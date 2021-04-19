---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Berechnet aktualisierte Gewichtungen (Parameter) mithilfe der angegebenen Farbverläufe basierend auf dem Adam-Algorithmus (**Ada** ptive **M** oment-Schätzung). Dieser Operator ist ein Optimierer und wird in der Regel im Schritt zum Aktualisieren von Gewichtungen einer Trainings Schleife verwendet, um den gradientenabstieg auszuführen.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: a4acd26f5174bf6c6ae53f5edfdc28cc6c9b1a3d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354253"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>DML_ADAM_OPTIMIZER_OPERATOR_DESC-Struktur (directml. h)

Berechnet aktualisierte Gewichtungen (Parameter) mithilfe der angegebenen Farbverläufe basierend auf dem Adam-Algorithmus (**Ada** ptive **M** oment-Schätzung). Dieser Operator ist ein Optimierer und wird in der Regel im Schritt zum Aktualisieren von Gewichtungen einer Trainings Schleife verwendet, um den gradientenabstieg auszuführen.

Dieser Operator führt die folgende Berechnung aus:

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

Zusätzlich zur Berechnung der aktualisierten Gewichtungs Parameter (zurückgegeben in *outputparameterstensor*) gibt dieser Operator auch die aktualisierten ersten und zweiten Moment Schätzungen in *outputfirstmomenttensor* bzw. *outputsecondmomenttensor* zurück. In der Regel sollten Sie diese geschätzten ersten und zweiten Moment Schätzungen speichern und während des nachfolgenden Trainings Schritts als Eingaben angeben.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a>Member

`InputParametersTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow mit den Parametern (Gewichtungen), auf die dieser Optimierer angewendet werden soll. Die Werte für den Verlauf, den ersten und den zweiten Zeitpunkt, den aktuellen Trainingsschritt sowie Hyperparameter *learningrate*, *Beta1* und *Beta2* werden von diesem Operator verwendet, um den gradientenabstieg der Gewichtungswerte in diesem Mandanten auszuführen.

`InputFirstMomentTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die erste Moment Schätzung des Farbverlaufs für jeden Gewichtungswert enthält. Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über den *outputfirstaugentensor* abgerufen.

Wenn Sie diesen Optimierer zum ersten Mal auf einen Satz von Gewichtungen anwenden (z. b. während des anfänglichen Trainings Schritts), sollten die Werte dieses Mandanten in der Regel mit 0 (null) initialisiert werden. Bei nachfolgenden Ausführungen sollten die Werte verwendet werden, die in *outputfirstmomenttensor* zurückgegeben werden.

Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.

`InputSecondMomentTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein tensorflow, der die zweite Schätzung des Farbverlaufs für jeden Gewichtungswert enthält. Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über den *outputsecondmomenttensor* abgerufen.

Wenn Sie diesen Optimierer zum ersten Mal auf einen Satz von Gewichtungen anwenden (z. b. während des anfänglichen Trainings Schritts), sollten die Werte dieses Mandanten in der Regel mit 0 (null) initialisiert werden. Bei nachfolgenden Ausführungen sollten die in *outputsecondmomenttensor* zurückgegebenen Werte verwendet werden.

Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.

`GradientTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Die Farbverläufe, die auf die Eingabeparameter (Gewichtungen) für den Verlaufs Abstieg angewendet werden sollen. Farbverläufe werden in der Regel während des Trainings in einem Rück propagierungs Durchlauf abgerufen.

Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.

`TrainingStepTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein skalartensor mit einem einzelnen ganzzahligen Wert, der die aktuelle Anzahl der Trainingsschritte darstellt. Dieser Wert wird zusammen mit *Beta1* und *Beta2* verwendet, um den exponentiellen Zerfall der ersten und zweiten Moment Schätzwerte zu berechnen.

Normalerweise beginnt der Wert für den Trainingsschritt am Anfang des Trainings bei 0 und wird bei jedem aufeinander folgenden Trainingsschritt um 1 erhöht. Dieser Operator aktualisiert nicht den Wert für den Trainingsschritt. Sie sollten dies manuell durchführen, z. b. mit [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Dieser tensorflow muss ein Skalar sein (d. h. alle *Größen* gleich 1), und der Datentyp [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein ausgabetensor, der die aktualisierten Parameterwerte (Gewichtung) nach dem Anwenden des gradientenauslaufs enthält.

Während der Bindung ist dieser tensorflow berechtigt, einen berechtigten Eingabe Mandanten Alias zu verwenden, der zum Ausführen eines direkten Updates dieses Mandanten verwendet werden kann. Weitere Informationen finden Sie im Abschnitt " [Hinweise](#remarks) ".

Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.

`OutputFirstMomentTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein ausgabetensor mit aktualisierten ersten Moment Schätzungen. Sie sollten die Werte dieses Mandanten speichern und während des nachfolgenden Trainings Schritts in *inputfirstmomenttensor* bereitstellen.

Während der Bindung ist dieser tensorflow berechtigt, einen berechtigten Eingabe Mandanten Alias zu verwenden, der zum Ausführen eines direkten Updates dieses Mandanten verwendet werden kann. Weitere Informationen finden Sie im Abschnitt " [Hinweise](#remarks) ".

Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.

`OutputSecondMomentTensor`

Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein ausgabetensor, der aktualisierte Sekunden Zeitschätzungen enthält. Sie sollten die Werte dieses Mandanten speichern und während des nachfolgenden Trainings Schritts in *inputsecondmomenttensor* bereitstellen.

Während der Bindung ist dieser tensorflow berechtigt, einen berechtigten Eingabe Mandanten Alias zu verwenden, der zum Ausführen eines direkten Updates dieses Mandanten verwendet werden kann. Weitere Informationen finden Sie im Abschnitt " [Hinweise](#remarks) ".

Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.

`LearningRate`

Typ: **float**

Die Lernrate, auch als *Schrittgröße* bezeichnet. Die Lernrate ist ein Hyperparameter, der die Größe des Gewichtungs Updates entlang des Farbverlaufs Vektors bei jedem Trainingsschritt bestimmt.

`Beta1`

Typ: **float**

Ein Hyperparameter, der die exponentielle Zerfallsrate der ersten Moment Schätzung des Farbverlaufs darstellt. Dieser Wert muss zwischen 0,0 und 1,0 liegen. Ein Wert von 0.9 f ist typisch.

`Beta2`

Typ: **float**

Ein Hyperparameter, der die exponentielle Zerfallsrate der zweiten Moment Schätzung des Farbverlaufs darstellt. Dieser Wert muss zwischen 0,0 und 1,0 liegen. Der Wert 0,999 f ist typisch.

`Epsilon`

Typ: **float**

Ein kleiner Wert, der zur Unterstützung der numerischen Stabilität beiträgt, indem Division durch 0 (null) verhindert wird. Bei Gleit Komma Eingaben mit 32 Bit enthalten typische Werte 1E-8 oder `FLT_EPSILON` .

## <a name="remarks"></a>Bemerkungen
Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass jeder Ausgabe Mandanten bei der Bindung einen Alias für einen berechtigten Eingabe Mandanten zulässt. Beispielsweise ist es möglich, dieselbe Ressource sowohl für input *parameterstensor* als auch für *outputparameterstensor* zu binden, um eine direkte Aktualisierung der Eingabeparameter zu erzielen. Alle Eingabe-Tensoren dieses Operators, mit Ausnahme von *trainingsteptensor*, sind auf diese Weise als Alias berechtigt.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *Gradienttensor*, *inputfirstmomenttensor*, *inputparameterstensor*, *inputsecondmomenttensor*, *outputfirstmomenttensor*, *outputparameterstensor*, *outputsecondmomenttensor* und *trainingsteptensor* müssen denselben *Datentyp* aufweisen.
* *Gradienttensor*, *inputfirstmomenttensor*, *inputparameterstensor*, *inputsecondmomenttensor*, *outputfirstmomenttensor*, *outputparameterstensor* und *outputsecondmomenttensor* müssen die gleichen *Größen* aufweisen.

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensorflow | Typ | Dimensionen | Unterstützte Dimensions Anzahl | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Input parameterstensor | Eingabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |
| Inputfirstmomenttensor | Eingabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |
| Inputsecondmomenttensor | Eingabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |
| Gradienttensor | Eingabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |
| Trainingsteptensor | Eingabe | {1, 1, 1} | 4 | Float32, FLOAT16 |
| Outputparameterstensor | Ausgabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |
| Outputfirstmomenttensor | Ausgabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |
| Outputsecondmomenttensor | Ausgabe | {D0, D1, D2, D3} | 4 | Float32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |