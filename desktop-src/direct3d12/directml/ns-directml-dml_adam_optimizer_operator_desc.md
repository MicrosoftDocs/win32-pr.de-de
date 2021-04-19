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
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="85b6e-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC-Struktur (directml. h)</span><span class="sxs-lookup"><span data-stu-id="85b6e-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="85b6e-105">Berechnet aktualisierte Gewichtungen (Parameter) mithilfe der angegebenen Farbverläufe basierend auf dem Adam-Algorithmus (**Ada** ptive **M** oment-Schätzung).</span><span class="sxs-lookup"><span data-stu-id="85b6e-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="85b6e-106">Dieser Operator ist ein Optimierer und wird in der Regel im Schritt zum Aktualisieren von Gewichtungen einer Trainings Schleife verwendet, um den gradientenabstieg auszuführen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="85b6e-107">Dieser Operator führt die folgende Berechnung aus:</span><span class="sxs-lookup"><span data-stu-id="85b6e-107">This operator performs the following computation:</span></span>

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

<span data-ttu-id="85b6e-108">Zusätzlich zur Berechnung der aktualisierten Gewichtungs Parameter (zurückgegeben in *outputparameterstensor*) gibt dieser Operator auch die aktualisierten ersten und zweiten Moment Schätzungen in *outputfirstmomenttensor* bzw. *outputsecondmomenttensor* zurück.</span><span class="sxs-lookup"><span data-stu-id="85b6e-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="85b6e-109">In der Regel sollten Sie diese geschätzten ersten und zweiten Moment Schätzungen speichern und während des nachfolgenden Trainings Schritts als Eingaben angeben.</span><span class="sxs-lookup"><span data-stu-id="85b6e-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85b6e-110">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="85b6e-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="85b6e-111">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="85b6e-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="85b6e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="85b6e-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="85b6e-113">Member</span><span class="sxs-lookup"><span data-stu-id="85b6e-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="85b6e-114">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-115">Ein tensorflow mit den Parametern (Gewichtungen), auf die dieser Optimierer angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85b6e-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="85b6e-116">Die Werte für den Verlauf, den ersten und den zweiten Zeitpunkt, den aktuellen Trainingsschritt sowie Hyperparameter *learningrate*, *Beta1* und *Beta2* werden von diesem Operator verwendet, um den gradientenabstieg der Gewichtungswerte in diesem Mandanten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="85b6e-117">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-118">Ein tensorflow, der die erste Moment Schätzung des Farbverlaufs für jeden Gewichtungswert enthält.</span><span class="sxs-lookup"><span data-stu-id="85b6e-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="85b6e-119">Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über den *outputfirstaugentensor* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="85b6e-120">Wenn Sie diesen Optimierer zum ersten Mal auf einen Satz von Gewichtungen anwenden (z. b. während des anfänglichen Trainings Schritts), sollten die Werte dieses Mandanten in der Regel mit 0 (null) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="85b6e-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="85b6e-121">Bei nachfolgenden Ausführungen sollten die Werte verwendet werden, die in *outputfirstmomenttensor* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="85b6e-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="85b6e-122">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="85b6e-123">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-124">Ein tensorflow, der die zweite Schätzung des Farbverlaufs für jeden Gewichtungswert enthält.</span><span class="sxs-lookup"><span data-stu-id="85b6e-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="85b6e-125">Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über den *outputsecondmomenttensor* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="85b6e-126">Wenn Sie diesen Optimierer zum ersten Mal auf einen Satz von Gewichtungen anwenden (z. b. während des anfänglichen Trainings Schritts), sollten die Werte dieses Mandanten in der Regel mit 0 (null) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="85b6e-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="85b6e-127">Bei nachfolgenden Ausführungen sollten die in *outputsecondmomenttensor* zurückgegebenen Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85b6e-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="85b6e-128">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="85b6e-129">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-130">Die Farbverläufe, die auf die Eingabeparameter (Gewichtungen) für den Verlaufs Abstieg angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="85b6e-131">Farbverläufe werden in der Regel während des Trainings in einem Rück propagierungs Durchlauf abgerufen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="85b6e-132">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="85b6e-133">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-134">Ein skalartensor mit einem einzelnen ganzzahligen Wert, der die aktuelle Anzahl der Trainingsschritte darstellt.</span><span class="sxs-lookup"><span data-stu-id="85b6e-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="85b6e-135">Dieser Wert wird zusammen mit *Beta1* und *Beta2* verwendet, um den exponentiellen Zerfall der ersten und zweiten Moment Schätzwerte zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="85b6e-136">Normalerweise beginnt der Wert für den Trainingsschritt am Anfang des Trainings bei 0 und wird bei jedem aufeinander folgenden Trainingsschritt um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="85b6e-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="85b6e-137">Dieser Operator aktualisiert nicht den Wert für den Trainingsschritt. Sie sollten dies manuell durchführen, z. b. mit [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="85b6e-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="85b6e-138">Dieser tensorflow muss ein Skalar sein (d. h. alle *Größen* gleich 1), und der Datentyp [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="85b6e-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="85b6e-139">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-140">Ein ausgabetensor, der die aktualisierten Parameterwerte (Gewichtung) nach dem Anwenden des gradientenauslaufs enthält.</span><span class="sxs-lookup"><span data-stu-id="85b6e-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="85b6e-141">Während der Bindung ist dieser tensorflow berechtigt, einen berechtigten Eingabe Mandanten Alias zu verwenden, der zum Ausführen eines direkten Updates dieses Mandanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85b6e-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="85b6e-142">Weitere Informationen finden Sie im Abschnitt " [Hinweise](#remarks) ".</span><span class="sxs-lookup"><span data-stu-id="85b6e-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="85b6e-143">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="85b6e-144">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-145">Ein ausgabetensor mit aktualisierten ersten Moment Schätzungen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="85b6e-146">Sie sollten die Werte dieses Mandanten speichern und während des nachfolgenden Trainings Schritts in *inputfirstmomenttensor* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="85b6e-147">Während der Bindung ist dieser tensorflow berechtigt, einen berechtigten Eingabe Mandanten Alias zu verwenden, der zum Ausführen eines direkten Updates dieses Mandanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85b6e-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="85b6e-148">Weitere Informationen finden Sie im Abschnitt " [Hinweise](#remarks) ".</span><span class="sxs-lookup"><span data-stu-id="85b6e-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="85b6e-149">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="85b6e-150">Typ: Konstante **[DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="85b6e-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="85b6e-151">Ein ausgabetensor, der aktualisierte Sekunden Zeitschätzungen enthält.</span><span class="sxs-lookup"><span data-stu-id="85b6e-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="85b6e-152">Sie sollten die Werte dieses Mandanten speichern und während des nachfolgenden Trainings Schritts in *inputsecondmomenttensor* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="85b6e-153">Während der Bindung ist dieser tensorflow berechtigt, einen berechtigten Eingabe Mandanten Alias zu verwenden, der zum Ausführen eines direkten Updates dieses Mandanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85b6e-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="85b6e-154">Weitere Informationen finden Sie im Abschnitt " [Hinweise](#remarks) ".</span><span class="sxs-lookup"><span data-stu-id="85b6e-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="85b6e-155">Die *Größen* und der *Datentyp* dieses Mandanten müssen genau mit denen des *Input parameterstensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="85b6e-156">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="85b6e-156">Type: **float**</span></span>

<span data-ttu-id="85b6e-157">Die Lernrate, auch als *Schrittgröße* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="85b6e-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="85b6e-158">Die Lernrate ist ein Hyperparameter, der die Größe des Gewichtungs Updates entlang des Farbverlaufs Vektors bei jedem Trainingsschritt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="85b6e-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="85b6e-159">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="85b6e-159">Type: **float**</span></span>

<span data-ttu-id="85b6e-160">Ein Hyperparameter, der die exponentielle Zerfallsrate der ersten Moment Schätzung des Farbverlaufs darstellt.</span><span class="sxs-lookup"><span data-stu-id="85b6e-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="85b6e-161">Dieser Wert muss zwischen 0,0 und 1,0 liegen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="85b6e-162">Ein Wert von 0.9 f ist typisch.</span><span class="sxs-lookup"><span data-stu-id="85b6e-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="85b6e-163">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="85b6e-163">Type: **float**</span></span>

<span data-ttu-id="85b6e-164">Ein Hyperparameter, der die exponentielle Zerfallsrate der zweiten Moment Schätzung des Farbverlaufs darstellt.</span><span class="sxs-lookup"><span data-stu-id="85b6e-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="85b6e-165">Dieser Wert muss zwischen 0,0 und 1,0 liegen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="85b6e-166">Der Wert 0,999 f ist typisch.</span><span class="sxs-lookup"><span data-stu-id="85b6e-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="85b6e-167">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="85b6e-167">Type: **float**</span></span>

<span data-ttu-id="85b6e-168">Ein kleiner Wert, der zur Unterstützung der numerischen Stabilität beiträgt, indem Division durch 0 (null) verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="85b6e-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="85b6e-169">Bei Gleit Komma Eingaben mit 32 Bit enthalten typische Werte 1E-8 oder `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="85b6e-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="85b6e-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85b6e-170">Remarks</span></span>
<span data-ttu-id="85b6e-171">Dieser Operator unterstützt die direkte Ausführung. Dies bedeutet, dass jeder Ausgabe Mandanten bei der Bindung einen Alias für einen berechtigten Eingabe Mandanten zulässt.</span><span class="sxs-lookup"><span data-stu-id="85b6e-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="85b6e-172">Beispielsweise ist es möglich, dieselbe Ressource sowohl für input *parameterstensor* als auch für *outputparameterstensor* zu binden, um eine direkte Aktualisierung der Eingabeparameter zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="85b6e-173">Alle Eingabe-Tensoren dieses Operators, mit Ausnahme von *trainingsteptensor*, sind auf diese Weise als Alias berechtigt.</span><span class="sxs-lookup"><span data-stu-id="85b6e-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="85b6e-174">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="85b6e-174">Availability</span></span>
<span data-ttu-id="85b6e-175">Dieser Operator wurde in eingeführt `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="85b6e-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="85b6e-176">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="85b6e-176">Tensor constraints</span></span>
* <span data-ttu-id="85b6e-177">*Gradienttensor*, *inputfirstmomenttensor*, *inputparameterstensor*, *inputsecondmomenttensor*, *outputfirstmomenttensor*, *outputparameterstensor*, *outputsecondmomenttensor* und *trainingsteptensor* müssen denselben *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="85b6e-178">*Gradienttensor*, *inputfirstmomenttensor*, *inputparameterstensor*, *inputsecondmomenttensor*, *outputfirstmomenttensor*, *outputparameterstensor* und *outputsecondmomenttensor* müssen die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="85b6e-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="85b6e-179">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="85b6e-179">Tensor support</span></span>
| <span data-ttu-id="85b6e-180">Tensorflow</span><span class="sxs-lookup"><span data-stu-id="85b6e-180">Tensor</span></span> | <span data-ttu-id="85b6e-181">Typ</span><span class="sxs-lookup"><span data-stu-id="85b6e-181">Kind</span></span> | <span data-ttu-id="85b6e-182">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="85b6e-182">Dimensions</span></span> | <span data-ttu-id="85b6e-183">Unterstützte Dimensions Anzahl</span><span class="sxs-lookup"><span data-stu-id="85b6e-183">Supported dimension counts</span></span> | <span data-ttu-id="85b6e-184">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="85b6e-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="85b6e-185">Input parameterstensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-185">InputParametersTensor</span></span> | <span data-ttu-id="85b6e-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-186">Input</span></span> | <span data-ttu-id="85b6e-187">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-188">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-188">4</span></span> | <span data-ttu-id="85b6e-189">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-190">Inputfirstmomenttensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="85b6e-191">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-191">Input</span></span> | <span data-ttu-id="85b6e-192">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-193">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-193">4</span></span> | <span data-ttu-id="85b6e-194">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-195">Inputsecondmomenttensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="85b6e-196">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-196">Input</span></span> | <span data-ttu-id="85b6e-197">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-198">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-198">4</span></span> | <span data-ttu-id="85b6e-199">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-200">Gradienttensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-200">GradientTensor</span></span> | <span data-ttu-id="85b6e-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-201">Input</span></span> | <span data-ttu-id="85b6e-202">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-203">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-203">4</span></span> | <span data-ttu-id="85b6e-204">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-205">Trainingsteptensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-205">TrainingStepTensor</span></span> | <span data-ttu-id="85b6e-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-206">Input</span></span> | <span data-ttu-id="85b6e-207">{1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="85b6e-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="85b6e-208">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-208">4</span></span> | <span data-ttu-id="85b6e-209">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-210">Outputparameterstensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-210">OutputParametersTensor</span></span> | <span data-ttu-id="85b6e-211">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-211">Output</span></span> | <span data-ttu-id="85b6e-212">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-213">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-213">4</span></span> | <span data-ttu-id="85b6e-214">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-215">Outputfirstmomenttensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="85b6e-216">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-216">Output</span></span> | <span data-ttu-id="85b6e-217">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-218">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-218">4</span></span> | <span data-ttu-id="85b6e-219">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="85b6e-220">Outputsecondmomenttensor</span><span class="sxs-lookup"><span data-stu-id="85b6e-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="85b6e-221">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="85b6e-221">Output</span></span> | <span data-ttu-id="85b6e-222">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="85b6e-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="85b6e-223">4</span><span class="sxs-lookup"><span data-stu-id="85b6e-223">4</span></span> | <span data-ttu-id="85b6e-224">Float32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="85b6e-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="85b6e-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85b6e-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="85b6e-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="85b6e-226">**Header**</span></span> | <span data-ttu-id="85b6e-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="85b6e-227">directml.h</span></span> |