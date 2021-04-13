---
title: Ersten Schritten mit Windows-Finger Eingabenachrichten
description: In diesem Abschnitt werden die Aufgaben erläutert, die im Zusammenhang mit der Verwendung von Windows-Fingereingabe Eingaben in Ihre Anwendung
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows-Fingereingabe, Meldungen
- Windows-Fingereingabe, registrieren für Fingereingabe
- Windows-Fingereingabe, Testen von Eingabe-Digitalisierern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390455"
---
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="be844-106">Ersten Schritten mit Windows-Finger Eingabenachrichten</span><span class="sxs-lookup"><span data-stu-id="be844-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="be844-107">In diesem Abschnitt werden die Aufgaben erläutert, die im Zusammenhang mit der Verwendung von Windows-Fingereingabe Eingaben in Ihre Anwendung</span><span class="sxs-lookup"><span data-stu-id="be844-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="be844-108">Die folgenden Schritte werden in der Regel beim Arbeiten mit Windows-Finger Eingabenachrichten ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="be844-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="be844-109">Testen Sie die Funktionen des eingabedigitalisierers.</span><span class="sxs-lookup"><span data-stu-id="be844-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="be844-110">Registrieren Sie sich, um Windows-Berührungs Nachrichten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="be844-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="be844-111">Behandeln Sie die Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="be844-111">Handle the messages.</span></span>

<span data-ttu-id="be844-112">Die für Windows-Fingereingabe verwendete Nachricht ist WM-Fingerabdruck. [**\_**](wm-touchdown.md)</span><span class="sxs-lookup"><span data-stu-id="be844-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="be844-113">Diese Meldung gibt die verschiedenen Kontakt Zustände mit einem Digitalisierer an.</span><span class="sxs-lookup"><span data-stu-id="be844-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="be844-114">Testen der Funktionen des Eingabe-Digitalisierers</span><span class="sxs-lookup"><span data-stu-id="be844-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="be844-115">Die [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion kann verwendet werden, um die Funktionen des Eingabe-Digitalisierers abzufragen, indem der *nIndex* -Wert von **SM- \_ Digitalisierer** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="be844-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="be844-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) gibt ein Bitfeld zurück, das angibt, ob das Gerät bereit ist, ob das Gerät Stift oder Fingereingabe unterstützt, ob das Eingabegerät integriert oder extern ist und ob das Gerät mehrere Eingaben unterstützt (Windows-Fingereingabe).</span><span class="sxs-lookup"><span data-stu-id="be844-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="be844-117">In der folgenden Tabelle sind die Bits für die verschiedenen Felder aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="be844-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="be844-118">bit</span><span class="sxs-lookup"><span data-stu-id="be844-118">Bit</span></span>   | <span data-ttu-id="be844-119">8</span><span class="sxs-lookup"><span data-stu-id="be844-119">8</span></span>           | <span data-ttu-id="be844-120">7</span><span class="sxs-lookup"><span data-stu-id="be844-120">7</span></span>           | <span data-ttu-id="be844-121">6</span><span class="sxs-lookup"><span data-stu-id="be844-121">6</span></span>        | <span data-ttu-id="be844-122">5</span><span class="sxs-lookup"><span data-stu-id="be844-122">5</span></span>        | <span data-ttu-id="be844-123">4</span><span class="sxs-lookup"><span data-stu-id="be844-123">4</span></span>            | <span data-ttu-id="be844-124">3</span><span class="sxs-lookup"><span data-stu-id="be844-124">3</span></span>              | <span data-ttu-id="be844-125">2</span><span class="sxs-lookup"><span data-stu-id="be844-125">2</span></span>              | <span data-ttu-id="be844-126">1</span><span class="sxs-lookup"><span data-stu-id="be844-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="be844-127">Wert</span><span class="sxs-lookup"><span data-stu-id="be844-127">Value</span></span> | <span data-ttu-id="be844-128">Stapel bereit</span><span class="sxs-lookup"><span data-stu-id="be844-128">Stack Ready</span></span> | <span data-ttu-id="be844-129">Mehrere Eingaben</span><span class="sxs-lookup"><span data-stu-id="be844-129">Multi-input</span></span> | <span data-ttu-id="be844-130">Reserviert</span><span class="sxs-lookup"><span data-stu-id="be844-130">Reserved</span></span> | <span data-ttu-id="be844-131">Reserviert</span><span class="sxs-lookup"><span data-stu-id="be844-131">Reserved</span></span> | <span data-ttu-id="be844-132">Externer Stift</span><span class="sxs-lookup"><span data-stu-id="be844-132">External Pen</span></span> | <span data-ttu-id="be844-133">Integrierter Stift</span><span class="sxs-lookup"><span data-stu-id="be844-133">Integrated Pen</span></span> | <span data-ttu-id="be844-134">Externer Touchscreen</span><span class="sxs-lookup"><span data-stu-id="be844-134">External Touch</span></span> | <span data-ttu-id="be844-135">Integrierter Touchscreen</span><span class="sxs-lookup"><span data-stu-id="be844-135">Integrated Touch</span></span> |



 

