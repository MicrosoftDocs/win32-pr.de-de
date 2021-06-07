---
title: Problembehandlung bei Anwendungen
description: Dieser Abschnitt enthält Lösungen für häufige Probleme.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch,Problembehandlung bei Anwendungen
- Windows Touch,Ablehnung von Hand
- Ablehnung von Blättern
- Windows Touch,Legacyunterstützung
- Problembehandlung Windows Touch
- Trägheit, Problembehandlung bei Anwendungen
- Manipulationen,Problembehandlung bei Anwendungen
- Gesten,Problembehandlung bei Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389d200cedc57b7f128a535355b12a9288c6e9eb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443146"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="285bb-111">Problembehandlung bei Anwendungen</span><span class="sxs-lookup"><span data-stu-id="285bb-111">Troubleshooting Applications</span></span>

<span data-ttu-id="285bb-112">Dieser Abschnitt enthält Lösungen für häufige Probleme.</span><span class="sxs-lookup"><span data-stu-id="285bb-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="285bb-113">Allgemeine Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="285bb-113">General Troubleshooting</span></span>



| <span data-ttu-id="285bb-114">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-114">Category</span></span> | <span data-ttu-id="285bb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-115">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-116">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-116">Issue</span></span>    | <span data-ttu-id="285bb-117">Ich verarbeite Windows Server 2008, und Windows Touch Funktionen funktionieren nicht.</span><span class="sxs-lookup"><span data-stu-id="285bb-117">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="285bb-118">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-118">Cause</span></span>    | <span data-ttu-id="285bb-119">Sie haben die Desktoperfahrung nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="285bb-119">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="285bb-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-120">Solution</span></span> | <span data-ttu-id="285bb-121">Öffnen Sie Server-Manager Verwaltungstool: Klicken Sie **auf Start**, zeigen Sie **auf Verwaltung,** und klicken Sie dann **auf Server-Manager.**</span><span class="sxs-lookup"><span data-stu-id="285bb-121">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="285bb-122">Klicken Sie **in der** linken Spalte auf das Element Features.</span><span class="sxs-lookup"><span data-stu-id="285bb-122">Click the **Features** item in the left column.</span></span> <span data-ttu-id="285bb-123">Klicken **Sie im Abschnitt** Features auf **Features** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="285bb-123">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="285bb-124">Wählen **Sie Desktop experience (Desktoperfahrung)** **aus, klicken Sie auf Next**(Weiter), und klicken Sie dann auf Install **(Installieren).**</span><span class="sxs-lookup"><span data-stu-id="285bb-124">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



| <span data-ttu-id="285bb-125">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-125">Category</span></span> | <span data-ttu-id="285bb-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-126">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-127">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-127">Issue</span></span>    | <span data-ttu-id="285bb-128">Wenn ich meinen Finger schnell über meine Anwendung bewegen kann, wird ein Pfeil angezeigt, und meine Geste oder Bearbeitung wird nicht ordnungsgemäß registriert.</span><span class="sxs-lookup"><span data-stu-id="285bb-128">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="285bb-129">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-129">Cause</span></span>    | <span data-ttu-id="285bb-130">Aktivieren von Flicks, wenn Sie sie nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="285bb-130">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="285bb-131">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-131">Solution</span></span> | <span data-ttu-id="285bb-132">Sie haben Flicks aktiviert, wenn sie deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="285bb-132">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="285bb-133">Informationen [zum Deaktivieren von Stiftflicks](legacy-support-for-panning-with-scrollbars.md) finden Sie unter Legacy-Unterstützung für Schwenken mit Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="285bb-133">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="285bb-134">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-134">Issue</span></span></td>
<td><span data-ttu-id="285bb-135">Ich kann nicht zwischen Mauseingaben und Windows Touch unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="285bb-135">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="285bb-136">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-136">Cause</span></span></td>
<td><span data-ttu-id="285bb-137">Windows generiert Mausmeldungen für legacy-Unterstützung, wenn ein Benutzer auf den Bildschirm klickt.</span><span class="sxs-lookup"><span data-stu-id="285bb-137">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="285bb-138">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-138">Solution</span></span></td>
<td><span data-ttu-id="285bb-139">Sie können <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> <strong></strong> für die WM_LBUTTONDOWN aufrufen und <strong>WM_LBUTTONUP,</strong> um die Quelle zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="285bb-139">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="285bb-140">Der folgende Code zeigt, wie dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="285bb-140">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="285bb-141">C++</span><span class="sxs-lookup"><span data-stu-id="285bb-141">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="285bb-142">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-142">Category</span></span> | <span data-ttu-id="285bb-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-143">Description</span></span> |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-144">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-144">Issue</span></span>    | <span data-ttu-id="285bb-145">Gewusst wie Microsoft PixelSense-Anwendungen unter Windows 7 ausführen?</span><span class="sxs-lookup"><span data-stu-id="285bb-145">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="285bb-146">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-146">Cause</span></span>    | <span data-ttu-id="285bb-147">Windows Touch und Microsoft PixelSense sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="285bb-147">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="285bb-148">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-148">Solution</span></span> | <span data-ttu-id="285bb-149">Sie müssen entweder die Windows 7-Plattform oder die Microsoft PixelSense-Plattform als Ziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="285bb-149">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="285bb-150">Problembehandlung bei Manipulationen und Trägheit</span><span class="sxs-lookup"><span data-stu-id="285bb-150">Troubleshooting Manipulations and Inertia</span></span>



