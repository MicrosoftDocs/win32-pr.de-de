---
description: In diesem Thema wird beschrieben, wie ein Drucker Gerätekontext abgerufen wird.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Vorgehensweise: Abrufen eines Drucker Geräte Kontexts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356292"
---
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="22863-103">Vorgehensweise: Abrufen eines Drucker Geräte Kontexts</span><span class="sxs-lookup"><span data-stu-id="22863-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="22863-104">In diesem Thema wird beschrieben, wie ein Drucker Gerätekontext abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="22863-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="22863-105">Sie können einen Drucker Gerätekontext abrufen, indem Sie die [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) -Funktion direkt aufrufen, oder Sie können von einem Dialogfeld " **Drucken** " zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22863-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="22863-106">Wenn Sie ein Dialogfeld " **Drucken** " anzeigen, kann ein Benutzer den Drucker, die Seiten des Dokuments und die Anzahl der zu druckenden Dokument Kopien auswählen.</span><span class="sxs-lookup"><span data-stu-id="22863-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="22863-107">Im Dialogfeld **Drucken** (allgemein) werden diese Auswahlmöglichkeiten in einer Datenstruktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22863-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="22863-108">In diesem Thema wird beschrieben, wie Sie den Kontext eines Drucker Geräts mithilfe der folgenden Methoden abrufen.</span><span class="sxs-lookup"><span data-stu-id="22863-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="22863-109">Aufrufen von "kreatedc"</span><span class="sxs-lookup"><span data-stu-id="22863-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="22863-110">Anzeigen eines allgemeinen Druck Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="22863-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="22863-111">Verwenden der printdlgex-Funktion</span><span class="sxs-lookup"><span data-stu-id="22863-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="22863-112">Verwenden der PrintDlg-Funktion</span><span class="sxs-lookup"><span data-stu-id="22863-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="22863-113">Aufrufen von "kreatedc"</span><span class="sxs-lookup"><span data-stu-id="22863-113">Call CreateDC</span></span>

