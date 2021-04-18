---
description: Die Methode "*-wapinputs" gibt an, ob die Übergangs Eingaben ausgetauscht werden.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: Iamtimelinetrans::-Methode für die wapinputs-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371757"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="6d863-103">Iamtimelinetrans::-Methode für die wapinputs-Methode</span><span class="sxs-lookup"><span data-stu-id="6d863-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="6d863-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6d863-104">\[Deprecated.</span></span> <span data-ttu-id="6d863-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6d863-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d863-106">Die- `SetSwapInputs` Methode gibt an, ob die Übergangs Eingaben ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="6d863-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="6d863-107">Standardmäßig wird ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zu der Ebene, auf der sich der Übergang befindet, durchläuft.</span><span class="sxs-lookup"><span data-stu-id="6d863-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="6d863-108">Sie können diesen Fortschritt umkehren, sodass der Übergang von der Ebene, in der er sich wieder auf die Zusammensetzung der Ebenen mit niedrigerer Priorität befindet, erfolgt.</span><span class="sxs-lookup"><span data-stu-id="6d863-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="6d863-109">Weitere Informationen finden Sie unter [Übergangs Richtung](transition-direction.md).</span><span class="sxs-lookup"><span data-stu-id="6d863-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d863-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d863-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="6d863-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d863-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d863-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="6d863-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="6d863-113">Gibt an, ob die Eingaben ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="6d863-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="6d863-114">Wenn der Wert **false** ist, wird der Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Übergangs Ebene durchgegangen.</span><span class="sxs-lookup"><span data-stu-id="6d863-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="6d863-115">**True** gibt an, dass der Übergang in die entgegengesetzte Richtung verläuft.</span><span class="sxs-lookup"><span data-stu-id="6d863-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d863-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d863-116">Return value</span></span>

<span data-ttu-id="6d863-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6d863-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d863-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d863-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d863-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d863-119">Remarks</span></span>

<span data-ttu-id="6d863-120">Diese Methode ändert nicht die Richtung des visuellen Effekts.</span><span class="sxs-lookup"><span data-stu-id="6d863-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="6d863-121">Beispielsweise wird von links nach rechts die zurück Löschung von links nach rechts fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d863-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="6d863-122">Um die Richtung zu ändern, legen Sie **die Eigenschaft Status** mithilfe der [**ipropertysetter**](ipropertysetter.md) -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="6d863-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="6d863-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6d863-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d863-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="6d863-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6d863-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d863-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d863-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d863-126">Requirements</span></span>



| <span data-ttu-id="6d863-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d863-127">Requirement</span></span> | <span data-ttu-id="6d863-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6d863-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d863-129">Header</span><span class="sxs-lookup"><span data-stu-id="6d863-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6d863-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6d863-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6d863-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d863-131">Library</span></span><br/> | <dl> <span data-ttu-id="6d863-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="6d863-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d863-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d863-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d863-134">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6d863-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="6d863-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="6d863-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




