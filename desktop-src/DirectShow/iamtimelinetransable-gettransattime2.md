---
description: 'Die GetTransAtTime2-Methode ruft den Übergang, der dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab. Diese Methode entspricht iamtimelinetransable:: gettransattime, erfordert aber einen reftime-Parameter.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Iamtimelinetransable:: GetTransAtTime2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372487"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="87ffe-104">Iamtimelinetransable:: GetTransAtTime2-Methode</span><span class="sxs-lookup"><span data-stu-id="87ffe-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="87ffe-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="87ffe-105">\[Deprecated.</span></span> <span data-ttu-id="87ffe-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="87ffe-107">Die- `GetTransAtTime2` Methode ruft den Übergang, der dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.</span><span class="sxs-lookup"><span data-stu-id="87ffe-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="87ffe-108">Diese Methode entspricht [**iamtimelinetransable:: gettransattime**](iamtimelinetransable-gettransattime.md), erfordert aber einen [**reftime**](reftime.md) -Parameter.</span><span class="sxs-lookup"><span data-stu-id="87ffe-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ffe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="87ffe-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="87ffe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="87ffe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ffe-111">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Übergangs.</span><span class="sxs-lookup"><span data-stu-id="87ffe-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="87ffe-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="87ffe-114">Der Zeitpunkt, ab dem mit der Suche begonnen werden soll (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="87ffe-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-115">*Suchrichtung*</span><span class="sxs-lookup"><span data-stu-id="87ffe-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="87ffe-116">Member des [**dexterf- \_ \_ \_ Suchflags**](dexterf-track-search-flags.md) enumerierten Typs, der die begrenzungsbedingungen für die Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="87ffe-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ffe-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87ffe-117">Return value</span></span>

<span data-ttu-id="87ffe-118">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="87ffe-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="87ffe-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="87ffe-119">Return code</span></span>                                                                                  | <span data-ttu-id="87ffe-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87ffe-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="87ffe-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="87ffe-122">Es wurde kein Übergang gefunden.</span><span class="sxs-lookup"><span data-stu-id="87ffe-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="87ffe-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="87ffe-124">Der Übergang wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="87ffe-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="87ffe-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="87ffe-126">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="87ffe-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="87ffe-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="87ffe-128">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="87ffe-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87ffe-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87ffe-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87ffe-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="87ffe-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="87ffe-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="87ffe-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="87ffe-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="87ffe-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87ffe-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87ffe-133">Requirements</span></span>



| <span data-ttu-id="87ffe-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87ffe-134">Requirement</span></span> | <span data-ttu-id="87ffe-135">Wert</span><span class="sxs-lookup"><span data-stu-id="87ffe-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ffe-136">Header</span><span class="sxs-lookup"><span data-stu-id="87ffe-136">Header</span></span><br/>  | <dl> <span data-ttu-id="87ffe-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="87ffe-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87ffe-138">Library</span></span><br/> | <dl> <span data-ttu-id="87ffe-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ffe-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87ffe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ffe-141">**Iamtimelinetransable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="87ffe-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="87ffe-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="87ffe-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




