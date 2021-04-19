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
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="7570b-103">Gewusst wie: direktes Senden von Daten an einen GDI-Drucker</span><span class="sxs-lookup"><span data-stu-id="7570b-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="7570b-104">Im Codebeispiel weiter unten in diesem Thema wird gezeigt, wie Drucker Steuerungsdaten direkt an Drucker gesendet werden, die GDI-basierte Druckertreiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="7570b-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="7570b-105">In den folgenden Schritten wird beschrieben, wie Daten direkt an einen Drucker gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7570b-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="7570b-106">Diese Schritte werden auch im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7570b-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="7570b-107">[**Öffnen Sie OpenPrinter**](openprinter.md) , um ein Handle für den Drucker abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7570b-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="7570b-108">Initialisieren Sie eine [**DocInfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) -Struktur mit den Druckerdaten.</span><span class="sxs-lookup"><span data-stu-id="7570b-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="7570b-109">Aufrufen von [**StartDocPrinter**](startdocprinter.md) , um anzugeben, dass die Anwendung Dokument Daten an den Drucker sendet.</span><span class="sxs-lookup"><span data-stu-id="7570b-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="7570b-110">Aufrufen von [**startpageprinter**](startpageprinter.md) , um anzugeben, dass die Anwendung eine neue Seite an den Drucker sendet.</span><span class="sxs-lookup"><span data-stu-id="7570b-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="7570b-111">Schreiben Sie " [**Write-Printer**](writeprinter.md) ", um die Daten zu senden.</span><span class="sxs-lookup"><span data-stu-id="7570b-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="7570b-112">Ruft [**endpageprinter**](endpageprinter.md) auf, um anzugeben, dass alle Daten für die aktuelle Seite gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7570b-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="7570b-113">Ruft [**enddocprinter**](enddocprinter.md) auf, um anzugeben, dass alle Daten für dieses Dokument gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7570b-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="7570b-114">Ruft [**closeprinter**](closeprinter.md) auf, um die Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7570b-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="7570b-115">Senden Sie Drucker Steuerungsdaten direkt an Drucker, die GDI-basierte Druckertreiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="7570b-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7570b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7570b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7570b-117">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="7570b-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="7570b-118">**Enddocprinter**</span><span class="sxs-lookup"><span data-stu-id="7570b-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="7570b-119">**Endpageprinter**</span><span class="sxs-lookup"><span data-stu-id="7570b-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="7570b-120">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="7570b-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="7570b-121">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="7570b-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="7570b-122">**Startpageprinter**</span><span class="sxs-lookup"><span data-stu-id="7570b-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="7570b-123">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="7570b-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
