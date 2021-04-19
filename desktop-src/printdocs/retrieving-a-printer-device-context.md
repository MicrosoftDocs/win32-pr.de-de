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
# <a name="how-to-retrieve-a-printer-device-context"></a>Vorgehensweise: Abrufen eines Drucker Geräte Kontexts

In diesem Thema wird beschrieben, wie ein Drucker Gerätekontext abgerufen wird. Sie können einen Drucker Gerätekontext abrufen, indem Sie die [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) -Funktion direkt aufrufen, oder Sie können von einem Dialogfeld " **Drucken** " zurückgegeben werden.

Wenn Sie ein Dialogfeld " **Drucken** " anzeigen, kann ein Benutzer den Drucker, die Seiten des Dokuments und die Anzahl der zu druckenden Dokument Kopien auswählen. Im Dialogfeld **Drucken** (allgemein) werden diese Auswahlmöglichkeiten in einer Datenstruktur zurückgegeben.

In diesem Thema wird beschrieben, wie Sie den Kontext eines Drucker Geräts mithilfe der folgenden Methoden abrufen.

-   [Aufrufen von "kreatedc"](#call-createdc)
-   [Anzeigen eines allgemeinen Druck Dialogfelds](#display-a-print-common-dialog-box)
    -   [Verwenden der printdlgex-Funktion](#using-the-printdlgex-function)
    -   [Verwenden der PrintDlg-Funktion](#using-the-printdlg-function)

## <a name="call-createdc"></a>Aufrufen von "kreatedc"

Wenn Sie das Gerät kennen, das Sie drucken möchten, können Sie " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) " aufrufen und diese Informationen direkt an die Funktion übergeben. " **Kreatedc** " gibt einen Gerätekontext zurück, in den der zu druckende Inhalt dargestellt werden kann.

Der einfachste Abruf zum Abrufen eines Geräte Kontexts wird im folgenden Codebeispiel gezeigt. Der Code in diesem Beispiel ruft einen Gerätekontext zum Standard Anzeigegerät ab.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Zum Renderingvorgang für einen bestimmten Drucker müssen Sie "winspool" als Gerät angeben und den richtigen Drucker Namen an " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca)" übergeben. Sie können auch eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur im Aufrufen von " **anatedc** " übergeben, wenn Sie gerätespezifische Initialisierungs Daten für den Gerätetreiber bereitstellen möchten, wenn Sie den Gerätekontext erstellen.

Das folgende Beispiel zeigt einen Aufrufen von " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ", bei dem der "winspool"-Treiber ausgewählt und der Druckername anhand des Namens angegeben wird.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



Sie können die exakte Zeichenfolge des Drucker namens abrufen, die an [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) übergeben werden soll, indem Sie die [**enumprinter**](enumprinters.md) -Funktion aufrufen. Im folgenden Codebeispiel wird gezeigt, wie Sie **enumprinter** aufzurufen und die Namen der lokalen und lokal verbundenen Drucker abrufen. Da die Größe des erforderlichen Puffers nicht im Voraus bekannt sein kann, wird der **enumprinter** zweimal aufgerufen. Der erste-Befehl gibt die Größe des erforderlichen Puffers zurück. Diese Informationen werden verwendet, um einen Puffer mit der erforderlichen Größe zuzuweisen, und der zweite aufzurufende aufzurufende Daten gibt die gewünschten **Daten zurück.**


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



## <a name="display-a-print-common-dialog-box"></a>Anzeigen eines allgemeinen Druck Dialogfelds

Sie können zwischen zwei **Druck** Dialogfeldern auswählen, die für einen Benutzer angezeigt werden sollen. das neuere Dialogfeld, das Sie anzeigen können, indem Sie die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion aufrufen, und das Dialogfeld für die ältere Formatvorlage, das Sie durch Aufrufen der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion anzeigen können. In den folgenden Abschnitten wird beschrieben, wie jedes Dialogfeld von einer Anwendung aufgerufen wird.

### <a name="using-the-printdlgex-function"></a>Verwenden der printdlgex-Funktion

Aufrufen der [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion, um das **Druck** Eigenschaften Blatt anzuzeigen. Mithilfe des Eigenschaften Blatts kann der Benutzerinformationen zum Druckauftrag angeben. Beispielsweise kann der Benutzer einen Seitenbereich auswählen, der gedruckt werden soll, die Anzahl der Kopien usw. Mit **printdlgex** kann auch ein Handle für einen Gerätekontext für den ausgewählten Drucker abgerufen werden. Sie können das Handle verwenden, um die Ausgabe auf dem Drucker zu Rendering.

Beispielcode, der die Verwendung von [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) zum Abrufen eines Drucker Geräte Kontexts veranschaulicht, finden Sie unter "Verwenden des Druckeigenschaften Blatts" in [Verwenden von allgemeinen Dialog Feldern](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Verwenden der PrintDlg-Funktion

Wenn die Anwendung auf einem System ausgeführt werden muss, das die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion nicht unterstützt, z. b. auf einem System, auf dem eine frühere Windows-Version als Windows 2000 ausgeführt wird, oder die zusätzliche Funktionalität nicht benötigt, die die **printdlgex** -Funktion bereitstellt, verwenden Sie die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion. In den folgenden Schritten wird beschrieben, wie Sie das Dialogfeld für den älteren Stil **Drucken** anzeigen.

1.  Initialisieren Sie die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Datenstruktur.
2.  Aufrufen von [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , um dem Benutzer das Dialogfeld "Allgemein **Drucken** " anzuzeigen.
3.  Wenn der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Rückruf **true** zurückgibt, Sperren Sie den zurückgegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur Arbeitsspeicher. Wenn der **PRINTDLG** -Rückruf " **false**" zurückgibt, hat der Benutzer die Schaltfläche " **Abbrechen** " im Dialogfeld "Allgemein **Drucken** " gedrückt, sodass nichts mehr verarbeitet werden kann.
4.  Zuordnen eines lokalen Speicherpuffers, der groß genug ist, um eine Kopie der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur zu enthalten.
5.  Kopieren Sie die zurückgegebene [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur in die lokal zugeordnete.
6.  Speichern Sie weitere Informationen, die in der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur zurückgegeben werden und die Sie verarbeiten müssen, um den Druckauftrag zu verarbeiten.
7.  Freigeben der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) und der Speicherpuffer, auf die verwiesen wird.

Der folgende Beispielcode veranschaulicht, wie die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion verwendet wird, um den Gerätekontext und den Namen des ausgewählten Druckers zu erhalten.


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



Weitere Informationen zur [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion finden Sie unter "Anzeigen des Druck Dialogfelds" in [Verwenden von allgemeinen Dialog Feldern](../dlgbox/using-common-dialog-boxes.md).

 

 
