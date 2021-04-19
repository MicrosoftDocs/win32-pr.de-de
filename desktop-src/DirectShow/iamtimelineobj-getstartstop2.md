---
description: 'Die GetStartStop2-Methode ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab. Diese Methode entspricht iamtimelineobj:: getstartstation, erfordert jedoch reftime-Werte.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Iamtimelineobj:: GetStartStop2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358047"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="19872-104">Iamtimelineobj:: GetStartStop2-Methode</span><span class="sxs-lookup"><span data-stu-id="19872-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="19872-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="19872-105">\[Deprecated.</span></span> <span data-ttu-id="19872-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="19872-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="19872-107">Die `GetStartStop2` -Methode ruft die Start-und Endzeit des Objekts relativ zum übergeordneten Element des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="19872-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="19872-108">Diese Methode entspricht [**iamtimelineobj:: getstartstation**](iamtimelineobj-getstartstop.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="19872-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="19872-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19872-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="19872-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19872-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19872-111">*PStart*</span><span class="sxs-lookup"><span data-stu-id="19872-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="19872-112">Empfängt die Startzeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="19872-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="19872-113">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="19872-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="19872-114">Empfängt die Endzeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="19872-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19872-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19872-115">Return value</span></span>

<span data-ttu-id="19872-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="19872-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19872-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19872-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19872-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19872-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="19872-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="19872-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="19872-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="19872-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="19872-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19872-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19872-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19872-122">Requirements</span></span>



| <span data-ttu-id="19872-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19872-123">Requirement</span></span> | <span data-ttu-id="19872-124">Wert</span><span class="sxs-lookup"><span data-stu-id="19872-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19872-125">Header</span><span class="sxs-lookup"><span data-stu-id="19872-125">Header</span></span><br/>  | <dl> <span data-ttu-id="19872-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="19872-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="19872-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19872-127">Library</span></span><br/> | <dl> <span data-ttu-id="19872-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="19872-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19872-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19872-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19872-130">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="19872-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="19872-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="19872-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




