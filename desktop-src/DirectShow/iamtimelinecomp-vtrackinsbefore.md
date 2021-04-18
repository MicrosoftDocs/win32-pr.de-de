---
description: Die vtrackinsbefore-Methode fügt eine virtuelle Spur mit der angegebenen Priorität in die Komposition ein.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Iamtimelinecomp:: vtrackinsbefore-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354755"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="ac975-103">Iamtimelinecomp:: vtrackinsbefore-Methode</span><span class="sxs-lookup"><span data-stu-id="ac975-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="ac975-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ac975-104">\[Deprecated.</span></span> <span data-ttu-id="ac975-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ac975-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ac975-106">Die- `VTrackInsBefore` Methode fügt eine virtuelle Spur mit der angegebenen Priorität in die Komposition ein.</span><span class="sxs-lookup"><span data-stu-id="ac975-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac975-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac975-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="ac975-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac975-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac975-109">*pvirtualtrack*</span><span class="sxs-lookup"><span data-stu-id="ac975-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="ac975-110">Ein Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des virtuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="ac975-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="ac975-111">*Priority*</span><span class="sxs-lookup"><span data-stu-id="ac975-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="ac975-112">Die Priorität, mit der der virtuelle Track eingefügt werden soll, oder – 1, um den virtuellen Titel am Ende der Prioritäts Liste einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ac975-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="ac975-113">Die Prioritäts Liste bestimmt, welche Clips sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="ac975-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="ac975-114">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ac975-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac975-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac975-115">Return value</span></span>

<span data-ttu-id="ac975-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="ac975-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ac975-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac975-117">Return code</span></span>                                                                                   | <span data-ttu-id="ac975-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac975-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ac975-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac975-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ac975-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ac975-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ac975-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ac975-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ac975-122">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="ac975-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="ac975-123"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="ac975-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="ac975-124">Das Objekt ist kein virtueller Titel.</span><span class="sxs-lookup"><span data-stu-id="ac975-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac975-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac975-125">Remarks</span></span>

<span data-ttu-id="ac975-126">Jeder virtuelle Titel in der Komposition verfügt über eine eindeutige Prioritätsstufe.</span><span class="sxs-lookup"><span data-stu-id="ac975-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="ac975-127">Die Prioritätsstufen liegen zwischen 0 und *n* -1, wobei *n* die Anzahl der virtuellen Spuren in der Komposition ist.</span><span class="sxs-lookup"><span data-stu-id="ac975-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="ac975-128">Bei Video Gruppen verbirgt eine virtuelle Spur alle virtuellen Spuren mit einer niedrigeren Prioritätsstufe, außer an Orten, an denen der Titel leer ist oder einen Übergang enthält.</span><span class="sxs-lookup"><span data-stu-id="ac975-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="ac975-129">Virtuelle Spuren können als Ebenen in der endgültigen Komposition betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="ac975-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="ac975-130">Track 1 ist oberhalb von Track 0, Track 2 oberhalb von Track 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="ac975-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="ac975-131">Wenn Sie-1 für den *Priority* -Parameter angeben, wird der virtuelle Track am Ende der Liste mit einem höheren Prioritätswert als die vorhandenen Spuren eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ac975-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="ac975-132">Wenn Sie einen Prioritätswert angeben, der bereits in der Komposition vorhanden ist, wird jede Spur mit der gleichen oder höheren Priorität um eine Prioritätsstufe nach oben verschoben.</span><span class="sxs-lookup"><span data-stu-id="ac975-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="ac975-133">**Beispiel**: Nachverfolgung A hat Priorität 0, und Track B hat Priorität 1.</span><span class="sxs-lookup"><span data-stu-id="ac975-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="ac975-134">Wenn Track C mit Priorität 0 eingefügt wird, verfolgen Sie eine Verschiebung zu Priorität 1, und Nachverfolgen B wechselt zu Priorität 2.</span><span class="sxs-lookup"><span data-stu-id="ac975-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="ac975-135">Wenn die angegebene Priorität größer ist als die aktuelle Anzahl von Spuren in der Komposition, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="ac975-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="ac975-136">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ac975-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ac975-137">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ac975-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ac975-138">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac975-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac975-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac975-139">Requirements</span></span>



| <span data-ttu-id="ac975-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac975-140">Requirement</span></span> | <span data-ttu-id="ac975-141">Wert</span><span class="sxs-lookup"><span data-stu-id="ac975-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac975-142">Header</span><span class="sxs-lookup"><span data-stu-id="ac975-142">Header</span></span><br/>  | <dl> <span data-ttu-id="ac975-143"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ac975-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ac975-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac975-144">Library</span></span><br/> | <dl> <span data-ttu-id="ac975-145"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ac975-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac975-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac975-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac975-147">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ac975-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="ac975-148">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ac975-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




