---
title: Problembehandlung bei Anwendungen
description: In diesem Abschnitt finden Sie Lösungen für häufige Probleme.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows-Interaktion, Problembehandlung bei Anwendungen
- Windows-Fingereingabe, Palm Ablehnung
- Palmen Ablehnung
- Windows-Fingereingabe, Legacy Unterstützung
- Problembehandlung bei Windows berühren
- Trägheit, Problembehandlung bei Anwendungen
- Manipulationen, Problembehandlung bei Anwendungen
- Gesten, Problembehandlung bei Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1aeb37f139ea9063c07dd7d629ac5579229863
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961274"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="a5b23-111">Problembehandlung bei Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a5b23-111">Troubleshooting Applications</span></span>

<span data-ttu-id="a5b23-112">In diesem Abschnitt finden Sie Lösungen für häufige Probleme.</span><span class="sxs-lookup"><span data-stu-id="a5b23-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="a5b23-113">Allgemeine Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="a5b23-113">General Troubleshooting</span></span>



|          |                                                                                                                                                                                                                                                                                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-114">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-114">Issue</span></span>    | <span data-ttu-id="a5b23-115">Ich führe Windows Server 2008 aus, und die Windows-Berührungs Features funktionieren nicht.</span><span class="sxs-lookup"><span data-stu-id="a5b23-115">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="a5b23-116">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-116">Cause</span></span>    | <span data-ttu-id="a5b23-117">Sie haben die Desktop Darstellung nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a5b23-117">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5b23-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-118">Solution</span></span> | <span data-ttu-id="a5b23-119">Öffnen Sie das Server-Manager Verwaltungs Tool: Klicken Sie auf **Start**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Server-Manager**.</span><span class="sxs-lookup"><span data-stu-id="a5b23-119">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="a5b23-120">Klicken Sie in der linken Spalte auf das Element **Features** .</span><span class="sxs-lookup"><span data-stu-id="a5b23-120">Click the **Features** item in the left column.</span></span> <span data-ttu-id="a5b23-121">Klicken Sie im Abschnitt **Features** auf **Features hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="a5b23-121">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="a5b23-122">Wählen Sie **Desktop** Darstellung aus, klicken Sie auf **weiter**, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="a5b23-122">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



|          |                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-123">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-123">Issue</span></span>    | <span data-ttu-id="a5b23-124">Jedes Mal, wenn ich meinen Finger schnell über die Anwendung hinweg bewege, wird ein Pfeil angezeigt, und meine Geste oder Manipulation wird nicht ordnungsgemäß registriert.</span><span class="sxs-lookup"><span data-stu-id="a5b23-124">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="a5b23-125">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-125">Cause</span></span>    | <span data-ttu-id="a5b23-126">Sie haben schnelle Stift Bewegungen aktiviert, wenn Sie Sie nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-126">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a5b23-127">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-127">Solution</span></span> | <span data-ttu-id="a5b23-128">Sie haben schnelle Stift Bewegungen aktiviert, wenn Sie Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a5b23-128">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="a5b23-129">Informationen zum Deaktivieren von Stift Flicks finden Sie [unter Legacy Unterstützung für das Schwenken mit Scrollleisten](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b23-129">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5b23-130">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-130">Issue</span></span></td>
<td><span data-ttu-id="a5b23-131">Ich kann nicht zwischen Maus Eingaben und Windows-Eingabe Eingaben erkennen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-131">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5b23-132">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-132">Cause</span></span></td>
<td><span data-ttu-id="a5b23-133">Windows generiert Maus Meldungen für die Legacy Unterstützung, wenn ein Benutzer auf den Bildschirm klickt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-133">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5b23-134">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-134">Solution</span></span></td>
<td><span data-ttu-id="a5b23-135">Sie können <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">getMessageExtraInfo</a> für den <strong>WM_LBUTTONDOWN</strong> und <strong>WM_LBUTTONUP</strong> Nachrichten aufrufen, um die Quelle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a5b23-135">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="a5b23-136">Der folgende Code zeigt, wie dies möglich wäre.</span><span class="sxs-lookup"><span data-stu-id="a5b23-136">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5b23-137">C++</span><span class="sxs-lookup"><span data-stu-id="a5b23-137">C++</span></span></th>
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



 



