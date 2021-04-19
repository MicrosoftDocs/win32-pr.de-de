---
description: Die GetIpStatistics-Funktion füllt einen Zeiger auf eine MIB \_ -ipstats-Struktur mit Informationen über die aktuelle IP-Statistik aus, die dem System zugeordnet ist.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Abrufen von Informationen mithilfe von GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368809"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="08f1f-103">Abrufen von Informationen mithilfe von GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="08f1f-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="08f1f-104">Die [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) -Funktion füllt einen Zeiger auf eine [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Struktur mit Informationen über die aktuelle IP-Statistik aus, die dem System zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08f1f-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="08f1f-105">**So verwenden Sie "GetIpStatistics"**</span><span class="sxs-lookup"><span data-stu-id="08f1f-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="08f1f-106">Deklarieren Sie einige erforderliche Variablen.</span><span class="sxs-lookup"><span data-stu-id="08f1f-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="08f1f-107">Deklarieren Sie eine **DWORD** -Variable `dwRetval` , die für Fehler Überprüfungs Funktionsaufrufe verwendet.</span><span class="sxs-lookup"><span data-stu-id="08f1f-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="08f1f-108">Deklarieren Sie einen Zeiger auf eine [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Variable mit dem Namen *pStats*, und weisen Sie der Struktur Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="08f1f-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="08f1f-109">Überprüfen Sie, ob Arbeitsspeicher zugeordnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="08f1f-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="08f1f-110">Rufen Sie die Funktion [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) mit dem *pStats* -Parameter auf, um IP-Statistiken für den lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="08f1f-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="08f1f-111">Überprüfen Sie auf Fehler, und geben Sie den Fehlerwert in der **DWORD** -Variablen zurück `dwRetval` .</span><span class="sxs-lookup"><span data-stu-id="08f1f-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="08f1f-112">Wenn ein Fehler auftritt, `dwRetval` kann die Variable für eine umfassendere Fehlerüberprüfung und Berichterstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08f1f-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="08f1f-113">Wenn der Aufrufen von [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) erfolgreich war, können Sie einige der Daten in der [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Struktur ausgeben, auf die der *pStats* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="08f1f-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="08f1f-114">Gibt den für die [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Struktur zugeordneten Arbeitsspeicher frei, auf den der *pStats* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="08f1f-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="08f1f-115">Dies sollte erfolgen, wenn die Anwendung die Daten nicht mehr benötigt, die vom *pStats* -Parameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08f1f-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="08f1f-116">Nächster Schritt: [Abrufen von Informationen mithilfe von GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="08f1f-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="08f1f-117">Vorheriger Schritt: [Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="08f1f-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 
