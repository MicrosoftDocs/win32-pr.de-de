---
description: 'Die iamtimelinegroup-Schnittstelle legt Eigenschaften für Gruppen in DirectShow-Bearbeitungs Diensten fest und ruft Sie ab. Eine Gruppe enthält eine oder mehrere Spuren und möglicherweise eine oder mehrere Kompositionen, die wiederum Quell Clips eines einheitlichen Typs enthalten, z. b. Video oder Audiodaten. Gruppen sind die obersten Kompositionen in einer Zeitachse und machen außerdem die iamtimelinecomp-Schnittstelle verfügbar. Eine Zeitachse kann mehrere Gruppen enthalten. Jede Gruppe verfügt über die folgenden Attribute. Ein zugeordneter Medientyp. Die Framerate, bei der die Gruppe in Frames pro Sekunde (fps) gerendert wird. Alle Änderungen erfolgen zu einem Zeitpunkt, der auf die nächste Frame Grenze gerundet wird, wie in der FPS-Einstellung der Gruppe definiert. Eine Prioritätsstufe zum Schreiben von Dateien mit mehreren Streams desselben Medientyps (z. b. eine Datei mit zwei Video-Stream-AVI). Um ein Gruppen Objekt zu erstellen, rufen Sie iamtimeline:: kreateemptynode mit dem Wert Timeline \_ Major \_ Type \_ Group auf. Sie können den zurückgegebenen iamtimelineobj-Zeiger für die iamtimelinegroup-Schnittstelle Abfragen.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Iamtimelinegroup-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370854"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="02e55-107">Iamtimelinegroup-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="02e55-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="02e55-108">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="02e55-108">\[Deprecated.</span></span> <span data-ttu-id="02e55-109">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="02e55-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="02e55-110">Die `IAMTimelineGroup` -Schnittstelle legt Eigenschaften für Gruppen in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="02e55-111">Eine Gruppe enthält eine oder mehrere Spuren und möglicherweise eine oder mehrere Kompositionen, die wiederum Quell Clips eines einheitlichen Typs enthalten, z. b. Video oder Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="02e55-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="02e55-112">Gruppen sind die obersten Kompositionen in einer Zeitachse und machen außerdem die [**iamtimelinecomp**](iamtimelinecomp.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02e55-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="02e55-113">Eine Zeitachse kann mehrere Gruppen enthalten.</span><span class="sxs-lookup"><span data-stu-id="02e55-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="02e55-114">Jede Gruppe verfügt über die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="02e55-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="02e55-115">Ein zugeordneter Medientyp.</span><span class="sxs-lookup"><span data-stu-id="02e55-115">An associated media type.</span></span>
-   <span data-ttu-id="02e55-116">Die Framerate, bei der die Gruppe in Frames pro Sekunde (fps) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="02e55-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="02e55-117">Alle Änderungen erfolgen zu einem Zeitpunkt, der auf die nächste Frame Grenze gerundet wird, wie in der FPS-Einstellung der Gruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="02e55-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="02e55-118">Eine Prioritätsstufe zum Schreiben von Dateien mit mehreren Streams desselben Medientyps (z. b. eine Datei mit zwei Video-Stream-AVI).</span><span class="sxs-lookup"><span data-stu-id="02e55-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="02e55-119">Um ein Gruppen Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline \_ Major \_ Type \_ Group auf.</span><span class="sxs-lookup"><span data-stu-id="02e55-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="02e55-120">Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die **iamtimelinegroup** -Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="02e55-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="02e55-121">Member</span><span class="sxs-lookup"><span data-stu-id="02e55-121">Members</span></span>

<span data-ttu-id="02e55-122">Die **iamtimelinegroup** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="02e55-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="02e55-123">**Iamtimelinegroup** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02e55-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="02e55-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="02e55-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="02e55-125">Methoden</span><span class="sxs-lookup"><span data-stu-id="02e55-125">Methods</span></span>

