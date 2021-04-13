---
title: WM_GESTURE Meldung (Winuser. h)
description: Übergibt Informationen über eine Geste.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- Windows-Fingereingabe für WM_GESTURE Meldung
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392052"
---
# <a name="wm_gesture-message"></a><span data-ttu-id="08f87-104">WM- \_ Gesten Meldung</span><span class="sxs-lookup"><span data-stu-id="08f87-104">WM\_GESTURE message</span></span>

<span data-ttu-id="08f87-105">Übergibt Informationen über eine Geste.</span><span class="sxs-lookup"><span data-stu-id="08f87-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="08f87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08f87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08f87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08f87-108">Stellt Informationen bereit, mit denen der Gesten Befehl und Gesten spezifische Argument Werte identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="08f87-109">Dabei handelt es sich um dieselben Informationen, die im **ullarguments** -Member der [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Struktur weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="08f87-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08f87-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08f87-111">Stellt ein Handle für Informationen bereit, mit denen der Gesten Befehl und Gesten spezifische Argument Werte identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="08f87-112">Diese Informationen werden abgerufen, indem [**getgestureinfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="08f87-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f87-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08f87-113">Return value</span></span>

<span data-ttu-id="08f87-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08f87-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="08f87-115">Wenn die Anwendung die Nachricht nicht verarbeitet, muss Sie [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="08f87-116">Wenn Sie dies nicht tun, wird der Arbeitsspeicher von der Anwendung nicht mehr verwendet, da der Fingereingabe Handle nicht geschlossen und zugeordneter Prozess Speicher nicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08f87-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f87-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08f87-117">Remarks</span></span>

