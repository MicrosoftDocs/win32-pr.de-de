---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Berechnet aktualisierte Gewichtungen (Parameter) mithilfe der angegebenen Farbverläufe basierend auf dem Adam-Algorithmus **(ADA** ptive **M** oment estimation). Dieser Operator ist ein Optimierer und wird in der Regel im Schritt der Gewichtungsaktualisierung einer Trainingsschleife verwendet, um einen Gradientenabstieg durchzuführen.
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
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803525"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>DML_ADAM_OPTIMIZER_OPERATOR_DESC-Struktur (directml.h)

Berechnet aktualisierte Gewichtungen (Parameter) mithilfe der angegebenen Farbverläufe basierend auf dem Adam-Algorithmus **(ADA** ptive **M** oment estimation). Dieser Operator ist ein Optimierer und wird in der Regel im Schritt der Gewichtungsaktualisierung einer Trainingsschleife verwendet, um einen Gradientenabstieg durchzuführen.

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

Zusätzlich zum Berechnen der aktualisierten Gewichtungsparameter (zurückgegeben in *OutputParametersTensor)* gibt dieser Operator auch die aktualisierten Schätzungen des ersten und zweiten Moments in *OutputFirstMomentTensor* bzw. *OutputSecondMomentTensor* zurück. In der Regel sollten Sie diese Schätzungen für den ersten und zweiten Moment speichern und sie während des nachfolgenden Trainingsschritts als Eingaben bereitstellen.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Parameter (Gewichtungen) enthält, auf die dieser Optimierer angewendet werden soll. Die Schätzwerte für den Farbverlauf, den ersten und zweiten Moment, den aktuellen Trainingsschritt sowie die Hyperparameter *LearningRate,* *Beta1* und *Beta2* werden von diesem Operator verwendet, um den Gradientenabstieg für die gewichtigen Werte durchzuführen, die in diesem Tensor angegeben sind.

`InputFirstMomentTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der die Schätzung des Farbverlaufs für jeden Gewichtungswert des ersten Moments enthält. Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über *outputFirstMomentTensor* abgerufen.

Wenn sie diesen Optimierer zum ersten Mal auf eine Gruppe von Gewichtungen anwenden (z. B. während des ersten Trainingsschritts), sollten die Werte dieses Tensors in der Regel mit 0 initialisiert werden. Nachfolgende Ausführungen sollten die in *OutputFirstMomentTensor zurückgegebenen Werte verwenden.*

Die *Größen und* der Datentyp *dieses* Tensors müssen genau mit denen des *InputParametersTensor übereinstimmen.*

`InputSecondMomentTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Tensor, der den zweiten Moment der Schätzung des Farbverlaufs für jeden Gewichtungswert enthält. Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über *outputSecondMomentTensor erhalten.*

Wenn sie diesen Optimierer zum ersten Mal auf eine Gruppe von Gewichtungen anwenden (z. B. während des ersten Trainingsschritts), sollten die Werte dieses Tensors in der Regel mit 0 initialisiert werden. Nachfolgende Ausführungen sollten die in *OutputSecondMomentTensor zurückgegebenen Werte verwenden.*

Die *Größen und* der Datentyp *dieses* Tensors müssen genau mit denen des *InputParametersTensor übereinstimmen.*

`GradientTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Die Farbverläufe, die auf die Eingabeparameter (Gewichtungen) für den Gradientenabstieg angewendet werden. Farbverläufe werden in der Regel während des Trainings in einem Rückpropagation-Durchgang ermittelt.

Die *Größen und* der Datentyp *dieses* Tensors müssen genau mit denen des *InputParametersTensor übereinstimmen.*

`TrainingStepTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein skalarer Tensor, der einen einzelnen ganzzahligen Wert enthält, der die aktuelle Anzahl von Trainingsschritten darstellt. Dieser Wert wird zusammen *mit Beta1* und *Beta2* verwendet, um den exponentiellen Verfall des ersten und zweiten Moments der Schätzung der Tensoren zu berechnen.

