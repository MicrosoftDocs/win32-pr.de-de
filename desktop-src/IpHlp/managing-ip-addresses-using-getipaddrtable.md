---
description: Die GetIpAddrTable-Funktion füllt einen Zeiger auf eine \_ MIB-IPADDRTABLE-Struktur mit Informationen zu den aktuellen IP-Adressen, die dem System zugeordnet sind.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Verwalten von IP-Adressen mit getIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090bdb1e73d3f770eafb3a5e70893253918eb68573ebd05aa6ec40a609a7ba4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146683"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Verwalten von IP-Adressen mit getIpAddrTable

Die [**GetIpAddrTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) füllt einen Zeiger auf eine [**\_ MIB-IPADDRTABLE-Struktur**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) mit Informationen zu den aktuellen IP-Adressen, die dem System zugeordnet sind.

**So verwenden Sie GetIpAddrTable**

1.  Deklarieren Sie einen Zeiger auf ein [**\_ MIB-IPADDRTABLE-Objekt**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) namens *pIPAddrTable* und ein **DWORD-Objekt** mit dem Namen *dwSize.* Diese Variablen werden als Parameter an die [**GetIpAddrTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) übergeben. Erstellen Sie außerdem eine **DWORD-Variable** namens *dwRetVal* (wird für die Fehlerüberprüfung verwendet).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Zuordnen von Arbeitsspeicher für die Struktur.
    > [!Note]  
    > Die Größe von *dwSize* reicht nicht aus, um die Informationen zu speichern. Weitere Informationen finden Sie im nächsten Schritt.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Rufen [**Sie getIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) zunächst auf, um die erforderliche Größe in der *dwSize-Variablen* abzurufen.
    > [!Note]  
    > Dieser Aufruf der Funktion soll fehlschlagen und wird verwendet, um sicherzustellen, dass die *dwSize-Variable* eine Größe angibt, die ausreicht, um alle an *pIPAddrTable zurückgegebenen* Informationen zu enthalten. Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Erstellen Sie einen zweiten Aufruf von [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) mit allgemeiner Fehlerüberprüfung, und geben Sie dessen Wert an die **DWORD-Variable** *dwRetVal* zurück (für eine erweiterte Fehlerüberprüfung).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Wenn der Aufruf erfolgreich war, greifen Sie über die *Datenstruktur pIPAddrTable* auf die Daten zu.
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Freigeben des für die *pIPAddrTable-Struktur* belegten Arbeitsspeichers.
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Die **DWORD-Objekte** *dwAddr* und *dwMask* werden als numerische Werte in der Host-Bytereihenfolge und nicht in der Netzwerk-Bytereihenfolge zurückgegeben. Diese Werte sind keine gepunkteten IP-Adressen.

 

Nächster Schritt: [Verwalten von DHCP-Leases mit ipReleaseAddress und IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Vorheriger Schritt: [Verwalten von Schnittstellen mit GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
