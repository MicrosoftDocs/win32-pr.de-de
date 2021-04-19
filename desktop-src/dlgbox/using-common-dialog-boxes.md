---
title: Verwenden von allgemeinen Dialogfeldern
description: In diesem Abschnitt werden Aufgaben behandelt, die allgemeine Dialogfelder aufrufen.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Common Dialog Box Library,tasks
- Allgemeine Dialogfelder, verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773382a34b048e812a3fb093da0492b0c628fb14
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590657"
---
# <a name="using-common-dialog-boxes"></a>Verwenden von allgemeinen Dialogfeldern

In diesem Abschnitt werden Aufgaben behandelt, die allgemeine Dialogfelder aufrufen:

-   [Auswählen einer Farbe](#choosing-a-color)
-   [Auswählen einer Schriftart](#choosing-a-font)
-   [Öffnen einer Datei](#opening-a-file)
-   [Anzeigen des Dialogfelds "Drucken"](#displaying-the-print-dialog-box)
-   [Verwenden des Druckeigenschaftenblatts](#using-the-print-property-sheet)
-   [Einrichten der gedruckten Seite](#setting-up-the-printed-page)
-   [Suchen von Text](#finding-text)

## <a name="choosing-a-color"></a>Auswählen einer Farbe

In diesem Thema wird Beispielcode beschrieben, in dem ein Dialogfeld **Farbe** angezeigt wird, sodass ein Benutzer eine Farbe auswählen kann. Der Beispielcode initialisiert zuerst eine [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) und ruft dann die [**ChooseColor-Funktion**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) auf, um das Dialogfeld anzuzeigen. Wenn die Funktion **TRUE** zurückgibt und angibt, dass der Benutzer eine Farbe ausgewählt hat, verwendet der Beispielcode die ausgewählte Farbe, um einen neuen Volltonpinsel zu erstellen.

In diesem Beispiel wird die [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) verwendet, um das Dialogfeld wie folgt zu initialisieren:

-   Initialisiert den **lpCustColors-Member** mit einem Zeiger auf ein statisches Array von Werten. Die Farben im Array sind anfänglich schwarz, aber das statische Array behält benutzerdefinierte Farben bei, die vom Benutzer für nachfolgende [**ChooseColor-Aufrufe**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) erstellt wurden.
-   Legt das **CC \_ RGBINIT-Flag** fest und initialisiert den **rgbResult-Member,** um die Farbe anzugeben, die beim Öffnen des Dialogfelds anfänglich ausgewählt wird. Wenn keine Angabe erfolgt, ist die anfängliche Auswahl schwarz. Im Beispiel wird die *statische Variable rgbCurrent* verwendet, um den ausgewählten Wert zwischen Aufrufen von [**ChooseColor beibewahren.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))
-   Legt das **CC \_ FULLOPEN-Flag** fest, sodass die benutzerdefinierte Farberweiterung des Dialogfelds immer angezeigt wird.


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a>Auswählen einer Schriftart

In diesem Thema wird Beispielcode beschrieben, in dem ein **Dialogfeld Schriftart** angezeigt wird, sodass ein Benutzer die Attribute einer Schriftart auswählen kann. Der Beispielcode initialisiert zuerst eine [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) und ruft dann die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel wird das **CF \_ SCREENFONTS-Flag** so festgelegt, dass im Dialogfeld nur Bildschirmschriftarten angezeigt werden sollen. Es legt das **CF \_ EFFECTS-Flag** so fest, dass Steuerelemente angezeigt werden, die es dem Benutzer ermöglichen, Diebungs-, Unterstrich- und Farboptionen auszuwählen.

Wenn [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **TRUE** zurückgibt und angibt, dass der Benutzer auf die Schaltfläche **OK** geklickt hat, enthält die [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Informationen, die die vom Benutzer ausgewählten Schriftart- und Schriftartattribute beschreiben, einschließlich der Elemente der [**LOGFONT-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-logfonta) auf die das **lpLogFont-Element** zeigt. Das **rgbColors-Element** enthält die ausgewählte Textfarbe. Im Beispielcode werden diese Informationen verwendet, um die Schriftart und Textfarbe für den Gerätekontext, der dem Besitzerfenster zugeordnet ist, zu setzen.


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a>Öffnen einer Datei

> [!Note]  
> Ab Windows Vista wurde das Dialogfeld "Allgemeine Datei" durch das Dialogfeld "Allgemeines Element" ersetzt, wenn es zum Öffnen einer Datei verwendet wird. Es wird empfohlen, anstelle der API für den Dialog für allgemeine Dateien die Api für den Allgemeinen Elementdialog zu verwenden. Weitere Informationen finden Sie unter [Allgemeines Elementdialogfeld.](/windows/win32/shell/common-file-dialog)

 

In diesem Thema wird Beispielcode beschrieben, in dem ein Dialogfeld Öffnen angezeigt wird, sodass ein Benutzer das Laufwerk, das Verzeichnis und den Namen einer zu öffnenden Datei angeben kann.  Der Beispielcode initialisiert zunächst eine [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) und ruft dann die [**GetOpenFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel ist der **lpstrFilter-Member** ein Zeiger auf einen Puffer, der zwei Dateinamenfilter angibt, die der Benutzer auswählen kann, um die angezeigten Dateinamen einzuschränken. Der Puffer enthält ein auf doppelt NULL endendes Array von Zeichenfolgen, in dem jedes Zeichenfolgenpaar einen Filter angibt. Der **nFilterIndex-Member** gibt an, dass beim Erstellen des Dialogfelds das erste Muster verwendet wird.

In diesem Beispiel werden die Flags **OFN \_ PATHMUSTEXIST** und **OFN \_ FILEMUSTEXIST** im **Flags-Member** festgelegt. Diese Flags bewirken, dass das Dialogfeld vor der Rückgabe überprüft, ob der vom Benutzer angegebene Pfad und Dateiname tatsächlich vorhanden ist.

Die [**GetOpenFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) gibt **TRUE** zurück, wenn der Benutzer auf die Schaltfläche **OK** klickt und der angegebene Pfad und Dateiname vorhanden sind. In diesem Fall enthält der Puffer, auf den der **lpstrFile-Member** zeigt, den Pfad und den Dateinamen. Im Beispielcode werden diese Informationen in einem Aufruf der -Funktion verwendet, um die Datei zu öffnen.

Obwohl in diesem Beispiel das **\_ OFN-EXPLORER-Flag** nicht festgelegt ist, wird weiterhin das Standarddialogfeld **Öffnen** im Explorer-Stil angezeigt. Wenn Sie jedoch eine Hookprozedur oder eine benutzerdefinierte Vorlage bereitstellen möchten und die Explorer-Benutzeroberfläche verwenden möchten, müssen Sie das **FLAG OFN \_ EXPLORER** festlegen.

> [!Note]  
> In der Programmiersprache C ist eine Zeichenfolge, die in Anführungszeichen eingeschlossen ist, NULL-terminiert.

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a>Anzeigen des Dialogfelds "Drucken"

In diesem Thema wird Beispielcode beschrieben, in dem ein Dialogfeld **Drucken** angezeigt wird, sodass ein Benutzer Optionen zum Drucken eines Dokuments auswählen kann. Der Beispielcode initialisiert zuerst eine [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) und ruft dann die [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel wird das **PD \_ RETURNDC-Flag** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) festgelegt. Dadurch gibt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ein Gerätekontexthandle an den ausgewählten Drucker im **hDC-Member** zurück. Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu rendern.

Bei der Eingabe legt der Beispielcode die **Member hDevMode** und **hDevNames auf** **NULL fest.** Wenn die Funktion **TRUE zurückgibt,** geben diese Member Handles an [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurück, die die Benutzereingabe und Informationen zum Drucker enthalten. Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet wird.


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a>Verwenden des Druckeigenschaftsblatts

In diesem Thema wird Beispielcode beschrieben, der ein **Druck-Eigenschaftenblatt** anzeigt, sodass ein Benutzer Optionen zum Drucken eines Dokuments auswählen kann. Der Beispielcode initialisiert zuerst eine [**PRINTDLGEX-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) und ruft dann die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) auf, um das Eigenschaftenblatt anzuzeigen.

Der Beispielcode legt das **PD \_ RETURNDC-Flag** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) fest. Dadurch gibt die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) ein Gerätekontexthandl an den ausgewählten Drucker im **hDC-Member** zurück.

Bei der Eingabe legt der Beispielcode die **Member hDevMode** und **hDevNames auf** **NULL fest.** Wenn die Funktion **S \_ OK zurückgibt,** geben diese Member Handles an [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurück, die die Benutzereingabe und Informationen zum Drucker enthalten. Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet wird.

Nach Abschluss des Druckvorgang gibt der Beispielcode die [**Puffer DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)und [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) frei und ruft die [**DeleteDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) auf, um den Gerätekontext zu löschen.


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a>Einrichten der gedruckten Seite

In diesem Thema wird Beispielcode beschrieben, der ein Dialogfeld "Seiteneinrichtung" anzeigt, sodass ein Benutzer die Attribute der gedruckten Seite auswählen kann, z. B. den Papiertyp, die Papierquelle, die Seitenausrichtung und die Seitenränder.  Der Beispielcode initialisiert zuerst eine [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) und ruft dann die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel wird das **\_ PSD-MARGIN-Flag** im **Flags-Member** festgelegt und der **rtMargin-Member** verwendet, um die anfänglichen Randwerte anzugeben. Es legt das **\_ PSD-Flag INTHOUSANDTHSOFINCHES** fest, um sicherzustellen, dass das Dialogfeld Randdimensionen in Tausendstel Zoll ausdrückt.

Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **NULL** fest. Wenn die Funktion **TRUE** zurückgibt, verwendet die Funktion diese Member, um Handles an [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurückzugeben, die die Benutzereingabe und Informationen zum Drucker enthalten. Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet werden soll.

Im folgenden Beispiel wird auch eine [**PagePaintHook-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) aktiviert, um das Zeichnen des Inhalts der Beispielseite anzupassen.


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



Das folgende Beispiel zeigt eine [**PagePaintHook-Beispielhook-Hookprozedur,**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) die das Randrechteck im Beispielseitenbereich zeichnet:


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a>Suchen von Text

In diesem Thema wird Beispielcode beschrieben, der **ein** Suchdialogfeld anzeigt und verwaltet, sodass der Benutzer die Parameter eines Suchvorgangs angeben kann. Das Dialogfeld sendet Nachrichten an die Fensterprozedur, damit Sie den Suchvorgang ausführen können.

Der Code zum Anzeigen und Verwalten eines Dialogfelds **Ersetzen** ist ähnlich, mit der Ausnahme, dass die [**Funktion ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) verwendet wird, um das Dialogfeld anzuzeigen. Das Dialogfeld **Ersetzen** sendet auch Nachrichten als Reaktion auf Benutzerklicks auf die Schaltflächen **Ersetzen** und **Alle ersetzen.**

Um das Dialogfeld **Suchen** oder **Ersetzen** zu verwenden, müssen Sie drei separate Aufgaben ausführen:

1.  Abrufen eines Nachrichtenbezeichners für die registrierte [**FINDMSGSTRING-Nachricht.**](findmsgstring.md)
2.  Zeigt das Dialogfeld an.
3.  Verarbeiten Sie [**FINDMSGSTRING-Meldungen,**](findmsgstring.md) wenn das Dialogfeld geöffnet ist.

Wenn Sie Ihre Anwendung initialisieren, rufen Sie die [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) auf, um einen Nachrichtenbezeichner für die registrierte [**FINDMSGSTRING-Nachricht**](findmsgstring.md) abzurufen.


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Initialisieren Sie zum **Anzeigen eines Dialogfelds** Suchen zuerst eine [**FINDREPLACE-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) und rufen Sie dann die [**FindText-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) auf. Beachten Sie, dass die **FINDREPLACE-Struktur** und der Puffer für die Suchzeichenfolge eine globale oder statische Variable sein sollten, damit sie nicht aus dem Gültigkeitsbereich geht, bevor das Dialogfeld geschlossen wird. Sie müssen das **hwndOwner-Member** festlegen, um das Fenster anzugeben, das die registrierten Nachrichten empfängt. Nachdem Sie das Dialogfeld erstellt haben, können Sie es mithilfe des zurückgegebenen Handles verschieben oder bearbeiten.


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



Wenn das Dialogfeld geöffnet ist, muss Ihre Hauptnachrichtenschleife einen Aufruf der [**IsDialogMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) enthalten. Übergeben Sie ein Handle als Parameter im **IsDialogMessage-Aufruf** an das Dialogfeld. Dadurch wird sichergestellt, dass das Dialogfeld Tastaturmeldungen ordnungsgemäß verarbeitet.

Zum Überwachen von Nachrichten, die über das Dialogfeld gesendet werden, muss Ihre Fensterprozedur nach der registrierten [**FINDMSGSTRING-Nachricht**](findmsgstring.md) suchen und die in der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) übergebenen Werte verarbeiten, wie im folgenden Beispiel dargestellt.


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