|          |                                                                                    |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-138">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-138">Issue</span></span>    | <span data-ttu-id="a5b23-139">Gewusst wie Microsoft Pixel Sense-Anwendungen unter Windows 7 ausführen?</span><span class="sxs-lookup"><span data-stu-id="a5b23-139">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="a5b23-140">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-140">Cause</span></span>    | <span data-ttu-id="a5b23-141">Windows-Fingereingabe und Microsoft Pixel Sense sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a5b23-141">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="a5b23-142">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-142">Solution</span></span> | <span data-ttu-id="a5b23-143">Sie müssen entweder die Windows 7-Plattform oder die Microsoft Pixel Sense-Plattform als Zielplattform haben.</span><span class="sxs-lookup"><span data-stu-id="a5b23-143">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="a5b23-144">Problembehandlung bei Manipulationen und Trägheit</span><span class="sxs-lookup"><span data-stu-id="a5b23-144">Troubleshooting Manipulations and Inertia</span></span>



|          |                                                                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-145">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-145">Issue</span></span>    | <span data-ttu-id="a5b23-146">Meine Anwendung wird aus irgendeinem Grund eingefroren.</span><span class="sxs-lookup"><span data-stu-id="a5b23-146">My application is freezing for no reason.</span></span> <span data-ttu-id="a5b23-147">Ich erhalte Zugriffs Verletzungen, wenn ich meine Objekt Schnittstellen initialisierte.</span><span class="sxs-lookup"><span data-stu-id="a5b23-147">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="a5b23-148">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-148">Cause</span></span>    | <span data-ttu-id="a5b23-149">Ein Aufruf von **CoInitialize** fehlt, wenn die Schnittstellen [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) oder [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5b23-149">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="a5b23-150">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-150">Solution</span></span> | <span data-ttu-id="a5b23-151">Dies kann dadurch verursacht werden, dass die Windows-Fingereingabe Component Object Model (com)-Objekte instanziiert werden, ohne CoInitialize Aufrufs</span><span class="sxs-lookup"><span data-stu-id="a5b23-151">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="a5b23-152">Dies tritt manchmal auf, wenn Sie Projekte von der Verwendung von Gesten in mithilfe der Manipulationen oder der Trägheits Schnittstellen umrechnen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-152">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-153">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-153">Issue</span></span>    | <span data-ttu-id="a5b23-154">Das Objekt wird beim Übersetzen nicht ordnungsgemäß rotiert.</span><span class="sxs-lookup"><span data-stu-id="a5b23-154">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="a5b23-155">Die Einzel Finger Drehung funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="a5b23-155">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5b23-156">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-156">Cause</span></span>    | <span data-ttu-id="a5b23-157">Nicht ordnungsgemäß Festlegung von Pivots für ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-157">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a5b23-158">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-158">Solution</span></span> | <span data-ttu-id="a5b23-159">Sie richten die Manipulations Punkt Punkte nicht ordnungsgemäß ein.</span><span class="sxs-lookup"><span data-stu-id="a5b23-159">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="a5b23-160">Legen Sie die Eigenschaften [**pivotpointx**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) und [**pivotpointy**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) auf den Mittelpunkt des Objekts oder Punkts fest, um das Sie drehen möchten, und legen Sie die Eigenschaft [**pivotradius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) auf den RADIUS Ihres Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="a5b23-160">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="a5b23-161">Problembehandlung bei Windows-Eingabe Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5b23-161">Troubleshooting Windows Touch Input</span></span>



