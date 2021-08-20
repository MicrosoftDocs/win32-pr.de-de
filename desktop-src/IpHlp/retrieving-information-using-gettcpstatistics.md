---
description: Die GetTcpStatistics-Funktion füllt einen Zeiger auf eine MIB-TCPSTATS-Struktur mit Informationen zu den TCP-Protokollstatistiken für \_ den lokalen Computer.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Abrufen von Informationen mit GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb51b1a71c9dc0ff98a40c31894aa3fcf8c0c0ace7b6b05812940cb9808cced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146593"
---
# <a name="retrieving-information-using-gettcpstatistics"></a>Abrufen von Informationen mit GetTcpStatistics

Die [**GetTcpStatistics-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) füllt einen Zeiger auf eine [**\_ MIB-TCPSTATS-Struktur**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) mit Informationen zu den TCP-Protokollstatistiken für den lokalen Computer.

**So verwenden Sie GetTcpStatistics**

1.  Deklarieren Sie einige benötigte Variablen.

    Deklarieren Sie **eine DWORD-Variable,** `dwRetVal` die für Funktionsaufrufe zur Fehlerüberprüfung verwendet wird. Deklarieren Sie einen Zeiger auf eine [**\_ MIB-TCPSTATS-Variable**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) namens *pTCPStats,* und weisen Sie Arbeitsspeicher für die Struktur zu. Überprüfen Sie, ob Arbeitsspeicher zugeordnet werden kann.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Rufen Sie [**die GetTcpStatistics-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) mit dem *pTCPStats-Parameter* auf, um TCP-Statistiken für IPv4 auf dem lokalen Computer abzurufen. Überprüfen Sie auf Fehler, und geben Sie den Fehlerwert in der **DWORD-Variablen** `dwRetVal` zurück. Wenn ein Fehler auftritt, kann die Variable für umfangreichere `dwRetVal` Fehlerüberprüfungen und -berichte verwendet werden.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Wenn der Aufruf erfolgreich war, greifen Sie auf die Daten zu, die in [**der \_ MIB-TCPSTATS-Datei zurückgegeben**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) werden, auf die der *pTCPStats-Parameter* zeigt.
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Geben Sie den Für die [**\_ MIB-TCPSTATS-Struktur zugeordneten Arbeitsspeicher**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) frei, auf den der *pTCPStats-Parameter* zeigt. Dies sollte erfolgen, wenn die Anwendung die vom *pTCPStats-Parameter* zurückgegebenen Daten nicht mehr benötigt.
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Nächster Schritt: [Abrufen von Informationen mit GetIpStatistics](retrieving-information-using-getipstatistics.md)

Vorheriger Schritt: [Abrufen von Informationen mit getIpStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Vollständiger Quellcode

-   [Vollständiger Quellcode der IP-Hilfsanwendung](complete-ip-helper-application-source-code.md)

 

 
