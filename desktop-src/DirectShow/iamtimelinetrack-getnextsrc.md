---
description: Mit der getnexzrc-Methode wird der Titel nach der nächsten Quelle durchsucht, die zum angegebenen Zeitpunkt oder später angezeigt wird.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Iamtimelinetrack:: getnextrc-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364820"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="2228a-103">Iamtimelinetrack:: getnexzrc-Methode</span><span class="sxs-lookup"><span data-stu-id="2228a-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="2228a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2228a-104">\[Deprecated.</span></span> <span data-ttu-id="2228a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="2228a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2228a-106">Die- `GetNextSrc` Methode durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2228a-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="2228a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2228a-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="2228a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2228a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2228a-109">*ppsrc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2228a-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2228a-110">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="2228a-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2228a-111">*Pinout*</span><span class="sxs-lookup"><span data-stu-id="2228a-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="2228a-112">Ein Zeiger auf eine Variable, die die Startzeit für die Suche enthält, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="2228a-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="2228a-113">Wenn die Methode eine Quelle abruft, wird der Wert auf die Endzeit der Quelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2228a-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="2228a-114">Wenn die Methode keine Quelle abruft, wird der Wert ungültig, und die Anwendung sollte ihn nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="2228a-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2228a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2228a-115">Return value</span></span>

<span data-ttu-id="2228a-116">Gibt "s OK" zurück \_ , wenn die Methode eine Quelle abruft, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="2228a-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2228a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2228a-117">Remarks</span></span>

<span data-ttu-id="2228a-118">Wenn die durch *Pinout* angegebene Zeit zwischen den Start-und Endzeiten einer Quelle liegt, ruft die Methode diese Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="2228a-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="2228a-119">Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="2228a-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="2228a-120">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="2228a-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="2228a-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2228a-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2228a-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="2228a-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2228a-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2228a-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2228a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2228a-124">Requirements</span></span>



| <span data-ttu-id="2228a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2228a-125">Requirement</span></span> | <span data-ttu-id="2228a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2228a-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2228a-127">Header</span><span class="sxs-lookup"><span data-stu-id="2228a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2228a-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2228a-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2228a-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2228a-129">Library</span></span><br/> | <dl> <span data-ttu-id="2228a-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="2228a-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2228a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2228a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2228a-132">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2228a-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="2228a-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="2228a-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




