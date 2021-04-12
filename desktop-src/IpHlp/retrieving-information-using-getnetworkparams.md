---
description: Füllt einen Zeiger auf eine fixierte \_ Informationsstruktur mit Daten über die aktuellen Netzwerkeinstellungen.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Abrufen von Informationen mithilfe von getnetworkpara Metern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216384"
---
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="80863-103">Abrufen von Informationen mithilfe von getnetworkpara Metern</span><span class="sxs-lookup"><span data-stu-id="80863-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="80863-104">Die [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) -Funktion füllt einen Zeiger auf eine [**fixierte \_ Informations**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) Struktur mit Daten über die aktuellen Netzwerkeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="80863-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="80863-105">**So verwenden Sie "getnetworkparameams"**</span><span class="sxs-lookup"><span data-stu-id="80863-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="80863-106">Deklarieren Sie einen Zeiger auf ein [**festes \_ Info**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) Objekt mit dem Namen *pfixedinfo* und ein **ulong** -Objekt mit dem Namen *uloutbuflen*.</span><span class="sxs-lookup"><span data-stu-id="80863-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="80863-107">Diese Variablen werden als Parameter an die [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) -Funktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="80863-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="80863-108">Erstellen Sie außerdem eine **DWORD** -Variable *dwretval* (für die Fehlerüberprüfung verwendet).</span><span class="sxs-lookup"><span data-stu-id="80863-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="80863-109">Zuweisen von Arbeitsspeicher für die Strukturen.</span><span class="sxs-lookup"><span data-stu-id="80863-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="80863-110">Die Größe von *uloutbuflen* reicht nicht aus, um die Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="80863-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="80863-111">Weitere Informationen finden Sie im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="80863-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="80863-112">Führen Sie einen ersten Rückruf an [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) aus, um die für die *uloutbuflen* -Variable erforderliche Größe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="80863-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="80863-113">Diese Funktions Funktion schlägt fehl und wird verwendet, um sicherzustellen, dass die *uloutbuflen* -Variable eine ausreichende Größe für die Speicherung aller an *pfixedinfo* zurückgegebenen Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="80863-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="80863-114">Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="80863-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="80863-115">Erstellen Sie einen zweiten Rückruf von [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) mithilfe allgemeiner Fehlerüberprüfung, und geben Sie den Wert an die **DWORD** -Variable *dwretval* zurück. wird für erweiterte Fehlerüberprüfungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="80863-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="80863-116">Wenn der-Vorgang erfolgreich war, greifen Sie auf die Daten aus der *pfixedinfo* -Datenstruktur zu.</span><span class="sxs-lookup"><span data-stu-id="80863-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  <span data-ttu-id="80863-117">Gibt den für die *pfixedinfo* -Struktur zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="80863-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="80863-118">Nächster Schritt: [Verwalten von Netzwerkadaptern mit getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="80863-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="80863-119">Vorheriger Schritt: [Erstellen einer grundlegenden IP-Hilfsanwendung](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="80863-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 



