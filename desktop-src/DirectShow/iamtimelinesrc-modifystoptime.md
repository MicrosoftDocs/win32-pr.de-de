---
description: Die modifystoptime-Methode legt die Endzeit relativ zur Zeitachse fest.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'Iamtimelinesrc:: modifystoptime-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354792"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="d4542-103">Iamtimelinesrc:: modifystoptime-Methode</span><span class="sxs-lookup"><span data-stu-id="d4542-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="d4542-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4542-104">\[Deprecated.</span></span> <span data-ttu-id="d4542-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d4542-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4542-106">Die- `ModifyStopTime` Methode legt die Endzeit relativ zur Zeitachse fest.</span><span class="sxs-lookup"><span data-stu-id="d4542-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4542-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4542-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="d4542-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4542-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4542-109">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="d4542-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="d4542-110">Neue Endzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d4542-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4542-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4542-111">Return value</span></span>

<span data-ttu-id="d4542-112">Gibt S \_ OK oder E \_ invalidArg zurück, wenn die angegebene Zeit nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d4542-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4542-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4542-113">Remarks</span></span>

<span data-ttu-id="d4542-114">Diese Methode entspricht dem Aufrufen von [**iamtimelineobj:: setstartset**](iamtimelineobj-setstartstop.md) mit der ursprünglichen Startzeit und einer neuen Endzeit.</span><span class="sxs-lookup"><span data-stu-id="d4542-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="d4542-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d4542-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4542-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d4542-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d4542-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4542-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4542-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4542-118">Requirements</span></span>



| <span data-ttu-id="d4542-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4542-119">Requirement</span></span> | <span data-ttu-id="d4542-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d4542-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4542-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4542-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d4542-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d4542-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d4542-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4542-123">Library</span></span><br/> | <dl> <span data-ttu-id="d4542-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d4542-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4542-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4542-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4542-126">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d4542-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d4542-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="d4542-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




