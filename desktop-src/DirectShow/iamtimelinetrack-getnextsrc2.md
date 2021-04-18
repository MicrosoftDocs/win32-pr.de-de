---
description: 'Mit der GetNextSrc2-Methode wird der Titel nach der nächsten Quelle durchsucht, die zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht iamtimelinetrack:: getnexzrc, aber nimmt einen reftime-Wert an.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Iamtimelinetrack:: GetNextSrc2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352878"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="e2a5d-104">Iamtimelinetrack:: GetNextSrc2-Methode</span><span class="sxs-lookup"><span data-stu-id="e2a5d-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="e2a5d-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-105">\[Deprecated.</span></span> <span data-ttu-id="e2a5d-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e2a5d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e2a5d-107">Die- `GetNextSrc2` Methode durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="e2a5d-108">Diese Methode entspricht [**iamtimelinetrack:: getnexzrc**](iamtimelinetrack-getnextsrc.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a5d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a5d-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="e2a5d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2a5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2a5d-111">*ppsrc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2a5d-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2a5d-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e2a5d-113">*Pinout*</span><span class="sxs-lookup"><span data-stu-id="e2a5d-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="e2a5d-114">Enthält bei Eingabe die Startzeit für die Suche in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="e2a5d-115">Wenn die Methode eine Quelle abruft, wird der Wert auf die Endzeit der Quelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="e2a5d-116">Wenn die Methode keine Quelle abruft, wird der Wert ungültig, und die Anwendung sollte ihn nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2a5d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2a5d-117">Return value</span></span>

<span data-ttu-id="e2a5d-118">Gibt "s OK" zurück \_ , wenn die Methode eine Quelle abruft, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="e2a5d-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2a5d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2a5d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2a5d-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e2a5d-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e2a5d-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2a5d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2a5d-123">Requirements</span></span>



| <span data-ttu-id="e2a5d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2a5d-124">Requirement</span></span> | <span data-ttu-id="e2a5d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e2a5d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a5d-126">Header</span><span class="sxs-lookup"><span data-stu-id="e2a5d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2a5d-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e2a5d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e2a5d-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2a5d-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2a5d-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e2a5d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a5d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a5d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a5d-131">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2a5d-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="e2a5d-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e2a5d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