|          |                                                                                                                                                                                                                                                                                                                                        |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-162">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-162">Issue</span></span>    | <span data-ttu-id="a5b23-163">Nachdem ich die [**WM- \_ touchnachricht**](wm-touchdown.md) verarbeitet habe, erhalte ich kein Feedback mehr.</span><span class="sxs-lookup"><span data-stu-id="a5b23-163">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5b23-164">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-164">Cause</span></span>    | <span data-ttu-id="a5b23-165">Verwenden der [**WM \_**](wm-touchdown.md) -Fingereingabe Nachricht, ohne Sie zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="a5b23-165">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5b23-166">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-166">Solution</span></span> | <span data-ttu-id="a5b23-167">Sie verbrauchen wahrscheinlich eine Windows-Berührungs Nachricht, ohne Sie an **defwindowproc** weiterzuleiten, was zu unerwartetem Verhalten führt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-167">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="a5b23-168">Weitere Informationen zur ordnungsgemäßen Behandlung von WM-Fingerabdruck Nachrichten finden Sie unter [**\_**](wm-touchdown.md) [Getting Started with Windows Touchscreen Messages](getting-started-with-multi-touch-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b23-168">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5b23-169">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-169">Issue</span></span></td>
<td><span data-ttu-id="a5b23-170">Ich füge Windows. h ein, aber es wird immer noch angegeben, dass <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a5b23-170">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5b23-171">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-171">Cause</span></span></td>
<td><span data-ttu-id="a5b23-172">Die Windows-Version in "targetver. h" ist falsch.</span><span class="sxs-lookup"><span data-stu-id="a5b23-172">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5b23-173">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-173">Solution</span></span></td>
<td><span data-ttu-id="a5b23-174">Sie haben die richtige Windows-Version nicht in Ihrem Projekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-174">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="a5b23-175">Der folgende Code veranschaulicht die ordnungsgemäße Festlegung von Windows-Versionen für Windows-Finger Eingaben in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a5b23-175">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5b23-176">C++</span><span class="sxs-lookup"><span data-stu-id="a5b23-176">C++</span></span></th>
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
<td><span data-ttu-id="a5b23-177">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-177">Issue</span></span></td>
<td><span data-ttu-id="a5b23-178">Die x-Koordinaten und y-Koordinaten für die Fingereingabe sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="a5b23-178">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="a5b23-179">Dabei handelt es sich entweder um größere Werte als erwartet, oder es handelt sich um negative Werte.</span><span class="sxs-lookup"><span data-stu-id="a5b23-179">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5b23-180">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-180">Cause</span></span></td>
<td><span data-ttu-id="a5b23-181">Möglicherweise müssen Sie Ihre touchpunkte in Pixel konvertieren, oder Sie müssen die Bildschirm Koordinaten konvertieren.</span><span class="sxs-lookup"><span data-stu-id="a5b23-181">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5b23-182">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-182">Solution</span></span></td>
<td><span data-ttu-id="a5b23-183">Stellen Sie sicher, dass Sie <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> und <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-183">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="a5b23-184">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a5b23-184">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5b23-185">C++</span><span class="sxs-lookup"><span data-stu-id="a5b23-185">C++</span></span></th>
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
<span data-ttu-id="a5b23-186">Um die <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> -Funktion verwenden zu können, müssen Sie in Ihrer Anwendung über eine hohe dpi-Unterstützung verfügen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-186">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="a5b23-187">Weitere Informationen zur Unterstützung von High dpi finden Sie im Abschnitt " <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High dpi</a> " in MSDN.</span><span class="sxs-lookup"><span data-stu-id="a5b23-187">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-188">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-188">Issue</span></span>    | <span data-ttu-id="a5b23-189">Ich sehe keine [**WM- \_ touchnachrichten**](wm-touchdown.md) , aber ich weiß, dass die Windows-Toucheingabe funktioniert, weil ich [**WM- \_ Gesten**](wm-gesture.md) Meldungen sehe.</span><span class="sxs-lookup"><span data-stu-id="a5b23-189">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="a5b23-190">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-190">Cause</span></span>    | <span data-ttu-id="a5b23-191">Fehlendes Aufrufen von [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="a5b23-191">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="a5b23-192">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-192">Solution</span></span> | <span data-ttu-id="a5b23-193">[**WM \_ Touchnachrichten**](wm-touchdown.md) und [**WM- \_ Gesten**](wm-gesture.md) schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="a5b23-193">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="a5b23-194">Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)nicht aufrufen, werden nur Nachrichten der **WM- \_ Geste** empfangen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-194">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-195">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-195">Issue</span></span>    | <span data-ttu-id="a5b23-196">Ich sehe kleine Verzögerungen ab dem Zeitpunkt, an dem ich meinen Finger eingebe, wenn ich Eingaben in meiner Anwendung erhalte.</span><span class="sxs-lookup"><span data-stu-id="a5b23-196">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a5b23-197">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-197">Cause</span></span>    | <span data-ttu-id="a5b23-198">Bei der über Gabe von Palmen wird die Eingabe verzögert.</span><span class="sxs-lookup"><span data-stu-id="a5b23-198">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a5b23-199">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-199">Solution</span></span> | <span data-ttu-id="a5b23-200">Wenn **TWF \_ wantpalm** in Aufrufen von [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)festgelegt ist, ist die Überlegung von Palmen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a5b23-200">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="a5b23-201">Dies verursacht eine kurze (100 ms) Verzögerung, während die Software testet, ob die Eingabe von einem Finger, Stift oder der Benutzer Palme stammt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-201">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="a5b23-202">Deaktivieren Sie die durch den Aufruf von " **RegisterTouchWindow** " mit aktiviertem **TWF- \_ wantpalm** -Flag.</span><span class="sxs-lookup"><span data-stu-id="a5b23-202">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="a5b23-203">Problembehandlung bei Windows-Touchgesten</span><span class="sxs-lookup"><span data-stu-id="a5b23-203">Troubleshooting Windows Touch Gestures</span></span>



|          |                                                                                                                                                                                                                                                                                                                                                                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-204">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-204">Issue</span></span>    | <span data-ttu-id="a5b23-205">Nach der Verarbeitung der [**WM- \_ Gesten**](wm-gesture.md) Nachricht wird das Feedback zu Grenzen nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-205">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="a5b23-206">Oder eine Geste, die zuvor funktionierte, funktioniert jetzt nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="a5b23-206">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="a5b23-207">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-207">Cause</span></span>    | <span data-ttu-id="a5b23-208">Verwenden der [**WM- \_ Gesten**](wm-gesture.md) Nachricht, ohne Sie zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="a5b23-208">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a5b23-209">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-209">Solution</span></span> | <span data-ttu-id="a5b23-210">Sie verbrauchen wahrscheinlich eine Windows-Berührungs Nachricht, ohne Sie an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)weiterzuleiten, was zu unerwartetem Verhalten führt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-210">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="a5b23-211">Weitere Informationen zum ordnungsgemäßen verarbeiten von WM-Gesten Nachrichten finden Sie unter [**\_**](wm-gesture.md) [Getting Started with Windows Gesten](getting-started-with-multi-touch-gestures.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b23-211">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



