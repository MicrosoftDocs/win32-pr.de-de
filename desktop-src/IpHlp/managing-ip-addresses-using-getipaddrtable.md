---
description: Die getipaddrtable-Funktion füllt einen Zeiger auf eine MIB \_ ipaddrtable-Struktur mit Informationen zu den aktuellen IP-Adressen, die dem System zugeordnet sind.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Verwalten von IP-Adressen mit getipaddrtable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864875"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Verwalten von IP-Adressen mit getipaddrtable

Die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion füllt einen Zeiger auf eine [**MIB \_ ipaddrtable**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) -Struktur mit Informationen zu den aktuellen IP-Adressen, die dem System zugeordnet sind.

**So verwenden Sie "getipaddrtable"**

1.  Deklarieren Sie einen Zeiger auf ein [**MIB \_ ipaddrtable**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) -Objekt namens *pipaddrtable* und ein **DWORD** -Objekt mit dem Namen *dwSize*. Diese Variablen werden als Parameter an die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion übermittelt. Erstellen Sie außerdem eine **DWORD** -Variable mit dem Namen *dwretval* (für die Fehlerüberprüfung verwendet).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Zuweisen von Speicher für die Struktur.
    > [!Note]  
    > Die Größe von *dwSize* reicht nicht aus, um die Informationen zu speichern. Weitere Informationen finden Sie im nächsten Schritt.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Führen Sie einen anfänglichen Aufrufen von [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) aus, um die benötigte Größe in die *dwSize* -Variable zu übernehmen.
    > [!Note]  
    > Dieser Aufrufen der-Funktion soll fehlschlagen und wird verwendet, um sicherzustellen, dass die *dwSize* -Variable eine ausreichende Größe angibt, um alle an *pipaddrtable* zurückgegebenen Informationen zu speichern. Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Erstellen Sie einen zweiten Aufrufen von [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) mit allgemeiner Fehlerüberprüfung, und geben Sie den Wert an die **DWORD** -Variable *dwretval* zurück (für eine erweiterte Fehlerüberprüfung).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Wenn der-Befehl erfolgreich ausgeführt wurde, greifen Sie auf die Daten aus der *pipaddrtable* -Datenstruktur zu.
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Gibt den für die *pipaddrtable* -Struktur zugeordneten Arbeitsspeicher frei.
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Die **DWORD** -Objekte *dwaddr* und *dwMask* werden als numerische Werte in der Host-Byte Reihenfolge und nicht in der netzwerkbyte Reihenfolge zurückgegeben Diese Werte sind keine gepunkteten IP-Adressen.

 

Nächster Schritt: [Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Vorheriger Schritt: [Verwalten von Schnittstellen mithilfe von getinterfakeinfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
