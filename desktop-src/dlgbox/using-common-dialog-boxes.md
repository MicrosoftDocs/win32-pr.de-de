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
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="b2eed-105">Verwenden von allgemeinen Dialogfeldern</span><span class="sxs-lookup"><span data-stu-id="b2eed-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="b2eed-106">In diesem Abschnitt werden Aufgaben behandelt, die allgemeine Dialogfelder aufrufen:</span><span class="sxs-lookup"><span data-stu-id="b2eed-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="b2eed-107">Auswählen einer Farbe</span><span class="sxs-lookup"><span data-stu-id="b2eed-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="b2eed-108">Auswählen einer Schriftart</span><span class="sxs-lookup"><span data-stu-id="b2eed-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="b2eed-109">Öffnen einer Datei</span><span class="sxs-lookup"><span data-stu-id="b2eed-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="b2eed-110">Anzeigen des Dialogfelds "Drucken"</span><span class="sxs-lookup"><span data-stu-id="b2eed-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="b2eed-111">Verwenden des Druckeigenschaftenblatts</span><span class="sxs-lookup"><span data-stu-id="b2eed-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="b2eed-112">Einrichten der gedruckten Seite</span><span class="sxs-lookup"><span data-stu-id="b2eed-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="b2eed-113">Suchen von Text</span><span class="sxs-lookup"><span data-stu-id="b2eed-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="b2eed-114">Auswählen einer Farbe</span><span class="sxs-lookup"><span data-stu-id="b2eed-114">Choosing a Color</span></span>

