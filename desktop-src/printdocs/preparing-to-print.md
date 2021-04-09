---
description: In diesem Thema wird beschrieben, wie Druckauftrags Informationen vom Benutzer gesammelt werden.
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: 'Gewusst wie: Sammeln von Druckauftrags Informationen vom Benutzer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042246"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a><span data-ttu-id="a4096-103">Gewusst wie: Sammeln von Druckauftrags Informationen vom Benutzer</span><span class="sxs-lookup"><span data-stu-id="a4096-103">How To: Collect Print Job Information from the User</span></span>

<span data-ttu-id="a4096-104">In diesem Thema wird beschrieben, wie Druckauftrags Informationen vom Benutzer gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="a4096-104">This topic describes how to collect print job information from the user.</span></span>

## <a name="overview"></a><span data-ttu-id="a4096-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a4096-105">Overview</span></span>

<span data-ttu-id="a4096-106">Sammeln von Druckauftrags Informationen vom Benutzer durch Aufrufen der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a4096-106">Collect print job information from the user by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="a4096-107">Diese Funktion zeigt dem Benutzer das Dialogfeld "Allgemein **Drucken** " an und gibt die Druckauftrags Informationen in einer [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Datenstruktur zurück.</span><span class="sxs-lookup"><span data-stu-id="a4096-107">This function displays the **Print** common dialog box to the user, and returns the print job information in a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>

<span data-ttu-id="a4096-108">Das Dialogfeld **Drucken** (allgemein) wird angezeigt, wenn der Benutzer einen Druckauftrag startet.</span><span class="sxs-lookup"><span data-stu-id="a4096-108">The **Print** common dialog box is displayed when the user starts a print job.</span></span> <span data-ttu-id="a4096-109">Das Dialogfeld **Drucken** (allgemein) ist ein modales Dialogfeld. Dies bedeutet, dass der Benutzer nicht mit dem Hauptfenster interagieren kann, bis das Dialogfeld "Allgemein" geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a4096-109">The **Print** common dialog box is a modal dialog box, which means that the user cannot interact with the main window until the common dialog box is closed.</span></span>

## <a name="collecting-print-job-information"></a><span data-ttu-id="a4096-110">Sammeln von Druckauftrags Informationen</span><span class="sxs-lookup"><span data-stu-id="a4096-110">Collecting Print Job Information</span></span>

1.  <span data-ttu-id="a4096-111">Initialisieren Sie das [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Structure-Element.</span><span class="sxs-lookup"><span data-stu-id="a4096-111">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure element.</span></span>

    <span data-ttu-id="a4096-112">Bevor ein Programm das Dialogfeld " **Drucken** " anzeigen kann, muss es eine [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur zuordnen und initialisieren.</span><span class="sxs-lookup"><span data-stu-id="a4096-112">Before a program can display the **Print** common dialog box , it must allocate and initialize a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="a4096-113">Anschließend übergibt Sie diese Struktur an die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion, die das Dialogfeld anzeigt und die Druckauftrags Daten in derselben Struktur zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a4096-113">It then passes this structure to the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, which displays the dialog and returns the print job data in the same structure.</span></span> <span data-ttu-id="a4096-114">Im folgenden Codebeispiel wird gezeigt, wie dieser Schritt vom Beispielprogramm durchführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4096-114">The following code example shows how the sample program performs this step.</span></span>

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  <span data-ttu-id="a4096-115">Zeigt das Dialogfeld **Drucken** (allgemein) an.</span><span class="sxs-lookup"><span data-stu-id="a4096-115">Display the **Print** common dialog box.</span></span>

    <span data-ttu-id="a4096-116">Aufrufen von [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) mit der initialisierten [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, um das Dialogfeld " **Drucken** " (allgemein) anzuzeigen und die Benutzerdaten zu erfassen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4096-116">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) with the initialized [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to display the **Print** common dialog box and collect the user data, as shown in the following code example.</span></span>

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  <span data-ttu-id="a4096-117">Speichern Sie die Felder aus der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, und starten Sie den Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="a4096-117">Save the fields from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and start the print job.</span></span>

    <span data-ttu-id="a4096-118">Die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur enthält die Daten, die die Auswahl beschreiben, die der Benutzer im Dialogfeld Drucken getroffen hat.</span><span class="sxs-lookup"><span data-stu-id="a4096-118">The [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure contains the data that describes the selections that the user made in the print dialog box.</span></span> <span data-ttu-id="a4096-119">Einige Member der **PRINTDLG** -Struktur sind Handles für globale Speicher Objekte.</span><span class="sxs-lookup"><span data-stu-id="a4096-119">Some members of the **PRINTDLG** structure are handles to global memory objects.</span></span> <span data-ttu-id="a4096-120">Das [Print Sample-Programm](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) kopiert die Daten aus den globalen Speicher Objekten in vom Programm verwaltete Speicherblöcke und kopiert andere Felder aus der **PRINTDLG** -Struktur in Felder in einer Datenstruktur, die vom Programm definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a4096-120">The [Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copies the data from the global memory objects to memory blocks that the program manages and copies other fields from the **PRINTDLG** structure to fields in a data structure that the program defined.</span></span>

    <span data-ttu-id="a4096-121">Nachdem Sie die Daten aus der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur in der Datenstruktur des Programms gespeichert haben, können Sie das Dialogfeld Druckfortschritt öffnen.</span><span class="sxs-lookup"><span data-stu-id="a4096-121">After you store the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure in the program's data structure, you can open the print progress dialog box.</span></span> <span data-ttu-id="a4096-122">Die Prozedur zum Drucken des Dialog Felds verarbeitet die Dialogfeld Meldungen und startet den druckverarbeitungs Thread.</span><span class="sxs-lookup"><span data-stu-id="a4096-122">The print progress dialog box procedure handles the dialog box messages and starts the print processing thread.</span></span>

    <span data-ttu-id="a4096-123">Im folgenden Codebeispiel wird gezeigt, wie Sie die Daten aus der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur in die Datenstruktur des Programms kopieren und den Druckauftrag starten.</span><span class="sxs-lookup"><span data-stu-id="a4096-123">The following code example shows how to copy the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to the program's data structure and how to start the print job.</span></span>

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  <span data-ttu-id="a4096-124">Wenn der Benutzer im Dialogfeld " **Drucken** " auf die Schaltfläche **Abbrechen** klickt, wird keine weitere Verarbeitung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4096-124">If the user clicks the **Cancel** button in the **Print** common dialog box, no further processing is performed.</span></span>

 

 
