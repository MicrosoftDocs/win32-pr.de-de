---
title: Behandeln von Bildschirmschonern
description: Die Microsoft Win32-API unterstützt spezielle Anwendungen, die als Bildschirmschoner bezeichnet werden.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- Bildschirmschoner
- Systemsteuerung, Bildschirmschoner
- ScreenSaverConfigureDialog
- Moduldefinitionsdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61343cd586ed022c334b797a77320ee25eccdf48653b4732adc597f4aedde26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975720"
---
# <a name="handling-screen-savers"></a>Behandeln von Bildschirmschonern

Die Microsoft Win32-API unterstützt spezielle Anwendungen, die als *Bildschirmschoner* bezeichnet werden. Bildschirmschoner werden gestartet, wenn sich Maus und Tastatur für einen bestimmten Zeitraum im Leerlauf befinden. Sie werden aus den folgenden beiden Gründen verwendet:

-   Zum Schutz eines Bildschirms vor Einembrand, der durch statische Bilder verursacht wird.
-   Zum Verbergen vertraulicher Informationen, die auf einem Bildschirm übrig bleiben.

Dieses Thema ist in die folgenden Abschnitte unterteilt.

-   [Informationen zu Bildschirmschonern](#about-screen-savers)
-   [Verwenden der Bildschirmschonerfunktionen](#using-the-screen-saver-functions)
    -   [Erstellen eines Bildschirmschonrs](#creating-a-screen-saver)
    -   [Installieren neuer Bildschirmschoner](#installing-new-screen-savers)
    -   [Hinzufügen von Hilfe zum Dialogfeld "Konfiguration des Bildschirmschoner"](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>Informationen zu Bildschirmschonern

Mit der Desktopanwendung im Windows Systemsteuerung können Benutzer aus einer Liste von Bildschirmschonern auswählen, angeben, wie viel Zeit verstreichen soll, bevor der Bildschirmschoner gestartet wird, Bildschirmschoner konfigurieren und Bildschirmschoner in der Vorschau anzeigen. Bildschirmschoner werden automatisch geladen, wenn Windows gestartet wird oder wenn ein Benutzer den Bildschirmschoner über die Systemsteuerung aktiviert.

Sobald ein Bildschirmschoner ausgewählt wurde, überwacht Windows Tastatureingaben und Mausbewegungen und startet den Bildschirmschoner nach einem Zeitraum der Inaktivität. Windows startet den Bildschirmschoner jedoch nicht, wenn eine der folgenden Bedingungen erfüllt ist:

-   Die aktive Anwendung ist keine Windows-basierte Anwendung.
-   Ein Computerbasiertes Trainingsfenster (CBT) ist vorhanden.
-   Die aktive Anwendung empfängt die [ \_ WM-SYSCOMMAND-Nachricht](../menurc/wm-syscommand.md) mit dem *wParam-Parameter,* der auf den SC \_ SCREENSAVE-Wert festgelegt ist, übergibt die Nachricht jedoch nicht an die [DefWindowProc-Funktion.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

**Sicherheitskontext des Bildschirmschoners**

Der Sicherheitskontext des Bildschirmschonrs hängt davon ab, ob ein Benutzer interaktiv angemeldet ist. Wenn ein Benutzer interaktiv angemeldet ist, wenn der Bildschirmschoner aufgerufen wird, wird der Bildschirmschoner im Sicherheitskontext des interaktiven Benutzers ausgeführt. Wenn kein Benutzer angemeldet ist, hängt der Sicherheitskontext des Bildschirmschonrs von der Verwendeten Version von Windows ab.

-   Windows XP und Windows 2000: Bildschirmschoner wird im Kontext von LocalSystem mit eingeschränkten Konten ausgeführt.
-   Windows 2003 wird der Bildschirmschoner im Kontext von LocalService ausgeführt, wobei alle Berechtigungen entfernt und die Administratorengruppe deaktiviert ist.
-   Gilt nicht für Windows NT4.

Der Sicherheitskontext bestimmt die Ebene der privilegierten Vorgänge, die über einen Bildschirmschoner ausgeführt werden können.

**Windows Vista und höher:** Wenn der Kennwortschutz durch eine Richtlinie aktiviert ist, wird der Bildschirmschoner unabhängig davon gestartet, was eine Anwendung mit der SC \_ SCREENSAVE-Benachrichtigung macht.

Bildschirmschoner enthalten bestimmte exportierte Funktionen, Ressourcendefinitionen und Variablendeklarationen. Die Bildschirmschonerbibliothek enthält die **Hauptfunktion** und anderen Startcode, die für einen Bildschirmschoner erforderlich sind. Wenn ein Bildschirmschoner gestartet wird, erstellt der Startcode in der Bildschirmschonerbibliothek ein Vollbildfenster. Die Fensterklasse für dieses Fenster wird wie folgt deklariert:


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



Um einen Bildschirmschoner zu erstellen, erstellen die meisten Entwickler ein Quellcodemodul mit drei erforderlichen Funktionen und verknüpfen sie mit der Bildschirmschonerbibliothek. Ein Bildschirmschonermodul ist nur für die Konfiguration selbst und die Bereitstellung visueller Effekte verantwortlich.

Eine der drei erforderlichen Funktionen in einem Bildschirmschonermodul ist [**ScreenSaverProc.**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) Diese Funktion verarbeitet bestimmte Nachrichten und übergibt alle nicht verarbeiteten Nachrichten zurück an die Bildschirmschonerbibliothek. Im Folgenden sind einige der typischen Nachrichten dargestellt, die von **ScreenSaverProc** verarbeitet werden.



| Nachricht        | Bedeutung                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CREATE     | Rufen Sie alle Initialisierungsdaten aus der Regedit.ini-Datei ab. Legen Sie einen Fenstertimer für das Bildschirmschonerfenster fest. Führen Sie alle anderen erforderlichen Initialisierungen aus.                                     |
| WM \_ ERASEBKGND | Löschen Sie das Bildschirmschonerfenster, und bereiten Sie sich auf nachfolgende Zeichnungsvorgänge vor.                                                                                                               |
| WM \_ TIMER      | Ausführen von Zeichnungsvorgängen.                                                                                                                                                                |
| WM \_ DESTROY    | Zerstören Sie die Timer, die erstellt wurden, als die Anwendung die [WM \_ CREATE-Nachricht](../winmsg/wm-create.md) verarbeitet hat. Führen Sie alle zusätzlichen erforderlichen Bereinigungen durch. |



 

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) übergibt nicht verarbeitete Nachrichten an die Bildschirmschonerbibliothek, indem die [**DefScreenSaverProc-Funktion**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) aufgerufen wird. In der folgenden Tabelle wird beschrieben, wie diese Funktion verschiedene Nachrichten verarbeitet.



| `Message`         | Aktion                                                                    |
|-----------------|---------------------------------------------------------------------------|
| WM \_ SETCURSOR   | Legen Sie den Cursor auf den NULL-Cursor fest, und entfernen Sie ihn vom Bildschirm.           |
| WM \_ PAINT       | Paint den Hintergrund des Bildschirms.                                              |
| WM \_ LBUTTONDOWN | Beenden Sie den Bildschirmschoner.                                               |
| WM \_ MBUTTONDOWN | Beenden Sie den Bildschirmschoner.                                               |
| WM \_ RBUTTONDOWN | Beenden Sie den Bildschirmschoner.                                               |
| WM \_ KEYDOWN     | Beenden Sie den Bildschirmschoner.                                               |
| WM \_ MOUSEMOVE   | Beenden Sie den Bildschirmschoner.                                               |
| WM \_ ACTIVATE    | Beenden Sie den Bildschirmschoner, wenn der *wParam-Parameter* auf **FALSE** festgelegt ist. |



 

Die zweite erforderliche Funktion in einem Bildschirmschonermodul ist [**ScreenSaverConfigureDialog.**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) Diese Funktion zeigt ein Dialogfeld an, in dem der Benutzer den Bildschirmschoner konfigurieren kann (eine Anwendung muss eine entsprechende Dialogfeldvorlage bereitstellen). Windows zeigt das Konfigurationsdialogfeld an, wenn der Benutzer im Dialogfeld Bildschirmschoner des Systemsteuerung die Schaltfläche **Setup** auswählt.

Die dritte erforderliche Funktion in einem Bildschirmschonermodul ist [**RegisterDialogClasses.**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) Diese Funktion muss von allen Bildschirmschoneranwendungen aufgerufen werden. Anwendungen, die keine speziellen Fenster oder benutzerdefinierten Steuerelemente im Konfigurationsdialogfeld benötigen, können jedoch einfach **TRUE** zurückgeben. Anwendungen, die spezielle Fenster oder benutzerdefinierte Steuerelemente erfordern, sollten diese Funktion verwenden, um die entsprechenden Fensterklassen zu registrieren.

Zusätzlich zum Erstellen eines Moduls, das die drei soeben beschriebenen Funktionen unterstützt, sollte ein Bildschirmschoner ein Symbol bereitstellen. Dieses Symbol ist nur sichtbar, wenn der Bildschirmschoner als eigenständige Anwendung ausgeführt wird. (Um vom Systemsteuerung ausgeführt zu werden, muss ein Bildschirmschoner die Dateinamenerweiterung .scr aufweisen. Um als eigenständige Anwendung ausgeführt werden zu können, muss er über die Dateinamenerweiterung .exe verfügen.) Das Symbol muss in der Ressourcendatei des Bildschirmschoners durch die konstante ID APP identifiziert \_ werden, die in der Headerdatei Scrnsave.h definiert ist.

Eine letzte Anforderung ist eine Beschreibungszeichenfolge für den Bildschirmschoner. Die Ressourcendatei für einen Bildschirmschoner muss eine Zeichenfolge enthalten, die der Systemsteuerung als Namen des Bildschirmschonrs anzeigt. Die Beschreibungszeichenfolge muss die erste Zeichenfolge in der Zeichenfolgentabelle der Ressourcendatei sein (identifiziert mit dem Ordnungswert 1). Die Beschreibungszeichenfolge wird jedoch vom Systemsteuerung ignoriert, wenn der Bildschirmschoner einen langen Dateinamen hat. In diesem Fall wird der Dateiname als Beschreibungszeichenfolge verwendet.

## <a name="using-the-screen-saver-functions"></a>Verwenden der Bildschirmschonerfunktionen

In diesem Abschnitt wird Beispielcode aus einer Bildschirmschoneranwendung verwendet, um die folgenden Aufgaben zu veranschaulichen:

-   [Erstellen eines Bildschirmschonrs](#creating-a-screen-saver)
-   [Installieren neuer Bildschirmschoner](#installing-new-screen-savers)
-   [Hinzufügen von Hilfe zum Dialogfeld "Konfiguration des Bildschirmschoner"](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Erstellen eines Bildschirmschonrs

In Intervallen zwischen 1 und 10 Sekunden wird der Bildschirm von der Anwendung in diesem Beispiel mit einer von vier Farben neu gezeichnet: Weiß, Hellgrau, Dunkelgrau und Schwarz. Die Anwendung zeichnet den Bildschirm jedes Mal, wenn sie eine [WM \_ TIMER-Nachricht](../winmsg/wm-timer.md) empfängt. Der Benutzer kann das Intervall anpassen, in dem diese Nachricht gesendet wird, indem er das Konfigurationsdialogfeld der Anwendung auswählt und eine einzelne horizontale Scrollleiste anpasst.

### <a name="screen-saver-library"></a>Bildschirmschonerbibliothek

Die statischen Bildschirmschonerfunktionen sind in der Bildschirmschonerbibliothek enthalten. Es sind zwei Versionen der Bibliothek verfügbar: Scrnsave.lib und Scrnsavw.lib. Sie müssen Ihr Projekt mit einem dieser Verknüpfungen verknüpfen. Scrnsave.lib wird für Bildschirmschoner verwendet, die ANSI-Zeichen verwenden, und Scrnsavw.lib wird für Bildschirmschoner verwendet, die Unicode-Zeichen verwenden. Ein Bildschirmschoner, der mit Scrnsavw.lib verknüpft ist, wird nur auf Windows Plattformen ausgeführt, die Unicode unterstützen, während ein mit Scrnsave.lib verknüpfter Bildschirmschoner auf jeder Windows Plattform ausgeführt wird.

### <a name="supporting-the-configuration-dialog-box"></a>Unterstützen des Konfigurationsdialogfelds

Die meisten Bildschirmschoner stellen ein Konfigurationsdialogfeld bereit, in dem der Benutzer Anpassungsdaten wie eindeutige Farben, Zeichnungsgeschwindigkeiten, Linienstärke, Schriftarten usw. angeben kann. Um das Konfigurationsdialogfeld zu unterstützen, muss die Anwendung eine Dialogfeldvorlage bereitstellen und außerdem die [**ScreenSaverConfigureDialog-Funktion**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) unterstützen. Im Folgenden finden Sie die Dialogfeldvorlage für die Beispielanwendung.


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



Sie müssen die Konstante definieren, die zum Identifizieren der Dialogfeldvorlage verwendet wird, indem Sie den Dezimalwert 2003 verwenden, wie im folgenden Beispiel gezeigt:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



Das folgende Beispiel zeigt die [**ScreenSaverConfigureDialog-Funktion**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) in der Beispielanwendung.


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



Zusätzlich zur Bereitstellung der Dialogfeldvorlage und zur Unterstützung der [**ScreenSaverConfigureDialog-Funktion**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) muss eine Anwendung auch die [**RegisterDialogClasses-Funktion**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) unterstützen. Diese Funktion registriert alle nicht standardmäßigen Fensterklassen, die vom Bildschirmschoner benötigt werden. Da die Beispielanwendung in ihrer Dialogfeldprozedur nur Standardfensterklassen verwendet hat, gibt diese Funktion einfach **TRUE** zurück, wie im folgenden Beispiel:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Unterstützen der Bildschirmschonerfensterprozedur

Jeder Bildschirmschoner muss eine Fensterprozedur mit dem Namen [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)unterstützen. Wie die meisten Fensterprozeduren verarbeitet **ScreenSaverProc** eine Reihe bestimmter Nachrichten und übergibt alle nicht verarbeiteten Nachrichten an eine Standardprozedur. Anstatt sie jedoch an die [DefWindowProc-Funktion](/windows/win32/api/winuser/nf-winuser-defwindowproca) zu übergeben, übergibt **ScreenSaverProc** nicht verarbeitete Nachrichten an die [**DefScreenSaverProc-Funktion.**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) Ein weiterer Unterschied zwischen **ScreenSaverProc** und einer normalen Fensterprozedur besteht darin, dass das an **ScreenSaverProc übergebene** Handle den gesamten Desktop anstelle eines Clientfensters identifiziert. Das folgende Beispiel zeigt die **ScreenSaverProc-Fensterprozedur** für den Beispielbildschirmschoner.


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a>Erstellen einer Moduldefinitionsdatei

Die Funktionen [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) und [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) müssen in die Moduldefinitionsdatei der Anwendung exportiert werden. [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) sollte jedoch nicht exportiert werden. Das folgende Beispiel zeigt die Moduldefinitionsdatei für die Beispielanwendung.


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a>Installieren neuer Bildschirmschoner

Beim Kompilieren der Liste der verfügbaren Bildschirmschoner durchsucht der Systemsteuerung das Windows Startverzeichnis nach Dateien mit der Erweiterung .scr. Da Bildschirmschoner standardmäßig Windows ausführbaren Dateien mit .exe Erweiterungen sind, müssen Sie sie umbenennen, damit sie über SCR-Erweiterungen verfügen, und sie in das richtige Verzeichnis kopieren.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Hinzufügen von Hilfe zum Dialogfeld "Konfiguration des Bildschirmschoner"

Das Konfigurationsdialogfeld für einen Bildschirmschoner enthält in der Regel eine **Hilfeschaltfläche.** Bildschirmschoneranwendungen können nach dem Bezeichner der Schaltfläche Hilfe suchen und die [**WinHelp-Funktion**](/windows/desktop/api/winuser/nf-winuser-winhelpa) auf die gleiche Weise aufrufen, wie die Hilfe in anderen Windows-basierten Anwendungen bereitgestellt wird.

 

 