<span data-ttu-id="be844-136">Um das Ergebnis des Befehls für ein bestimmtes Feature zu testen, können Sie den bitweisen & Operator und das zu testende Bit verwenden.</span><span class="sxs-lookup"><span data-stu-id="be844-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="be844-137">Wenn Sie z. b. auf Windows-Finger Eingaben testen möchten, testen Sie, ob das-Bit der siebten Ordnung festgelegt ist (0x40 in Hex).</span><span class="sxs-lookup"><span data-stu-id="be844-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="be844-138">Im folgenden Codebeispiel wird gezeigt, wie diese Werte getestet werden können.</span><span class="sxs-lookup"><span data-stu-id="be844-138">The following code example shows how these values could be tested.</span></span>


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



<span data-ttu-id="be844-139">In der folgenden Tabelle sind die Konstanten aufgelistet, die in Windows. h zum Testen von Berührungs Funktionen des Eingabe-Digitalisierers definiert sind.</span><span class="sxs-lookup"><span data-stu-id="be844-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="be844-140">Name</span><span class="sxs-lookup"><span data-stu-id="be844-140">Name</span></span>                   | <span data-ttu-id="be844-141">Wert</span><span class="sxs-lookup"><span data-stu-id="be844-141">Value</span></span>      | <span data-ttu-id="be844-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be844-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be844-143">Tablet \_ config \_ None</span><span class="sxs-lookup"><span data-stu-id="be844-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="be844-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be844-144">0x00000000</span></span> | <span data-ttu-id="be844-145">Der eingabedigitalisierer hat keine Berührungs Funktionen.</span><span class="sxs-lookup"><span data-stu-id="be844-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="be844-146">NID- \_ integrierter \_ Touchscreen</span><span class="sxs-lookup"><span data-stu-id="be844-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="be844-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be844-147">0x00000001</span></span> | <span data-ttu-id="be844-148">Ein integrierter Touchscreen-Digitalisierer wird für Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="be844-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="be844-149">NID \_ externe Fingereingabe \_</span><span class="sxs-lookup"><span data-stu-id="be844-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="be844-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="be844-150">0x00000002</span></span> | <span data-ttu-id="be844-151">Ein externer Fingerabdruck-Digitalisierer wird für Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="be844-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="be844-152">NID \_ integrierter \_ Stift</span><span class="sxs-lookup"><span data-stu-id="be844-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="be844-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="be844-153">0x00000004</span></span> | <span data-ttu-id="be844-154">Ein integrierter Stift-Digitalisierer wird für Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="be844-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="be844-155">externer NID- \_ \_ Stift</span><span class="sxs-lookup"><span data-stu-id="be844-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="be844-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="be844-156">0x00000008</span></span> | <span data-ttu-id="be844-157">Ein externer Stift-Digitalisierer wird für die Eingabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="be844-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="be844-158">NID \_ - \_ multieingabe</span><span class="sxs-lookup"><span data-stu-id="be844-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="be844-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="be844-159">0x00000040</span></span> | <span data-ttu-id="be844-160">Für die Eingabe wird ein Eingabe-Digitalisierer mit Unterstützung für mehrere Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="be844-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="be844-161">NID \_ bereit</span><span class="sxs-lookup"><span data-stu-id="be844-161">NID\_READY</span></span>             | <span data-ttu-id="be844-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="be844-162">0x00000080</span></span> | <span data-ttu-id="be844-163">Der eingabedigitalisierer ist bereit für die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="be844-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="be844-164">Wenn dieser Wert nicht festgelegt ist, kann dies bedeuten, dass der Tablet-Dienst beendet wird, der Digitalisierer nicht unterstützt wird oder keine Digitalisierungs Treiber installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="be844-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="be844-165">Das Überprüfen der NID- \_ \* Werte ist eine nützliche Möglichkeit, um die Funktionen des Computers eines Benutzers zu überprüfen, um die Anwendung für die Eingabe von Finger Eingaben, Pen oder nicht-Tablet-Eingaben zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="be844-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="be844-166">Wenn Sie z. b. eine dynamische Benutzeroberfläche (UI) haben und einige davon automatisch konfigurieren möchten, können Sie die Option NID \_ Integrated \_ Touch, NID \_ Multitouch und die maximale Anzahl von Berührungen erhalten, wenn ein Benutzer die Anwendung zum ersten Mal ausführt.</span><span class="sxs-lookup"><span data-stu-id="be844-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="be844-167">Es gibt einige Einschränkungen für SM \_ GetSystemMetrics.</span><span class="sxs-lookup"><span data-stu-id="be844-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="be844-168">Beispielsweise gibt es keine Unterstützung für Plug & amp; Play.</span><span class="sxs-lookup"><span data-stu-id="be844-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="be844-169">Verwenden Sie aus diesem Grund Vorsicht, wenn Sie diese Funktion als Mittel für die permanente Konfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="be844-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="be844-170">Registrieren für den Empfang von Windows-Eingabe Eingaben</span><span class="sxs-lookup"><span data-stu-id="be844-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="be844-171">Vor dem Empfang von Windows-Fingereingabe Eingaben müssen Anwendungen zuerst registriert werden, um Windows-Eingabe Eingaben zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="be844-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="be844-172">Wenn Sie das Anwendungsfenster registrieren, gibt die Anwendung an, dass Sie Berührungs kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="be844-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="be844-173">Nachdem die Anwendung das Fenster registriert hat, werden Benachrichtigungen vom Windows-Fingerabdruck Treiber an die Anwendung weitergeleitet, wenn Eingaben im Fenster vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="be844-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="be844-174">Wenn die Anwendung heruntergefahren wird, hebt Sie die Registrierung Ihres Fensters auf, um Benachrichtigungen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="be844-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="be844-175">[**WM \_ Berührungs**](wm-touchdown.md) Nachrichten sind zurzeit "gierige".</span><span class="sxs-lookup"><span data-stu-id="be844-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="be844-176">Nachdem die erste Fingereingabe Nachricht in einem Fenster empfangen wurde, werden alle Berührungs Meldungen an dieses Fenster gesendet, bis ein anderes Fenster den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="be844-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="be844-177">Standardmäßig erhalten Sie [**WM- \_ Gesten**](wm-gesture.md) Nachrichten anstelle von [**WM- \_ touchnachrichten**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="be844-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="be844-178">Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, wird der Empfang von **WM- \_ Gesten** Nachrichten beendet.</span><span class="sxs-lookup"><span data-stu-id="be844-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="be844-179">Der folgende Code veranschaulicht, wie eine Anwendung registriert werden kann, um Windows-Fingerabdruck Nachrichten in einer Win32-Anwendung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="be844-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="be844-180">Verarbeiten von Windows-Fingerabdruck Meldungen</span><span class="sxs-lookup"><span data-stu-id="be844-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="be844-181">Sie können die Windows-Finger Eingabenachrichten von Anwendungen in Windows-Betriebssystemen in vielerlei Hinsicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="be844-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="be844-182">Wenn Sie eine GUI-Anwendung programmieren, fügen Sie Code in der Funktion hinzu, `WndProc` um die Nachrichten zu verarbeiten, die von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="be844-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="be844-183">Wenn Sie eine Microsoft Foundation Class (MFC) oder eine verwaltete Anwendung programmieren, fügen Sie Handler für die Nachrichten ein, die von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="be844-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="be844-184">Im folgenden Codebeispiel wird gezeigt, wie Berührungs Nachrichten von WndProc in einer Windows-basierten Anwendung verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="be844-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





<span data-ttu-id="be844-185">Der folgende Code zeigt, wie Sie die Meldungs Zuordnung und einen Nachrichten Handler implementieren können.</span><span class="sxs-lookup"><span data-stu-id="be844-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="be844-186">Beachten Sie, dass die Nachrichten in der Meldungs Zuordnung deklariert werden müssen. Anschließend sollte der Handler für die Nachricht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="be844-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="be844-187">In einer MFC-Anwendung könnte dies z. b. im Dialog Code deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="be844-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="be844-188">Beachten Sie auch, dass die- `OnInitDialog` Funktion für das Dialogfenster einen aufzurufenden [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) -Befehl enthalten muss, z `RegisterTouchWindow(m_hWnd, 0)` . b..</span><span class="sxs-lookup"><span data-stu-id="be844-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



<span data-ttu-id="be844-189">Wenn Sie das Fenster berühren, werden Berührungen aus einem Popup Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="be844-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be844-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be844-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be844-191">Windows-Eingabe Eingabe</span><span class="sxs-lookup"><span data-stu-id="be844-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 