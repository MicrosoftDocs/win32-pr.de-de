---
description: Die gettransattime-Methode ruft den Übergang, der dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'Iamtimelinetransable:: gettransattime-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373997"
---
# <a name="iamtimelinetransablegettransattime-method"></a><span data-ttu-id="32c0e-103">Iamtimelinetransable:: gettransattime-Methode</span><span class="sxs-lookup"><span data-stu-id="32c0e-103">IAMTimelineTransable::GetTransAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="32c0e-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="32c0e-104">\[Deprecated.</span></span> <span data-ttu-id="32c0e-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="32c0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="32c0e-106">Die- `GetTransAtTime` Methode ruft den Übergang, der dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.</span><span class="sxs-lookup"><span data-stu-id="32c0e-106">The `GetTransAtTime` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c0e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="32c0e-107">Syntax</span></span>


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="32c0e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32c0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c0e-109">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="32c0e-109">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32c0e-110">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Übergangs.</span><span class="sxs-lookup"><span data-stu-id="32c0e-110">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="32c0e-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="32c0e-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="32c0e-112">Der Zeitpunkt, ab dem mit der Suche begonnen werden soll, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="32c0e-112">Time from which to begin the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="32c0e-113">*Suchrichtung*</span><span class="sxs-lookup"><span data-stu-id="32c0e-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="32c0e-114">Member des [**dexterf- \_ \_ \_ Suchflags**](dexterf-track-search-flags.md) enumerierten Typs, der die begrenzungsbedingungen für die Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="32c0e-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c0e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32c0e-115">Return value</span></span>

<span data-ttu-id="32c0e-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="32c0e-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="32c0e-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="32c0e-117">Return code</span></span>                                                                                  | <span data-ttu-id="32c0e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32c0e-118">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="32c0e-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="32c0e-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="32c0e-120">Es wurde kein Übergang gefunden.</span><span class="sxs-lookup"><span data-stu-id="32c0e-120">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="32c0e-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32c0e-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="32c0e-122">Der Übergang wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="32c0e-122">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="32c0e-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="32c0e-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="32c0e-124">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="32c0e-124">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="32c0e-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="32c0e-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="32c0e-126">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="32c0e-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32c0e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32c0e-127">Remarks</span></span>

<span data-ttu-id="32c0e-128">Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="32c0e-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="32c0e-129">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="32c0e-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="32c0e-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="32c0e-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="32c0e-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="32c0e-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="32c0e-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32c0e-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="32c0e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32c0e-133">Requirements</span></span>



| <span data-ttu-id="32c0e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32c0e-134">Requirement</span></span> | <span data-ttu-id="32c0e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="32c0e-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32c0e-136">Header</span><span class="sxs-lookup"><span data-stu-id="32c0e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="32c0e-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="32c0e-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="32c0e-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32c0e-138">Library</span></span><br/> | <dl> <span data-ttu-id="32c0e-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="32c0e-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c0e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32c0e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c0e-141">**Iamtimelinetransable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="32c0e-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="32c0e-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="32c0e-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




