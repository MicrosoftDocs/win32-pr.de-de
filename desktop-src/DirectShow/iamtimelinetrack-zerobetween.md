---
description: Die zerobetween-Methode entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten. Diese Methode teilt alle Objekte, die den angegebenen Zeitbereich überspannen, und entfernt die Teile, die innerhalb des Bereichs liegen.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'Iamtimelinetrack:: zerobetween-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bef669bae5e5e5c4c31a49b545fcfc7f58285f97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373655"
---
# <a name="iamtimelinetrackzerobetween-method"></a><span data-ttu-id="1f656-104">Iamtimelinetrack:: zerobetween-Methode</span><span class="sxs-lookup"><span data-stu-id="1f656-104">IAMTimelineTrack::ZeroBetween method</span></span>

> [!Note]  
> <span data-ttu-id="1f656-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1f656-105">\[Deprecated.</span></span> <span data-ttu-id="1f656-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1f656-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1f656-107">Die- `ZeroBetween` Methode entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten.</span><span class="sxs-lookup"><span data-stu-id="1f656-107">The `ZeroBetween` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="1f656-108">Diese Methode teilt alle Objekte, die den angegebenen Zeitbereich überspannen, und entfernt die Teile, die innerhalb des Bereichs liegen.</span><span class="sxs-lookup"><span data-stu-id="1f656-108">This method splits any objects that span the specified time range and removes the pieces that fall within the range.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f656-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f656-109">Syntax</span></span>


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="1f656-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f656-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f656-111">*rtstart*</span><span class="sxs-lookup"><span data-stu-id="1f656-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="1f656-112">Der Anfang des Bereichs, der gelöscht werden soll, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1f656-112">Beginning of the range to clear, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1f656-113">*rtend*</span><span class="sxs-lookup"><span data-stu-id="1f656-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1f656-114">Das Ende des Bereichs, der gelöscht werden soll, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1f656-114">End of the range to clear, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f656-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f656-115">Return value</span></span>

<span data-ttu-id="1f656-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1f656-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1f656-117">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="1f656-117">Possible values include the following.</span></span>



| <span data-ttu-id="1f656-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1f656-118">Return code</span></span>                                                                             | <span data-ttu-id="1f656-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f656-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1f656-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1f656-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1f656-121">Der Zeitbereich fällt über alle Elemente in der Spur hinaus.</span><span class="sxs-lookup"><span data-stu-id="1f656-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="1f656-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f656-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1f656-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1f656-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="1f656-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f656-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f656-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1f656-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1f656-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1f656-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1f656-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f656-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f656-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f656-128">Requirements</span></span>



| <span data-ttu-id="1f656-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f656-129">Requirement</span></span> | <span data-ttu-id="1f656-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1f656-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f656-131">Header</span><span class="sxs-lookup"><span data-stu-id="1f656-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1f656-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1f656-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1f656-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f656-133">Library</span></span><br/> | <dl> <span data-ttu-id="1f656-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1f656-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f656-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f656-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f656-136">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1f656-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="1f656-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="1f656-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




