---
description: Die Insertspace-Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt zwischen Ihnen Leerzeichen ein.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Iamtimelinetrack:: Insertspace-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368323"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="3598d-103">Iamtimelinetrack:: Insertspace-Methode</span><span class="sxs-lookup"><span data-stu-id="3598d-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="3598d-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3598d-104">\[Deprecated.</span></span> <span data-ttu-id="3598d-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3598d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3598d-106">Die `InsertSpace` -Methode teilt alle-Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein.</span><span class="sxs-lookup"><span data-stu-id="3598d-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="3598d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3598d-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="3598d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3598d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3598d-109">*rtstart*</span><span class="sxs-lookup"><span data-stu-id="3598d-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3598d-110">Der Zeitpunkt, zu dem die Aufteilung erstellt werden soll, und der Anfangspunkt des eingefügten Leerraums in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="3598d-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3598d-111">*rtend*</span><span class="sxs-lookup"><span data-stu-id="3598d-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="3598d-112">Endpunkt des eingefügten Raums in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="3598d-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3598d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3598d-113">Return value</span></span>

<span data-ttu-id="3598d-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3598d-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3598d-115">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="3598d-115">Possible return values include the following:</span></span>



| <span data-ttu-id="3598d-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3598d-116">Return code</span></span>                                                                                   | <span data-ttu-id="3598d-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3598d-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="3598d-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3598d-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="3598d-119">Es sind keine Objekte zum angegebenen Zeitpunkt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3598d-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="3598d-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3598d-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3598d-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3598d-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3598d-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3598d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3598d-123">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="3598d-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="3598d-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3598d-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3598d-125">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3598d-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="3598d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3598d-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3598d-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3598d-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3598d-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="3598d-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3598d-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3598d-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3598d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3598d-130">Requirements</span></span>



| <span data-ttu-id="3598d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3598d-131">Requirement</span></span> | <span data-ttu-id="3598d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3598d-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3598d-133">Header</span><span class="sxs-lookup"><span data-stu-id="3598d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3598d-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3598d-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3598d-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3598d-135">Library</span></span><br/> | <dl> <span data-ttu-id="3598d-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="3598d-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3598d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3598d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3598d-138">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3598d-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="3598d-139">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="3598d-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




