---
description: 'Die GetSrcAtTime2-Methode ruft das Quell Objekt, das dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab. Diese Methode entspricht iamtimelinetrack:: gezrtortime, aber nimmt einen reftime-Wert an.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'Iamtimelinetrack:: GetSrcAtTime2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369987"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="809c6-104">Iamtimelinetrack:: GetSrcAtTime2-Methode</span><span class="sxs-lookup"><span data-stu-id="809c6-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="809c6-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="809c6-105">\[Deprecated.</span></span> <span data-ttu-id="809c6-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="809c6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="809c6-107">Die- `GetSrcAtTime2` Methode ruft das Quell Objekt, das dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.</span><span class="sxs-lookup"><span data-stu-id="809c6-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="809c6-108">Diese Methode entspricht [**iamtimelinetrack:: gezrtortime**](iamtimelinetrack-getsrcattime.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="809c6-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="809c6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="809c6-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="809c6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="809c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="809c6-111">*ppsrc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="809c6-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="809c6-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="809c6-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="809c6-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="809c6-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="809c6-114">Startzeit für die Suche in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="809c6-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="809c6-115">*Suchrichtung*</span><span class="sxs-lookup"><span data-stu-id="809c6-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="809c6-116">Member des [**dexterf- \_ \_ \_ Suchflags**](dexterf-track-search-flags.md) enumerierten Typs, der die begrenzungsbedingungen für die Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="809c6-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="809c6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809c6-117">Return value</span></span>

<span data-ttu-id="809c6-118">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="809c6-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="809c6-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="809c6-119">Return code</span></span>                                                                                  | <span data-ttu-id="809c6-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809c6-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="809c6-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="809c6-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="809c6-122">Es wurde kein Quell Objekt gefunden.</span><span class="sxs-lookup"><span data-stu-id="809c6-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="809c6-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="809c6-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="809c6-124">Ein Quell Objekt gefunden.</span><span class="sxs-lookup"><span data-stu-id="809c6-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="809c6-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="809c6-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="809c6-126">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="809c6-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="809c6-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="809c6-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="809c6-128">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="809c6-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="809c6-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="809c6-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="809c6-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="809c6-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="809c6-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="809c6-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="809c6-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="809c6-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="809c6-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="809c6-133">Requirements</span></span>



| <span data-ttu-id="809c6-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="809c6-134">Requirement</span></span> | <span data-ttu-id="809c6-135">Wert</span><span class="sxs-lookup"><span data-stu-id="809c6-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="809c6-136">Header</span><span class="sxs-lookup"><span data-stu-id="809c6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="809c6-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="809c6-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="809c6-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="809c6-138">Library</span></span><br/> | <dl> <span data-ttu-id="809c6-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="809c6-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="809c6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="809c6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809c6-141">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="809c6-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="809c6-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="809c6-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




