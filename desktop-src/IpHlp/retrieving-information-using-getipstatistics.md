---
description: Die GetIpStatistics-Funktion füllt einen Zeiger auf eine MIB-IPSTATS-Struktur mit Informationen zu den aktuellen IP-Statistiken, die \_ dem System zugeordnet sind.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Abrufen von Informationen mit getIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c383c49b316eb48e240a8272957dae8ee3ec1671304df8d466b869b7bf4ec0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050270"
---
# <a name="retrieving-information-using-getipstatistics"></a>Abrufen von Informationen mit getIpStatistics

Die [**GetIpStatistics-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) füllt einen Zeiger auf eine [**\_ MIB-IPSTATS-Struktur**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) mit Informationen zu den aktuellen IP-Statistiken, die dem System zugeordnet sind.

**So verwenden Sie GetIpStatistics**

1.  Deklarieren Sie einige benötigte Variablen.

    Deklarieren Sie **eine DWORD-Variable,** `dwRetval` die für Funktionsaufrufe zur Fehlerüberprüfung verwendet wird. Deklarieren Sie einen Zeiger auf eine [**\_ MIB-IPSTATS-Variable**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) namens *pStats,* und weisen Sie Arbeitsspeicher für die Struktur zu. Überprüfen Sie, ob Arbeitsspeicher zugeordnet werden kann.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Rufen Sie [**die GetIpStatistics-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) mit dem *pStats-Parameter* auf, um IP-Statistiken für den lokalen Computer abzurufen. Überprüfen Sie auf Fehler, und geben Sie den Fehlerwert in der **DWORD-Variablen** `dwRetval` zurück. Wenn ein Fehler auftritt, kann die Variable für umfangreichere `dwRetval` Fehlerüberprüfungen und -berichte verwendet werden.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Wenn der Aufruf von [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) erfolgreich war, geben Sie einige der Daten in der [**\_ MIB-IPSTATS-Struktur**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) aus, auf die der *pStats-Parameter* zeigt.
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Geben Sie den Für die [**\_ MIB-IPSTATS-Struktur zugeordneten Arbeitsspeicher**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) frei, auf den der *pStats-Parameter* zeigt. Dies sollte erfolgen, sobald die Anwendung die vom *pStats-Parameter* zurückgegebenen Daten nicht mehr benötigt.
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Nächster Schritt: [Abrufen von Informationen mit GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Vorheriger Schritt: [Verwalten von IP-Adressen mit addIPAddress und DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
