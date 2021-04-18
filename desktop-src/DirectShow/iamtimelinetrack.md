---
description: Die iamtimelinetrack-Schnittstelle stellt Methoden zum Bearbeiten von Track-Objekten in DirectShow-Bearbeitungs Diensten bereit. Eine Spur enthält eine Liste der Quellen, die in der endgültigen Ausgabe gerendert werden.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Iamtimelinetrack-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371784"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="12c09-103">Iamtimelinetrack-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="12c09-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="12c09-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="12c09-104">\[Deprecated.</span></span> <span data-ttu-id="12c09-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="12c09-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="12c09-106">Die- `IAMTimelineTrack` Schnittstelle stellt Methoden zum Bearbeiten von *Track* -Objekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="12c09-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="12c09-107">Eine Spur enthält eine Liste der Quellen, die in der endgültigen Ausgabe gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="12c09-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="12c09-108">Quellen innerhalb desselben Titels können sich möglicherweise nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="12c09-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="12c09-109">Video Spuren können sowohl Effekte als auch Übergänge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="12c09-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="12c09-110">Die Renderingengine wendet die Auswirkungen an, bevor Übergänge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="12c09-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="12c09-111">Audiospuren können Effekte, aber keine Übergänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="12c09-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="12c09-112">Weitere Informationen finden Sie [im Zeitachsen Modell](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="12c09-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="12c09-113">Um ein Track-Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline \_ Major \_ Type \_ Track auf.</span><span class="sxs-lookup"><span data-stu-id="12c09-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="12c09-114">Sie können den zurückgegebenen **iamtimelineobj** -Zeiger für die- `IAMTimelineTrack` Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="12c09-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="12c09-115">Member</span><span class="sxs-lookup"><span data-stu-id="12c09-115">Members</span></span>

<span data-ttu-id="12c09-116">Die **iamtimelinetrack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="12c09-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="12c09-117">**Iamtimelinetrack** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="12c09-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="12c09-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="12c09-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="12c09-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="12c09-119">Methods</span></span>

<span data-ttu-id="12c09-120">Die **iamtimelinetrack** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="12c09-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="12c09-121">Methode</span><span class="sxs-lookup"><span data-stu-id="12c09-121">Method</span></span>                                                          | <span data-ttu-id="12c09-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12c09-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12c09-123">**Areyoublank**</span><span class="sxs-lookup"><span data-stu-id="12c09-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="12c09-124">Bestimmt, ob der Titel leer ist (enthält keine Quell Objekte).</span><span class="sxs-lookup"><span data-stu-id="12c09-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="12c09-125">**Getnexnerrc**</span><span class="sxs-lookup"><span data-stu-id="12c09-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="12c09-126">Durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="12c09-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="12c09-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="12c09-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="12c09-128">Durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird, wobei die angegebene als [**ref**](reftime.md) -Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="12c09-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="12c09-129">**Getnexzrcex**</span><span class="sxs-lookup"><span data-stu-id="12c09-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="12c09-130">Ruft die nächste Quelle nach der angegebenen Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="12c09-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="12c09-131">**Getsourcescount**</span><span class="sxs-lookup"><span data-stu-id="12c09-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="12c09-132">Ruft die Anzahl der Quellen in der Spur ab.</span><span class="sxs-lookup"><span data-stu-id="12c09-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="12c09-133">**Gezr\time**</span><span class="sxs-lookup"><span data-stu-id="12c09-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="12c09-134">Ruft das Quell Objekt, das dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.</span><span class="sxs-lookup"><span data-stu-id="12c09-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="12c09-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="12c09-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="12c09-136">Ruft das Quell Objekt ab, das dem angegebenen Zeitpunkt am nächsten liegt, das als [**reftime**](reftime.md) -Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="12c09-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="12c09-137">**Insertspace**</span><span class="sxs-lookup"><span data-stu-id="12c09-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="12c09-138">Teilt alle-Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein.</span><span class="sxs-lookup"><span data-stu-id="12c09-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="12c09-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="12c09-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="12c09-140">Teilt alle Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt mithilfe von [**ref Time**](reftime.md) -Werten Leerzeichen zwischen diesen ein.</span><span class="sxs-lookup"><span data-stu-id="12c09-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="12c09-141">**"Muveeverythingby"**</span><span class="sxs-lookup"><span data-stu-id="12c09-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="12c09-142">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12c09-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="12c09-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="12c09-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="12c09-144">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12c09-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="12c09-145">**Srcadd**</span><span class="sxs-lookup"><span data-stu-id="12c09-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="12c09-146">Fügt der Spur eine Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="12c09-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="12c09-147">**NULL**</span><span class="sxs-lookup"><span data-stu-id="12c09-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="12c09-148">Entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten.</span><span class="sxs-lookup"><span data-stu-id="12c09-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="12c09-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="12c09-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="12c09-150">Entfernt alle Elemente aus der Spur zwischen den angegebenen Zeiten, die als [**ref-Zeit**](reftime.md) Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12c09-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="12c09-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12c09-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12c09-152">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="12c09-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="12c09-153">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="12c09-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="12c09-154">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12c09-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12c09-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12c09-155">Requirements</span></span>



| <span data-ttu-id="12c09-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12c09-156">Requirement</span></span> | <span data-ttu-id="12c09-157">Wert</span><span class="sxs-lookup"><span data-stu-id="12c09-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12c09-158">Header</span><span class="sxs-lookup"><span data-stu-id="12c09-158">Header</span></span><br/>  | <dl> <span data-ttu-id="12c09-159"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="12c09-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="12c09-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12c09-160">Library</span></span><br/> | <dl> <span data-ttu-id="12c09-161"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="12c09-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
