---
title: Erste Schritte mit Windows Touchnachrichten
description: In diesem Abschnitt werden die Aufgaben erläutert, die mit dem Abrufen Windows Toucheingabe verbunden sind, um in Ihrer Anwendung zu funktionieren.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch,Nachrichten
- Windows Toucheingabe,Registrierung für Toucheingabe
- Windows Toucheingabe,Testen von Eingabedymierern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3f1daac2aacf8ac4c34ccbf9b1ab8be63058c45096e181c8b2eecf4f5d2de6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055900"
---
# <a name="getting-started-with-windows-touch-messages"></a>Erste Schritte mit Windows Touchnachrichten

In diesem Abschnitt werden die Aufgaben erläutert, die mit dem Abrufen Windows Toucheingabe verbunden sind, um in Ihrer Anwendung zu funktionieren.

Die folgenden Schritte werden in der Regel bei der Arbeit mit Touchnachrichten Windows ausgeführt:

1.  Testen Sie die Funktionen des Eingabedymierers.
2.  Registrieren Sie sich für den Empfang Windows Touch-Nachrichten.
3.  Verarbeiten Sie die Nachrichten.

Die für touch verwendete Meldung Windows WM [**\_ TOUCH.**](wm-touchdown.md) Diese Meldung gibt die verschiedenen Kontaktzustände mit einem Digitizer an.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Testen der Funktionen des Eingabedymierers

Die [GetSystemMetrics-Funktion](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) kann verwendet werden, um die Funktionen des Eingabed digitizers durch Übergabe des *nIndex-Werts* von **SM \_ DIGITIZER abfragt.** [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) gibt ein Bitfeld zurück, das angibt, ob das Gerät bereit ist, ob das Gerät Stift oder Touch unterstützt, ob das Eingabegerät integriert oder extern ist und ob das Gerät mehrere Eingaben (Windows Touch) unterstützt. In der folgenden Tabelle sind die Bits für die verschiedenen Felder aufgeführt.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Wert | Stapelbereit | Mehrere Eingaben | Reserviert | Reserviert | Externer Stift | Integrierter Stift | Externe Touch-Touch-Verbindung | Integrierte Touch-Touch-Verbindung |



 

Um das Ergebnis des Befehls für ein bestimmtes Feature zu testen, können Sie den bitweise &-Operator und das bestimmte Bit verwenden, das Sie testen. Um z. B. auf Windows Touch zu testen, würden Sie testen, ob das Bit der siebten Ordnung festgelegt ist (0x40 hexadezimal). Das folgende Codebeispiel zeigt, wie diese Werte getestet werden können.


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



In der folgenden Tabelle sind die Konstanten aufgeführt, die in windows.h zum Testen der Touchfunktionen des Eingabedisierers definiert sind.



| Name                   | Wert      | BESCHREIBUNG                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TABLET \_ CONFIG \_ NONE   | 0x00000000 | Der Eingabed digitizer verfügt nicht über Touchfunktionen.                                                                                                                                         |
| NID \_ INTEGRATED \_ TOUCH | 0x00000001 | Ein integrierter Touch-Digitizer wird für die Eingabe verwendet.                                                                                                                                              |
| NID \_ EXTERNAL \_ TOUCH   | 0x00000002 | Ein externer Touch-Digitizer wird für die Eingabe verwendet.                                                                                                                                                |
| NID \_ INTEGRATED \_ PEN   | 0x00000004 | Ein integrierter Stiftdisierer wird für die Eingabe verwendet.                                                                                                                                                |
| NID \_ EXTERNAL \_ PEN     | 0x00000008 | Ein externer Stiftdisierer wird für die Eingabe verwendet.                                                                                                                                                  |
| NID \_ MULTI \_ INPUT      | 0x00000040 | Ein Eingabed digitizer mit Unterstützung für mehrere Eingaben wird für die Eingabe verwendet.                                                                                                                        |
| NID \_ READY             | 0x00000080 | Der Eingabed digitizer ist für die Eingabe bereit. Wenn dieser Wert nicht fest ist, kann dies bedeuten, dass der Tablettdienst beendet wird, der Digitizer nicht unterstützt wird oder keine Digitizertreiber installiert wurden. |



 

