---
title: Verwalten von IP-Adressen mit addipaddress, deleteipaddress
description: Die addipaddress-Funktion fügt dem angegebenen Adapter die angegebene IPv4-Adresse hinzu.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351668"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Verwalten von IP-Adressen mit addipaddress, deleteipaddress

Die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion fügt dem angegebenen Adapter die angegebene IPv4-Adresse hinzu. Die [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion löscht die angegebene IPv4-Adresse aus dem angegebenen Adapter. Diese Funktionen können zum Hinzufügen und Löschen von IPv4-Adressen zu einem Netzwerkadapter verwendet werden.

Eine von der [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion hinzugefügte IPv4-Adresse ist nicht persistent. Die IPv4-Adresse ist nur so lange vorhanden, wie das Adapter Objekt vorhanden ist. Durch einen Neustart des Computers wird die IPv4-Adresse zerstört, da die Netzwerkschnittstellenkarte (NIC) manuell zurückgesetzt wird.

Nachdem [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) erfolgreich aufgerufen wurde, wird DHCP für die hinzugefügte IP-Adresse deaktiviert. Daher sind Funktionen wie [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), die DHCP aktivieren müssen, für die hinzugefügte IP-Adresse nicht funktionsfähig. Die [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion kann verwendet werden, um die hinzugefügte IPv4-Adresse zu löschen.

> [!Note]  
> Gruppenrichtlinien, Unternehmensrichtlinien und andere Einschränkungen im Netzwerk verhindern möglicherweise, dass diese Funktionen erfolgreich abgeschlossen werden. Stellen Sie sicher, dass die Anwendung über die erforderlichen Netzwerk Berechtigungen verfügt, bevor Sie versuchen, diese Funktionen zu verwenden.

 

**So verwenden Sie addipaddress**

1.  Deklarieren Sie **ulong** `NTEContext` -Variablen `NTEInstance` mit dem Namen und, beide werden auf NULL initialisiert.
    > [!Note]  
    > Die `NTEContext` -Variable ist der einzige Parameter der [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion. zum Löschen der hinzugefügten IP-Adresse `NTEContext` muss gespeichert und unverändert sein.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Deklarieren Sie Variablen für die ipaddr-und ipmask-Strukturen mit den Namen `iaIPAddress` `iaIPMask` bzw.. Diese Werte sind einfach ganze Zahlen ohne Vorzeichen. Initialisieren `iaIPAddress` Sie die `iaIPMask` Variablen und mithilfe der Funktion " [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) ".
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Ruft die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion auf, um die IPv4-Adresse hinzuzufügen. Überprüfen Sie, ob Fehler vorliegen, und geben Sie den Fehlerwert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > Der dritte Parameter ist der Adapter Index, der durch Aufrufen der [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion abgerufen werden kann. Es wird davon ausgegangen, dass die von dieser Funktion zurückgegebene Variable den Namen hat `pIPAddrTable` . Hilfe zur **getipaddrtable** -Funktion finden Sie unter [Verwalten der IP-Adresse mithilfe von getipaddrtable](managing-ip-addresses-using-getipaddrtable.md).

     

**So verwenden Sie deleteipaddress**

-   Aufrufen der [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion, wobei die `NTEContext` Variable als Parameter übergeben wird. Überprüfen Sie, ob Fehler vorliegen, und geben Sie den Fehlerwert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Um [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)zu verwenden, muss [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) zuerst aufgerufen werden, um das Handle zu erhalten `NTEContext` . Bei der vorherigen Prozedur wird davon ausgegangen, dass **addipaddress** bereits irgendwo im Code aufgerufen wurde und `NTEContext` gespeichert wurde und unbeschädigt ist.

 

Nächster Schritt: [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)

Vorheriger Schritt: [Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
