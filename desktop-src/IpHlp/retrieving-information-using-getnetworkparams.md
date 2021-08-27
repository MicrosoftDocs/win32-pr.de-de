---
description: Füllt einen Zeiger auf eine FIXED \_ INFO-Struktur mit Daten zu den aktuellen Netzwerkeinstellungen.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Abrufen von Informationen mit GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bbe1d03cd619af3a6e73e7995876431a804b3ec723cf9a132df5dba517e719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102039"
---
# <a name="retrieving-information-using-getnetworkparams"></a>Abrufen von Informationen mit GetNetworkParams

Die [**GetNetworkParams-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) füllt einen Zeiger auf eine [**FIXED \_ INFO-Struktur**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) mit Daten zu den aktuellen Netzwerkeinstellungen auf.

**So verwenden Sie GetNetworkParams**

1.  Deklarieren Sie einen Zeiger auf ein [**FIXED \_ INFO-Objekt**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) namens *pFixedInfo* und ein **ULONG-Objekt** namens *ulOutBufLen.* Diese Variablen werden als Parameter an die [**GetNetworkParams-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) übergeben. Erstellen Sie außerdem die **DWORD-Variable** *dwRetVal* (wird für die Fehlerüberprüfung verwendet).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Ordnen Sie Arbeitsspeicher für die Strukturen zu.
    > [!Note]  
    > Die Größe von *ulOutBufLen* reicht nicht aus, um die Informationen zu enthalten. Weitere Informationen finden Sie im nächsten Schritt.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Rufen Sie zunächst [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) auf, um die erforderliche Größe für *die Variable ulOutBufLen* zu erhalten.
    > [!Note]  
    > Diese Funktionsfunktion führt zu einem Fehler und wird verwendet, um sicherzustellen, dass die *variable ulOutBufLen* eine größe angibt, die zum Halten aller an *pFixedInfo* zurückgegebenen Daten ausreicht. Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Führen Sie einen zweiten Aufruf von [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) durch, indem Sie die allgemeine Fehlerüberprüfung verwenden und ihren Wert an die **DWORD-Variable** *dwRetVal zurückgeben.* wird für eine erweiterte Fehlerüberprüfung verwendet.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Wenn der Aufruf erfolgreich war, greifen Sie über die *pFixedInfo-Datenstruktur* auf die Daten zu.
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

    

6.  Geben Sie den für die *pFixedInfo-Struktur zugeordneten Arbeitsspeicher* frei.
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Nächster Schritt: [Verwalten von Netzwerkadaptern mit GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

Vorheriger Schritt: [Erstellen einer einfachen IP-Hilfsanwendung](creating-a-basic-ip-helper-application.md)

 

 



