---
description: Die setcutsonly-Methode gibt an, ob der Übergang als Ausschneiden gerendert wird. Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf. Wenn eine Umstellung lange dauert, können Sie Sie als eine Ausschneide-und Geschwindigkeits Vorschau anzeigen.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Iamtimelinetrans:: setcutsonly-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367857"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="a17f9-105">Iamtimelinetrans:: setcutsonly-Methode</span><span class="sxs-lookup"><span data-stu-id="a17f9-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="a17f9-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a17f9-106">\[Deprecated.</span></span> <span data-ttu-id="a17f9-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a17f9-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a17f9-108">Die- `SetCutsOnly` Methode gibt an, ob der Übergang als Ausschneiden gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a17f9-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="a17f9-109">Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf.</span><span class="sxs-lookup"><span data-stu-id="a17f9-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="a17f9-110">Wenn eine Umstellung lange dauert, können Sie Sie als eine Ausschneide-und Geschwindigkeits Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a17f9-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17f9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a17f9-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="a17f9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a17f9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a17f9-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="a17f9-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="a17f9-114">Gibt an, ob der Übergang als Ausschneide gereinigen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a17f9-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="a17f9-115">**True** gibt an, dass der Übergang als sofortige Ausschneide gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a17f9-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="a17f9-116">**False** gibt an, dass der Übergang über seine normale Dauer gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a17f9-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a17f9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a17f9-117">Return value</span></span>

<span data-ttu-id="a17f9-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a17f9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a17f9-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a17f9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a17f9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a17f9-120">Remarks</span></span>

<span data-ttu-id="a17f9-121">Das Rendern eines Übergangs als Ausschneiden ist nicht kompatibel mit dem Austauschen der Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a17f9-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="a17f9-122">(Weitere Informationen finden Sie unter [**iamtimelinetrans:: sswapinputs**](iamtimelinetrans-setswapinputs.md).) Wenn Sie `SetCutsOnly` mit dem Wert **true** aufzurufen, wird die Einstellung "Setting- **wapinputs** " vorübergehend überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a17f9-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="a17f9-123">Die Einstellung nur für die Kürzung ist für die Vorschau vorgesehen. Daher hat diese Einschränkung keinen Einfluss auf die Dateiausgabe – vergessen Sie nicht, `SetCutsOnly` mit dem Wert **false** aufzurufen, bevor Sie die Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="a17f9-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="a17f9-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a17f9-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a17f9-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a17f9-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a17f9-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a17f9-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a17f9-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a17f9-127">Requirements</span></span>



| <span data-ttu-id="a17f9-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a17f9-128">Requirement</span></span> | <span data-ttu-id="a17f9-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a17f9-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a17f9-130">Header</span><span class="sxs-lookup"><span data-stu-id="a17f9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a17f9-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a17f9-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a17f9-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a17f9-132">Library</span></span><br/> | <dl> <span data-ttu-id="a17f9-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a17f9-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a17f9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a17f9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17f9-135">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a17f9-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="a17f9-136">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a17f9-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