<span data-ttu-id="02e55-126">Die **iamtimelinegroup** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="02e55-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="02e55-127">Methode</span><span class="sxs-lookup"><span data-stu-id="02e55-127">Method</span></span>                                                                            | <span data-ttu-id="02e55-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e55-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02e55-129">**Clearrecompressformatdirty**</span><span class="sxs-lookup"><span data-stu-id="02e55-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="02e55-130">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02e55-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="02e55-131">**Getgroupname**</span><span class="sxs-lookup"><span data-stu-id="02e55-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="02e55-132">Ruft den von der Anwendung definierten Namen der Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="02e55-133">**Getmediatype**</span><span class="sxs-lookup"><span data-stu-id="02e55-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="02e55-134">Ruft den unkomprimierten Medientyp für die Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="02e55-135">**Getoutputbuffereing**</span><span class="sxs-lookup"><span data-stu-id="02e55-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="02e55-136">Ruft die Anzahl der Frames ab, die während der Vorschau im Voraus gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="02e55-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="02e55-137">**Getoutputfps**</span><span class="sxs-lookup"><span data-stu-id="02e55-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="02e55-138">Ruft die Ausgabe Rahmenrate dieser Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="02e55-139">**Getpreviewmode**</span><span class="sxs-lookup"><span data-stu-id="02e55-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="02e55-140">Ruft den Vorschaumodus für die Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="02e55-141">**GetPriority**</span><span class="sxs-lookup"><span data-stu-id="02e55-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="02e55-142">Ruft die Priorität der Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="02e55-143">**Geffs martrecompressformat**</span><span class="sxs-lookup"><span data-stu-id="02e55-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="02e55-144">Ruft das aktuelle Komprimierungs Format für die intelligente Neukomprimierung ab.</span><span class="sxs-lookup"><span data-stu-id="02e55-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="02e55-145">**GetTimeline**</span><span class="sxs-lookup"><span data-stu-id="02e55-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="02e55-146">Ruft die Zeitachse ab, zu der diese Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="02e55-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="02e55-147">**Isrecompressformatdirty**</span><span class="sxs-lookup"><span data-stu-id="02e55-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="02e55-148">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02e55-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="02e55-149">**Issmartrecompressformatset**</span><span class="sxs-lookup"><span data-stu-id="02e55-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="02e55-150">Bestimmt, ob ein intelligentes Komprimierungs Format für die Gruppe festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="02e55-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="02e55-151">**Setgroupname**</span><span class="sxs-lookup"><span data-stu-id="02e55-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="02e55-152">Legt den von der Anwendung definierten Namen der Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="02e55-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="02e55-153">**Setmediatype**</span><span class="sxs-lookup"><span data-stu-id="02e55-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="02e55-154">Legt den unkomprimierten Medientyp für die Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="02e55-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="02e55-155">**Setmediatypeer forvb**</span><span class="sxs-lookup"><span data-stu-id="02e55-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="02e55-156">Gibt den Gruppen Medientyp für Automatisierungs Clients an.</span><span class="sxs-lookup"><span data-stu-id="02e55-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="02e55-157">**Setoutputbuffereing**</span><span class="sxs-lookup"><span data-stu-id="02e55-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="02e55-158">Gibt an, wie viele Frames während der Vorschau vorab gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="02e55-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="02e55-159">**Setoutputfps**</span><span class="sxs-lookup"><span data-stu-id="02e55-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="02e55-160">Legt die nicht komprimierte Ausgabe Frame Rate für diese Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="02e55-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="02e55-161">**SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="02e55-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="02e55-162">Legt den Vorschaumodus für die Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="02e55-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="02e55-163">**"Abbild compformatfromsource"**</span><span class="sxs-lookup"><span data-stu-id="02e55-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="02e55-164">Legt das Format der Video Neukomprimierung mit dem Komprimierungs Format aus einer Quelldatei fest.</span><span class="sxs-lookup"><span data-stu-id="02e55-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="02e55-165">**"-Martrecompressformat"**</span><span class="sxs-lookup"><span data-stu-id="02e55-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="02e55-166">Gibt ein für die intelligente Neukomprimierung zu verwendende Komprimierungs Format an.</span><span class="sxs-lookup"><span data-stu-id="02e55-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="02e55-167">**Settimeline**</span><span class="sxs-lookup"><span data-stu-id="02e55-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="02e55-168">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02e55-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="02e55-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e55-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02e55-170">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="02e55-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="02e55-171">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="02e55-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="02e55-172">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02e55-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02e55-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02e55-173">Requirements</span></span>



| <span data-ttu-id="02e55-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02e55-174">Requirement</span></span> | <span data-ttu-id="02e55-175">Wert</span><span class="sxs-lookup"><span data-stu-id="02e55-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e55-176">Header</span><span class="sxs-lookup"><span data-stu-id="02e55-176">Header</span></span><br/>  | <dl> <span data-ttu-id="02e55-177"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="02e55-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="02e55-178">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02e55-178">Library</span></span><br/> | <dl> <span data-ttu-id="02e55-179"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="02e55-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