| <span data-ttu-id="285bb-151">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-151">Category</span></span> | <span data-ttu-id="285bb-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-152">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-153">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-153">Issue</span></span>    | <span data-ttu-id="285bb-154">Meine Anwendung wird ohne Grund einfriert.</span><span class="sxs-lookup"><span data-stu-id="285bb-154">My application is freezing for no reason.</span></span> <span data-ttu-id="285bb-155">Ich habe Zugriffsverletzungen, wenn ich meine Objektschnittstellen initialisiere.</span><span class="sxs-lookup"><span data-stu-id="285bb-155">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="285bb-156">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-156">Cause</span></span>    | <span data-ttu-id="285bb-157">Fehlender Aufruf von **CoInitialize bei** Verwendung der [**Schnittstellen IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) oder [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)</span><span class="sxs-lookup"><span data-stu-id="285bb-157">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="285bb-158">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-158">Solution</span></span> | <span data-ttu-id="285bb-159">Dies kann durch instanziieren der Windows Touch Component Object Model (COM)-Objekte verursacht werden, ohne CoInitialize auf aufruft.</span><span class="sxs-lookup"><span data-stu-id="285bb-159">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="285bb-160">Dies geschieht manchmal, wenn Sie Projekte von der Verwendung von Gesten in die Verwendung der Manipulations- oder Trägheitsschnittstellen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="285bb-160">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



| <span data-ttu-id="285bb-161">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-161">Category</span></span> | <span data-ttu-id="285bb-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-162">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-163">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-163">Issue</span></span>    | <span data-ttu-id="285bb-164">Mein Objekt wird nicht ordnungsgemäß gedreht, wenn es übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="285bb-164">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="285bb-165">Die Drehung mit einem Finger funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="285bb-165">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="285bb-166">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-166">Cause</span></span>    | <span data-ttu-id="285bb-167">Falsches Festlegen von Pivots für ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="285bb-167">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="285bb-168">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-168">Solution</span></span> | <span data-ttu-id="285bb-169">Die Pivotpunkte für die Bearbeitung werden nicht ordnungsgemäß eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="285bb-169">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="285bb-170">Legen Sie die [**PivotPointX-**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) und [**PivotPointY-Eigenschaften**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) auf die Mitte des Objekts oder Punkts fest, um das bzw. den Sie drehen möchten, und legen Sie die [**PivotRadius-Eigenschaft**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) auf den Radius Ihres Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="285bb-170">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="285bb-171">Problembehandlung Windows Touch Eingabe</span><span class="sxs-lookup"><span data-stu-id="285bb-171">Troubleshooting Windows Touch Input</span></span>



