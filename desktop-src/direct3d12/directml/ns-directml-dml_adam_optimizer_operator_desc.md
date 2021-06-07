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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417778"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="d8d43-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC-Struktur (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d8d43-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d8d43-105">Berechnet aktualisierte Gewichtungen (Parameter) mithilfe der angegebenen Farbverläufe basierend auf dem Adam-Algorithmus **(ADA** ptive **M** oment estimation).</span><span class="sxs-lookup"><span data-stu-id="d8d43-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="d8d43-106">Dieser Operator ist ein Optimierer und wird in der Regel im Schritt der Gewichtungsaktualisierung einer Trainingsschleife verwendet, um einen Gradientenabstieg durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="d8d43-107">Dieser Operator führt die folgende Berechnung aus:</span><span class="sxs-lookup"><span data-stu-id="d8d43-107">This operator performs the following computation:</span></span>

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

<span data-ttu-id="d8d43-108">Zusätzlich zum Berechnen der aktualisierten Gewichtungsparameter (zurückgegeben in *OutputParametersTensor)* gibt dieser Operator auch die aktualisierten Schätzungen des ersten und zweiten Moments in *OutputFirstMomentTensor* bzw. *OutputSecondMomentTensor* zurück.</span><span class="sxs-lookup"><span data-stu-id="d8d43-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="d8d43-109">In der Regel sollten Sie diese Schätzungen für den ersten und zweiten Moment speichern und sie während des nachfolgenden Trainingsschritts als Eingaben bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8d43-110">Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="d8d43-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d8d43-111">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d8d43-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d43-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8d43-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="d8d43-113">Member</span><span class="sxs-lookup"><span data-stu-id="d8d43-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="d8d43-114">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-115">Ein Tensor, der die Parameter (Gewichtungen) enthält, auf die dieser Optimierer angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8d43-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="d8d43-116">Die Schätzwerte für den Farbverlauf, den ersten und zweiten Moment, den aktuellen Trainingsschritt sowie die Hyperparameter *LearningRate,* *Beta1* und *Beta2* werden von diesem Operator verwendet, um den Gradientenabstieg für die gewichtigen Werte durchzuführen, die in diesem Tensor angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d8d43-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="d8d43-117">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-118">Ein Tensor, der die Schätzung des Farbverlaufs des ersten Moments für jeden Gewichtungswert enthält.</span><span class="sxs-lookup"><span data-stu-id="d8d43-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="d8d43-119">Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über *outputFirstMomentTensor* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="d8d43-120">Beim erstmaligen Anwenden dieses Optimierers auf eine Gruppe von Gewichtungen (z. B. während des ersten Trainingsschritts) sollten die Werte dieses Tensors in der Regel mit 0 (null) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8d43-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="d8d43-121">Nachfolgende Ausführungen sollten die in *OutputFirstMomentTensor zurückgegebenen* Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8d43-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="d8d43-122">Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="d8d43-123">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-124">Ein Tensor, der die Schätzung des Farbverlaufs im zweiten Moment für jeden Gewichtungswert enthält.</span><span class="sxs-lookup"><span data-stu-id="d8d43-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="d8d43-125">Diese Werte werden in der Regel als Ergebnis einer vorherigen Ausführung dieses Operators über *outputSecondMomentTensor* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="d8d43-126">Beim erstmaligen Anwenden dieses Optimierers auf eine Gruppe von Gewichtungen (z. B. während des ersten Trainingsschritts) sollten die Werte dieses Tensors in der Regel mit 0 (null) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8d43-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="d8d43-127">Nachfolgende Ausführungen sollten die in *OutputSecondMomentTensor zurückgegebenen* Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8d43-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="d8d43-128">Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="d8d43-129">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-130">Die Farbverläufe, die auf die Eingabeparameter (Gewichtungen) für den Gradientenabstieg angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="d8d43-131">Farbverläufe werden in der Regel während des Trainings in einem Rückpropagierungsdurchlauf abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="d8d43-132">Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="d8d43-133">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-134">Ein skalarer Tensor, der einen einzelnen ganzzahligen Wert enthält, der die aktuelle Anzahl von Trainingsschritten darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8d43-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="d8d43-135">Dieser Wert wird zusammen mit *Beta1* und *Beta2* verwendet, um den exponentiellen Verfall der Geschätzten Tensoren des ersten und zweiten Moments zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="d8d43-136">In der Regel beginnt der Wert des Trainingsschritts bei 0 zu Beginn des Trainings und wird bei jedem nachfolgenden Trainingsschritt um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="d8d43-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="d8d43-137">Dieser Operator aktualisiert den Wert des Trainingsschritts nicht. Sie sollten dies manuell durchführen, z. B. mit [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="d8d43-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="d8d43-138">Dieser Tensor muss ein Skalar (d. h. alle *Größen* gleich 1) sein und den Datentyp [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="d8d43-139">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-140">Ein Ausgabe-Tensor, der die aktualisierten Parameterwerte (Gewichtung) enthält, nachdem der Gradientenabstieg angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d8d43-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="d8d43-141">Während der Bindung ist dieser Tensor berechtigt, einen geeigneten Eingabe-Tensor als Alias zu verwenden, der zum Ausführen eines direkt aktualisierten Tensors verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8d43-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="d8d43-142">Weitere Informationen finden Sie im Abschnitt ["Hinweise".](#remarks)</span><span class="sxs-lookup"><span data-stu-id="d8d43-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="d8d43-143">Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="d8d43-144">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-145">Ein Ausgabe-Tensor, der aktualisierte Schätzungen des ersten Moments enthält.</span><span class="sxs-lookup"><span data-stu-id="d8d43-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="d8d43-146">Sie sollten die Werte dieses Tensors speichern und während des nachfolgenden Trainingsschritts in *InputFirstMomentTensor* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="d8d43-147">Während der Bindung ist dieser Tensor berechtigt, einen geeigneten Eingabe-Tensor als Alias zu verwenden, der zum Ausführen eines direkt aktualisierten Tensors verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8d43-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="d8d43-148">Weitere Informationen finden Sie im Abschnitt ["Hinweise".](#remarks)</span><span class="sxs-lookup"><span data-stu-id="d8d43-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="d8d43-149">Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="d8d43-150">Typ: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d8d43-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d8d43-151">Ein Ausgabe-Tensor, der aktualisierte Schätzungen des zweiten Moments enthält.</span><span class="sxs-lookup"><span data-stu-id="d8d43-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="d8d43-152">Sie sollten die Werte dieses Tensors speichern und während des nachfolgenden Trainingsschritts in *InputSecondMomentTensor* bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="d8d43-153">Während der Bindung ist dieser Tensor berechtigt, einen geeigneten Eingabe-Tensor als Alias zu verwenden, der zum Ausführen eines direkt aktualisierten Tensors verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8d43-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="d8d43-154">Weitere Informationen finden Sie im Abschnitt ["Hinweise".](#remarks)</span><span class="sxs-lookup"><span data-stu-id="d8d43-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="d8d43-155">Die *Größen* und *der Datentyp* dieses Tensors müssen genau mit denen des *InputParametersTensor* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="d8d43-156">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d8d43-156">Type: **float**</span></span>

<span data-ttu-id="d8d43-157">Die Lernrate, die auch häufig als *Schrittgröße* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d8d43-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="d8d43-158">Die Lernrate ist ein Hyperparameter, der die Größe der Gewichtungsaktualisierung entlang des Farbverlaufsvektors für jeden Trainingsschritt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d8d43-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="d8d43-159">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d8d43-159">Type: **float**</span></span>

<span data-ttu-id="d8d43-160">Ein Hyperparameter, der die exponentielle Verfallsrate der Schätzung des ersten Moments des Farbverlaufs darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8d43-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="d8d43-161">Dieser Wert sollte zwischen 0,0 und 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="d8d43-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="d8d43-162">Ein Wert von 0,9f ist typisch.</span><span class="sxs-lookup"><span data-stu-id="d8d43-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="d8d43-163">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d8d43-163">Type: **float**</span></span>

<span data-ttu-id="d8d43-164">Ein Hyperparameter, der die exponentielle Verfallsrate der Schätzung des zweiten Moments des Farbverlaufs darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8d43-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="d8d43-165">Dieser Wert sollte zwischen 0,0 und 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="d8d43-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="d8d43-166">Ein Wert von 0,999f ist typisch.</span><span class="sxs-lookup"><span data-stu-id="d8d43-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="d8d43-167">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d8d43-167">Type: **float**</span></span>

<span data-ttu-id="d8d43-168">Ein kleiner Wert, der zur Unterstützung der numerischen Stabilität verwendet wird, indem Division durch Null verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="d8d43-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="d8d43-169">Für 32-Bit-Gleitkommaeingaben umfassen typische Werte 1e-8 oder `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="d8d43-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d43-170">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d8d43-170">Remarks</span></span>
<span data-ttu-id="d8d43-171">Dieser Operator unterstützt die direkt ausgeführte Ausführung, was bedeutet, dass jeder Ausgabe-Tensor während der Bindung ein Alias für einen geeigneten Eingabe-Tensor sein darf.</span><span class="sxs-lookup"><span data-stu-id="d8d43-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="d8d43-172">Beispielsweise ist es möglich, die gleiche Ressource sowohl für *InputParametersTensor* als auch für *OutputParametersTensor* zu binden, um effektiv eine aktuelle Aktualisierung der Eingabeparameter zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="d8d43-173">Alle Eingabe-Tensoren dieses Operators, mit Ausnahme von *TrainingStepTensor,* können auf diese Weise als Alias verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8d43-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="d8d43-174">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="d8d43-174">Availability</span></span>
<span data-ttu-id="d8d43-175">Dieser Operator wurde in `DML_FEATURE_LEVEL_3_0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d8d43-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d8d43-176">Tensoreinschränkungen</span><span class="sxs-lookup"><span data-stu-id="d8d43-176">Tensor constraints</span></span>
* <span data-ttu-id="d8d43-177">*GradientTensor,* *InputFirstMomentTensor,* *InputParametersTensor,* *InputSecondMomentTensor,* *OutputFirstMomentTensor,* *OutputParametersTensor,* *OutputSecondMomentTensor* und *TrainingStepTensor* müssen den gleichen *Datentyp* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="d8d43-178">*GradientTensor,* *InputFirstMomentTensor,* *InputParametersTensor,* *InputSecondMomentTensor,* *OutputFirstMomentTensor,* *OutputParametersTensor* und *OutputSecondMomentTensor* müssen die gleichen *Größen* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8d43-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d8d43-179">Tensor-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d8d43-179">Tensor support</span></span>
| <span data-ttu-id="d8d43-180">Tensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-180">Tensor</span></span> | <span data-ttu-id="d8d43-181">Typ</span><span class="sxs-lookup"><span data-stu-id="d8d43-181">Kind</span></span> | <span data-ttu-id="d8d43-182">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="d8d43-182">Dimensions</span></span> | <span data-ttu-id="d8d43-183">Unterstützte Dimensionsanzahlen</span><span class="sxs-lookup"><span data-stu-id="d8d43-183">Supported dimension counts</span></span> | <span data-ttu-id="d8d43-184">Unterstützte Datentypen</span><span class="sxs-lookup"><span data-stu-id="d8d43-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="d8d43-185">InputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-185">InputParametersTensor</span></span> | <span data-ttu-id="d8d43-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-186">Input</span></span> | <span data-ttu-id="d8d43-187">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-188">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-188">4</span></span> | <span data-ttu-id="d8d43-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-190">InputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="d8d43-191">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-191">Input</span></span> | <span data-ttu-id="d8d43-192">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-193">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-193">4</span></span> | <span data-ttu-id="d8d43-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-195">InputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="d8d43-196">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-196">Input</span></span> | <span data-ttu-id="d8d43-197">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-198">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-198">4</span></span> | <span data-ttu-id="d8d43-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-200">GradientTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-200">GradientTensor</span></span> | <span data-ttu-id="d8d43-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-201">Input</span></span> | <span data-ttu-id="d8d43-202">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-203">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-203">4</span></span> | <span data-ttu-id="d8d43-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-205">TrainingStepTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-205">TrainingStepTensor</span></span> | <span data-ttu-id="d8d43-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-206">Input</span></span> | <span data-ttu-id="d8d43-207">{ 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="d8d43-208">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-208">4</span></span> | <span data-ttu-id="d8d43-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-210">OutputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-210">OutputParametersTensor</span></span> | <span data-ttu-id="d8d43-211">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-211">Output</span></span> | <span data-ttu-id="d8d43-212">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-213">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-213">4</span></span> | <span data-ttu-id="d8d43-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-215">OutputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="d8d43-216">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-216">Output</span></span> | <span data-ttu-id="d8d43-217">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-218">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-218">4</span></span> | <span data-ttu-id="d8d43-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d8d43-220">OutputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="d8d43-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="d8d43-221">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="d8d43-221">Output</span></span> | <span data-ttu-id="d8d43-222">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="d8d43-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="d8d43-223">4</span><span class="sxs-lookup"><span data-stu-id="d8d43-223">4</span></span> | <span data-ttu-id="d8d43-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d8d43-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="d8d43-225">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d8d43-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d8d43-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="d8d43-226">**Header**</span></span> | <span data-ttu-id="d8d43-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="d8d43-227">directml.h</span></span> |