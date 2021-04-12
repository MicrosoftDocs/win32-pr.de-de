---
title: Behandeln von Bildschirm Schonern
description: Die Microsoft Win32-API unterstützt spezielle Anwendungen namens Bildschirmschoner.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- Bildschirmschoner
- Systemsteuerung, Bildschirmschoner
- Screensaverkonfiguriredialog
- Modul Definitions Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473020"
---
# <a name="handling-screen-savers"></a>Behandeln von Bildschirm Schonern

Die Microsoft Win32-API unterstützt spezielle Anwendungen namens *Bildschirmschoner*. Bildschirmschoner beginnen, wenn sich die Maus und die Tastatur für einen angegebenen Zeitraum im Leerlauf befanden. Sie werden aus zwei Gründen verwendet:

-   Zum Schützen eines Bildschirms vor der durch statische Bilder verursachten Phosphor Verbrennung.
-   , Um vertrauliche Informationen auf einem Bildschirm zu verbergen.

Dieses Thema ist in die folgenden Abschnitte unterteilt.

-   [Informationen zu Bildschirmschoner](#about-screen-savers)
-   [Verwenden der Bildschirmschoner-Funktionen](#using-the-screen-saver-functions)
    -   [Erstellen eines Bildschirmschoners](#creating-a-screen-saver)
    -   [Installieren neuer Bildschirmschoner](#installing-new-screen-savers)
    -   [Hinzufügen von Hilfe zum Dialog Feld "Bildschirmschoner-Konfiguration"](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>Informationen zu Bildschirmschoner

Mithilfe der Desktop Anwendung in der Windows-Systemsteuerung können Benutzer aus einer Liste von Bildschirm Schonern auswählen, wie viel Zeit vergehen muss, bevor der Bildschirmschoner beginnt, Bildschirmschoner konfigurieren und Bildschirmschoner in der Vorschau anzeigen. Bildschirmschoner werden automatisch geladen, wenn Windows gestartet wird oder wenn ein Benutzer den Bildschirmschoner über die Systemsteuerung aktiviert.

Sobald ein Bildschirmschoner ausgewählt ist, überwacht Windows Tastatureingaben und Mausbewegungen und startet dann den Bildschirmschoner nach einer gewissen Zeit der Inaktivität. Windows startet den Bildschirmschoner jedoch nicht, wenn eine der folgenden Bedingungen zutrifft:

-   Bei der aktiven Anwendung handelt es sich nicht um eine Windows-basierte Anwendung.
-   Es ist ein computerbasiertes Schulungs Fenster (CBT) vorhanden.
-   Die aktive Anwendung empfängt die [WM- \_ syscommand](../menurc/wm-syscommand.md) -Nachricht, bei der der *wParam* -Parameter auf den SC \_ Screensave-Wert festgelegt ist, übergibt die Nachricht jedoch nicht an die [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion.

**Sicherheitskontext des Bildschirmschoners**

Der Sicherheitskontext des Bildschirmschoners ist davon abhängig, ob ein Benutzer interaktiv angemeldet ist. Wenn ein Benutzer beim Aufrufen des Bildschirmschoners interaktiv angemeldet ist, wird der Bildschirmschoner im Sicherheitskontext des interaktiven Benutzers ausgeführt. Wenn kein Benutzer angemeldet ist, ist der Sicherheitskontext des Bildschirmschoners abhängig von der verwendeten Windows-Version.

-   Windows XP und Windows 2000-Bildschirmschoner werden im Kontext von "LocalSystem" mit eingeschränkten Konten ausgeführt.
-   Windows 2003: der Bildschirmschoner wird im Kontext von "LocalService" mit allen entfernten Berechtigungen und der Gruppe "Administratoren" ausgeführt.
-   Gilt nicht für Windows NT4.

Der Sicherheitskontext bestimmt die Ebene privilegierter Vorgänge, die über einen Bildschirmschoner durchgeführt werden können.

**Windows Vista und höher:** Wenn der Kenn Wort Schutz durch eine Richtlinie aktiviert ist, wird der Bildschirmschoner unabhängig davon gestartet, was eine Anwendung mit der SC \_ Screensave-Benachrichtigung bewirkt.

Bildschirmschoner enthalten bestimmte exportierte Funktionen, Ressourcen Definitionen und Variablen Deklarationen. Die Bildschirmschoner-Bibliothek enthält die **Main** -Funktion und anderen Startcode, der für einen Bildschirmschoner erforderlich ist. Wenn ein Bildschirmschoner gestartet wird, erstellt der Startcode in der Bildschirmschoner-Bibliothek ein voll Bildfenster. Die Fenster Klasse für dieses Fenster wird wie folgt deklariert:


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



Zum Erstellen eines Bildschirmschoners erstellen die meisten Entwickler ein Quell Code Modul, das drei erforderliche Funktionen enthält, und verknüpfen Sie mit der Bildschirmschoner-Bibliothek. Ein Bildschirmschoner-Modul ist nur für die Konfiguration und das Bereitstellen von visuellen Effekten zuständig.

Eine der drei erforderlichen Funktionen in einem Bildschirmschoner-Modul ist [**screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Diese Funktion verarbeitet bestimmte Nachrichten und übergibt alle nicht verarbeiteten Nachrichten an die Bildschirmschoner-Bibliothek zurück. Im folgenden finden Sie einige der typischen Nachrichten, die von **screensaverproc** verarbeitet werden.



| Nachricht        | Bedeutung                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ Erstellen     | Abrufen von Initialisierungs Daten aus der Regedit.ini Datei. Legen Sie einen Fenster Zeit Geber für das Fenster "Bildschirmschoner" fest. Führen Sie eine beliebige andere erforderliche Initialisierung aus.                                     |
| WM- \_ erasebkgnd | Löschen Sie das Fenster "Bildschirmschoner", und bereiten Sie nachfolgende Zeichnungsvorgänge vor.                                                                                                               |
| WM- \_ Timer      | Ausführen von Zeichnungs Vorgängen.                                                                                                                                                                |
| WM \_ zerstören    | Die beim Verarbeiten der [WM \_ Create](../winmsg/wm-create.md) -Nachricht erstellten Timer werden zerstört Führen Sie alle zusätzlichen erforderlichen Bereinigungs Vorgänge aus. |



 

[**Screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) übergibt nicht verarbeitete Nachrichten durch Aufrufen der [**defscreensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) -Funktion an die Bildschirmschoner-Bibliothek. In der folgenden Tabelle wird beschrieben, wie die Funktion verschiedene Nachrichten verarbeitet.



| `Message`         | Aktion                                                                    |
|-----------------|---------------------------------------------------------------------------|
| WM- \_ SetCursor   | Legen Sie den Cursor auf den NULL-Cursor fest, und entfernen Sie ihn aus dem Bildschirm.           |
| WM- \_ Paint       | Zeichnen Sie den Bildschirmhintergrund.                                              |
| WM \_ lbuttondown | Beenden Sie den Bildschirmschoner.                                               |
| WM- \_ mbuttondown | Beenden Sie den Bildschirmschoner.                                               |
| WM- \_ rbuttondown | Beenden Sie den Bildschirmschoner.                                               |
| WM- \_ KeyDown     | Beenden Sie den Bildschirmschoner.                                               |
| WM- \_ mouseelmove   | Beenden Sie den Bildschirmschoner.                                               |
| WM \_ aktivieren    | Beenden Sie den Bildschirmschoner, wenn der *wParam* -Parameter auf " **false**" festgelegt ist. |



 

Die zweite erforderliche Funktion in einem Bildschirmschoner-Modul ist [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Diese Funktion zeigt ein Dialogfeld an, in dem der Benutzer den Bildschirmschoner konfigurieren kann (eine Anwendung muss eine entsprechende Dialogfeld Vorlage bereitstellen). In Windows wird das Dialogfeld Konfiguration angezeigt, wenn der Benutzer die Schaltfläche **Setup** im Dialogfeld Bildschirmschoner der Systemsteuerung auswählt.

Die dritte erforderliche Funktion in einem Bildschirmschoner-Modul ist [**registerdialogclasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses). Diese Funktion muss von allen Bildschirmschoner-Anwendungen aufgerufen werden. Anwendungen, für die keine speziellen Fenster oder benutzerdefinierten Steuerelemente im Konfigurations Dialogfeld erforderlich sind, können jedoch einfach " **true**" zurückgeben. Anwendungen, die besondere Fenster oder benutzerdefinierte Steuerelemente erfordern, sollten diese Funktion verwenden, um die entsprechenden Fenster Klassen zu registrieren.

Zusätzlich zum Erstellen eines Moduls, das die drei soeben beschriebenen Funktionen unterstützt, sollte ein Bildschirmschoner ein Symbol bereitstellen. Dieses Symbol ist nur sichtbar, wenn der Bildschirmschoner als eigenständige Anwendung ausgeführt wird. (Um in der Systemsteuerung ausgeführt zu werden, muss ein Bildschirmschoner über die Dateinamenerweiterung. SCR verfügen, die als eigenständige Anwendung ausgeführt werden muss. exe muss die Dateinamenerweiterung. exe aufweisen.) Das Symbol muss in der Ressourcen Datei des Bildschirmschoners durch die Konstante-ID-App identifiziert werden \_ , die in der Header Datei "Scrnsave. h" definiert ist.

Eine abschließende Anforderung ist eine Bildschirmschoner-Beschreibungs Zeichenfolge. Die Ressourcen Datei für einen Bildschirmschoner muss eine Zeichenfolge enthalten, die in der Systemsteuerung als Bildschirmschoner Name angezeigt wird. Die Beschreibungs Zeichenfolge muss die erste Zeichenfolge in der Zeichen folgen Tabelle der Ressourcen Datei (identifiziert durch den Ordinalwert 1) sein. Die Beschreibungs Zeichenfolge wird jedoch von der Systemsteuerung ignoriert, wenn der Bildschirmschoner über einen langen Dateinamen verfügt. In diesem Fall wird der Dateiname als Beschreibungs Zeichenfolge verwendet.

## <a name="using-the-screen-saver-functions"></a>Verwenden der Bildschirmschoner-Funktionen

In diesem Abschnitt wird ein Beispielcode aus einer Bildschirmschoner Anwendung verwendet, um die folgenden Aufgaben zu veranschaulichen:

-   [Erstellen eines Bildschirmschoners](#creating-a-screen-saver)
-   [Installieren neuer Bildschirmschoner](#installing-new-screen-savers)
-   [Hinzufügen von Hilfe zum Dialog Feld "Bildschirmschoner-Konfiguration"](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Erstellen eines Bildschirmschoners

In Intervallen von 1 bis 10 Sekunden zeichnet die Anwendung in diesem Beispiel den Bildschirm mit einer von vier Farben auf: weiß, hellgrau, dunkelgrau und schwarz. Die Anwendung zeichnet den Bildschirm jedes Mal, wenn [eine \_ WM](../winmsg/wm-timer.md) -Zeit Geber Nachricht empfangen wird. Der Benutzer kann das Intervall, in dem diese Nachricht gesendet wird, anpassen, indem er das Konfigurations Dialogfeld der Anwendung auswählt und eine einzelne horizontale Schiebe Leiste anpasst.

### <a name="screen-saver-library"></a>Bildschirmschoner-Bibliothek

Die statischen Bildschirmschoner-Funktionen sind in der Bildschirmschoner-Bibliothek enthalten. Es sind zwei Versionen der Bibliothek verfügbar: SCRNSAVE. lib und scrnsavw. lib. Sie müssen Ihr Projekt mit einem dieser Verknüpfungen verknüpfen. SCRNSAVE. lib wird für Bildschirmschoner verwendet, die ANSI-Zeichen verwenden, und scrnsavw. lib wird für Bildschirmschoner verwendet, die Unicode-Zeichen verwenden. Ein Bildschirmschoner, der mit scrnsavw. lib verknüpft ist, kann nur auf Windows-Plattformen ausgeführt werden, die Unicode unterstützen, während ein mit SCRNSAVE. lib verknüpfter Bildschirmschoner auf jeder Windows-Plattform ausgeführt werden kann.

### <a name="supporting-the-configuration-dialog-box"></a>Unterstützen des Konfigurations Dialogfelds

Die meisten Bildschirmschoner stellen ein Konfigurations Dialogfeld bereit, mit dem der Benutzer Anpassungsdaten, z. b. eindeutige Farben, Zeichen Geschwindigkeiten, Linienstärke, Schriftarten usw., angeben kann. Um das Dialogfeld "Konfiguration" zu unterstützen, muss die Anwendung eine Dialogfeld Vorlage bereitstellen. Außerdem muss die Funktion " [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) " unterstützt werden. Im folgenden finden Sie die Dialogfeld Vorlage für die Beispielanwendung.


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



Sie müssen die Konstante definieren, die zum Identifizieren der Dialogfeld Vorlage verwendet wird, indem Sie den Dezimalwert 2003 verwenden, wie im folgenden Beispiel gezeigt:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



Das folgende Beispiel zeigt die [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) -Funktion, die in der Beispielanwendung enthalten ist.


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



Neben der Bereitstellung der Dialogfeld Vorlage und der Unterstützung der [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) -Funktion muss eine Anwendung auch die [**registerdialogclasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) -Funktion unterstützen. Diese Funktion registriert alle nicht standardmäßigen Fenster Klassen, die für den Bildschirmschoner erforderlich sind. Da in der Beispielanwendung nur Standardfenster Klassen in der entsprechenden Dialogfeld Prozedur verwendet wurden, gibt diese Funktion einfach **true** zurück, wie im folgenden Beispiel gezeigt:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Unterstützen der Prozedur für den Bildschirmschoner-Fenster

Jeder Bildschirmschoner muss eine Fenster Prozedur mit dem Namen [**screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)unterstützen. Wie die meisten Fenster Prozeduren verarbeitet **screensaverproc** eine Reihe spezifischer Nachrichten und übergibt alle nicht verarbeiteten Nachrichten an eine Standardprozedur. Doch anstatt Sie an die [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion zu übergeben, übergibt **screensaverproc** nicht verarbeitete Nachrichten an die [**defscreensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) -Funktion. Ein weiterer Unterschied zwischen **screensaverproc** und einer normalen Fenster Prozedur besteht darin, dass das an **screensaverproc** übermittelte Handle den gesamten Desktop und nicht ein Client Fenster identifiziert. Das folgende Beispiel zeigt die Prozedur **screensaverproc** Window für den Beispiel Bildschirmschoner.


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



### <a name="creating-a-module-definition-file"></a>Erstellen einer Modul Definitionsdatei

Die Funktionen [**screensaverproc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) und [**screensaverkonfiguriredialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) müssen in der Modul Definitionsdatei der Anwendung exportiert werden. " [**Registerdialogclasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) " sollte jedoch nicht exportiert werden. Das folgende Beispiel zeigt die Modul Definitionsdatei für die Beispielanwendung.


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

Beim Kompilieren der Liste der verfügbaren Bildschirmschoner durchsucht die Systemsteuerung das Windows-Start Verzeichnis nach Dateien mit der Erweiterung. scr. Da Bildschirmschoner standardmäßige ausführbare Windows-Dateien mit exe-Erweiterungen sind, müssen Sie diese so umbenennen, dass Sie über. SCR-Erweiterungen verfügen, und Sie in das richtige Verzeichnis kopieren.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Hinzufügen von Hilfe zum Dialog Feld "Bildschirmschoner-Konfiguration"

Das Konfigurations Dialogfeld für einen Bildschirmschoner enthält in der Regel eine Schaltfläche **Hilfe** . Bildschirmschoner-Anwendungen können den Bezeichner der Hilfe Schaltfläche Überprüfen und die [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) -Funktion auf die gleiche Weise wie in anderen Windows-basierten Anwendungen bereitstellen.

 

 