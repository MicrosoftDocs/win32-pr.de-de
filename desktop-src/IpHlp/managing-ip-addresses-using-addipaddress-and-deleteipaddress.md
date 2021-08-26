---
title: Verwalten von IP-Adressen mit AddIPAddress, DeleteIPAddress
description: Die AddIPAddress-Funktion fügt dem angegebenen Adapter die angegebene IPv4-Adresse hinzu.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e726a2e5785641532abb739d61143f9fabfdd10c38e4b51fcd529f20d92503d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870090"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Verwalten von IP-Adressen mit AddIPAddress, DeleteIPAddress

Die [**AddIPAddress-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) fügt dem angegebenen Adapter die angegebene IPv4-Adresse hinzu. Die [**DeleteIPAddress-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) löscht die angegebene IPv4-Adresse aus dem angegebenen Adapter. Diese Funktionen können zum Hinzufügen und Löschen von IPv4-Adressen zu einem Netzwerkadapter verwendet werden.

Eine von der [**AddIPAddress-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) hinzugefügte IPv4-Adresse ist nicht persistent. Die IPv4-Adresse ist nur vorhanden, solange das Adapterobjekt vorhanden ist. Durch einen Neustart des Computers wird die IPv4-Adresse zerstört, ebenso wie das manuelle Zurücksetzen der Netzwerkschnittstellenkarte (NIC).

Nachdem [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) erfolgreich aufgerufen wurde, wird DHCP für die hinzugefügte IP-Adresse deaktiviert. Daher sind Funktionen wie [**IpReleaseAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)für die DHCP aktiviert werden muss, für die hinzugefügte IP-Adresse nicht funktionsfähig. Die [**DeleteIPAddress-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) kann verwendet werden, um die hinzugefügte IPv4-Adresse zu löschen.

> [!Note]  
> Gruppenrichtlinien, Unternehmensrichtlinien und andere Einschränkungen im Netzwerk können verhindern, dass diese Funktionen erfolgreich abgeschlossen werden. Stellen Sie sicher, dass die Anwendung über die erforderlichen Netzwerkberechtigungen verfügt, bevor Sie versuchen, diese Funktionen zu verwenden.

 

**So verwenden Sie AddIPAddress**

1.  **Deklarieren Sie ULONG-Variablen** mit `NTEContext` den Namen und , die beide mit `NTEInstance` 0 initialisiert wurden.
    > [!Note]  
    > Die Variable ist der einzige Parameter für die `NTEContext` [**DeleteIPAddress-Funktion.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) Zum Löschen der hinzugefügten IP-Adresse `NTEContext` muss gespeichert und unverändert sein.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Deklarieren Sie Variablen für die IPAddr- und IPMask-Strukturen mit `iaIPAddress` den Namen `iaIPMask` bzw. . Bei diesen Werten handelt es sich einfach um ganze Zahlen ohne Vorzeichen. Initialisieren Sie `iaIPAddress` die `iaIPMask` Variablen und mithilfe der [**\_ addr-Funktion inet.**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Rufen Sie die [**AddIPAddress-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) auf, um die IPv4-Adresse hinzuzufügen. Suchen Sie nach Fehlern, und geben Sie den Fehlerwert an die **DWORD-Variable** `dwRetVal` zurück (für eine ausführlichere Fehlerüberprüfung).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > Der dritte Parameter ist der Adapterindex, der durch Aufrufen der [**GetIpAddrTable-Funktion ermittelt werden**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) kann. Es wird davon ausgegangen, dass die von dieser Funktion zurückgegebene Variable den Namen `pIPAddrTable` hat. Hilfe zur **GetIpAddrTable-Funktion** finden Sie unter [Managing IP Address Using GetIpAddrTable (Verwalten von IP-Adressen mit GetIpAddrTable).](managing-ip-addresses-using-getipaddrtable.md)

     

**So verwenden Sie DeleteIpAddress**

-   Rufen Sie die [**DeleteIPAddress-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) auf, und übergeben Sie `NTEContext` die Variable als Parameter. Suchen Sie nach Fehlern, und geben Sie den Fehlerwert an die **DWORD-Variable** `dwRetVal` zurück (für eine ausführlichere Fehlerüberprüfung).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Um [**DeleteIPAddress zu verwenden,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) [**muss addIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) zuerst aufgerufen werden, um das Handle zu `NTEContext` erhalten. In der vorherigen Prozedur wird davon ausgegangen, dass **AddIPAddress** bereits an einer stelle im Code aufgerufen wurde und gespeichert wurde und `NTEContext` nicht korrupiert bleibt.

 

Nächster Schritt: [Abrufen von Informationen mit GetIpStatistics](retrieving-information-using-getipstatistics.md)

Vorheriger Schritt: [Verwalten von DHCP-Leases mit ipReleaseAddress und IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
