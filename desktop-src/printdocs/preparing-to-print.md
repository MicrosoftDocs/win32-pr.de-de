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
# <a name="how-to-collect-print-job-information-from-the-user"></a>Gewusst wie: Sammeln von Druckauftrags Informationen vom Benutzer

In diesem Thema wird beschrieben, wie Druckauftrags Informationen vom Benutzer gesammelt werden.

## <a name="overview"></a>Übersicht

Sammeln von Druckauftrags Informationen vom Benutzer durch Aufrufen der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion. Diese Funktion zeigt dem Benutzer das Dialogfeld "Allgemein **Drucken** " an und gibt die Druckauftrags Informationen in einer [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Datenstruktur zurück.

Das Dialogfeld **Drucken** (allgemein) wird angezeigt, wenn der Benutzer einen Druckauftrag startet. Das Dialogfeld **Drucken** (allgemein) ist ein modales Dialogfeld. Dies bedeutet, dass der Benutzer nicht mit dem Hauptfenster interagieren kann, bis das Dialogfeld "Allgemein" geschlossen wird.

## <a name="collecting-print-job-information"></a>Sammeln von Druckauftrags Informationen

1.  Initialisieren Sie das [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Structure-Element.

    Bevor ein Programm das Dialogfeld " **Drucken** " anzeigen kann, muss es eine [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur zuordnen und initialisieren. Anschließend übergibt Sie diese Struktur an die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion, die das Dialogfeld anzeigt und die Druckauftrags Daten in derselben Struktur zurückgibt. Im folgenden Codebeispiel wird gezeigt, wie dieser Schritt vom Beispielprogramm durchführt wird.

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

    

2.  Zeigt das Dialogfeld **Drucken** (allgemein) an.

    Aufrufen von [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) mit der initialisierten [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, um das Dialogfeld " **Drucken** " (allgemein) anzuzeigen und die Benutzerdaten zu erfassen, wie im folgenden Codebeispiel gezeigt.

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  Speichern Sie die Felder aus der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, und starten Sie den Druckauftrag.

    Die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur enthält die Daten, die die Auswahl beschreiben, die der Benutzer im Dialogfeld Drucken getroffen hat. Einige Member der **PRINTDLG** -Struktur sind Handles für globale Speicher Objekte. Das [Print Sample-Programm](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) kopiert die Daten aus den globalen Speicher Objekten in vom Programm verwaltete Speicherblöcke und kopiert andere Felder aus der **PRINTDLG** -Struktur in Felder in einer Datenstruktur, die vom Programm definiert wurde.

    Nachdem Sie die Daten aus der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur in der Datenstruktur des Programms gespeichert haben, können Sie das Dialogfeld Druckfortschritt öffnen. Die Prozedur zum Drucken des Dialog Felds verarbeitet die Dialogfeld Meldungen und startet den druckverarbeitungs Thread.

    Im folgenden Codebeispiel wird gezeigt, wie Sie die Daten aus der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur in die Datenstruktur des Programms kopieren und den Druckauftrag starten.

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

    

4.  Wenn der Benutzer im Dialogfeld " **Drucken** " auf die Schaltfläche **Abbrechen** klickt, wird keine weitere Verarbeitung durchgeführt.

 

 