<span data-ttu-id="08f87-118">In der folgenden Tabelle sind die unterstützten Gesten Befehle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="08f87-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="08f87-119">Gesten-ID</span><span class="sxs-lookup"><span data-stu-id="08f87-119">Gesture ID</span></span>            | <span data-ttu-id="08f87-120">Wert (*dwID*)</span><span class="sxs-lookup"><span data-stu-id="08f87-120">Value (*dwID*)</span></span> | <span data-ttu-id="08f87-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08f87-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f87-122">**GID- \_ Anfang**</span><span class="sxs-lookup"><span data-stu-id="08f87-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="08f87-123">1</span><span class="sxs-lookup"><span data-stu-id="08f87-123">1</span></span>              | <span data-ttu-id="08f87-124">Gibt an, dass eine generische Geste beginnt.</span><span class="sxs-lookup"><span data-stu-id="08f87-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="08f87-125">**GID- \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="08f87-125">**GID\_END**</span></span>          | <span data-ttu-id="08f87-126">2</span><span class="sxs-lookup"><span data-stu-id="08f87-126">2</span></span>              | <span data-ttu-id="08f87-127">Gibt eine generische Gesten Ende an.</span><span class="sxs-lookup"><span data-stu-id="08f87-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="08f87-128">**GID- \_ Zoom**</span><span class="sxs-lookup"><span data-stu-id="08f87-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="08f87-129">3</span><span class="sxs-lookup"><span data-stu-id="08f87-129">3</span></span>              | <span data-ttu-id="08f87-130">Gibt den Zoom-, Zoom-oder Zoomvorgang an.</span><span class="sxs-lookup"><span data-stu-id="08f87-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="08f87-131">Die erste **gid \_ Zoom** -Befehls Meldung beginnt einen Zoom, bewirkt aber keine Vergrößerung.</span><span class="sxs-lookup"><span data-stu-id="08f87-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="08f87-132">Der zweite **gid- \_ Zoom** Befehl löst einen Zoom in Relation zum Zustand aus, der im ersten **gid- \_ Zoom** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="08f87-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="08f87-133">**GID- \_ Pan**</span><span class="sxs-lookup"><span data-stu-id="08f87-133">**GID\_PAN**</span></span>          | <span data-ttu-id="08f87-134">4</span><span class="sxs-lookup"><span data-stu-id="08f87-134">4</span></span>              | <span data-ttu-id="08f87-135">Gibt an, dass schwenken oder Schwenken schwenken.</span><span class="sxs-lookup"><span data-stu-id="08f87-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="08f87-136">Der erste Befehl mit der **gid \_ Pan** gibt an, dass ein Schwenken gestartet wird, führt aber keine schwenken aus.</span><span class="sxs-lookup"><span data-stu-id="08f87-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="08f87-137">Mit der zweiten **gid \_ Pan** -Befehls Meldung beginnt die Anwendung mit dem schwenken.</span><span class="sxs-lookup"><span data-stu-id="08f87-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="08f87-138">**GID \_ drehen**</span><span class="sxs-lookup"><span data-stu-id="08f87-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="08f87-139">5</span><span class="sxs-lookup"><span data-stu-id="08f87-139">5</span></span>              | <span data-ttu-id="08f87-140">Gibt den Drehungs-oder Drehungs Start an.</span><span class="sxs-lookup"><span data-stu-id="08f87-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="08f87-141">Die erste **gid- \_ Rotation** -Befehls Meldung weist auf einen Drehungs-oder Drehungs Start hin, wird jedoch nicht gedreht.</span><span class="sxs-lookup"><span data-stu-id="08f87-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="08f87-142">Die zweite **gid \_** -Rotation-Befehls Meldung löst einen Rotations Vorgang in Relation zum Zustand aus, der in der ersten **gid- \_ Drehung** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="08f87-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="08f87-143">**GID \_ twofingertap**</span><span class="sxs-lookup"><span data-stu-id="08f87-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="08f87-144">6</span><span class="sxs-lookup"><span data-stu-id="08f87-144">6</span></span>              | <span data-ttu-id="08f87-145">Gibt die zwei-Finger-Tap-Bewegung an.</span><span class="sxs-lookup"><span data-stu-id="08f87-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="08f87-146">**GID- \_ pressandtap**</span><span class="sxs-lookup"><span data-stu-id="08f87-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="08f87-147">7</span><span class="sxs-lookup"><span data-stu-id="08f87-147">7</span></span>              | <span data-ttu-id="08f87-148">Gibt die Bewegung zum Drücken und tippen an.</span><span class="sxs-lookup"><span data-stu-id="08f87-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="08f87-149">Um die Legacy Unterstützung zu aktivieren, müssen Nachrichten mit den Befehlen **gid \_ Begin** und **gid \_ End** Geste mithilfe von [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="08f87-150">In der folgenden Tabelle sind die Gesten Argumente angegeben, die in den *LPARAM* -und *wParam* -Parametern angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="08f87-151">Gesten-ID</span><span class="sxs-lookup"><span data-stu-id="08f87-151">Gesture ID</span></span>            | <span data-ttu-id="08f87-152">Geste</span><span class="sxs-lookup"><span data-stu-id="08f87-152">Gesture</span></span>        | <span data-ttu-id="08f87-153">*ullargument*</span><span class="sxs-lookup"><span data-stu-id="08f87-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="08f87-154">*ptsLocation* in der [**GESTUREINFO**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) -Struktur</span><span class="sxs-lookup"><span data-stu-id="08f87-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f87-155">**GID- \_ Zoom**</span><span class="sxs-lookup"><span data-stu-id="08f87-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="08f87-156">Vergrößern/verkleinern</span><span class="sxs-lookup"><span data-stu-id="08f87-156">Zoom In/Out</span></span>    | <span data-ttu-id="08f87-157">Gibt den Abstand zwischen den beiden Punkten an.</span><span class="sxs-lookup"><span data-stu-id="08f87-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="08f87-158">Gibt den Mittelpunkt des Zoom Punkts an.</span><span class="sxs-lookup"><span data-stu-id="08f87-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="08f87-159">**GID- \_ Pan**</span><span class="sxs-lookup"><span data-stu-id="08f87-159">**GID\_PAN**</span></span>          | <span data-ttu-id="08f87-160">Schwenken</span><span class="sxs-lookup"><span data-stu-id="08f87-160">Pan</span></span>            | <span data-ttu-id="08f87-161">Gibt den Abstand zwischen den beiden Punkten an.</span><span class="sxs-lookup"><span data-stu-id="08f87-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="08f87-162">Gibt die aktuelle Position der schwenken an.</span><span class="sxs-lookup"><span data-stu-id="08f87-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="08f87-163">**GID \_ drehen**</span><span class="sxs-lookup"><span data-stu-id="08f87-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="08f87-164">Drehen (Pivot)</span><span class="sxs-lookup"><span data-stu-id="08f87-164">Rotate (pivot)</span></span> | <span data-ttu-id="08f87-165">Gibt den Drehwinkel an, wenn **das \_ FL** -Startflag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="08f87-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="08f87-166">Andernfalls ist dies die Winkel Änderung, seit die Drehung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="08f87-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="08f87-167">Dies wird signiert, um die Richtung der Drehung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="08f87-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="08f87-168">Verwenden Sie den gid-Winkel [**\_ Drehung \_ \_ von \_ Argument**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) und [**gid \_ Drehung \_ \_ in \_ Argument**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) Makros, um den Winkelwert zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="08f87-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="08f87-169">Dies gibt den Mittelpunkt der Drehung an, bei dem es sich um den stationären Punkt handelt, um den das Zielobjekt gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="08f87-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="08f87-170">**GID \_ twofingertap**</span><span class="sxs-lookup"><span data-stu-id="08f87-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="08f87-171">Zwei-Finger-Tippen</span><span class="sxs-lookup"><span data-stu-id="08f87-171">Two-finger Tap</span></span> | <span data-ttu-id="08f87-172">Gibt den Abstand zwischen den beiden Fingern an.</span><span class="sxs-lookup"><span data-stu-id="08f87-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="08f87-173">Gibt die Mitte der beiden Finger an.</span><span class="sxs-lookup"><span data-stu-id="08f87-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="08f87-174">**GID- \_ pressandtap**</span><span class="sxs-lookup"><span data-stu-id="08f87-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="08f87-175">Drücken und tippen</span><span class="sxs-lookup"><span data-stu-id="08f87-175">Press and Tap</span></span>  | <span data-ttu-id="08f87-176">Gibt das Delta zwischen dem ersten und dem zweiten Finger an.</span><span class="sxs-lookup"><span data-stu-id="08f87-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="08f87-177">Dieser Wert wird in den unteren 32 Bits von *ullargument* in einer **Punkt** Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08f87-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="08f87-178">Gibt die Position an, an der der erste Finger angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08f87-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="08f87-179">Alle Entfernungen und Positionen werden in physischen Bildschirm Koordinaten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="08f87-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="08f87-180">Die Parameter " *dwID* " und " *ullargument* " sollten nur als begleitende gid-Befehle angesehen werden \_ \* und sollten nicht von Anwendungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08f87-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="08f87-181">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08f87-181">Examples</span></span>

