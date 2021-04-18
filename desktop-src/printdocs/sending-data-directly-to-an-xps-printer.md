---
description: In diesem Thema wird beschrieben, wie Drucker Steuerungsdaten direkt an Drucker gesendet werden, die XPSDrv-Druckertreiber verwenden.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'Gewusst wie: direktes Senden von Daten an einen XPS-Drucker'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78a8c36d6862860862059f9bbcc8db25e171b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347341"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>Gewusst wie: direktes Senden von Daten an einen XPS-Drucker

In diesem Thema wird beschrieben, wie Drucker Steuerungsdaten direkt an Drucker gesendet werden, die XPSDrv-Druckertreiber verwenden.

In den folgenden Schritten wird beschrieben, wie Daten direkt an einen Drucker gesendet werden. Diese Schritte werden auch im folgenden Codebeispiel veranschaulicht.

1.  [**Öffnen Sie OpenPrinter**](openprinter.md) , um ein Handle für den Drucker abzurufen.
2.  Initialisieren Sie eine [**DocInfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) -Struktur mit den Druckerdaten.
3.  Aufrufen von [**StartDocPrinter**](startdocprinter.md) , um anzugeben, dass die Anwendung Dokument Daten an den Drucker sendet.
4.  Schreiben Sie " [**Write-Printer**](writeprinter.md) ", um die Daten zu senden.
5.  Ruft [**enddocprinter**](enddocprinter.md) auf, um anzugeben, dass alle Daten für dieses Dokument gesendet wurden.
6.  Ruft [**closeprinter**](closeprinter.md) auf, um die Ressourcen freizugeben.

Senden Sie Drucker Steuerungsdaten direkt an Drucker, die XPSDrv-Druckertreiber verwenden.


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
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

 

 
