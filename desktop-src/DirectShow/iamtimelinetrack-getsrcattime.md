---
description: Die gezr| Time-Methode ruft das Quell Objekt ab, das dem angegebenen Zeitpunkt gemäß den angegebenen begrenzungsbedingungen am nächsten liegt.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'Iamtimelinetrack:: gezr| Time-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365960"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a><span data-ttu-id="e5772-103">Iamtimelinetrack:: gezr| Time-Methode</span><span class="sxs-lookup"><span data-stu-id="e5772-103">IAMTimelineTrack::GetSrcAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="e5772-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e5772-104">\[Deprecated.</span></span> <span data-ttu-id="e5772-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e5772-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e5772-106">Die- `GetSrcAtTime` Methode ruft das Quell Objekt, das dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.</span><span class="sxs-lookup"><span data-stu-id="e5772-106">The `GetSrcAtTime` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5772-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5772-107">Syntax</span></span>


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="e5772-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5772-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5772-109">*ppsrc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e5772-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5772-110">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="e5772-110">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="e5772-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="e5772-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="e5772-112">Startzeit für die Suche in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="e5772-112">Start time for the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e5772-113">*Suchrichtung*</span><span class="sxs-lookup"><span data-stu-id="e5772-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="e5772-114">Member des [**dexterf- \_ \_ \_ Suchflags**](dexterf-track-search-flags.md) enumerierten Typs, der die begrenzungsbedingungen für die Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="e5772-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5772-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5772-115">Return value</span></span>

<span data-ttu-id="e5772-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="e5772-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e5772-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e5772-117">Return code</span></span>                                                                                  | <span data-ttu-id="e5772-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5772-118">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="e5772-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e5772-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="e5772-120">Es wurde kein Quell Objekt gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5772-120">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="e5772-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5772-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e5772-122">Ein Quell Objekt gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5772-122">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="e5772-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e5772-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e5772-124">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="e5772-124">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="e5772-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e5772-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e5772-126">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="e5772-126">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e5772-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5772-127">Remarks</span></span>

<span data-ttu-id="e5772-128">Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="e5772-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="e5772-129">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="e5772-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e5772-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e5772-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e5772-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e5772-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e5772-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5772-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5772-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5772-133">Requirements</span></span>



| <span data-ttu-id="e5772-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5772-134">Requirement</span></span> | <span data-ttu-id="e5772-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e5772-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5772-136">Header</span><span class="sxs-lookup"><span data-stu-id="e5772-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e5772-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e5772-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e5772-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5772-138">Library</span></span><br/> | <dl> <span data-ttu-id="e5772-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e5772-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5772-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5772-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5772-141">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e5772-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="e5772-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e5772-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