|          |                                                                                                                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-212">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-212">Issue</span></span>    | <span data-ttu-id="a5b23-213">Ich sehe keine [**WM- \_ Gesten**](wm-gesture.md) Meldungen, aber ich weiß, dass die Windows-Toucheingabe funktioniert, weil ich [**WM- \_ touchnachrichten**](wm-touchdown.md) sehe.</span><span class="sxs-lookup"><span data-stu-id="a5b23-213">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="a5b23-214">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-214">Cause</span></span>    | <span data-ttu-id="a5b23-215">[**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-215">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="a5b23-216">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-216">Solution</span></span> | <span data-ttu-id="a5b23-217">[**WM \_ Touchnachrichten**](wm-touchdown.md) und [**WM- \_ Gesten**](wm-gesture.md) schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="a5b23-217">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="a5b23-218">Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, werden keine Nachrichten der **WM- \_ Geste** empfangen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-218">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5b23-219">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-219">Issue</span></span></td>
<td><span data-ttu-id="a5b23-220">Ich sehe nicht alle Gesten, die ich erwarte.</span><span class="sxs-lookup"><span data-stu-id="a5b23-220">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="a5b23-221">Ich sehe z. b. Gesten mit dem Bezeichner <strong>GID_PAN</strong> , aber nicht <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5b23-221">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5b23-222">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-222">Cause</span></span></td>
<td><span data-ttu-id="a5b23-223">Einige Gesten, wie z. b. die Drehungs Bewegung, sind standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a5b23-223">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5b23-224">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-224">Solution</span></span></td>
<td><span data-ttu-id="a5b23-225">Sie müssen <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>setgestureconfig</strong></a> aufrufen, wenn Sie eine <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> Nachricht erhalten, wie in der <strong>WM_GESTURENOTIFY</strong> Referenz beschrieben, oder Sie müssen einen Handler für die <strong>WM_GESTURENOTIFY</strong> Nachricht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-225">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="a5b23-226">Der folgende Code zeigt, wie ein Handler implementiert werden kann, um die Unterstützung für die Rotation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a5b23-226">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5b23-227">C++</span><span class="sxs-lookup"><span data-stu-id="a5b23-227">C++</span></span></th>
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

