---
description: Die GetTcpStatistics-Funktion füllt einen Zeiger auf eine MIB \_ tcpstats-Struktur mit Informationen zu den TCP-Protokoll Statistiken für den lokalen Computer.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Abrufen von Informationen mithilfe von GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362287"
---
# <a name="retrieving-information-using-gettcpstatistics"></a>Abrufen von Informationen mithilfe von GetTcpStatistics

Die [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) -Funktion füllt einen Zeiger auf eine [**MIB \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Struktur mit Informationen zu den TCP-Protokoll Statistiken für den lokalen Computer.

**So verwenden Sie GetTcpStatistics**

1.  Deklarieren Sie einige erforderliche Variablen.

    Deklarieren Sie eine **DWORD** -Variable `dwRetVal` , die für Fehler Überprüfungs Funktionsaufrufe verwendet. Deklarieren Sie einen Zeiger auf eine [**MIB- \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Variable mit dem Namen *ptcpstats*, und weisen Sie der Struktur Arbeitsspeicher zu. Überprüfen Sie, ob Arbeitsspeicher zugeordnet werden konnte.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Rufen Sie die Funktion " [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) " mit dem Parameter " *ptcpstats* " auf, um TCP-Statistiken für IPv4 auf dem lokalen Computer abzurufen. Überprüfen Sie auf Fehler, und geben Sie den Fehlerwert in der **DWORD** -Variablen zurück `dwRetVal` . Wenn ein Fehler auftritt, `dwRetVal` kann die Variable für eine umfassendere Fehlerüberprüfung und Berichterstellung verwendet werden.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Wenn der-Befehl erfolgreich ausgeführt wurde, greifen Sie auf die Daten zu *, die in* den [**MIB- \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Werten zurückgegeben werden
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Gibt den Arbeitsspeicher frei, der für die [**MIB \_ tcpstats**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) -Struktur reserviert ist, auf die der *ptcpstats* -Parameter verweist. Dies sollte erfolgen, wenn die Anwendung die Daten nicht mehr benötigt, die vom *ptcpstats* -Parameter zurückgegeben werden.
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Nächster Schritt: [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)

Vorheriger Schritt: [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Vervollständigen des Quellcodes

-   [Vollständiger IP-hilfsanwendungs-Quellcode](complete-ip-helper-application-source-code.md)

 

 
