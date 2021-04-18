---
description: 'Die GetNextTrans2-Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht iamtimelinetransable:: getnexttrans, aber nimmt einen reftime-Wert an.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'Iamtimelinetransable:: GetNextTrans2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364526"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="fbf39-104">Iamtimelinetransable:: GetNextTrans2-Methode</span><span class="sxs-lookup"><span data-stu-id="fbf39-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="fbf39-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fbf39-105">\[Deprecated.</span></span> <span data-ttu-id="fbf39-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fbf39-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fbf39-107">Die- `GetNextTrans2` Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fbf39-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="fbf39-108">Diese Methode entspricht [**iamtimelinetransable:: getnexttrans**](iamtimelinetransable-getnexttrans.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="fbf39-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf39-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf39-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="fbf39-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbf39-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf39-111">*pptrans* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fbf39-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf39-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Übergangs Objekts.</span><span class="sxs-lookup"><span data-stu-id="fbf39-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="fbf39-113">*Pinout*</span><span class="sxs-lookup"><span data-stu-id="fbf39-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="fbf39-114">Ein Zeiger auf eine Variable, die die Zeit in Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="fbf39-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="fbf39-115">Bei der Eingabe gibt dieser Wert die Zeit an, nach der der Übergang gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbf39-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="fbf39-116">Bei der Ausgabe wird dieser Wert auf die Endzeit des Übergangs festgelegt, wenn ein Übergang abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fbf39-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf39-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbf39-117">Return value</span></span>

<span data-ttu-id="fbf39-118">Gibt s \_ OK zurück, wenn die Methode einen Übergang abruft, oder s \_ false, wenn kein Übergang gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="fbf39-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="fbf39-119">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="fbf39-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbf39-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbf39-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fbf39-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fbf39-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fbf39-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fbf39-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fbf39-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fbf39-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbf39-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf39-124">Requirements</span></span>



| <span data-ttu-id="fbf39-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf39-125">Requirement</span></span> | <span data-ttu-id="fbf39-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf39-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf39-127">Header</span><span class="sxs-lookup"><span data-stu-id="fbf39-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fbf39-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fbf39-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fbf39-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fbf39-129">Library</span></span><br/> | <dl> <span data-ttu-id="fbf39-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fbf39-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf39-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf39-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf39-132">**Iamtimelinetransable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fbf39-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="fbf39-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="fbf39-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