Das Überprüfen der NID-Werte ist eine nützliche Möglichkeit, die Funktionen des Computers eines Benutzers zu überprüfen, um Ihre Anwendung für Toucheingaben, Stifte oder \_ \* Nicht-Tablet-Eingaben zu konfigurieren. Wenn Sie beispielsweise über eine dynamische Benutzeroberfläche (UI) verfügen und einige davon automatisch konfigurieren möchten, können Sie nach NID \_ INTEGRATED TOUCH und NID MULTITOUCH überprüfen und die maximale Anzahl von Berührungen erhalten, wenn ein Benutzer Ihre Anwendung zum ersten Mal \_ \_ ausgeführt.

> [!Note]  
> Es gibt einige inhärente Einschränkungen für SM \_ GETSYSTEMMETRICS. Plug & Play wird beispielsweise nicht unterstützt. Aus diesem Grund sollten Sie bei der Verwendung dieser Funktion als Mittel für eine dauerhafte Konfiguration mit Vorsicht vorgehen.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registrieren für den Empfang Windows Toucheingabe

Vor dem Empfang Windows Toucheingabe müssen sich Anwendungen zuerst registrieren, um touch-Windows empfangen zu können. Durch die Registrierung des Anwendungsfensters gibt die Anwendung an, dass es touchkompatibel ist. Nachdem die Anwendung ihr Fenster registriert hat, werden Benachrichtigungen vom Windows Touch-Treiber an die Anwendung weitergeleitet, wenn eine Eingabe im Fenster erfolgt. Wenn die Anwendung heruntergefahren wird, wird die Registrierung ihres Fensters aufgehoben, um Benachrichtigungen zu deaktivieren.

> [!Note]  
> [**WM \_ TOUCH-Nachrichten**](wm-touchdown.md) sind derzeit "gierig". Nachdem die erste Berührungsnachricht in einem Fenster empfangen wurde, werden alle Touchnachrichten an dieses Fenster gesendet, bis ein anderes Fenster den Fokus erhält.

 

> [!Note]  
> Standardmäßig erhalten Sie [**WM \_ GESTURE-Nachrichten**](wm-gesture.md) anstelle von [**WM \_ TOUCH-Nachrichten.**](wm-touchdown.md) Wenn Sie [**RegisterTouchWindow aufrufen,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)empfangen Sie keine **WM \_ GESTURE-Nachrichten** mehr.

 

Der folgende Code veranschaulicht, wie sich eine Anwendung für den Empfang Windows Touch-Nachrichten in einer Win32-Anwendung registrieren kann.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Behandeln Windows Touchnachrichten

Sie können die Windows Touch-Nachrichten von Anwendungen in Windows betriebssystemen auf viele Verschiedenes verarbeiten. Wenn Sie eine GUI-Anwendung programmieren, fügen Sie Code innerhalb der Funktion `WndProc` hinzu, um die für Sie interessanten Nachrichten zu verarbeiten. Wenn Sie eine Microsoft Foundation Class (MFC) oder eine verwaltete Anwendung programmieren, fügen Sie Handler für die nachrichten von Interesse hinzu. Das folgende Codebeispiel zeigt, wie Touchnachrichten von WndProc in einer Windows-basierten Anwendung behandelt werden können.


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





Der folgende Code zeigt, wie Sie die Meldungszuordnung und einen Meldungshandler implementieren können. Beachten Sie, dass die Nachrichten in der Meldungszuordnung deklariert werden müssen, und dann sollte der Handler für die Nachricht implementiert werden. In einer MFC-Anwendung könnte dies beispielsweise im Dialogcode deklariert werden. Beachten Sie auch, dass die Funktion für Ihr Dialogfeld einen Aufruf von `OnInitDialog` [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) wie enthalten `RegisterTouchWindow(m_hWnd, 0)` muss.


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



Wenn Sie das Fenster berühren, werden Berührungen in einem Popupfenster angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Toucheingabe](guide-multi-touch-input.md)
</dt> </dl>

 

 