---
title: Verwalten von DHCP-Leases mit ipreleaseaddress, iprenewaddress
description: Die Funktionen ipreleaseaddress und iprenewaddress werden zum Freigeben und erneuern der aktuellen DHCP-Lease (Dynamic Host Configuration Protocol) verwendet.
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862439"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>Verwalten von DHCP-Leases mit ipreleaseaddress, iprenewaddress

Die Funktionen [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) und [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) werden zum Freigeben und erneuern der aktuellen DHCP-Lease (Dynamic Host Configuration Protocol) verwendet. Die **ipreleaseaddress** -Funktion gibt eine IPv4-Adresse frei, die zuvor über DHCP abgerufen wurde. Die **iprenewaddress** -Funktion erneuert eine Lease für eine IPv4-Adresse, die zuvor über DHCP abgerufen wurde. Es ist üblich, diese beiden Funktionen gemeinsam zu verwenden, zuerst die Lease mit einem **ipreleaseaddress**-Befehl freizugeben und dann die Lease mit einem-Rückruf der **iprenewaddress** -Funktion zu erneuern.

Wenn ein DHCP-Client zuvor eine DHCP-Lease abgerufen hat und [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) vor der [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion nicht aufgerufen wird, wird die DHCP-Client Anforderung an den DHCP-Server gesendet, der die anfängliche DHCP-Lease ausgegeben hat. Dieser DHCP-Server ist möglicherweise nicht verfügbar, oder die DHCP-Anforderung schlägt fehl. Wenn ein Host zuvor eine DHCP-Lease abgerufen hat und **ipreleaseaddress** vor der **iprenewaddress** -Funktion aufgerufen wird, gibt der DHCP-Client zunächst die erhaltene IP-Adresse frei und sendet eine DHCP-Client Anforderung für eine Antwort von einem beliebigen verfügbaren DHCP-Server.

> [!Note]  
> Die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion und die [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion erfordern, dass DHCP ordnungsgemäß ausgeführt wird.

 

Die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion nimmt einen Zeiger auf eine [**IP- \_ Adapter \_ Index \_ Struktur-**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur als einzigen Parameter an. Rufen Sie zum Abrufen dieses Parameters zuerst [**getinterfacetten Info**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)auf. Hilfe zur Funktion **getinterfacetten** Info finden Sie unter Verwalten von [Schnittstellen mithilfe von getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info.

**So verwenden Sie ipreleaseaddress**

1.  Rufen Sie mithilfe der [**getinterfaceinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion einen Zeiger auf eine [**IP- \_ Adapter \_ Index \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur ab. (Hilfe zur getinterfacetten-Funktion finden Sie unter Verwalten von [Schnittstellen mit getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info). Erstellen Sie ein **DWORD** -Objekt `dwRetVal` (für die Fehlerüberprüfung verwendet). Es wird davon ausgegangen, dass die von **getinterfacetten Info** zurückgegebene Variable aufgerufen wird `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Wenn DHCP aktiviert ist, rufen Sie die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion auf, und übergeben Sie dabei die [**IP- \_ Adapter \_ Index \_ map-**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Variable `Adapter` als Parameter. Überprüfen Sie, ob allgemeine Fehler auftreten, und geben Sie den Wert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).
    > [!Note]  
    > Die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion gibt einen Parameter zurück, der verwendet werden kann, um zu überprüfen, ob DHCP aktiviert ist, bevor diese Funktionen aufgerufen werden. Hilfe zu **getadaptersinfo** finden Sie unter [Verwalten von Netzwerkadaptern mit "getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)".

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> Es ist üblich, diese beiden Funktionen gemeinsam zu verwenden, die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion aufzurufen und dann die [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion aufzurufen und die gleiche Struktur wie der Parameter an beide Funktionen zu übergeben. Bei der folgenden Prozedur wird davon ausgegangen, dass die Funktionen nicht gleichzeitig verwendet werden. Wenn die Funktionen jedoch gleichzeitig verwendet werden, überspringen Sie Schritt 1.

 

**So verwenden Sie iprenewaddress**

1.  Rufen Sie mithilfe der [**getinterfaceinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion einen Zeiger auf eine [**IP- \_ Adapter \_ Index \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur ab. (Hilfe zur **getinterfacetten** -Funktion finden Sie unter Verwalten von [Schnittstellen mit getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info). Deklarieren Sie ein **DWORD** -Objekt `dwRetVal` (für die Fehlerüberprüfung verwendet), wenn diese Variable nicht deklariert wurde. Es wird davon ausgegangen, dass die von **getinterfacetten Info** zurückgegebene Variable aufgerufen wird `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Aufrufen der [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion, wobei die [**IP- \_ Adapter \_ Index \_ map-**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Variable `Adapter` als Parameter übergeben wird. Überprüfen Sie, ob allgemeine Fehler auftreten, und geben Sie den Wert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

Nächster Schritt: [Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

Vorheriger Schritt: [Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md)

 

 



