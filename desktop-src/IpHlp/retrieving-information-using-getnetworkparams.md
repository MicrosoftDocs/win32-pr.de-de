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
# <a name="retrieving-information-using-getnetworkparams"></a>Abrufen von Informationen mithilfe von getnetworkpara Metern

Die [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) -Funktion füllt einen Zeiger auf eine [**fixierte \_ Informations**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) Struktur mit Daten über die aktuellen Netzwerkeinstellungen.

**So verwenden Sie "getnetworkparameams"**

1.  Deklarieren Sie einen Zeiger auf ein [**festes \_ Info**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) Objekt mit dem Namen *pfixedinfo* und ein **ulong** -Objekt mit dem Namen *uloutbuflen*. Diese Variablen werden als Parameter an die [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) -Funktion übermittelt. Erstellen Sie außerdem eine **DWORD** -Variable *dwretval* (für die Fehlerüberprüfung verwendet).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Zuweisen von Arbeitsspeicher für die Strukturen.
    > [!Note]  
    > Die Größe von *uloutbuflen* reicht nicht aus, um die Informationen zu speichern. Weitere Informationen finden Sie im nächsten Schritt.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Führen Sie einen ersten Rückruf an [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) aus, um die für die *uloutbuflen* -Variable erforderliche Größe abzurufen.
    > [!Note]  
    > Diese Funktions Funktion schlägt fehl und wird verwendet, um sicherzustellen, dass die *uloutbuflen* -Variable eine ausreichende Größe für die Speicherung aller an *pfixedinfo* zurückgegebenen Daten angibt. Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Erstellen Sie einen zweiten Rückruf von [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) mithilfe allgemeiner Fehlerüberprüfung, und geben Sie den Wert an die **DWORD** -Variable *dwretval* zurück. wird für erweiterte Fehlerüberprüfungen verwendet.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Wenn der-Vorgang erfolgreich war, greifen Sie auf die Daten aus der *pfixedinfo* -Datenstruktur zu.
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

    

6.  Gibt den für die *pfixedinfo* -Struktur zugeordneten Arbeitsspeicher frei.
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Nächster Schritt: [Verwalten von Netzwerkadaptern mit getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)

Vorheriger Schritt: [Erstellen einer grundlegenden IP-Hilfsanwendung](creating-a-basic-ip-helper-application.md)

 

 



