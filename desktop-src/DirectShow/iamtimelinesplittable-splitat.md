---
description: Die splitat-Methode teilt das Objekt zum angegebenen Zeitpunkt.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Iamtimelinesplicustom:: splitat-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371610"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="65412-103">Iamtimelinesplicustom:: splitat-Methode</span><span class="sxs-lookup"><span data-stu-id="65412-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="65412-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="65412-104">\[Deprecated.</span></span> <span data-ttu-id="65412-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="65412-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65412-106">Die- `SplitAt` Methode teilt das Objekt zum angegebenen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="65412-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="65412-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="65412-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="65412-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="65412-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65412-109">*Time*</span><span class="sxs-lookup"><span data-stu-id="65412-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="65412-110">Der Zeitpunkt, an dem das Objekt in Relation zum Anfang der Zeitachse aufgeteilt werden soll, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="65412-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65412-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65412-111">Return value</span></span>

<span data-ttu-id="65412-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="65412-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="65412-113">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="65412-113">Possible values include the following:</span></span>



| <span data-ttu-id="65412-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="65412-114">Return code</span></span>                                                                                   | <span data-ttu-id="65412-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65412-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="65412-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="65412-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="65412-117">Nichts zu teilen.</span><span class="sxs-lookup"><span data-stu-id="65412-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="65412-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65412-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="65412-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="65412-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="65412-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="65412-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="65412-121">Das Objekt ist zu diesem Zeitpunkt nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="65412-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="65412-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="65412-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="65412-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="65412-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="65412-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65412-124">Remarks</span></span>

<span data-ttu-id="65412-125">Wenn Sie eine Quelle, einen Effekt oder einen Übergang aufteilen, erstellt diese Methode ein zweites Objekt desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="65412-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="65412-126">Das ursprüngliche-Objekt wird zur angegebenen Teilzeit abgeschnitten, und das neue-Objekt ersetzt den abgeschnittene Teil.</span><span class="sxs-lookup"><span data-stu-id="65412-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="65412-127">Das neue-Objekt erbt alle gleichen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="65412-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="65412-128">In einem-Quell Objekt teilt die-Methode auch alle Effekte, die auf die geteilte Zeit fallen.</span><span class="sxs-lookup"><span data-stu-id="65412-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="65412-129">Wenn Sie diese Methode für einen Track aufrufen, werden alle Quellen, Effekte und Übergänge, die in der Spur enthalten sind, zur angegebenen Teilzeit aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="65412-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="65412-130">Es wird keine zweite Spur erstellt. (Ein Track beginnt bei der Zeit NULL und erstreckt sich auf unendlich.)</span><span class="sxs-lookup"><span data-stu-id="65412-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="65412-131">Bei einer Nachverfolgung gibt die Methode den Wert "false" zurück, wenn die Teilzeit nach dem Zeitpunkt der Nachverfolgung liegt \_ .</span><span class="sxs-lookup"><span data-stu-id="65412-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="65412-132">Wenn die Split-Zeit für ein beliebiges anderes Objekt nicht innerhalb des Objekts liegt, gibt die Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="65412-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="65412-133">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="65412-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65412-134">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="65412-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65412-135">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65412-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65412-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65412-136">Requirements</span></span>



| <span data-ttu-id="65412-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65412-137">Requirement</span></span> | <span data-ttu-id="65412-138">Wert</span><span class="sxs-lookup"><span data-stu-id="65412-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65412-139">Header</span><span class="sxs-lookup"><span data-stu-id="65412-139">Header</span></span><br/>  | <dl> <span data-ttu-id="65412-140"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="65412-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65412-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65412-141">Library</span></span><br/> | <dl> <span data-ttu-id="65412-142"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="65412-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65412-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65412-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65412-144">**Iamtimelinesplicustom-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="65412-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="65412-145">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="65412-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




