---
description: Die getadaptersinfo-Funktion füllt einen Zeiger auf eine IP- \_ Adapter \_ Informationsstruktur mit Informationen zu den dem System zugeordneten Netzwerkadaptern.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042614"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="71af2-103">Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo</span><span class="sxs-lookup"><span data-stu-id="71af2-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="71af2-104">Die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion füllt einen Zeiger auf eine [**IP- \_ Adapter \_**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) Informationsstruktur mit Informationen zu den dem System zugeordneten Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="71af2-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="71af2-105">**So verwenden Sie getadaptersinfo**</span><span class="sxs-lookup"><span data-stu-id="71af2-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="71af2-106">Deklarieren Sie einen Zeiger auf eine [**IP- \_ Adapter \_ Info-**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) Variable namens *padapterinfo* und eine **ulong** -Variable mit dem Namen *uloutbuflen*.</span><span class="sxs-lookup"><span data-stu-id="71af2-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="71af2-107">Diese Variablen werden als Parameter an die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="71af2-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="71af2-108">Erstellen Sie außerdem eine **DWORD** -Variable mit dem Namen *dwretval* (für die Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="71af2-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="71af2-109">Zuweisen von Arbeitsspeicher für die Strukturen.</span><span class="sxs-lookup"><span data-stu-id="71af2-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="71af2-110">Erstellen Sie zunächst [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , um die benötigte Größe in der *uloutbuflen* -Variablen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="71af2-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="71af2-111">Dieser Aufrufe der-Funktion soll fehlschlagen und verwendet werden, um sicherzustellen, dass die *uloutbuflen* -Variable eine ausreichende Größe für die Speicherung aller an *padapterinfo* zurückgegebenen Informationen angibt.</span><span class="sxs-lookup"><span data-stu-id="71af2-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="71af2-112">Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="71af2-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="71af2-113">Erstellen Sie einen zweiten Rückruf von [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), und übergeben Sie *padapterinfo* und *uloutbuflen* als Parameter und allgemeine Fehlerüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="71af2-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="71af2-114">Rückgabe des Werts an die **DWORD** -Variable *dwretval* (für eine umfassendere Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="71af2-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="71af2-115">Wenn der-Vorgang erfolgreich war, greifen Sie auf einige der Daten in der *padapterinfo* -Struktur zu.</span><span class="sxs-lookup"><span data-stu-id="71af2-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  <span data-ttu-id="71af2-116">Gibt den für die *padapterinfo* -Struktur zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="71af2-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="71af2-117">Nächster Schritt: [Verwalten von Schnittstellen mithilfe von getinterfakeinfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="71af2-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="71af2-118">Vorheriger Schritt: [Abrufen von Informationen mithilfe von getnetworkpara](retrieving-information-using-getnetworkparams.md) Metern</span><span class="sxs-lookup"><span data-stu-id="71af2-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 



