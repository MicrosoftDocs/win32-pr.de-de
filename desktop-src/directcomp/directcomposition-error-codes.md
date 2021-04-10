---
title: Directcomposition-Fehlercodes (Dcomp. h)
description: In diesem Abschnitt werden die Fehlercodes beschrieben, die für directcomposition spezifisch sind.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104894"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="c76c0-103">Directcomposition-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c76c0-103">DirectComposition error codes</span></span>

<span data-ttu-id="c76c0-104">Wenn ein Fehler auftritt, gibt Microsoft directcomposition einen Code als **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c76c0-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="c76c0-105">In diesem Abschnitt werden die Fehlercodes beschrieben, die für directcomposition spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="c76c0-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="c76c0-106">Eine Liste der allgemeinen Component Object Model (com)-Fehlercodes finden Sie unter [com-Fehlercodes](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c76c0-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c76c0-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**dcomposition- \_ Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="c76c0-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c76c0-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="c76c0-109">Das Fenster Handle, das in einem Aufrufen der [**idcompositiondevice:: foratetargetforhwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) -Methode angegeben wurde, gehört zu einem anderen Prozess als dem, der das Geräte Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="c76c0-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c76c0-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="c76c0-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c76c0-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="c76c0-112">Die Oberfläche wurde bereits gerendert, als die Anwendung die Methode [**idcompositionsurface:: beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**idcompositionsurface:: suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)oder [**idcompositionsurface:: resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="c76c0-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="c76c0-113">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="c76c0-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c76c0-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.**</span><span class="sxs-lookup"><span data-stu-id="c76c0-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="c76c0-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c76c0-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="c76c0-116">Die Anwendung hat die Methode [**idcompositionsurface:: suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**idcompositionsurface:: resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)oder [**idcompositionsurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) für eine Oberfläche aufgerufen, die nicht gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="c76c0-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="c76c0-117">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="c76c0-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c76c0-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**Das dcomposition- \_ Fehler \_ Fenster wurde \_ bereits \_ erstellt.**</span><span class="sxs-lookup"><span data-stu-id="c76c0-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="c76c0-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c76c0-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="c76c0-120">Die [**idcompositiondevice:: foratetargetforhwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) -Methode wurde mit *HWND* und den *obersten* Parametern aufgerufen, für die bereits eine visuelle Struktur vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c76c0-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c76c0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c76c0-121">Remarks</span></span>

<span data-ttu-id="c76c0-122">Wenn ein Aufrufen von [**idcompositionsurface:: beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) die letzte Aktion war:</span><span class="sxs-lookup"><span data-stu-id="c76c0-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="c76c0-123">Aufrufen dieser Methode:</span><span class="sxs-lookup"><span data-stu-id="c76c0-123">Calling this method:</span></span>                                    | <span data-ttu-id="c76c0-124">Gibt folgenden Wert zurück:</span><span class="sxs-lookup"><span data-stu-id="c76c0-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="c76c0-125">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="c76c0-126">**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="c76c0-127">**"EndDraw"**</span><span class="sxs-lookup"><span data-stu-id="c76c0-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="c76c0-128">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="c76c0-129">**Suspenddraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="c76c0-130">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="c76c0-131">**Resumedraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="c76c0-132">**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="c76c0-133">Bei einem Aufrufen von " [**idcompositionsurface:: suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) " handelt es sich um die letzte Aktion:</span><span class="sxs-lookup"><span data-stu-id="c76c0-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="c76c0-134">Aufrufen dieser Methode:</span><span class="sxs-lookup"><span data-stu-id="c76c0-134">Calling this method:</span></span>                                    | <span data-ttu-id="c76c0-135">Gibt folgenden Wert zurück:</span><span class="sxs-lookup"><span data-stu-id="c76c0-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="c76c0-136">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="c76c0-137">**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="c76c0-138">**"EndDraw"**</span><span class="sxs-lookup"><span data-stu-id="c76c0-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="c76c0-139">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="c76c0-140">**Suspenddraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="c76c0-141">**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="c76c0-142">**Resumedraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="c76c0-143">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="c76c0-144">Wenn ein Aufrufen von [**idcompositionsurface:: resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) die letzte Aktion war:</span><span class="sxs-lookup"><span data-stu-id="c76c0-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="c76c0-145">Aufrufen dieser Methode:</span><span class="sxs-lookup"><span data-stu-id="c76c0-145">Calling this method:</span></span>                                    | <span data-ttu-id="c76c0-146">Gibt folgenden Wert zurück:</span><span class="sxs-lookup"><span data-stu-id="c76c0-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c76c0-147">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="c76c0-148">**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**</span><span class="sxs-lookup"><span data-stu-id="c76c0-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="c76c0-149">**"EndDraw"**</span><span class="sxs-lookup"><span data-stu-id="c76c0-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="c76c0-150">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="c76c0-151">**Suspenddraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="c76c0-152">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="c76c0-153">**Resumedraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="c76c0-154">**dcomposition- \_ Fehler \_ Oberfläche, die \_ \_ gerendert wird.**</span><span class="sxs-lookup"><span data-stu-id="c76c0-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="c76c0-155">Wenn ein Aufrufen von [**idcompositionsurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) die letzte Aktion war:</span><span class="sxs-lookup"><span data-stu-id="c76c0-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="c76c0-156">Aufrufen dieser Methode:</span><span class="sxs-lookup"><span data-stu-id="c76c0-156">Calling this method:</span></span>                                    | <span data-ttu-id="c76c0-157">Gibt folgenden Wert zurück:</span><span class="sxs-lookup"><span data-stu-id="c76c0-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="c76c0-158">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="c76c0-159">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c76c0-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="c76c0-160">**"EndDraw"**</span><span class="sxs-lookup"><span data-stu-id="c76c0-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="c76c0-161">**dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.**</span><span class="sxs-lookup"><span data-stu-id="c76c0-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="c76c0-162">**Suspenddraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="c76c0-163">**dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.**</span><span class="sxs-lookup"><span data-stu-id="c76c0-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="c76c0-164">**Resumedraw**</span><span class="sxs-lookup"><span data-stu-id="c76c0-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="c76c0-165">**dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.**</span><span class="sxs-lookup"><span data-stu-id="c76c0-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c76c0-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c76c0-166">Requirements</span></span>



| <span data-ttu-id="c76c0-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c76c0-167">Requirement</span></span> | <span data-ttu-id="c76c0-168">Wert</span><span class="sxs-lookup"><span data-stu-id="c76c0-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c76c0-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c76c0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c76c0-170">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c76c0-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c76c0-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c76c0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c76c0-172">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c76c0-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c76c0-173">Header</span><span class="sxs-lookup"><span data-stu-id="c76c0-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="c76c0-174"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c76c0-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76c0-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c76c0-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76c0-176">Directcomposition-Referenz</span><span class="sxs-lookup"><span data-stu-id="c76c0-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

