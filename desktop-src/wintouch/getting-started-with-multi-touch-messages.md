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
# <a name="getting-started-with-windows-touch-messages"></a>Ersten Schritten mit Windows-Finger Eingabenachrichten

In diesem Abschnitt werden die Aufgaben erläutert, die im Zusammenhang mit der Verwendung von Windows-Fingereingabe Eingaben in Ihre Anwendung

Die folgenden Schritte werden in der Regel beim Arbeiten mit Windows-Finger Eingabenachrichten ausgeführt:

1.  Testen Sie die Funktionen des eingabedigitalisierers.
2.  Registrieren Sie sich, um Windows-Berührungs Nachrichten zu empfangen.
3.  Behandeln Sie die Nachrichten.

Die für Windows-Fingereingabe verwendete Nachricht ist WM-Fingerabdruck. [**\_**](wm-touchdown.md) Diese Meldung gibt die verschiedenen Kontakt Zustände mit einem Digitalisierer an.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Testen der Funktionen des Eingabe-Digitalisierers

Die [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion kann verwendet werden, um die Funktionen des Eingabe-Digitalisierers abzufragen, indem der *nIndex* -Wert von **SM- \_ Digitalisierer** übergeben wird. [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) gibt ein Bitfeld zurück, das angibt, ob das Gerät bereit ist, ob das Gerät Stift oder Fingereingabe unterstützt, ob das Eingabegerät integriert oder extern ist und ob das Gerät mehrere Eingaben unterstützt (Windows-Fingereingabe). In der folgenden Tabelle sind die Bits für die verschiedenen Felder aufgeführt.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Wert | Stapel bereit | Mehrere Eingaben | Reserviert | Reserviert | Externer Stift | Integrierter Stift | Externer Touchscreen | Integrierter Touchscreen |



 

Um das Ergebnis des Befehls für ein bestimmtes Feature zu testen, können Sie den bitweisen & Operator und das zu testende Bit verwenden. Wenn Sie z. b. auf Windows-Finger Eingaben testen möchten, testen Sie, ob das-Bit der siebten Ordnung festgelegt ist (0x40 in Hex). Im folgenden Codebeispiel wird gezeigt, wie diese Werte getestet werden können.


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



In der folgenden Tabelle sind die Konstanten aufgelistet, die in Windows. h zum Testen von Berührungs Funktionen des Eingabe-Digitalisierers definiert sind.



| Name                   | Wert      | BESCHREIBUNG                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tablet \_ config \_ None   | 0x00000000 | Der eingabedigitalisierer hat keine Berührungs Funktionen.                                                                                                                                         |
| NID- \_ integrierter \_ Touchscreen | 0x00000001 | Ein integrierter Touchscreen-Digitalisierer wird für Eingaben verwendet.                                                                                                                                              |
| NID \_ externe Fingereingabe \_   | 0x00000002 | Ein externer Fingerabdruck-Digitalisierer wird für Eingaben verwendet.                                                                                                                                                |
| NID \_ integrierter \_ Stift   | 0x00000004 | Ein integrierter Stift-Digitalisierer wird für Eingaben verwendet.                                                                                                                                                |
| externer NID- \_ \_ Stift     | 0x00000008 | Ein externer Stift-Digitalisierer wird für die Eingabe verwendet.                                                                                                                                                  |
| NID \_ - \_ multieingabe      | 0x00000040 | Für die Eingabe wird ein Eingabe-Digitalisierer mit Unterstützung für mehrere Eingaben verwendet.                                                                                                                        |
| NID \_ bereit             | 0x00000080 | Der eingabedigitalisierer ist bereit für die Eingabe. Wenn dieser Wert nicht festgelegt ist, kann dies bedeuten, dass der Tablet-Dienst beendet wird, der Digitalisierer nicht unterstützt wird oder keine Digitalisierungs Treiber installiert wurden. |



 

Das Überprüfen der NID- \_ \* Werte ist eine nützliche Möglichkeit, um die Funktionen des Computers eines Benutzers zu überprüfen, um die Anwendung für die Eingabe von Finger Eingaben, Pen oder nicht-Tablet-Eingaben zu konfigurieren. Wenn Sie z. b. eine dynamische Benutzeroberfläche (UI) haben und einige davon automatisch konfigurieren möchten, können Sie die Option NID \_ Integrated \_ Touch, NID \_ Multitouch und die maximale Anzahl von Berührungen erhalten, wenn ein Benutzer die Anwendung zum ersten Mal ausführt.

> [!Note]  
> Es gibt einige Einschränkungen für SM \_ GetSystemMetrics. Beispielsweise gibt es keine Unterstützung für Plug & amp; Play. Verwenden Sie aus diesem Grund Vorsicht, wenn Sie diese Funktion als Mittel für die permanente Konfiguration verwenden.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registrieren für den Empfang von Windows-Eingabe Eingaben

Vor dem Empfang von Windows-Fingereingabe Eingaben müssen Anwendungen zuerst registriert werden, um Windows-Eingabe Eingaben zu empfangen. Wenn Sie das Anwendungsfenster registrieren, gibt die Anwendung an, dass Sie Berührungs kompatibel ist. Nachdem die Anwendung das Fenster registriert hat, werden Benachrichtigungen vom Windows-Fingerabdruck Treiber an die Anwendung weitergeleitet, wenn Eingaben im Fenster vorgenommen werden. Wenn die Anwendung heruntergefahren wird, hebt Sie die Registrierung Ihres Fensters auf, um Benachrichtigungen zu deaktivieren.

> [!Note]  
> [**WM \_ Berührungs**](wm-touchdown.md) Nachrichten sind zurzeit "gierige". Nachdem die erste Fingereingabe Nachricht in einem Fenster empfangen wurde, werden alle Berührungs Meldungen an dieses Fenster gesendet, bis ein anderes Fenster den Fokus erhält.

 

> [!Note]  
> Standardmäßig erhalten Sie [**WM- \_ Gesten**](wm-gesture.md) Nachrichten anstelle von [**WM- \_ touchnachrichten**](wm-touchdown.md) . Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, wird der Empfang von **WM- \_ Gesten** Nachrichten beendet.

 

Der folgende Code veranschaulicht, wie eine Anwendung registriert werden kann, um Windows-Fingerabdruck Nachrichten in einer Win32-Anwendung zu empfangen.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Verarbeiten von Windows-Fingerabdruck Meldungen

Sie können die Windows-Finger Eingabenachrichten von Anwendungen in Windows-Betriebssystemen in vielerlei Hinsicht verarbeiten. Wenn Sie eine GUI-Anwendung programmieren, fügen Sie Code in der Funktion hinzu, `WndProc` um die Nachrichten zu verarbeiten, die von Interesse sind. Wenn Sie eine Microsoft Foundation Class (MFC) oder eine verwaltete Anwendung programmieren, fügen Sie Handler für die Nachrichten ein, die von Interesse sind. Im folgenden Codebeispiel wird gezeigt, wie Berührungs Nachrichten von WndProc in einer Windows-basierten Anwendung verarbeitet werden können.


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





Der folgende Code zeigt, wie Sie die Meldungs Zuordnung und einen Nachrichten Handler implementieren können. Beachten Sie, dass die Nachrichten in der Meldungs Zuordnung deklariert werden müssen. Anschließend sollte der Handler für die Nachricht implementiert werden. In einer MFC-Anwendung könnte dies z. b. im Dialog Code deklariert werden. Beachten Sie auch, dass die- `OnInitDialog` Funktion für das Dialogfenster einen aufzurufenden [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) -Befehl enthalten muss, z `RegisterTouchWindow(m_hWnd, 0)` . b..


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



Wenn Sie das Fenster berühren, werden Berührungen aus einem Popup Fenster angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eingabe Eingabe](guide-multi-touch-input.md)
</dt> </dl>

 

 