<span data-ttu-id="b2eed-115">In diesem Thema wird Beispielcode beschrieben, in dem ein Dialogfeld **Farbe** angezeigt wird, sodass ein Benutzer eine Farbe auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="b2eed-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="b2eed-116">Der Beispielcode initialisiert zuerst eine [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) und ruft dann die [**ChooseColor-Funktion**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="b2eed-117">Wenn die Funktion **TRUE** zurückgibt und angibt, dass der Benutzer eine Farbe ausgewählt hat, verwendet der Beispielcode die ausgewählte Farbe, um einen neuen Volltonpinsel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="b2eed-118">In diesem Beispiel wird die [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) verwendet, um das Dialogfeld wie folgt zu initialisieren:</span><span class="sxs-lookup"><span data-stu-id="b2eed-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="b2eed-119">Initialisiert den **lpCustColors-Member** mit einem Zeiger auf ein statisches Array von Werten.</span><span class="sxs-lookup"><span data-stu-id="b2eed-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="b2eed-120">Die Farben im Array sind anfänglich schwarz, aber das statische Array behält benutzerdefinierte Farben bei, die vom Benutzer für nachfolgende [**ChooseColor-Aufrufe**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b2eed-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="b2eed-121">Legt das **CC \_ RGBINIT-Flag** fest und initialisiert den **rgbResult-Member,** um die Farbe anzugeben, die beim Öffnen des Dialogfelds anfänglich ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="b2eed-122">Wenn keine Angabe erfolgt, ist die anfängliche Auswahl schwarz.</span><span class="sxs-lookup"><span data-stu-id="b2eed-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="b2eed-123">Im Beispiel wird die *statische Variable rgbCurrent* verwendet, um den ausgewählten Wert zwischen Aufrufen von [**ChooseColor beibewahren.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2eed-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="b2eed-124">Legt das **CC \_ FULLOPEN-Flag** fest, sodass die benutzerdefinierte Farberweiterung des Dialogfelds immer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


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



## <a name="choosing-a-font"></a><span data-ttu-id="b2eed-125">Auswählen einer Schriftart</span><span class="sxs-lookup"><span data-stu-id="b2eed-125">Choosing a Font</span></span>

<span data-ttu-id="b2eed-126">In diesem Thema wird Beispielcode beschrieben, in dem ein **Dialogfeld Schriftart** angezeigt wird, sodass ein Benutzer die Attribute einer Schriftart auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="b2eed-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="b2eed-127">Der Beispielcode initialisiert zuerst eine [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) und ruft dann die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="b2eed-128">In diesem Beispiel wird das **CF \_ SCREENFONTS-Flag** so festgelegt, dass im Dialogfeld nur Bildschirmschriftarten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="b2eed-129">Es legt das **CF \_ EFFECTS-Flag** so fest, dass Steuerelemente angezeigt werden, die es dem Benutzer ermöglichen, Diebungs-, Unterstrich- und Farboptionen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="b2eed-130">Wenn [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **TRUE** zurückgibt und angibt, dass der Benutzer auf die Schaltfläche **OK** geklickt hat, enthält die [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Informationen, die die vom Benutzer ausgewählten Schriftart- und Schriftartattribute beschreiben, einschließlich der Elemente der [**LOGFONT-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-logfonta) auf die das **lpLogFont-Element** zeigt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="b2eed-131">Das **rgbColors-Element** enthält die ausgewählte Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="b2eed-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="b2eed-132">Im Beispielcode werden diese Informationen verwendet, um die Schriftart und Textfarbe für den Gerätekontext, der dem Besitzerfenster zugeordnet ist, zu setzen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


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



## <a name="opening-a-file"></a><span data-ttu-id="b2eed-133">Öffnen einer Datei</span><span class="sxs-lookup"><span data-stu-id="b2eed-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="b2eed-134">Ab Windows Vista wurde das Dialogfeld "Allgemeine Datei" durch das Dialogfeld "Allgemeines Element" ersetzt, wenn es zum Öffnen einer Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="b2eed-135">Es wird empfohlen, anstelle der API für den Dialog für allgemeine Dateien die Api für den Allgemeinen Elementdialog zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2eed-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="b2eed-136">Weitere Informationen finden Sie unter [Allgemeines Elementdialogfeld.](/windows/win32/shell/common-file-dialog)</span><span class="sxs-lookup"><span data-stu-id="b2eed-136">For more information, see [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span>

 

<span data-ttu-id="b2eed-137">In diesem Thema wird Beispielcode beschrieben, in dem ein Dialogfeld Öffnen angezeigt wird, sodass ein Benutzer das Laufwerk, das Verzeichnis und den Namen einer zu öffnenden Datei angeben kann. </span><span class="sxs-lookup"><span data-stu-id="b2eed-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="b2eed-138">Der Beispielcode initialisiert zunächst eine [**OPENFILENAME-Struktur**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) und ruft dann die [**GetOpenFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="b2eed-139">In diesem Beispiel ist der **lpstrFilter-Member** ein Zeiger auf einen Puffer, der zwei Dateinamenfilter angibt, die der Benutzer auswählen kann, um die angezeigten Dateinamen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="b2eed-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="b2eed-140">Der Puffer enthält ein auf doppelt NULL endendes Array von Zeichenfolgen, in dem jedes Zeichenfolgenpaar einen Filter angibt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="b2eed-141">Der **nFilterIndex-Member** gibt an, dass beim Erstellen des Dialogfelds das erste Muster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="b2eed-142">In diesem Beispiel werden die Flags **OFN \_ PATHMUSTEXIST** und **OFN \_ FILEMUSTEXIST** im **Flags-Member** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="b2eed-143">Diese Flags bewirken, dass das Dialogfeld vor der Rückgabe überprüft, ob der vom Benutzer angegebene Pfad und Dateiname tatsächlich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b2eed-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="b2eed-144">Die [**GetOpenFileName-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) gibt **TRUE** zurück, wenn der Benutzer auf die Schaltfläche **OK** klickt und der angegebene Pfad und Dateiname vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b2eed-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="b2eed-145">In diesem Fall enthält der Puffer, auf den der **lpstrFile-Member** zeigt, den Pfad und den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="b2eed-146">Im Beispielcode werden diese Informationen in einem Aufruf der -Funktion verwendet, um die Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="b2eed-147">Obwohl in diesem Beispiel das **\_ OFN-EXPLORER-Flag** nicht festgelegt ist, wird weiterhin das Standarddialogfeld **Öffnen** im Explorer-Stil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="b2eed-148">Wenn Sie jedoch eine Hookprozedur oder eine benutzerdefinierte Vorlage bereitstellen möchten und die Explorer-Benutzeroberfläche verwenden möchten, müssen Sie das **FLAG OFN \_ EXPLORER** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="b2eed-149">In der Programmiersprache C ist eine Zeichenfolge, die in Anführungszeichen eingeschlossen ist, NULL-terminiert.</span><span class="sxs-lookup"><span data-stu-id="b2eed-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


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



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="b2eed-150">Anzeigen des Dialogfelds "Drucken"</span><span class="sxs-lookup"><span data-stu-id="b2eed-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="b2eed-151">In diesem Thema wird Beispielcode beschrieben, in dem ein Dialogfeld **Drucken** angezeigt wird, sodass ein Benutzer Optionen zum Drucken eines Dokuments auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="b2eed-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="b2eed-152">Der Beispielcode initialisiert zuerst eine [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) und ruft dann die [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="b2eed-153">In diesem Beispiel wird das **PD \_ RETURNDC-Flag** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="b2eed-154">Dadurch gibt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) ein Gerätekontexthandle an den ausgewählten Drucker im **hDC-Member** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2eed-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="b2eed-155">Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu rendern.</span><span class="sxs-lookup"><span data-stu-id="b2eed-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="b2eed-156">Bei der Eingabe legt der Beispielcode die **Member hDevMode** und **hDevNames auf** **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="b2eed-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="b2eed-157">Wenn die Funktion **TRUE zurückgibt,** geben diese Member Handles an [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurück, die die Benutzereingabe und Informationen zum Drucker enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2eed-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="b2eed-158">Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


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



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="b2eed-159">Verwenden des Druckeigenschaftsblatts</span><span class="sxs-lookup"><span data-stu-id="b2eed-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="b2eed-160">In diesem Thema wird Beispielcode beschrieben, der ein **Druck-Eigenschaftenblatt** anzeigt, sodass ein Benutzer Optionen zum Drucken eines Dokuments auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="b2eed-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="b2eed-161">Der Beispielcode initialisiert zuerst eine [**PRINTDLGEX-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) und ruft dann die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) auf, um das Eigenschaftenblatt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="b2eed-162">Der Beispielcode legt das **PD \_ RETURNDC-Flag** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) fest.</span><span class="sxs-lookup"><span data-stu-id="b2eed-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="b2eed-163">Dadurch gibt die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) ein Gerätekontexthandl an den ausgewählten Drucker im **hDC-Member** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2eed-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="b2eed-164">Bei der Eingabe legt der Beispielcode die **Member hDevMode** und **hDevNames auf** **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="b2eed-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="b2eed-165">Wenn die Funktion **S \_ OK zurückgibt,** geben diese Member Handles an [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurück, die die Benutzereingabe und Informationen zum Drucker enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2eed-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="b2eed-166">Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="b2eed-167">Nach Abschluss des Druckvorgang gibt der Beispielcode die [**Puffer DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)und [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) frei und ruft die [**DeleteDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) auf, um den Gerätekontext zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


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



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="b2eed-168">Einrichten der gedruckten Seite</span><span class="sxs-lookup"><span data-stu-id="b2eed-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="b2eed-169">In diesem Thema wird Beispielcode beschrieben, der ein Dialogfeld "Seiteneinrichtung" anzeigt, sodass ein Benutzer die Attribute der gedruckten Seite auswählen kann, z. B. den Papiertyp, die Papierquelle, die Seitenausrichtung und die Seitenränder. </span><span class="sxs-lookup"><span data-stu-id="b2eed-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="b2eed-170">Der Beispielcode initialisiert zuerst eine [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) und ruft dann die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) auf, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="b2eed-171">In diesem Beispiel wird das **\_ PSD-MARGIN-Flag** im **Flags-Member** festgelegt und der **rtMargin-Member** verwendet, um die anfänglichen Randwerte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b2eed-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="b2eed-172">Es legt das **\_ PSD-Flag INTHOUSANDTHSOFINCHES** fest, um sicherzustellen, dass das Dialogfeld Randdimensionen in Tausendstel Zoll ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="b2eed-173">Bei der Eingabe legt der Beispielcode die Member **hDevMode** und **hDevNames** auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="b2eed-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="b2eed-174">Wenn die Funktion **TRUE** zurückgibt, verwendet die Funktion diese Member, um Handles an [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurückzugeben, die die Benutzereingabe und Informationen zum Drucker enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2eed-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="b2eed-175">Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2eed-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="b2eed-176">Im folgenden Beispiel wird auch eine [**PagePaintHook-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) aktiviert, um das Zeichnen des Inhalts der Beispielseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


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



