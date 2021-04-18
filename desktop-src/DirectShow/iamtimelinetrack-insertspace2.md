---
description: 'Die InsertSpace2-Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein. Diese Methode entspricht iamtimelinetrack:: Insertspace, erfordert jedoch reftime-Werte.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Iamtimelinetrack:: InsertSpace2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364840"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="ebf81-104">Iamtimelinetrack:: InsertSpace2-Methode</span><span class="sxs-lookup"><span data-stu-id="ebf81-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="ebf81-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ebf81-105">\[Deprecated.</span></span> <span data-ttu-id="ebf81-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ebf81-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ebf81-107">Die `InsertSpace2` -Methode teilt alle-Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein.</span><span class="sxs-lookup"><span data-stu-id="ebf81-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="ebf81-108">Diese Methode entspricht [**iamtimelinetrack:: Insertspace**](iamtimelinetrack-insertspace.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="ebf81-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf81-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf81-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="ebf81-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebf81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf81-111">*rtstart*</span><span class="sxs-lookup"><span data-stu-id="ebf81-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf81-112">Der Zeitpunkt, zu dem die Aufteilung erstellt werden soll, und der Anfangspunkt des eingefügten Speicherplatzes (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="ebf81-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ebf81-113">*rtend*</span><span class="sxs-lookup"><span data-stu-id="ebf81-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf81-114">Endpunkt des eingefügten Raums in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ebf81-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf81-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebf81-115">Return value</span></span>

<span data-ttu-id="ebf81-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ebf81-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ebf81-117">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ebf81-117">Possible return values include the following:</span></span>



| <span data-ttu-id="ebf81-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ebf81-118">Return code</span></span>                                                                                   | <span data-ttu-id="ebf81-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebf81-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="ebf81-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ebf81-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="ebf81-121">Es sind keine Objekte zum angegebenen Zeitpunkt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ebf81-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="ebf81-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebf81-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ebf81-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ebf81-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ebf81-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ebf81-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ebf81-125">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="ebf81-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="ebf81-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ebf81-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ebf81-127">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ebf81-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ebf81-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebf81-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ebf81-129">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ebf81-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ebf81-130">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ebf81-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ebf81-131">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebf81-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ebf81-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebf81-132">Requirements</span></span>



| <span data-ttu-id="ebf81-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebf81-133">Requirement</span></span> | <span data-ttu-id="ebf81-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ebf81-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf81-135">Header</span><span class="sxs-lookup"><span data-stu-id="ebf81-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ebf81-136"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ebf81-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ebf81-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ebf81-137">Library</span></span><br/> | <dl> <span data-ttu-id="ebf81-138"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ebf81-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf81-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebf81-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf81-140">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ebf81-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="ebf81-141">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ebf81-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




