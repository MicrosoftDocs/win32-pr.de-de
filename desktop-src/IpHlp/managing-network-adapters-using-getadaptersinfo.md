---
description: Die GetAdaptersInfo-Funktion füllt einen Zeiger auf eine IP-Adapter-INFO-Struktur mit Informationen zu den Netzwerkadaptern, \_ die dem System zugeordnet \_ sind.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Verwalten von Netzwerkadaptern mit GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da19541572af89e9429b9deba68efd4f4670324ffd9ff824e6c123295108f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644630"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Verwalten von Netzwerkadaptern mit GetAdaptersInfo

Die [**GetAdaptersInfo-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) füllt einen Zeiger auf eine [**\_ IP-Adapter-INFO-Struktur \_**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) mit Informationen zu den Netzwerkadaptern, die dem System zugeordnet sind.

**So verwenden Sie GetAdaptersInfo**

1.  Deklarieren Sie einen Zeiger auf eine INFO-Variable des [**\_ \_ IP-Adapters**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) namens *pAdapterInfo* und eine **ULONG-Variable** namens *ulOutBufLen.* Diese Variablen werden als Parameter an die [**GetAdaptersInfo-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) übergeben. Erstellen Sie außerdem eine **DWORD-Variable** namens *dwRetVal* (für die Fehlerüberprüfung).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Ordnen Sie Arbeitsspeicher für die Strukturen zu.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Rufen Sie zunächst [**GetAdaptersInfo auf,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) um die benötigte Größe in die *Variable ulOutBufLen* zu erhalten.
    > [!Note]  
    > Dieser Aufruf der Funktion ist für einen Fehler gedacht und wird verwendet, um sicherzustellen, dass die *variable ulOutBufLen* eine größe angibt, die ausreicht, um alle an *pAdapterInfo* zurückgegebenen Informationen zu enthalten. Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Führen Sie einen zweiten Aufruf von [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)durch, übergeben *Sie pAdapterInfo* und *ulOutBufLen* als Parameter, und führen Sie eine allgemeine Fehlerüberprüfung durch. Geben Sie den Wert an die **DWORD-Variable** *dwRetVal zurück* (für eine ausführlichere Fehlerüberprüfung).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Wenn der Aufruf erfolgreich war, greifen Sie auf einige der Daten in der *pAdapterInfo-Struktur* zu.
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

    

6.  Geben Sie jeglichen Arbeitsspeicher frei, der für die *pAdapterInfo-Struktur zugeordnet* ist.
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Nächster Schritt: [Verwalten von Schnittstellen mit GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

Vorheriger Schritt: [Abrufen von Informationen mit GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 