<span data-ttu-id="08f87-182">Der folgende Code veranschaulicht das Abrufen von Gesten spezifischen Informationen, die dieser Nachricht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="08f87-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="08f87-183">Sie sollten unbehandelte Nachrichten immer an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) weiterleiten und das Eingabe Handle für Eingaben für Nachrichten schließen, die Sie mit einem Rückruf von [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle)verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="08f87-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="08f87-184">In diesem Beispiel wird das Standardverhalten des Gesten Handlers unterdrückt, da das TOUCHINPUT-Handle in jedem der Gesten Fälle geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="08f87-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="08f87-185">Wenn Sie die Fälle im obigen Code für nicht behandelte Nachrichten entfernt haben, verarbeitet der Standard Gesten Handler die Nachrichten, indem er im Standardfall an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="08f87-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a><span data-ttu-id="08f87-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08f87-186">Requirements</span></span>



| <span data-ttu-id="08f87-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08f87-187">Requirement</span></span> | <span data-ttu-id="08f87-188">Wert</span><span class="sxs-lookup"><span data-stu-id="08f87-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f87-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08f87-189">Minimum supported client</span></span><br/> | <span data-ttu-id="08f87-190">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08f87-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="08f87-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08f87-191">Minimum supported server</span></span><br/> | <span data-ttu-id="08f87-192">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08f87-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="08f87-193">Header</span><span class="sxs-lookup"><span data-stu-id="08f87-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="08f87-194"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="08f87-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f87-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08f87-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f87-196">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="08f87-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="08f87-197">Programmier Handbuch für Windows-Touchgesten</span><span class="sxs-lookup"><span data-stu-id="08f87-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

