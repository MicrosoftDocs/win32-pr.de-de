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
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo

Die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion füllt einen Zeiger auf eine [**IP- \_ Adapter \_**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) Informationsstruktur mit Informationen zu den dem System zugeordneten Netzwerkadaptern.

**So verwenden Sie getadaptersinfo**

1.  Deklarieren Sie einen Zeiger auf eine [**IP- \_ Adapter \_ Info-**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) Variable namens *padapterinfo* und eine **ulong** -Variable mit dem Namen *uloutbuflen*. Diese Variablen werden als Parameter an die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion übermittelt. Erstellen Sie außerdem eine **DWORD** -Variable mit dem Namen *dwretval* (für die Fehlerüberprüfung).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Zuweisen von Arbeitsspeicher für die Strukturen.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Erstellen Sie zunächst [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , um die benötigte Größe in der *uloutbuflen* -Variablen abzurufen.
    > [!Note]  
    > Dieser Aufrufe der-Funktion soll fehlschlagen und verwendet werden, um sicherzustellen, dass die *uloutbuflen* -Variable eine ausreichende Größe für die Speicherung aller an *padapterinfo* zurückgegebenen Informationen angibt. Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Erstellen Sie einen zweiten Rückruf von [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), und übergeben Sie *padapterinfo* und *uloutbuflen* als Parameter und allgemeine Fehlerüberprüfung. Rückgabe des Werts an die **DWORD** -Variable *dwretval* (für eine umfassendere Fehlerüberprüfung).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Wenn der-Vorgang erfolgreich war, greifen Sie auf einige der Daten in der *padapterinfo* -Struktur zu.
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

    

6.  Gibt den für die *padapterinfo* -Struktur zugeordneten Arbeitsspeicher frei.
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Nächster Schritt: [Verwalten von Schnittstellen mithilfe von getinterfakeinfo](managing-interfaces-using-getinterfaceinfo.md)

Vorheriger Schritt: [Abrufen von Informationen mithilfe von getnetworkpara](retrieving-information-using-getnetworkparams.md) Metern

 

 



