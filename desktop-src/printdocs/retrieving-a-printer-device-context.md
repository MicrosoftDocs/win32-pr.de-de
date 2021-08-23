---
description: In diesem Thema wird das Abrufen eines Druckergerätekontexts beschrieben.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'How To: Retrieve a Printer Device Context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f723ece0e00d58ed684029e0eb3202d637443bd7f0e9d8878024346b9d79ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600560"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>How To: Retrieve a Printer Device Context

In diesem Thema wird das Abrufen eines Druckergerätekontexts beschrieben. Sie können einen Druckergerätekontext abrufen, indem Sie die [**CreateDC-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createdca) direkt aufrufen, oder sie kann von einem allgemeinen Dialogfeld Drucken **zurückgegeben** werden.

Wenn Sie ein **Allgemeines** Dialogfeld Drucken anzeigen, kann ein Benutzer den Drucker, die Seiten des Dokuments und die Anzahl der Dokumentkopien auswählen, die er drucken möchte. Das **Dialogfeld Allgemein** drucken gibt diese Auswahl in einer Datenstruktur zurück.

In diesem Thema wird beschrieben, wie Sie mithilfe der folgenden Methoden einen Druckergerätekontext abrufen.

-   [Aufrufen von CreateDC](#call-createdc)
-   [Anzeigen eines allgemeinen Druckdialogfelds](#display-a-print-common-dialog-box)
    -   [Verwenden der PrintDlgEx-Funktion](#using-the-printdlgex-function)
    -   [Verwenden der PrintDlg-Funktion](#using-the-printdlg-function)

## <a name="call-createdc"></a>Aufrufen von CreateDC

Wenn Sie das Gerät kennen, auf dem Sie drucken möchten, können Sie [**CreateDC aufrufen**](/windows/desktop/api/wingdi/nf-wingdi-createdca) und diese Informationen direkt an die Funktion übergeben. **CreateDC gibt** einen Gerätekontext zurück, in dem Sie den zu druckenden Inhalt rendern können.

Der einfachste Aufruf zum Abrufen eines Gerätekontexts wird im folgenden Codebeispiel gezeigt. Der Code in diesem Beispiel ruft einen Gerätekontext auf das Standardanzeigegerät ab.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Um auf einem bestimmten Drucker zu rendern, müssen Sie "WINSPOOL" als Gerät angeben und den richtigen Namen des Druckers an [**CreateDC übergeben.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) Sie können auch eine [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) im Aufruf von **CreateDC** übergeben, wenn Sie beim Erstellen des Gerätekontexts gerätespezifische Initialisierungsdaten für den Gerätetreiber bereitstellen möchten.

Das folgende Beispiel zeigt einen Aufruf von [**CreateDC,**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in dem der WINSPOOL-Treiber ausgewählt und der Druckername durch den Namen angegeben wird.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



Sie können die exakte Druckernamenzeichenfolge abrufen, die an [**CreateDC übergeben werden soll,**](/windows/desktop/api/wingdi/nf-wingdi-createdca) indem Sie die [**EnumPrinters-Funktion**](enumprinters.md) aufrufen. Das folgende Codebeispiel zeigt, wie **Sie EnumPrinters** aufrufen und die Namen der lokalen und lokal verbundenen Drucker erhalten. Da die Größe des erforderlichen Puffers nicht im Voraus bekannt ist, wird **EnumPrinters** zweimal aufgerufen. Der erste Aufruf gibt die Größe des erforderlichen Puffers zurück. Diese Informationen werden verwendet, um einen Puffer der erforderlichen Größe zu reservieren, und der zweite Aufruf von **EnumPrinters** gibt die gewünschten Daten zurück.


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



## <a name="display-a-print-common-dialog-box"></a>Anzeigen eines allgemeinen Druckdialogfelds

Sie können zwischen  zwei allgemeinen Dialogfeldern drucken auswählen, um sie einem Benutzer anzuzeigen. das neuere Dialogfeld, das Sie anzeigen können, indem Sie die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) aufrufen, und das ältere Formatdialogfeld, das Sie anzeigen können, indem Sie die [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) aufrufen. In den folgenden Abschnitten wird beschrieben, wie sie die einzelnen Dialogfelder aus einer Anwendung aufrufen.

### <a name="using-the-printdlgex-function"></a>Verwenden der PrintDlgEx-Funktion

Rufen Sie die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) auf, um das **Eigenschaftenblatt Drucken** anzuzeigen. Mithilfe des Eigenschaftenblatts kann der Benutzer Informationen zum Druckauftrag angeben. Der Benutzer kann z. B. einen Bereich von seiten auswählen, der gedruckt werden soll, die Anzahl der Kopien und so weiter. **PrintDlgEx kann** auch ein Handle für einen Gerätekontext für den ausgewählten Drucker abrufen. Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu rendern.

Beispielcode, der die Verwendung von [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) zum Abrufen eines Druckergerätekontexts veranschaulicht, finden Sie unter "Verwenden des Druckeigenschaftenblatts" in Verwenden von [allgemeinen Dialogfeldern](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Verwenden der PrintDlg-Funktion

Wenn Ihre Anwendung auf einem System ausgeführt werden muss, das die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) nicht unterstützt, z. B. auf einem System, auf dem eine Version von Windows vor Windows 2000 ausgeführt wird, oder nicht die zusätzliche Funktionalität benötigt, die die **PrintDlgEx-Funktion** bietet, verwenden Sie die [**PrintDlg-Funktion.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) In den folgenden Schritten wird beschrieben, wie Sie das Dialogfeld "Allgemein **drucken"** im älteren Format anzeigen.

1.  Initialisieren Sie [**die PRINTDLG-Datenstruktur.**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
2.  Rufen [**Sie PrintDlg auf,**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **um** dem Benutzer das Dialogfeld Allgemein drucken anzuzeigen.
3.  Wenn der [**PrintDlg-Aufruf**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **TRUE zurückgibt,** sperren Sie den zurückgegebenen [**DEVMODE-Strukturspeicher.**](/windows/win32/api/wingdi/ns-wingdi-devmodea) Wenn der **PrintDlg-Aufruf** **FALSE zurückgibt,** hat  der Benutzer im Dialogfeld Allgemeines Drucken auf die Schaltfläche Abbrechen gedrückt, damit nichts weiter zu verarbeiten ist. 
4.  Ordnen Sie einen lokalen Speicherpuffer zu, der groß genug ist, um eine Kopie der [**DEVMODE-Struktur zu**](/windows/win32/api/wingdi/ns-wingdi-devmodea) enthalten.
5.  Kopieren Sie die [**zurückgegebene DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in die lokal zugeordnete Struktur.
6.  Speichern Sie weitere Informationen, die in der [**PRINTDLG-Struktur zurückgegeben**](/windows/win32/api/commdlg/ns-commdlg-printdlga) werden und die Sie zum Verarbeiten des Druckauftrags benötigen.
7.  Geben Sie [**die PRINTDLG und**](/windows/win32/api/commdlg/ns-commdlg-printdlga) die Speicherpuffer frei, auf die sie verweist.

Der folgende Beispielcode veranschaulicht die Verwendung der [**PrintDlg-Funktion,**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) um den Gerätekontext und den Namen des ausgewählten Druckers zu erhalten.


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



Weitere Informationen zur [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) finden Sie unter "Anzeigen des Druckdialogfelds" unter [Verwenden von allgemeinen Dialogfeldern.](../dlgbox/using-common-dialog-boxes.md)

 

 
