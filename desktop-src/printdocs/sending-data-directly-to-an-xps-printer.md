---
description: In diesem Thema wird beschrieben, wie Druckersteuerungsdaten direkt an Drucker gesendet werden, die XPSDrv-Druckertreiber verwenden.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'How To: Senden von Daten direkt an einen XPS-Drucker'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fba87578f9257290123b737f2d1d8c3e48f57e6a628110a20a232ddb290ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470152"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>How To: Senden von Daten direkt an einen XPS-Drucker

In diesem Thema wird beschrieben, wie Druckersteuerungsdaten direkt an Drucker gesendet werden, die XPSDrv-Druckertreiber verwenden.

In den folgenden Schritten wird beschrieben, wie Daten direkt an einen Drucker gesendet werden. Diese Schritte werden auch im folgenden Codebeispiel veranschaulicht.

1.  Rufen [**Sie OpenPrinter auf,**](openprinter.md) um ein Handle für den Drucker zu erhalten.
2.  Initialisieren Sie [**eine DOCINFO-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) mit den Druckerdaten.
3.  Rufen [**Sie StartDocPrinter auf,**](startdocprinter.md) um anzugeben, dass die Anwendung Dokumentdaten an den Drucker sendet.
4.  Rufen Sie [**WritePrinter auf,**](writeprinter.md) um die Daten zu senden.
5.  Rufen [**Sie EndDocPrinter auf,**](enddocprinter.md) um anzugeben, dass alle Daten für dieses Dokument gesendet wurden.
6.  Rufen [**Sie ClosePrinter auf,**](closeprinter.md) um die Ressourcen frei zu geben.

Senden Sie Druckersteuerungsdaten direkt an Drucker, die XPSDrv-Druckertreiber verwenden.


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

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 