<span data-ttu-id="22863-114">Wenn Sie das Gerät kennen, das Sie drucken möchten, können Sie " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) " aufrufen und diese Informationen direkt an die Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="22863-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="22863-115">" **Kreatedc** " gibt einen Gerätekontext zurück, in den der zu druckende Inhalt dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="22863-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="22863-116">Der einfachste Abruf zum Abrufen eines Geräte Kontexts wird im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="22863-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="22863-117">Der Code in diesem Beispiel ruft einen Gerätekontext zum Standard Anzeigegerät ab.</span><span class="sxs-lookup"><span data-stu-id="22863-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="22863-118">Zum Renderingvorgang für einen bestimmten Drucker müssen Sie "winspool" als Gerät angeben und den richtigen Drucker Namen an " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca)" übergeben.</span><span class="sxs-lookup"><span data-stu-id="22863-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="22863-119">Sie können auch eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur im Aufrufen von " **anatedc** " übergeben, wenn Sie gerätespezifische Initialisierungs Daten für den Gerätetreiber bereitstellen möchten, wenn Sie den Gerätekontext erstellen.</span><span class="sxs-lookup"><span data-stu-id="22863-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="22863-120">Das folgende Beispiel zeigt einen Aufrufen von " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ", bei dem der "winspool"-Treiber ausgewählt und der Druckername anhand des Namens angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="22863-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="22863-121">Sie können die exakte Zeichenfolge des Drucker namens abrufen, die an [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) übergeben werden soll, indem Sie die [**enumprinter**](enumprinters.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22863-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="22863-122">Im folgenden Codebeispiel wird gezeigt, wie Sie **enumprinter** aufzurufen und die Namen der lokalen und lokal verbundenen Drucker abrufen.</span><span class="sxs-lookup"><span data-stu-id="22863-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="22863-123">Da die Größe des erforderlichen Puffers nicht im Voraus bekannt sein kann, wird der **enumprinter** zweimal aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="22863-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="22863-124">Der erste-Befehl gibt die Größe des erforderlichen Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="22863-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="22863-125">Diese Informationen werden verwendet, um einen Puffer mit der erforderlichen Größe zuzuweisen, und der zweite aufzurufende aufzurufende Daten gibt die gewünschten **Daten zurück.**</span><span class="sxs-lookup"><span data-stu-id="22863-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="22863-126">Anzeigen eines allgemeinen Druck Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="22863-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="22863-127">Sie können zwischen zwei **Druck** Dialogfeldern auswählen, die für einen Benutzer angezeigt werden sollen. das neuere Dialogfeld, das Sie anzeigen können, indem Sie die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion aufrufen, und das Dialogfeld für die ältere Formatvorlage, das Sie durch Aufrufen der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="22863-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="22863-128">In den folgenden Abschnitten wird beschrieben, wie jedes Dialogfeld von einer Anwendung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="22863-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="22863-129">Verwenden der printdlgex-Funktion</span><span class="sxs-lookup"><span data-stu-id="22863-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="22863-130">Aufrufen der [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion, um das **Druck** Eigenschaften Blatt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22863-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="22863-131">Mithilfe des Eigenschaften Blatts kann der Benutzerinformationen zum Druckauftrag angeben.</span><span class="sxs-lookup"><span data-stu-id="22863-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="22863-132">Beispielsweise kann der Benutzer einen Seitenbereich auswählen, der gedruckt werden soll, die Anzahl der Kopien usw.</span><span class="sxs-lookup"><span data-stu-id="22863-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="22863-133">Mit **printdlgex** kann auch ein Handle für einen Gerätekontext für den ausgewählten Drucker abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="22863-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="22863-134">Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="22863-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="22863-135">Beispielcode, der die Verwendung von [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) zum Abrufen eines Drucker Geräte Kontexts veranschaulicht, finden Sie unter "Verwenden des Druckeigenschaften Blatts" in [Verwenden von allgemeinen Dialog Feldern](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="22863-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="22863-136">Verwenden der PrintDlg-Funktion</span><span class="sxs-lookup"><span data-stu-id="22863-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="22863-137">Wenn die Anwendung auf einem System ausgeführt werden muss, das die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion nicht unterstützt, z. b. auf einem System, auf dem eine frühere Windows-Version als Windows 2000 ausgeführt wird, oder die zusätzliche Funktionalität nicht benötigt, die die **printdlgex** -Funktion bereitstellt, verwenden Sie die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="22863-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="22863-138">In den folgenden Schritten wird beschrieben, wie Sie das Dialogfeld für den älteren Stil **Drucken** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="22863-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="22863-139">Initialisieren Sie die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="22863-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="22863-140">Aufrufen von [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , um dem Benutzer das Dialogfeld "Allgemein **Drucken** " anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22863-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="22863-141">Wenn der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Rückruf **true** zurückgibt, Sperren Sie den zurückgegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="22863-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="22863-142">Wenn der **PRINTDLG** -Rückruf " **false**" zurückgibt, hat der Benutzer die Schaltfläche " **Abbrechen** " im Dialogfeld "Allgemein **Drucken** " gedrückt, sodass nichts mehr verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="22863-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="22863-143">Zuordnen eines lokalen Speicherpuffers, der groß genug ist, um eine Kopie der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="22863-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="22863-144">Kopieren Sie die zurückgegebene [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur in die lokal zugeordnete.</span><span class="sxs-lookup"><span data-stu-id="22863-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="22863-145">Speichern Sie weitere Informationen, die in der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur zurückgegeben werden und die Sie verarbeiten müssen, um den Druckauftrag zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="22863-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="22863-146">Freigeben der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) und der Speicherpuffer, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="22863-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="22863-147">Der folgende Beispielcode veranschaulicht, wie die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion verwendet wird, um den Gerätekontext und den Namen des ausgewählten Druckers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22863-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



<span data-ttu-id="22863-148">Weitere Informationen zur [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion finden Sie unter "Anzeigen des Druck Dialogfelds" in [Verwenden von allgemeinen Dialog Feldern](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="22863-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