<span data-ttu-id="b2eed-177">Das folgende Beispiel zeigt eine [**PagePaintHook-Beispielhook-Hookprozedur,**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) die das Randrechteck im Beispielseitenbereich zeichnet:</span><span class="sxs-lookup"><span data-stu-id="b2eed-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


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



## <a name="finding-text"></a><span data-ttu-id="b2eed-178">Suchen von Text</span><span class="sxs-lookup"><span data-stu-id="b2eed-178">Finding Text</span></span>

<span data-ttu-id="b2eed-179">In diesem Thema wird Beispielcode beschrieben, der **ein** Suchdialogfeld anzeigt und verwaltet, sodass der Benutzer die Parameter eines Suchvorgangs angeben kann.</span><span class="sxs-lookup"><span data-stu-id="b2eed-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="b2eed-180">Das Dialogfeld sendet Nachrichten an die Fensterprozedur, damit Sie den Suchvorgang ausführen können.</span><span class="sxs-lookup"><span data-stu-id="b2eed-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="b2eed-181">Der Code zum Anzeigen und Verwalten eines Dialogfelds **Ersetzen** ist ähnlich, mit der Ausnahme, dass die [**Funktion ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) verwendet wird, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="b2eed-182">Das Dialogfeld **Ersetzen** sendet auch Nachrichten als Reaktion auf Benutzerklicks auf die Schaltflächen **Ersetzen** und **Alle ersetzen.**</span><span class="sxs-lookup"><span data-stu-id="b2eed-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="b2eed-183">Um das Dialogfeld **Suchen** oder **Ersetzen** zu verwenden, müssen Sie drei separate Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="b2eed-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="b2eed-184">Abrufen eines Nachrichtenbezeichners für die registrierte [**FINDMSGSTRING-Nachricht.**](findmsgstring.md)</span><span class="sxs-lookup"><span data-stu-id="b2eed-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="b2eed-185">Zeigt das Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="b2eed-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="b2eed-186">Verarbeiten Sie [**FINDMSGSTRING-Meldungen,**](findmsgstring.md) wenn das Dialogfeld geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b2eed-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="b2eed-187">Wenn Sie Ihre Anwendung initialisieren, rufen Sie die [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) auf, um einen Nachrichtenbezeichner für die registrierte [**FINDMSGSTRING-Nachricht**](findmsgstring.md) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b2eed-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="b2eed-188">Initialisieren Sie zum **Anzeigen eines Dialogfelds** Suchen zuerst eine [**FINDREPLACE-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) und rufen Sie dann die [**FindText-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) auf.</span><span class="sxs-lookup"><span data-stu-id="b2eed-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="b2eed-189">Beachten Sie, dass die **FINDREPLACE-Struktur** und der Puffer für die Suchzeichenfolge eine globale oder statische Variable sein sollten, damit sie nicht aus dem Gültigkeitsbereich geht, bevor das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b2eed-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="b2eed-190">Sie müssen das **hwndOwner-Member** festlegen, um das Fenster anzugeben, das die registrierten Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="b2eed-191">Nachdem Sie das Dialogfeld erstellt haben, können Sie es mithilfe des zurückgegebenen Handles verschieben oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b2eed-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


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



<span data-ttu-id="b2eed-192">Wenn das Dialogfeld geöffnet ist, muss Ihre Hauptnachrichtenschleife einen Aufruf der [**IsDialogMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2eed-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="b2eed-193">Übergeben Sie ein Handle als Parameter im **IsDialogMessage-Aufruf** an das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b2eed-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="b2eed-194">Dadurch wird sichergestellt, dass das Dialogfeld Tastaturmeldungen ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b2eed-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="b2eed-195">Zum Überwachen von Nachrichten, die über das Dialogfeld gesendet werden, muss Ihre Fensterprozedur nach der registrierten [**FINDMSGSTRING-Nachricht**](findmsgstring.md) suchen und die in der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) übergebenen Werte verarbeiten, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b2eed-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


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



 

 