| <span data-ttu-id="285bb-172">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-172">Category</span></span> | <span data-ttu-id="285bb-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-173">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-174">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-174">Issue</span></span>    | <span data-ttu-id="285bb-175">Nachdem ich die [**WM \_ TOUCH-Nachricht verarbeitet**](wm-touchdown.md) habe, kann ich keine Begrenzungsfeedback mehr erhalten.</span><span class="sxs-lookup"><span data-stu-id="285bb-175">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="285bb-176">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-176">Cause</span></span>    | <span data-ttu-id="285bb-177">Verwenden der [**WM \_ TOUCH-Nachricht,**](wm-touchdown.md) ohne sie zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="285bb-177">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="285bb-178">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-178">Solution</span></span> | <span data-ttu-id="285bb-179">Sie verwenden wahrscheinlich eine Windows Touch, ohne sie an **DefWindowProc** weiterzuleiten. Dies führt zu unerwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="285bb-179">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="285bb-180">Weitere [Erste Schritte mit Windows Touch-Nachrichten](getting-started-with-multi-touch-messages.md) finden Sie unter Ordnungsgemäßer Umgang mit [**WM \_ TOUCH-Nachrichten.**](wm-touchdown.md)</span><span class="sxs-lookup"><span data-stu-id="285bb-180">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="285bb-181">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-181">Issue</span></span></td>
<td><span data-ttu-id="285bb-182">Ich samt windows.h, aber es wird immer noch angezeigt, <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="285bb-182">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="285bb-183">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-183">Cause</span></span></td>
<td><span data-ttu-id="285bb-184">Die Windows-Version in Targetver.h ist falsch.</span><span class="sxs-lookup"><span data-stu-id="285bb-184">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="285bb-185">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-185">Solution</span></span></td>
<td><span data-ttu-id="285bb-186">Sie haben nicht die richtige Windows-Version in Ihrem Projekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="285bb-186">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="285bb-187">Der folgende Code veranschaulicht die ordnungsgemäß festgelegten Windows-Versionen für Windows Touch Windows 7.</span><span class="sxs-lookup"><span data-stu-id="285bb-187">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="285bb-188">C++</span><span class="sxs-lookup"><span data-stu-id="285bb-188">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="285bb-189">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-189">Issue</span></span></td>
<td><span data-ttu-id="285bb-190">Meine Toucheingabe-X-Koordinaten und y-Koordinaten scheinen ungültig zu sein.</span><span class="sxs-lookup"><span data-stu-id="285bb-190">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="285bb-191">Sie sind entweder größer als erwartet, oder sie sind negative Werte.</span><span class="sxs-lookup"><span data-stu-id="285bb-191">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="285bb-192">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-192">Cause</span></span></td>
<td><span data-ttu-id="285bb-193">Möglicherweise müssen Sie Ihre Berührungspunkte in Pixel konvertieren, oder Sie müssen die Bildschirmkoordinaten konvertieren.</span><span class="sxs-lookup"><span data-stu-id="285bb-193">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="285bb-194">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-194">Solution</span></span></td>
<td><span data-ttu-id="285bb-195">Stellen Sie sicher, dass Sie <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>und ScreenToClient aufrufen.</strong></a></span><span class="sxs-lookup"><span data-stu-id="285bb-195">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="285bb-196">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="285bb-196">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="285bb-197">C++</span><span class="sxs-lookup"><span data-stu-id="285bb-197">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="285bb-198">Um die <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient-Funktion verwenden zu</strong></a> können, müssen Sie eine hohe DPI-Unterstützung in Ihrer Anwendung haben.</span><span class="sxs-lookup"><span data-stu-id="285bb-198">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="285bb-199">Weitere Informationen zur Unterstützung eines hohen DPI-Werts finden Sie im <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">MSDN-Abschnitt</a> Mit hohem DPI-Wert.</span><span class="sxs-lookup"><span data-stu-id="285bb-199">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="285bb-200">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-200">Category</span></span> | <span data-ttu-id="285bb-201">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-201">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-202">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-202">Issue</span></span>    | <span data-ttu-id="285bb-203">Mir werden keine [**WM \_ TOUCH-Nachrichten**](wm-touchdown.md) angezeigt, aber ich weiß, dass Windows Touch funktioniert, da wm gesture-Meldungen angezeigt [**\_ werden.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="285bb-203">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="285bb-204">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-204">Cause</span></span>    | <span data-ttu-id="285bb-205">Es fehlt ein Aufruf von [**RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)</span><span class="sxs-lookup"><span data-stu-id="285bb-205">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="285bb-206">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-206">Solution</span></span> | <span data-ttu-id="285bb-207">[**WM \_ TOUCH-**](wm-touchdown.md) und [**WM \_ GESTURE-Nachrichten**](wm-gesture.md) schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="285bb-207">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="285bb-208">Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)nicht aufrufen, erhalten Sie nur **WM \_ GESTURE-Meldungen.**</span><span class="sxs-lookup"><span data-stu-id="285bb-208">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