In der Regel beginnt der Wert des Trainingsschritts bei 0 am Anfang des Trainings und wird bei jedem nachfolgenden Trainingsschritt um 1 erhöht. Dieser Operator aktualisiert den Wert des Trainingsschritts nicht. Sie sollten dies manuell durchführen, z. B. mit [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Dieser Tensor muss ein Skalar (d. h. alle *Größen* gleich 1) sein und den Datentyp [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)aufweisen.

`OutputParametersTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der die aktualisierten Parameterwerte (Gewichtung) enthält, nachdem der Gradientenabstieg angewendet wurde.

Während der Bindung darf dieser Tensor ein Alias für einen geeigneten Eingabe-Tensor verwenden, der zum Ausführen eines direkt aktualisierten Tensors verwendet werden kann. Weitere Informationen finden Sie im Abschnitt ["Hinweise".](#remarks)

Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.

`OutputFirstMomentTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der aktualisierte Schätzungen des ersten Moments enthält. Sie sollten die Werte dieses Tensors speichern und während des nachfolgenden Trainingsschritts in *InputFirstMomentTensor* bereitstellen.

Während der Bindung darf dieser Tensor ein Alias für einen geeigneten Eingabe-Tensor verwenden, der zum Ausführen eines direkt aktualisierten Tensors verwendet werden kann. Weitere Informationen finden Sie im Abschnitt ["Hinweise".](#remarks)

Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.

`OutputSecondMomentTensor`

Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ein Ausgabe-Tensor, der aktualisierte Schätzungen des zweiten Moments enthält. Sie sollten die Werte dieses Tensors speichern und während des nachfolgenden Trainingsschritts in *InputSecondMomentTensor* bereitstellen.

Während der Bindung darf dieser Tensor ein Alias für einen geeigneten Eingabe-Tensor verwenden, der zum Ausführen eines direkt aktualisierten Tensors verwendet werden kann. Weitere Informationen finden Sie im Abschnitt ["Hinweise".](#remarks)

Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.

`LearningRate`

Typ: **float**

Die Lernrate, die auch häufig als *Schrittgröße* bezeichnet wird. Die Lernrate ist ein Hyperparameter, der die Größe der Gewichtungsaktualisierung entlang des Farbverlaufsvektors für jeden Trainingsschritt bestimmt.

`Beta1`

Typ: **float**

Ein Hyperparameter, der die exponentielle Abklingrate der Schätzung des ersten Moments des Farbverlaufs darstellt. Dieser Wert sollte zwischen 0,0 und 1,0 liegen. Der Wert 0,9f ist typisch.

`Beta2`

Typ: **float**

Ein Hyperparameter, der die exponentielle Abklingrate der Schätzung des zweiten Moments des Farbverlaufs darstellt. Dieser Wert sollte zwischen 0,0 und 1,0 liegen. Der Wert 0,999f ist typisch.

`Epsilon`

Typ: **float**

Ein kleiner Wert, der zur Unterstützung der numerischen Stabilität verwendet wird, indem division-by-zero verhindert wird. Für 32-Bit-Gleitkommaeingaben sind typische Werte 1e-8 oder `FLT_EPSILON` .

## <a name="remarks"></a>Hinweise
Dieser Operator unterstützt die ausführungsbasierte Ausführung. Dies bedeutet, dass jeder Ausgabe tensor während der Bindung einen Alias für einen berechtigten Eingabetensor verwenden darf. Beispielsweise ist es möglich, dieselbe Ressource sowohl für *inputParametersTensor* als auch *für OutputParametersTensor* zu binden, um effektiv eine direkt aktualisierten Eingabeparameter zu erzielen. Alle Eingabetensoren dieses Operators, mit Ausnahme von *TrainingStepTensor,* können auf diese Weise als Alias verwendet werden.

## <a name="availability"></a>Verfügbarkeit
Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.

## <a name="tensor-constraints"></a>Tensor-Einschränkungen
* *GradientTensor,* *InputFirstMomentTensor,* *InputParametersTensor,* *InputSecondMomentTensor,* *OutputFirstMomentTensor,* *OutputParametersTensor,* *OutputSecondMomentTensor* und *TrainingStepTensor* müssen denselben *Datentyp haben.*
* *GradientTensor,* *InputFirstMomentTensor,* *InputParametersTensor,* *InputSecondMomentTensor,* *OutputFirstMomentTensor,* *OutputParametersTensor* und *OutputSecondMomentTensor* müssen die gleichen *Größen haben.*

## <a name="tensor-support"></a>Tensor-Unterstützung
| Tensor | Typ | Dimensionen | Unterstützte Dimensionsanzahlen | Unterstützte Datentypen |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Eingabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Eingabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Eingabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Eingabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Eingabe | { 1, 1, 1, 1 } | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Ausgabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Ausgabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Ausgabe | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |