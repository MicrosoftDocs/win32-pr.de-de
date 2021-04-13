---
title: Idcompositionmatrixtransform setmatrixelement (int, int, idcompositionanimation)-Methode
description: Animiert den Wert eines Elements der Matrix dieser 2D-Transformation.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Setmatrixelement-Methode directcomposition
- Setmatrixelement-Methode directcomposition, idcompositionmatrixtransform-Schnittstelle
- Idcompositionmatrixtransform-Schnittstelle directcomposition, setmatrixelement-Methode
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390750"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="aceb6-106">Idcompositionmatrixtransform:: setmatrixelement (int, int, idcompositionanimation \* )-Methode</span><span class="sxs-lookup"><span data-stu-id="aceb6-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="aceb6-107">Animiert den Wert eines Elements der Matrix dieser 2D-Transformation.</span><span class="sxs-lookup"><span data-stu-id="aceb6-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="aceb6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aceb6-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="aceb6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aceb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aceb6-110">*Zeile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aceb6-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aceb6-111">Der Zeilen Index des Elements, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aceb6-111">The row index of the element to change.</span></span> <span data-ttu-id="aceb6-112">Dieser Wert muss zwischen 0 und 2 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="aceb6-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="aceb6-113">*Spalte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aceb6-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aceb6-114">Der Spalten Index des Elements, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aceb6-114">The column index of the element to change.</span></span> <span data-ttu-id="aceb6-115">Dieser Wert muss zwischen 0 und 1 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="aceb6-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="aceb6-116">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aceb6-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aceb6-117">Eine Animation, die darstellt, wie sich der Wert des angegebenen Elements im Laufe der Zeit ändert.</span><span class="sxs-lookup"><span data-stu-id="aceb6-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="aceb6-118">Dieser Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="aceb6-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aceb6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aceb6-119">Return value</span></span>

<span data-ttu-id="aceb6-120">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="aceb6-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="aceb6-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aceb6-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="aceb6-122">Eine Liste der Fehlercodes finden Sie unter [directcomposition-Fehlercodes](directcomposition-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="aceb6-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="aceb6-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aceb6-123">Remarks</span></span>

<span data-ttu-id="aceb6-124">Diese Methode erstellt eine Kopie der angegebenen Animation.</span><span class="sxs-lookup"><span data-stu-id="aceb6-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="aceb6-125">Wenn das Objekt, auf das der *Animations* Parameter verweist, nach dem Aufrufen dieser Methode geändert wird, wirkt sich die Änderung nicht auf das Element aus, es sei denn, diese Methode wird erneut aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aceb6-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="aceb6-126">Wenn das Element zuvor animiert wurde, ersetzt das Aufrufen dieser Methode die vorherige Animation durch die neue Animation.</span><span class="sxs-lookup"><span data-stu-id="aceb6-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="aceb6-127">Diese Methode schlägt fehl, wenn *Animation* ein ungültiger Zeiger ist oder wenn Sie nicht von derselben [**idcompositiondevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) -Schnittstelle wie die betroffene Transformation erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="aceb6-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="aceb6-128">Die Schnittstelle kann keine benutzerdefinierte Implementierung sein. mit dieser Methode können nur Schnittstellen verwendet werden, die von Microsoft directcomposition erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="aceb6-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="aceb6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aceb6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aceb6-130">**Idcompositionmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="aceb6-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 