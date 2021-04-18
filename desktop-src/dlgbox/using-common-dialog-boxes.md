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
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="cf0ce-105">Verwenden von allgemeinen Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="cf0ce-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="cf0ce-106">In diesem Abschnitt werden die Aufgaben erläutert, die allgemeine Dialogfelder aufrufen:</span><span class="sxs-lookup"><span data-stu-id="cf0ce-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="cf0ce-107">Auswählen einer Farbe</span><span class="sxs-lookup"><span data-stu-id="cf0ce-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="cf0ce-108">Auswählen einer Schriftart</span><span class="sxs-lookup"><span data-stu-id="cf0ce-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="cf0ce-109">Öffnen einer Datei</span><span class="sxs-lookup"><span data-stu-id="cf0ce-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="cf0ce-110">Anzeigen des Dialog Felds "Drucken"</span><span class="sxs-lookup"><span data-stu-id="cf0ce-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="cf0ce-111">Verwenden des Druckeigenschaften Blatts</span><span class="sxs-lookup"><span data-stu-id="cf0ce-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="cf0ce-112">Einrichten der gedruckten Seite</span><span class="sxs-lookup"><span data-stu-id="cf0ce-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="cf0ce-113">Suchen von Text</span><span class="sxs-lookup"><span data-stu-id="cf0ce-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="cf0ce-114">Auswählen einer Farbe</span><span class="sxs-lookup"><span data-stu-id="cf0ce-114">Choosing a Color</span></span>