| <span data-ttu-id="285bb-209">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-209">Category</span></span> | <span data-ttu-id="285bb-210">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-210">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-211">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-211">Issue</span></span>    | <span data-ttu-id="285bb-212">Ich stelle kleine Verzögerungen fest, von dem Zeitpunkt, an dem ich meinen Finger nach unten befasse, bis zu dem Zeitpunkt, zu dem ich Eingaben in meiner Anwendung erhalte.</span><span class="sxs-lookup"><span data-stu-id="285bb-212">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="285bb-213">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-213">Cause</span></span>    | <span data-ttu-id="285bb-214">Die Ablehnung von Handflächen führt zu Verzögerungen bei der Eingabe.</span><span class="sxs-lookup"><span data-stu-id="285bb-214">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="285bb-215">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-215">Solution</span></span> | <span data-ttu-id="285bb-216">Wenn **TWF \_ WANTPALM** in Aufrufen von [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)festgelegt ist, ist die Ablehnung von "hand" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="285bb-216">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="285bb-217">Dies führt zu einer kleinen Verzögerung (100 ms), während die Software testet, ob die Eingabe von einem Finger, Stift oder der Handfläche des Benutzers stammt.</span><span class="sxs-lookup"><span data-stu-id="285bb-217">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="285bb-218">Deaktivieren Sie die Ablehnung von Handflächen, indem **Sie RegisterTouchWindow** aufrufen, wobei das **\_ TWF-FLAG WANTPALM** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="285bb-218">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="285bb-219">Problembehandlung bei Windows Touch Gesten</span><span class="sxs-lookup"><span data-stu-id="285bb-219">Troubleshooting Windows Touch Gestures</span></span>



