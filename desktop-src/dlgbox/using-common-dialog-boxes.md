---
title: Verwenden von allgemeinen Dialog Feldern
description: In diesem Abschnitt werden Aufgaben behandelt, die allgemeine Dialogfelder aufrufen.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Allgemeine Dialog Feld Bibliothek, Aufgaben
- Allgemeine Dialogfelder, verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a973fee7c8f7cd88abad3097edfc0349cc9118c1
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "106337274"
---
# <a name="using-common-dialog-boxes"></a>Verwenden von allgemeinen Dialog Feldern

In diesem Abschnitt werden die Aufgaben erläutert, die allgemeine Dialogfelder aufrufen:

-   [Auswählen einer Farbe](#choosing-a-color)
-   [Auswählen einer Schriftart](#choosing-a-font)
-   [Öffnen einer Datei](#opening-a-file)
-   [Anzeigen des Dialog Felds "Drucken"](#displaying-the-print-dialog-box)
-   [Verwenden des Druckeigenschaften Blatts](#using-the-print-property-sheet)
-   [Einrichten der gedruckten Seite](#setting-up-the-printed-page)
-   [Suchen von Text](#finding-text)

## <a name="choosing-a-color"></a>Auswählen einer Farbe

In diesem Thema wird der Beispielcode beschrieben, der ein **Farb** Dialogfeld anzeigt, sodass ein Benutzer eine Farbe auswählen kann. Der Beispielcode initialisiert zuerst eine [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur und ruft dann die [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) -Funktion auf, um das Dialogfeld anzuzeigen. Wenn die Funktion **true** zurückgibt, um anzugeben, dass der Benutzer eine Farbe ausgewählt hat, verwendet der Beispielcode die ausgewählte Farbe, um einen neuen Pinsel zu erstellen.

In diesem Beispiel wird das Dialogfeld wie folgt mithilfe der [**chooancolor**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur initialisiert:

-   Initialisiert den **lpcustcolors** -Member mit einem Zeiger auf ein statisches Array von-Werten. Die Farben im Array sind anfänglich schwarz, aber das statische Array behält benutzerdefinierte Farben bei, die vom Benutzer für nachfolgende [**Auswahl**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) Farben aufgerufen wurden.
-   Legt das **CC \_ rgbinit** -Flag fest und initialisiert den **rgbresult** -Member, um die Farbe anzugeben, die beim Öffnen des Dialog Felds anfänglich ausgewählt wird. Wenn nicht angegeben, ist die anfängliche Auswahl schwarz. Im Beispiel wird die statische *rgbcurrent* -Variable verwendet, um den ausgewählten Wert zwischen den Aufrufen von [**chooelcolor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))beizubehalten.
-   Legt das **CC \_ FullOpen** -Flag so fest, dass die Erweiterung für benutzerdefinierte Farben des Dialog Felds immer angezeigt wird.


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

In diesem Thema wird der Beispielcode beschrieben, der ein Dialogfeld für die **Schriftart** anzeigt, sodass ein Benutzer die Attribute einer Schriftart auswählen kann. Der Beispielcode initialisiert zuerst eine [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur und ruft dann die [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Funktion auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel wird das **CF \_ screenfonts** -Flag festgelegt, um anzugeben, dass im Dialogfeld nur Bildschirm Schriftarten angezeigt werden sollen. Das Flag **CF \_ Effects** wird so festgelegt, dass Steuerelemente angezeigt werden, die es dem Benutzer ermöglichen, Optionen für das auslagern, unterstreichen und Farben auszuwählen.

Wenn Selected- [**Font**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **true** zurückgibt, um anzugeben, dass der Benutzer auf die Schaltfläche " **OK** " geklickt hat, enthält die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Informationen, die die vom Benutzer ausgewählten Schriftart-und Schriftart Attribute beschreiben, einschließlich der Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, auf die durch den **lplogfont** -Member verwiesen wird. Das **rgbcolors** -Element enthält die ausgewählte Textfarbe. Der Beispielcode verwendet diese Informationen zum Festlegen der Schriftart und der Textfarbe für den Gerätekontext, der dem Besitzer Fenster zugeordnet ist.


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
> Beginnend mit Windows Vista wurde das allgemeine Datei Dialogfeld durch das allgemeine Element Dialogfeld abgelöst, wenn zum Öffnen einer Datei verwendet wird. Es wird empfohlen, anstelle der allgemeinen Datei Dialogfeld-API die API für allgemeine Elemente zu verwenden. Weitere Informationen finden Sie unter [Dialog Feld "allgemeine Elemente](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))".

 

In diesem Thema wird der Beispielcode beschrieben, in dem ein Dialogfeld **Öffnen** angezeigt wird, in dem ein Benutzer das Laufwerk, das Verzeichnis und den Namen einer zu öffnenden Datei angeben kann. Der Beispielcode initialisiert zuerst eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur und ruft dann die [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) -Funktion auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel ist das **lpstrinfilter** -Element ein Zeiger auf einen Puffer, der zwei Dateinamen Filter angibt, die der Benutzer auswählen kann, um die angezeigten Dateinamen einzuschränken. Der Puffer enthält ein mit zwei Null endendes Array von Zeichen folgen, in denen jedes Paar von Zeichen folgen einen Filter angibt. Der **nfilterindex** -Member gibt an, dass das erste Muster verwendet wird, wenn das Dialogfeld erstellt wird.

In diesem Beispiel werden die **ofn \_ pathmustexist** -und **ofn \_ filemustexist** -Flags im **Flags** -Element festgelegt. Diese Flags bewirken, dass das Dialogfeld vor der Rückgabe überprüft, dass der Pfad und der Dateiname, die vom Benutzer angegeben werden, tatsächlich vorhanden sind.

Die [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) -Funktion gibt **true** zurück, wenn der Benutzer auf die Schaltfläche **OK** klickt und der angegebene Pfad und der Dateiname vorhanden sind. In diesem Fall enthält der Puffer, auf den der **lpstrinfile** -Member verweist, den Pfad und den Dateinamen. Der Beispielcode verwendet diese Informationen in einem-aufrufsbefehl, um die Datei zu öffnen.

Obwohl in diesem Beispiel das **ofn \_ Explorer** -Flag nicht festgelegt ist, wird weiterhin das Standard Dialogfeld Explorer-Format **Öffnen** angezeigt. Wenn Sie jedoch eine Hook-Prozedur oder eine benutzerdefinierte Vorlage bereitstellen möchten und die Explorer-Benutzeroberfläche benötigen, müssen Sie das Flag **ofn \_ Explorer** festlegen.

> [!Note]  
> In der Programmiersprache C wird eine in Anführungszeichen eingeschlossene Zeichenfolge mit Null beendet.

 


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



## <a name="displaying-the-print-dialog-box"></a>Anzeigen des Dialog Felds "Drucken"

In diesem Thema wird der Beispielcode beschrieben, der ein **Druck** Dialogfeld anzeigt, sodass ein Benutzeroptionen zum Drucken eines Dokuments auswählen kann. Der Beispielcode initialisiert zuerst eine [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur und ruft dann die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel wird das Flag " **PD \_ returndc** " im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur festgelegt. Dies bewirkt, dass [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ein Gerätekontext Handle an den ausgewählten Drucker im **hdc** -Mitglied zurückgibt. Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu Rendering.

Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **null** fest. Wenn die Funktion **true** zurückgibt, geben diese Member Handles an [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurück, die die Benutzereingaben und Informationen zum Drucker enthalten. Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.


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



## <a name="using-the-print-property-sheet"></a>Verwenden des Druckeigenschaften Blatts

In diesem Thema wird der Beispielcode beschrieben, der ein **Druck** Eigenschaften Blatt anzeigt, sodass ein Benutzeroptionen zum Drucken eines Dokuments auswählen kann. Der Beispielcode initialisiert zunächst eine [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur und ruft dann die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion auf, um das Eigenschaften Blatt anzuzeigen.

Der Beispielcode legt das Flag " **PD \_ returndc** " im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur fest. Dies bewirkt, dass die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion ein Gerätekontext Handle an den ausgewählten Drucker im **hdc** -Mitglied zurückgibt.

Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **null** fest. Wenn die Funktion **S \_ OK** zurückgibt, geben diese Member Handles an [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurück, die die Benutzereingaben und Informationen zum Drucker enthalten. Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.

Nachdem der Druckvorgang abgeschlossen wurde, gibt der Beispielcode den [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-, [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)-und [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) -Puffer frei und ruft die [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) -Funktion auf, um den Gerätekontext zu löschen.


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

In diesem Thema wird der Beispielcode beschrieben, der das Dialogfeld " **Seite einrichten** " anzeigt, sodass ein Benutzer die Attribute der gedruckten Seite auswählen kann, z. b. Papiertyp, Papier Quelle, Seitenausrichtung und Seitenränder. Der Beispielcode initialisiert zuerst eine [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur und ruft dann die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion auf, um das Dialogfeld anzuzeigen.

In diesem Beispiel wird das **PSD- \_ Ränder** -Flag im **Flags** -Member festgelegt, und der **rtmargin** -Member wird verwendet, um die anfänglichen Randwerte anzugeben. Dadurch wird das **PSD-Flag \_ intausendandthsofinches** festgelegt, um sicherzustellen, dass das Dialogfeld Rand Dimensionen in Tausendstel Zoll ausdrückt.

Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **null** fest. Wenn die Funktion **true** zurückgibt, verwendet die Funktion diese Member, um Handles an [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurückzugeben, die die Benutzereingaben und Informationen zum Drucker enthalten. Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.

Im folgenden Beispiel wird auch eine [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur aktiviert, um das Zeichnen des Inhalts der Beispielseite anzupassen.


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



Im folgenden Beispiel wird eine beispielhafte [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur gezeigt, die das Rand Rechteck im Bereich der Beispielseite zeichnet:


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

In diesem Thema wird der Beispielcode beschrieben, mit **dem ein Dialogfeld Suchen angezeigt** und verwaltet wird, sodass der Benutzer die Parameter eines Such Vorgangs angeben kann. Im Dialogfeld werden Meldungen an die Fenster Prozedur gesendet, sodass Sie den Suchvorgang ausführen können.

Der Code zum Anzeigen und Verwalten eines **Replace** -Dialog Felds ist ähnlich, mit der Ausnahme, dass es die [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) -Funktion verwendet, um das Dialogfeld anzuzeigen. Das Dialogfeld **ersetzen** sendet auch Nachrichten als Antwort auf Benutzer Klicks auf die Schaltflächen **ersetzen** und **Alle ersetzen** .

Um das Dialogfeld **Suchen** oder **ersetzen** zu verwenden, müssen Sie drei separate Aufgaben ausführen:

1.  Hiermit wird eine Nachrichten-ID für die registrierte Nachricht [**findmsgstring**](findmsgstring.md) ausgegeben.
2.  Zeigt das Dialogfeld an.
3.  Verarbeiten Sie [**findmsgstring**](findmsgstring.md) -Meldungen, wenn das Dialogfeld geöffnet ist.

Wenn Sie die Anwendung initialisieren, müssen Sie die [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufrufen, um eine Nachrichten-ID für die registrierte [**findmsgstring**](findmsgstring.md) -Nachricht zu erhalten.


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Wenn Sie ein Dialogfeld **Suchen** anzeigen möchten, initialisieren Sie zuerst eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, und klicken Sie dann auf die Funktion [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . Beachten Sie, dass die **FindReplace** -Struktur und der Puffer für die Such Zeichenfolge eine globale oder statische Variable sein sollten, damit Sie nicht den Gültigkeitsbereich verlässt, bevor das Dialogfeld geschlossen wird. Sie müssen das **hwndOwner** -Element festlegen, um das Fenster anzugeben, das die registrierten Nachrichten empfängt. Nachdem Sie das Dialogfeld erstellt haben, können Sie es mithilfe des zurückgegebenen Handles verschieben oder bearbeiten.


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



Wenn das Dialogfeld geöffnet ist, muss die Hauptnachrichten Schleife einen Aufrufe der [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion einschließen. Übergeben Sie als Parameter im **IsDialogMessage** -Befehl ein Handle an das Dialogfeld. Dadurch wird sichergestellt, dass das Dialogfeld Tastatur Meldungen ordnungsgemäß verarbeitet.

Zum Überwachen von Nachrichten, die vom Dialogfeld gesendet werden, muss die Fenster Prozedur nach der registrierten Nachricht [**findmsgstring**](findmsgstring.md) suchen und die in der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur übergebenen Werte wie im folgenden Beispiel verarbeiten.


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



 

 
