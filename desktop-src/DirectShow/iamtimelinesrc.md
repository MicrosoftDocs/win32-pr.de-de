---
description: Die iamtimelinesrc-Schnittstelle stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quell Objekte in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Iamtimelinesrc-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359251"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="6b837-103">Iamtimelinesrc-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6b837-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="6b837-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6b837-104">\[Deprecated.</span></span> <span data-ttu-id="6b837-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6b837-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6b837-106">Die `IAMTimelineSrc` -Schnittstelle stellt Methoden zum Bearbeiten und Festlegen von Eigenschaften für Quell Objekte in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="6b837-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="6b837-107">Ein-Quell Objekt stellt einen Stream aus einer Medienquelle dar.</span><span class="sxs-lookup"><span data-stu-id="6b837-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="6b837-108">Sie können einen Teil der Daten innerhalb einer Quelldatei verwenden, indem Sie die Start-und Medien Endzeiten der Medien festlegen.</span><span class="sxs-lookup"><span data-stu-id="6b837-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="6b837-109">Diese Werte geben den Anfang und das Ende des Quell Objekts relativ zur ursprünglichen Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="6b837-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="6b837-110">Die Medien Zeiten können sich von den Start-und Endzeiten des Objekts auf der Zeitachse unterscheiden, sodass eine schnelle oder langsame Bewegungs Wiedergabe ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="6b837-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="6b837-111">(Bei Audioquellen erfolgt die Verschiebung der Tonhöhe.)</span><span class="sxs-lookup"><span data-stu-id="6b837-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="6b837-112">Um ein Quell Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline- \_ \_ Haupttyp \_ Quelle auf.</span><span class="sxs-lookup"><span data-stu-id="6b837-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="6b837-113">Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die **iamtimelinesrc** -Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6b837-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="6b837-114">Weitere Informationen finden Sie unter [Erstellen einer Zeitachse](constructing-a-timeline.md) und [Arbeiten mit Quellen](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="6b837-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="6b837-115">Member</span><span class="sxs-lookup"><span data-stu-id="6b837-115">Members</span></span>

<span data-ttu-id="6b837-116">Die **iamtimelinesrc** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6b837-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6b837-117">**Iamtimelinesrc** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b837-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="6b837-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b837-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6b837-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b837-119">Methods</span></span>

<span data-ttu-id="6b837-120">Die **iamtimelinesrc** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6b837-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="6b837-121">Methode</span><span class="sxs-lookup"><span data-stu-id="6b837-121">Method</span></span>                                                    | <span data-ttu-id="6b837-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b837-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b837-123">**Fixmediatimes**</span><span class="sxs-lookup"><span data-stu-id="6b837-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="6b837-124">Rundet die angegebenen Uhrzeitwerte auf die nächste Frame Grenze.</span><span class="sxs-lookup"><span data-stu-id="6b837-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="6b837-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="6b837-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="6b837-126">Rundet die angegebenen Uhrzeitwerte, die als **reftime** -Werte angegeben sind, auf die nächste Frame Grenze.</span><span class="sxs-lookup"><span data-stu-id="6b837-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="6b837-127">**Getdefaultfps**</span><span class="sxs-lookup"><span data-stu-id="6b837-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="6b837-128">Ruft die Standardbildrate des Quell Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="6b837-129">**Getmedialength**</span><span class="sxs-lookup"><span data-stu-id="6b837-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="6b837-130">Ruft die Medien Länge dieses Quell Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="6b837-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="6b837-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="6b837-132">Ruft die Medien Länge dieses Quell Objekts als **ref** -Wert ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="6b837-133">**Getmedianame**</span><span class="sxs-lookup"><span data-stu-id="6b837-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="6b837-134">Ruft den Namen der Quelldatei ab, die durch dieses Quell Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6b837-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="6b837-135">**Getmediatimes**</span><span class="sxs-lookup"><span data-stu-id="6b837-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="6b837-136">Ruft die Start-und Endzeit des Mediums ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="6b837-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="6b837-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="6b837-138">Ruft die Start-und Endzeit Werte des Mediums als **ref-Zeit** Werte ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="6b837-139">**Getstreamnumber**</span><span class="sxs-lookup"><span data-stu-id="6b837-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="6b837-140">Ruft die aktuelle streamnummer für das Quell Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="6b837-141">**Getstretchmode**</span><span class="sxs-lookup"><span data-stu-id="6b837-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="6b837-142">Ruft den streckungs Modus einer Videoquelle ab.</span><span class="sxs-lookup"><span data-stu-id="6b837-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="6b837-143">**Isnormalrate**</span><span class="sxs-lookup"><span data-stu-id="6b837-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="6b837-144">Gibt an, ob der Clip mit der normalen Wiedergabe Rate wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b837-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="6b837-145">**Modifystoptime**</span><span class="sxs-lookup"><span data-stu-id="6b837-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="6b837-146">Legt die Endzeit relativ zur Zeitachse fest.</span><span class="sxs-lookup"><span data-stu-id="6b837-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="6b837-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="6b837-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="6b837-148">Legt die Endzeit als **ref** -Wert fest.</span><span class="sxs-lookup"><span data-stu-id="6b837-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="6b837-149">**Setdefaultfps**</span><span class="sxs-lookup"><span data-stu-id="6b837-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="6b837-150">Legt die Standardbildrate des Quell Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="6b837-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="6b837-151">**Setmedialength**</span><span class="sxs-lookup"><span data-stu-id="6b837-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="6b837-152">Gibt die Dauer der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="6b837-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="6b837-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="6b837-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="6b837-154">Gibt die Dauer der Quelldatei als **ref** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="6b837-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="6b837-155">**Setmedianame**</span><span class="sxs-lookup"><span data-stu-id="6b837-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="6b837-156">Gibt den Namen der Quelldatei an, die durch dieses Quell Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6b837-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="6b837-157">**Setmediatimes**</span><span class="sxs-lookup"><span data-stu-id="6b837-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="6b837-158">Legt die Start-und Startzeiten des Mediums fest.</span><span class="sxs-lookup"><span data-stu-id="6b837-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="6b837-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="6b837-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="6b837-160">Legt die Start-und Startzeiten der Medien als **ref-Zeit** Werte fest.</span><span class="sxs-lookup"><span data-stu-id="6b837-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="6b837-161">**Setstreamnumber**</span><span class="sxs-lookup"><span data-stu-id="6b837-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="6b837-162">Gibt an, welcher Stream aus der mit diesem Quell Objekt verknüpften Quelldatei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b837-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="6b837-163">**Setstretchmode**</span><span class="sxs-lookup"><span data-stu-id="6b837-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="6b837-164">Legt den streckungs Modus einer Videoquelle fest.</span><span class="sxs-lookup"><span data-stu-id="6b837-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="6b837-165">**Splicewithnext**</span><span class="sxs-lookup"><span data-stu-id="6b837-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="6b837-166">Verbindet dieses Quell Objekt mit einem anderen Quell Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b837-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="6b837-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b837-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b837-168">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6b837-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6b837-169">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="6b837-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6b837-170">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b837-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b837-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b837-171">Requirements</span></span>



| <span data-ttu-id="6b837-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b837-172">Requirement</span></span> | <span data-ttu-id="6b837-173">Wert</span><span class="sxs-lookup"><span data-stu-id="6b837-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b837-174">Header</span><span class="sxs-lookup"><span data-stu-id="6b837-174">Header</span></span><br/>  | <dl> <span data-ttu-id="6b837-175"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6b837-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6b837-176">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b837-176">Library</span></span><br/> | <dl> <span data-ttu-id="6b837-177"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="6b837-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