<span data-ttu-id="a5b23-228">Weitere Beispiele für typische Gesten Konfigurationen finden Sie unter <strong>setgestureconfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5b23-228">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-229">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-229">Issue</span></span>    | <span data-ttu-id="a5b23-230">Die benutzerdefinierten Schiebe leisten in meiner Anwendung führen beim Ausführen der Schwenkbewegung keinen Bildlauf durch.</span><span class="sxs-lookup"><span data-stu-id="a5b23-230">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a5b23-231">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-231">Cause</span></span>    | <span data-ttu-id="a5b23-232">Fehlende Handler für die korrekten WM- \_ \* scrollnachrichten.</span><span class="sxs-lookup"><span data-stu-id="a5b23-232">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a5b23-233">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-233">Solution</span></span> | <span data-ttu-id="a5b23-234">Sie behandeln nicht alle WM- \_ \* scrollnachrichten in den benutzerdefinierten Schiebe leisten.</span><span class="sxs-lookup"><span data-stu-id="a5b23-234">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="a5b23-235">Es wird empfohlen, die WM- [**\_ Gesten**](wm-gesture.md) Nachricht zu verarbeiten, anstatt die benutzerdefinierte Bild Lauf Leiste-Funktionalität durch Legacy Unterstützung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="a5b23-235">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="a5b23-236">Sie müssen Nachrichten unterstützen, wie im Abschnitt [Legacy Unterstützung für das Schwenken mit](legacy-support-for-panning-with-scrollbars.md)Bild Lauf leisten ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a5b23-236">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



|          |                                                                                                                                                                                                                                                                 |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b23-237">Problem</span><span class="sxs-lookup"><span data-stu-id="a5b23-237">Issue</span></span>    | <span data-ttu-id="a5b23-238">Ich erhalte Verzögerungen bei Gesten.</span><span class="sxs-lookup"><span data-stu-id="a5b23-238">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a5b23-239">Ursache</span><span class="sxs-lookup"><span data-stu-id="a5b23-239">Cause</span></span>    | <span data-ttu-id="a5b23-240">Flicks können Verzögerungen bei Gesten verursachen.</span><span class="sxs-lookup"><span data-stu-id="a5b23-240">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="a5b23-241">Lösung</span><span class="sxs-lookup"><span data-stu-id="a5b23-241">Solution</span></span> | <span data-ttu-id="a5b23-242">Flicks können Verzögerungen verursachen, wie lange es dauert, bis Ihre Anwendung [**WM- \_ Gesten**](wm-gesture.md) Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="a5b23-242">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="a5b23-243">Informationen zum Deaktivieren von Flicks finden Sie [unter Legacy Unterstützung für das Schwenken mit Scrollleisten](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b23-243">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a5b23-244">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5b23-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b23-245">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="a5b23-245">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 