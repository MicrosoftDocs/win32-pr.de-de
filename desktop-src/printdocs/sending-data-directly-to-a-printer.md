---
description: Im Codebeispiel weiter unten in diesem Thema wird gezeigt, wie Drucker Steuerungsdaten direkt an Drucker gesendet werden, die GDI-basierte Druckertreiber verwenden.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 'Gewusst wie: direktes Senden von Daten an einen GDI-Drucker'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349355"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>Gewusst wie: direktes Senden von Daten an einen GDI-Drucker

Im Codebeispiel weiter unten in diesem Thema wird gezeigt, wie Drucker Steuerungsdaten direkt an Drucker gesendet werden, die GDI-basierte Druckertreiber verwenden.

In den folgenden Schritten wird beschrieben, wie Daten direkt an einen Drucker gesendet werden. Diese Schritte werden auch im folgenden Codebeispiel veranschaulicht.

1.  [**Öffnen Sie OpenPrinter**](openprinter.md) , um ein Handle für den Drucker abzurufen.
2.  Initialisieren Sie eine [**DocInfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) -Struktur mit den Druckerdaten.
3.  Aufrufen von [**StartDocPrinter**](startdocprinter.md) , um anzugeben, dass die Anwendung Dokument Daten an den Drucker sendet.
4.  Aufrufen von [**startpageprinter**](startpageprinter.md) , um anzugeben, dass die Anwendung eine neue Seite an den Drucker sendet.
5.  Schreiben Sie " [**Write-Printer**](writeprinter.md) ", um die Daten zu senden.
6.  Ruft [**endpageprinter**](endpageprinter.md) auf, um anzugeben, dass alle Daten für die aktuelle Seite gesendet wurden.
7.  Ruft [**enddocprinter**](enddocprinter.md) auf, um anzugeben, dass alle Daten für dieses Dokument gesendet wurden.
8.  Ruft [**closeprinter**](closeprinter.md) auf, um die Ressourcen freizugeben.

Senden Sie Drucker Steuerungsdaten direkt an Drucker, die GDI-basierte Druckertreiber verwenden.


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }
    return bStatus;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Enddocprinter**](enddocprinter.md)
</dt> <dt>

[**Endpageprinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Startpageprinter**](startpageprinter.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> </dl>

 

 
