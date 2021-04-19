---
description: Die splicewithnext-Methode verbindet das Quell Objekt mit einem anderen Quell Objekt.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Iamtimelinesrc:: splicewithnext-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369962"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="7035b-103">Iamtimelinesrc:: splicewithnext-Methode</span><span class="sxs-lookup"><span data-stu-id="7035b-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="7035b-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7035b-104">\[Deprecated.</span></span> <span data-ttu-id="7035b-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7035b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7035b-106">Die- `SpliceWithNext` Methode verbindet das Quell Objekt mit einem anderen Quell Objekt.</span><span class="sxs-lookup"><span data-stu-id="7035b-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7035b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7035b-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="7035b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7035b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7035b-109">*pNext*</span><span class="sxs-lookup"><span data-stu-id="7035b-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="7035b-110">Ein Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts, das mit der aktuellen Quelle verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="7035b-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7035b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7035b-111">Return value</span></span>

<span data-ttu-id="7035b-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7035b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7035b-113">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="7035b-113">Possible return values include the following:</span></span>



| <span data-ttu-id="7035b-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7035b-114">Return code</span></span>                                                                                   | <span data-ttu-id="7035b-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7035b-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7035b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7035b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7035b-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7035b-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="7035b-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7035b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7035b-119">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="7035b-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="7035b-120"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="7035b-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="7035b-121">Das durch den *pNext* -Parameter angegebene Objekt ist kein Quell Objekt.</span><span class="sxs-lookup"><span data-stu-id="7035b-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="7035b-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7035b-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7035b-123">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="7035b-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="7035b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7035b-124">Remarks</span></span>

<span data-ttu-id="7035b-125">Wie momentan implementiert, verwirft diese Methode alle Auswirkungen auf *pNext*.</span><span class="sxs-lookup"><span data-stu-id="7035b-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="7035b-126">Damit diese Methode erfolgreich ausgeführt werden kann, muss *pNext* ein Übereinstimmungs Rahmen des aktuellen Quell Objekts sein, das wie folgt definiert wird:</span><span class="sxs-lookup"><span data-stu-id="7035b-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="7035b-127">Die gleiche Quelldatei muss gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="7035b-127">It must share the same source file.</span></span>
-   <span data-ttu-id="7035b-128">Die Start Zeit des Mediums muss der Medien Endzeit der aktuellen Quelle entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7035b-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="7035b-129">Die Wiedergabe Rate muss identisch sein.</span><span class="sxs-lookup"><span data-stu-id="7035b-129">The playback rate must be the same.</span></span> <span data-ttu-id="7035b-130">Die Wiedergabe Rate ist die Medien Dauer dividiert durch die Zeitachsen Dauer.</span><span class="sxs-lookup"><span data-stu-id="7035b-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="7035b-131">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7035b-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7035b-132">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7035b-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7035b-133">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7035b-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7035b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7035b-134">Requirements</span></span>



| <span data-ttu-id="7035b-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7035b-135">Requirement</span></span> | <span data-ttu-id="7035b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7035b-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7035b-137">Header</span><span class="sxs-lookup"><span data-stu-id="7035b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="7035b-138"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7035b-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7035b-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7035b-139">Library</span></span><br/> | <dl> <span data-ttu-id="7035b-140"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7035b-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7035b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7035b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7035b-142">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7035b-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="7035b-143">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7035b-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