<span data-ttu-id="cf0ce-115">In diesem Thema wird der Beispielcode beschrieben, der ein **Farb** Dialogfeld anzeigt, sodass ein Benutzer eine Farbe auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="cf0ce-116">Der Beispielcode initialisiert zuerst eine [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur und ruft dann die [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) -Funktion auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="cf0ce-117">Wenn die Funktion **true** zurückgibt, um anzugeben, dass der Benutzer eine Farbe ausgewählt hat, verwendet der Beispielcode die ausgewählte Farbe, um einen neuen Pinsel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="cf0ce-118">In diesem Beispiel wird das Dialogfeld wie folgt mithilfe der [**chooancolor**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur initialisiert:</span><span class="sxs-lookup"><span data-stu-id="cf0ce-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="cf0ce-119">Initialisiert den **lpcustcolors** -Member mit einem Zeiger auf ein statisches Array von-Werten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="cf0ce-120">Die Farben im Array sind anfänglich schwarz, aber das statische Array behält benutzerdefinierte Farben bei, die vom Benutzer für nachfolgende [**Auswahl**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) Farben aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="cf0ce-121">Legt das **CC \_ rgbinit** -Flag fest und initialisiert den **rgbresult** -Member, um die Farbe anzugeben, die beim Öffnen des Dialog Felds anfänglich ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="cf0ce-122">Wenn nicht angegeben, ist die anfängliche Auswahl schwarz.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="cf0ce-123">Im Beispiel wird die statische *rgbcurrent* -Variable verwendet, um den ausgewählten Wert zwischen den Aufrufen von [**chooelcolor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="cf0ce-124">Legt das **CC \_ FullOpen** -Flag so fest, dass die Erweiterung für benutzerdefinierte Farben des Dialog Felds immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


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



## <a name="choosing-a-font"></a><span data-ttu-id="cf0ce-125">Auswählen einer Schriftart</span><span class="sxs-lookup"><span data-stu-id="cf0ce-125">Choosing a Font</span></span>

<span data-ttu-id="cf0ce-126">In diesem Thema wird der Beispielcode beschrieben, der ein Dialogfeld für die **Schriftart** anzeigt, sodass ein Benutzer die Attribute einer Schriftart auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="cf0ce-127">Der Beispielcode initialisiert zuerst eine [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur und ruft dann die [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Funktion auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="cf0ce-128">In diesem Beispiel wird das **CF \_ screenfonts** -Flag festgelegt, um anzugeben, dass im Dialogfeld nur Bildschirm Schriftarten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="cf0ce-129">Das Flag **CF \_ Effects** wird so festgelegt, dass Steuerelemente angezeigt werden, die es dem Benutzer ermöglichen, Optionen für das auslagern, unterstreichen und Farben auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="cf0ce-130">Wenn Selected- [**Font**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **true** zurückgibt, um anzugeben, dass der Benutzer auf die Schaltfläche " **OK** " geklickt hat, enthält die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Informationen, die die vom Benutzer ausgewählten Schriftart-und Schriftart Attribute beschreiben, einschließlich der Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, auf die durch den **lplogfont** -Member verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="cf0ce-131">Das **rgbcolors** -Element enthält die ausgewählte Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="cf0ce-132">Der Beispielcode verwendet diese Informationen zum Festlegen der Schriftart und der Textfarbe für den Gerätekontext, der dem Besitzer Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


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



## <a name="opening-a-file"></a><span data-ttu-id="cf0ce-133">Öffnen einer Datei</span><span class="sxs-lookup"><span data-stu-id="cf0ce-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="cf0ce-134">Beginnend mit Windows Vista wurde das allgemeine Datei Dialogfeld durch das allgemeine Element Dialogfeld abgelöst, wenn zum Öffnen einer Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="cf0ce-135">Es wird empfohlen, anstelle der allgemeinen Datei Dialogfeld-API die API für allgemeine Elemente zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="cf0ce-136">Weitere Informationen finden Sie unter [Dialog Feld "allgemeine Elemente](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="cf0ce-136">For more information, see [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span>

 

<span data-ttu-id="cf0ce-137">In diesem Thema wird der Beispielcode beschrieben, in dem ein Dialogfeld **Öffnen** angezeigt wird, in dem ein Benutzer das Laufwerk, das Verzeichnis und den Namen einer zu öffnenden Datei angeben kann.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="cf0ce-138">Der Beispielcode initialisiert zuerst eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur und ruft dann die [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) -Funktion auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="cf0ce-139">In diesem Beispiel ist das **lpstrinfilter** -Element ein Zeiger auf einen Puffer, der zwei Dateinamen Filter angibt, die der Benutzer auswählen kann, um die angezeigten Dateinamen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="cf0ce-140">Der Puffer enthält ein mit zwei Null endendes Array von Zeichen folgen, in denen jedes Paar von Zeichen folgen einen Filter angibt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="cf0ce-141">Der **nfilterindex** -Member gibt an, dass das erste Muster verwendet wird, wenn das Dialogfeld erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="cf0ce-142">In diesem Beispiel werden die **ofn \_ pathmustexist** -und **ofn \_ filemustexist** -Flags im **Flags** -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="cf0ce-143">Diese Flags bewirken, dass das Dialogfeld vor der Rückgabe überprüft, dass der Pfad und der Dateiname, die vom Benutzer angegeben werden, tatsächlich vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="cf0ce-144">Die [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) -Funktion gibt **true** zurück, wenn der Benutzer auf die Schaltfläche **OK** klickt und der angegebene Pfad und der Dateiname vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="cf0ce-145">In diesem Fall enthält der Puffer, auf den der **lpstrinfile** -Member verweist, den Pfad und den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="cf0ce-146">Der Beispielcode verwendet diese Informationen in einem-aufrufsbefehl, um die Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="cf0ce-147">Obwohl in diesem Beispiel das **ofn \_ Explorer** -Flag nicht festgelegt ist, wird weiterhin das Standard Dialogfeld Explorer-Format **Öffnen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="cf0ce-148">Wenn Sie jedoch eine Hook-Prozedur oder eine benutzerdefinierte Vorlage bereitstellen möchten und die Explorer-Benutzeroberfläche benötigen, müssen Sie das Flag **ofn \_ Explorer** festlegen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="cf0ce-149">In der Programmiersprache C wird eine in Anführungszeichen eingeschlossene Zeichenfolge mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


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



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="cf0ce-150">Anzeigen des Dialog Felds "Drucken"</span><span class="sxs-lookup"><span data-stu-id="cf0ce-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="cf0ce-151">In diesem Thema wird der Beispielcode beschrieben, der ein **Druck** Dialogfeld anzeigt, sodass ein Benutzeroptionen zum Drucken eines Dokuments auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="cf0ce-152">Der Beispielcode initialisiert zuerst eine [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur und ruft dann die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="cf0ce-153">In diesem Beispiel wird das Flag " **PD \_ returndc** " im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="cf0ce-154">Dies bewirkt, dass [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ein Gerätekontext Handle an den ausgewählten Drucker im **hdc** -Mitglied zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="cf0ce-155">Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="cf0ce-156">Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="cf0ce-157">Wenn die Funktion **true** zurückgibt, geben diese Member Handles an [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurück, die die Benutzereingaben und Informationen zum Drucker enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="cf0ce-158">Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


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



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="cf0ce-159">Verwenden des Druckeigenschaften Blatts</span><span class="sxs-lookup"><span data-stu-id="cf0ce-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="cf0ce-160">In diesem Thema wird der Beispielcode beschrieben, der ein **Druck** Eigenschaften Blatt anzeigt, sodass ein Benutzeroptionen zum Drucken eines Dokuments auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="cf0ce-161">Der Beispielcode initialisiert zunächst eine [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur und ruft dann die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion auf, um das Eigenschaften Blatt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="cf0ce-162">Der Beispielcode legt das Flag " **PD \_ returndc** " im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="cf0ce-163">Dies bewirkt, dass die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion ein Gerätekontext Handle an den ausgewählten Drucker im **hdc** -Mitglied zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="cf0ce-164">Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="cf0ce-165">Wenn die Funktion **S \_ OK** zurückgibt, geben diese Member Handles an [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurück, die die Benutzereingaben und Informationen zum Drucker enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="cf0ce-166">Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="cf0ce-167">Nachdem der Druckvorgang abgeschlossen wurde, gibt der Beispielcode den [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-, [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)-und [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) -Puffer frei und ruft die [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) -Funktion auf, um den Gerätekontext zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


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



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="cf0ce-168">Einrichten der gedruckten Seite</span><span class="sxs-lookup"><span data-stu-id="cf0ce-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="cf0ce-169">In diesem Thema wird der Beispielcode beschrieben, der das Dialogfeld " **Seite einrichten** " anzeigt, sodass ein Benutzer die Attribute der gedruckten Seite auswählen kann, z. b. Papiertyp, Papier Quelle, Seitenausrichtung und Seitenränder.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="cf0ce-170">Der Beispielcode initialisiert zuerst eine [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur und ruft dann die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="cf0ce-171">In diesem Beispiel wird das **PSD- \_ Ränder** -Flag im **Flags** -Member festgelegt, und der **rtmargin** -Member wird verwendet, um die anfänglichen Randwerte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="cf0ce-172">Dadurch wird das **PSD-Flag \_ intausendandthsofinches** festgelegt, um sicherzustellen, dass das Dialogfeld Rand Dimensionen in Tausendstel Zoll ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="cf0ce-173">Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="cf0ce-174">Wenn die Funktion **true** zurückgibt, verwendet die Funktion diese Member, um Handles an [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurückzugeben, die die Benutzereingaben und Informationen zum Drucker enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="cf0ce-175">Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="cf0ce-176">Im folgenden Beispiel wird auch eine [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur aktiviert, um das Zeichnen des Inhalts der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


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



<span data-ttu-id="cf0ce-177">Im folgenden Beispiel wird eine beispielhafte [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur gezeigt, die das Rand Rechteck im Bereich der Beispielseite zeichnet:</span><span class="sxs-lookup"><span data-stu-id="cf0ce-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


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



## <a name="finding-text"></a><span data-ttu-id="cf0ce-178">Suchen von Text</span><span class="sxs-lookup"><span data-stu-id="cf0ce-178">Finding Text</span></span>

<span data-ttu-id="cf0ce-179">In diesem Thema wird der Beispielcode beschrieben, mit **dem ein Dialogfeld Suchen angezeigt** und verwaltet wird, sodass der Benutzer die Parameter eines Such Vorgangs angeben kann.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="cf0ce-180">Im Dialogfeld werden Meldungen an die Fenster Prozedur gesendet, sodass Sie den Suchvorgang ausführen können.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="cf0ce-181">Der Code zum Anzeigen und Verwalten eines **Replace** -Dialog Felds ist ähnlich, mit der Ausnahme, dass es die [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) -Funktion verwendet, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="cf0ce-182">Das Dialogfeld **ersetzen** sendet auch Nachrichten als Antwort auf Benutzer Klicks auf die Schaltflächen **ersetzen** und **Alle ersetzen** .</span><span class="sxs-lookup"><span data-stu-id="cf0ce-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="cf0ce-183">Um das Dialogfeld **Suchen** oder **ersetzen** zu verwenden, müssen Sie drei separate Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="cf0ce-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="cf0ce-184">Hiermit wird eine Nachrichten-ID für die registrierte Nachricht [**findmsgstring**](findmsgstring.md) ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="cf0ce-185">Zeigt das Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="cf0ce-186">Verarbeiten Sie [**findmsgstring**](findmsgstring.md) -Meldungen, wenn das Dialogfeld geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="cf0ce-187">Wenn Sie die Anwendung initialisieren, müssen Sie die [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufrufen, um eine Nachrichten-ID für die registrierte [**findmsgstring**](findmsgstring.md) -Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="cf0ce-188">Wenn Sie ein Dialogfeld **Suchen** anzeigen möchten, initialisieren Sie zuerst eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, und klicken Sie dann auf die Funktion [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="cf0ce-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="cf0ce-189">Beachten Sie, dass die **FindReplace** -Struktur und der Puffer für die Such Zeichenfolge eine globale oder statische Variable sein sollten, damit Sie nicht den Gültigkeitsbereich verlässt, bevor das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="cf0ce-190">Sie müssen das **hwndOwner** -Element festlegen, um das Fenster anzugeben, das die registrierten Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="cf0ce-191">Nachdem Sie das Dialogfeld erstellt haben, können Sie es mithilfe des zurückgegebenen Handles verschieben oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


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



<span data-ttu-id="cf0ce-192">Wenn das Dialogfeld geöffnet ist, muss die Hauptnachrichten Schleife einen Aufrufe der [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion einschließen.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="cf0ce-193">Übergeben Sie als Parameter im **IsDialogMessage** -Befehl ein Handle an das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="cf0ce-194">Dadurch wird sichergestellt, dass das Dialogfeld Tastatur Meldungen ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="cf0ce-195">Zum Überwachen von Nachrichten, die vom Dialogfeld gesendet werden, muss die Fenster Prozedur nach der registrierten Nachricht [**findmsgstring**](findmsgstring.md) suchen und die in der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur übergebenen Werte wie im folgenden Beispiel verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cf0ce-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


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



 

 