| <span data-ttu-id="285bb-220">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-220">Category</span></span> | <span data-ttu-id="285bb-221">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-221">Description</span></span> |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-222">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-222">Issue</span></span>    | <span data-ttu-id="285bb-223">Nachdem ich die [**\_ WM-GESTE-Nachricht**](wm-gesture.md) verarbeitet habe, erhalte ich keine Begrenzungsfeedback mehr.</span><span class="sxs-lookup"><span data-stu-id="285bb-223">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="285bb-224">Oder eine Geste, die zuvor funktioniert hat, funktioniert jetzt nicht.</span><span class="sxs-lookup"><span data-stu-id="285bb-224">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="285bb-225">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-225">Cause</span></span>    | <span data-ttu-id="285bb-226">Verwenden der [**WM \_ GESTURE-Nachricht,**](wm-gesture.md) ohne sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="285bb-226">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="285bb-227">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-227">Solution</span></span> | <span data-ttu-id="285bb-228">Sie verwenden wahrscheinlich eine Windows Touch Nachricht, ohne sie an [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)weiterzuleiten. Dies führt zu unerwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="285bb-228">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="285bb-229">Weitere Informationen zum ordnungsgemäßen Behandeln von WM GESTURE-Nachrichten finden Sie unter [Erste Schritte mit Windows-Gesten.](getting-started-with-multi-touch-gestures.md) [**\_**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="285bb-229">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



| <span data-ttu-id="285bb-230">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-230">Category</span></span> | <span data-ttu-id="285bb-231">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-231">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-232">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-232">Issue</span></span>    | <span data-ttu-id="285bb-233">Mir werden keine [**WM \_ GESTURE-Meldungen**](wm-gesture.md) angezeigt, aber ich weiß, dass Windows Touch funktioniert, da wm [**\_ touch-Nachrichten**](wm-touchdown.md) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="285bb-233">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="285bb-234">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-234">Cause</span></span>    | <span data-ttu-id="285bb-235">Aufrufen von [**RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)</span><span class="sxs-lookup"><span data-stu-id="285bb-235">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="285bb-236">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-236">Solution</span></span> | <span data-ttu-id="285bb-237">[**WM \_ TOUCH-**](wm-touchdown.md) und [**WM \_ GESTURE-Nachrichten**](wm-gesture.md) schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="285bb-237">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="285bb-238">Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, erhalten Sie keine **WM \_ GESTURE-Meldungen.**</span><span class="sxs-lookup"><span data-stu-id="285bb-238">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="285bb-239">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-239">Issue</span></span></td>
<td><span data-ttu-id="285bb-240">Ich sehe nicht alle Gesten, die ich erwartet.</span><span class="sxs-lookup"><span data-stu-id="285bb-240">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="285bb-241">Beispielsweise werden Gesten mit dem Bezeichner <strong>GID_PAN,</strong> aber nicht <strong>GID_ROTATE.</strong></span><span class="sxs-lookup"><span data-stu-id="285bb-241">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="285bb-242">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-242">Cause</span></span></td>
<td><span data-ttu-id="285bb-243">Einige Gesten, z. B. die Drehbewegung, sind standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="285bb-243">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="285bb-244">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-244">Solution</span></span></td>
<td><span data-ttu-id="285bb-245">Sie müssen <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> aufrufen, wenn Sie eine <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> Meldung erhalten, wie im <strong>WM_GESTURENOTIFY-Verweis</strong> beschrieben, oder Sie müssen einen Handler für die <strong>WM_GESTURENOTIFY</strong> Nachricht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="285bb-245">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="285bb-246">Der folgende Code zeigt, wie ein Handler implementiert werden kann, um die Unterstützung für die Rotation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="285bb-246">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="285bb-247">C++</span><span class="sxs-lookup"><span data-stu-id="285bb-247">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="285bb-248">Weitere Beispiele für typische Gestenkonfigurationen finden Sie unter <strong>SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="285bb-248">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="285bb-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-249">Category</span></span> | <span data-ttu-id="285bb-250">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-250">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-251">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-251">Issue</span></span>    | <span data-ttu-id="285bb-252">Die benutzerdefinierten Bildlaufleisten in meiner Anwendung scrollen nicht, wenn ich die Schwenkbewegung durchgezeig.</span><span class="sxs-lookup"><span data-stu-id="285bb-252">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="285bb-253">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-253">Cause</span></span>    | <span data-ttu-id="285bb-254">Fehlende Handler für die richtigen WM \_ \* SCROLL-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="285bb-254">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="285bb-255">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-255">Solution</span></span> | <span data-ttu-id="285bb-256">Sie verarbeiten nicht alle WM \_ \* SCROLL-Meldungen in Ihren benutzerdefinierten Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="285bb-256">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="285bb-257">Es wird empfohlen, die [**WM \_ GESTURE-Nachricht**](wm-gesture.md) zu verarbeiten, anstatt die benutzerdefinierte Scrollleistenfunktion über legacy-Unterstützung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="285bb-257">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="285bb-258">Sie müssen Meldungen unterstützen, wie im Abschnitt [Legacyunterstützung für Schwenken mit Scrollleisten](legacy-support-for-panning-with-scrollbars.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="285bb-258">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



| <span data-ttu-id="285bb-259">Kategorie</span><span class="sxs-lookup"><span data-stu-id="285bb-259">Category</span></span> | <span data-ttu-id="285bb-260">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285bb-260">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285bb-261">Problem</span><span class="sxs-lookup"><span data-stu-id="285bb-261">Issue</span></span>    | <span data-ttu-id="285bb-262">Ich erhalte Verzögerungen bei Gesten.</span><span class="sxs-lookup"><span data-stu-id="285bb-262">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="285bb-263">Ursache</span><span class="sxs-lookup"><span data-stu-id="285bb-263">Cause</span></span>    | <span data-ttu-id="285bb-264">Flimmer können zu Verzögerungen bei Gesten führen.</span><span class="sxs-lookup"><span data-stu-id="285bb-264">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="285bb-265">Lösung</span><span class="sxs-lookup"><span data-stu-id="285bb-265">Solution</span></span> | <span data-ttu-id="285bb-266">Bei Flimmern kann es zu Verzögerungen kommen, wie lange es dauert, bis Ihre Anwendung [**WM \_ GESTURE-Nachrichten**](wm-gesture.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="285bb-266">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="285bb-267">Informationen zum Deaktivieren von Flimmern finden Sie unter Legacyunterstützung für Schwenken [mit Scrollleisten.](legacy-support-for-panning-with-scrollbars.md)</span><span class="sxs-lookup"><span data-stu-id="285bb-267">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="285bb-268">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="285bb-268">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="285bb-269">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="285bb-269">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 