---
description: Die GetTcpStatistics-Funktion füllt einen Zeiger auf eine MIB \_ tcpstats-Struktur mit Informationen zu den TCP-Protokoll Statistiken für den lokalen Computer.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Abrufen von Informationen mithilfe von GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362287"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="c2753-103">Abrufen von Informationen mithilfe von GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="c2753-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="c2753-104">Die [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) -Funktion füllt einen Zeiger auf eine [**MIB \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Struktur mit Informationen zu den TCP-Protokoll Statistiken für den lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c2753-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="c2753-105">**So verwenden Sie GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="c2753-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="c2753-106">Deklarieren Sie einige erforderliche Variablen.</span><span class="sxs-lookup"><span data-stu-id="c2753-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="c2753-107">Deklarieren Sie eine **DWORD** -Variable `dwRetVal` , die für Fehler Überprüfungs Funktionsaufrufe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2753-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="c2753-108">Deklarieren Sie einen Zeiger auf eine [**MIB- \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Variable mit dem Namen *ptcpstats*, und weisen Sie der Struktur Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="c2753-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="c2753-109">Überprüfen Sie, ob Arbeitsspeicher zugeordnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="c2753-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="c2753-110">Rufen Sie die Funktion " [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) " mit dem Parameter " *ptcpstats* " auf, um TCP-Statistiken für IPv4 auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c2753-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="c2753-111">Überprüfen Sie auf Fehler, und geben Sie den Fehlerwert in der **DWORD** -Variablen zurück `dwRetVal` .</span><span class="sxs-lookup"><span data-stu-id="c2753-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="c2753-112">Wenn ein Fehler auftritt, `dwRetVal` kann die Variable für eine umfassendere Fehlerüberprüfung und Berichterstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2753-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="c2753-113">Wenn der-Befehl erfolgreich ausgeführt wurde, greifen Sie auf die Daten zu *, die in* den [**MIB- \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Werten zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="c2753-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="c2753-114">Gibt den Arbeitsspeicher frei, der für die [**MIB \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Struktur reserviert ist, auf die der *ptcpstats* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="c2753-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="c2753-115">Dies sollte erfolgen, wenn die Anwendung die Daten nicht mehr benötigt, die vom *ptcpstats* -Parameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2753-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="c2753-116">Nächster Schritt: [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="c2753-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="c2753-117">Vorheriger Schritt: [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="c2753-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="c2753-118">Vervollständigen des Quellcodes</span><span class="sxs-lookup"><span data-stu-id="c2753-118">Complete Source Code</span></span>

-   [<span data-ttu-id="c2753-119">Vollständiger IP-hilfsanwendungs-Quellcode</span><span class="sxs-lookup"><span data-stu-id="c2753-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 
