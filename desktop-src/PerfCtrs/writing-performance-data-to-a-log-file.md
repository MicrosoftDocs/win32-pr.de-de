---
description: Im folgenden Beispiel werden Leistungsdaten in Echtzeit in eine Protokolldatei geschrieben.
ms.assetid: a1bc40ea-d928-495a-abc0-daf097202a12
title: Schreiben von Leistungsdaten in eine Protokolldatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afce3c85b36d66f1b621e4c4f174bff327e6084a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368747"
---
# <a name="writing-performance-data-to-a-log-file"></a><span data-ttu-id="ab5bc-103">Schreiben von Leistungsdaten in eine Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="ab5bc-103">Writing Performance Data to a Log File</span></span>

<span data-ttu-id="ab5bc-104">Im folgenden Beispiel werden Leistungsdaten in Echtzeit in eine Protokolldatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab5bc-104">The following example writes real time performance data to a log file.</span></span> <span data-ttu-id="ab5bc-105">Im Beispiel werden die Funktionen " [**pdhopenquery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) " und " [**pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) " aufgerufen, um eine Abfrage zum Sammeln von Prozessorzeit-gegen Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab5bc-105">The example calls the [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) and [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) functions to create a query to collect Processor Time counter data.</span></span> <span data-ttu-id="ab5bc-106">Im Beispiel wird dann die [**pdhopenlog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) -Funktion aufgerufen, um die Protokolldatei zu erstellen, in die die Daten geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab5bc-106">The example then calls the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function to create the log file to write the data to.</span></span> <span data-ttu-id="ab5bc-107">Im Beispiel wird die [**pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) -Funktion aufgerufen, um ein Beispiel zu erfassen und die Protokolldatei einmal pro Sekunde für 20 Sekunden zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ab5bc-107">The example calls the [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) function to collect a sample and update the log file once a second for 20 seconds.</span></span>

<span data-ttu-id="ab5bc-108">Ein Beispiel, in dem die generierte Protokolldatei gelesen wird, finden Sie unter [Lesen von Leistungsdaten aus einer Protokolldatei](reading-performance-data-from-a-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="ab5bc-108">For an example that reads the generated log file, see [Reading Performance Data from a Log File](reading-performance-data-from-a-log-file.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH    = L"\\Processor(0)\\% Processor Time";
CONST ULONG SAMPLE_INTERVAL_MS = 1000;

void DisplayCommandLineHelp(void)
{
    wprintf(L"The command line must include a valid log file name.\n"); 
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HLOG hLog = NULL;
    PDH_STATUS pdhStatus;
    DWORD dwLogType = PDH_LOG_TYPE_CSV;
    HCOUNTER hCounter;
    DWORD dwCount;

    if (argc != 2) 
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Open a query object.
    pdhStatus = PdhOpenQuery(NULL, 0, &hQuery);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Add one counter that will provide the data.
    pdhStatus = PdhAddCounter(hQuery,
        COUNTER_PATH,
        0,
        &hCounter);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Open the log file for write access.
    pdhStatus = PdhOpenLog(argv[1], 
        PDH_LOG_WRITE_ACCESS | PDH_LOG_CREATE_ALWAYS,
        &dwLogType,
        hQuery,
        0, 
        NULL,
        &hLog);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenLog failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }
 
    // Write 10 records to the log file.
    for (dwCount = 0; dwCount < 10; dwCount++) 
    {
        wprintf(L"Writing record %d\n", dwCount);

        pdhStatus = PdhUpdateLog (hLog, NULL);
        if (ERROR_SUCCESS != pdhStatus)
        {
            wprintf(L"PdhUpdateLog failed with 0x%x\n", pdhStatus);
            goto cleanup;
        }

        // Wait one second between samples for a counter update.
        Sleep(SAMPLE_INTERVAL_MS); 
    }

cleanup:

    // Close the log file.
    if (hLog)
        PdhCloseLog (hLog, 0);

    // Close the query object.
    if (hQuery)
        PdhCloseQuery (hQuery);
}
```



 

 



