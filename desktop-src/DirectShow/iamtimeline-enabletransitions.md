---
description: Die enabletransitions-Methode aktiviert oder deaktiviert alle Übergänge in der Zeitachse.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Iamtimeline:: enabletransitions-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372327"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="c32a4-103">Iamtimeline:: enabletransitions-Methode</span><span class="sxs-lookup"><span data-stu-id="c32a4-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="c32a4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c32a4-104">\[Deprecated.</span></span> <span data-ttu-id="c32a4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c32a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c32a4-106">Die- `EnableTransitions` Methode aktiviert oder deaktiviert alle Übergänge in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="c32a4-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="c32a4-107">Wenn Übergänge deaktiviert sind, werden Sie von den Rendering-Engines als Schnitte behandelt. Das heißt, die gerenderte Ausgabe springt sofort von einem Track zum nächsten.</span><span class="sxs-lookup"><span data-stu-id="c32a4-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="c32a4-108">Der Standard Ausschneide Punkt liegt in der Mitte der Übergangs Dauer.</span><span class="sxs-lookup"><span data-stu-id="c32a4-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="c32a4-109">Sie können den Ausschneide Punkt ändern, indem Sie die [**iamtimelinetrans:: setcutpoint**](iamtimelinetrans-setcutpoint.md) -Methode für den Übergang aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c32a4-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="c32a4-110">Deaktivierte Übergänge werden nicht aus der Zeitachse entfernt.</span><span class="sxs-lookup"><span data-stu-id="c32a4-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="c32a4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c32a4-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="c32a4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c32a4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32a4-113">*fenabled*</span><span class="sxs-lookup"><span data-stu-id="c32a4-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="c32a4-114">Boolescher Wert, der angibt, ob Übergänge aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c32a4-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="c32a4-115">**True** gibt an, dass Übergänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c32a4-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="c32a4-116">Der Wert **false** gibt an, dass Übergänge deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c32a4-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32a4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c32a4-117">Return value</span></span>

<span data-ttu-id="c32a4-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c32a4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c32a4-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c32a4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32a4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c32a4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c32a4-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c32a4-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c32a4-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c32a4-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c32a4-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c32a4-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c32a4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c32a4-124">Requirements</span></span>



| <span data-ttu-id="c32a4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c32a4-125">Requirement</span></span> | <span data-ttu-id="c32a4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c32a4-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c32a4-127">Header</span><span class="sxs-lookup"><span data-stu-id="c32a4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c32a4-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c32a4-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c32a4-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c32a4-129">Library</span></span><br/> | <dl> <span data-ttu-id="c32a4-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c32a4-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32a4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c32a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32a4-132">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c32a4-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c32a4-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c32a4-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




