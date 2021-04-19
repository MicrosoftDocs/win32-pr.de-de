---
description: Die getstartend-Methode ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Iamtimelineobj:: getstartstoppt-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360394"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="7b079-103">Iamtimelineobj:: getstartstoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="7b079-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="7b079-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7b079-104">\[Deprecated.</span></span> <span data-ttu-id="7b079-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7b079-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7b079-106">Die `GetStartStop` -Methode ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="7b079-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b079-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b079-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="7b079-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b079-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b079-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="7b079-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="7b079-110">Empfängt die Startzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="7b079-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="7b079-111">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="7b079-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="7b079-112">Empfängt die Endzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="7b079-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b079-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b079-113">Return value</span></span>

<span data-ttu-id="7b079-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7b079-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b079-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b079-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b079-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b079-116">Remarks</span></span>

<span data-ttu-id="7b079-117">Komposition, Gruppen und Spuren haben immer eine Startzeit von 0.</span><span class="sxs-lookup"><span data-stu-id="7b079-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="7b079-118">Während des Renderings rundet der die Start-und Endzeit eines Objekts auf die nächste Frame Grenze.</span><span class="sxs-lookup"><span data-stu-id="7b079-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="7b079-119">Allerdings werden die Zeiten des Objekts von der nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7b079-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="7b079-120">Wenn Sie die Gruppen Frame Rate ändern, werden die gerundeten Zeiten immer aus den ursprünglichen Zeiten berechnet.</span><span class="sxs-lookup"><span data-stu-id="7b079-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="7b079-121">Weitere Informationen finden Sie unter [DirectShow-Bearbeitungs Dienste](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="7b079-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="7b079-122">Um die Start-und Endzeiten im gerenderten Projekt zu bestimmen, übergeben Sie die von zurückgegebenen Werte `GetStartStop` an die [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7b079-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="7b079-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7b079-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b079-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7b079-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7b079-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b079-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b079-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b079-126">Requirements</span></span>



| <span data-ttu-id="7b079-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b079-127">Requirement</span></span> | <span data-ttu-id="7b079-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7b079-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b079-129">Header</span><span class="sxs-lookup"><span data-stu-id="7b079-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7b079-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7b079-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7b079-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b079-131">Library</span></span><br/> | <dl> <span data-ttu-id="7b079-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7b079-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b079-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b079-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b079-134">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7b079-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="7b079-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7b079-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




