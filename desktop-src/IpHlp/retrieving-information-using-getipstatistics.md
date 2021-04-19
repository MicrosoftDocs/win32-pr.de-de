---
description: Die GetIpStatistics-Funktion füllt einen Zeiger auf eine MIB \_ -ipstats-Struktur mit Informationen über die aktuelle IP-Statistik aus, die dem System zugeordnet ist.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Abrufen von Informationen mithilfe von GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368809"
---
# <a name="retrieving-information-using-getipstatistics"></a>Abrufen von Informationen mithilfe von GetIpStatistics

Die [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) -Funktion füllt einen Zeiger auf eine [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Struktur mit Informationen über die aktuelle IP-Statistik aus, die dem System zugeordnet ist.

**So verwenden Sie "GetIpStatistics"**

1.  Deklarieren Sie einige erforderliche Variablen.

    Deklarieren Sie eine **DWORD** -Variable `dwRetval` , die für Fehler Überprüfungs Funktionsaufrufe verwendet. Deklarieren Sie einen Zeiger auf eine [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Variable mit dem Namen *pStats*, und weisen Sie der Struktur Arbeitsspeicher zu. Überprüfen Sie, ob Arbeitsspeicher zugeordnet werden konnte.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Rufen Sie die Funktion [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) mit dem *pStats* -Parameter auf, um IP-Statistiken für den lokalen Computer abzurufen. Überprüfen Sie auf Fehler, und geben Sie den Fehlerwert in der **DWORD** -Variablen zurück `dwRetval` . Wenn ein Fehler auftritt, `dwRetval` kann die Variable für eine umfassendere Fehlerüberprüfung und Berichterstellung verwendet werden.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Wenn der Aufrufen von [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) erfolgreich war, können Sie einige der Daten in der [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Struktur ausgeben, auf die der *pStats* -Parameter verweist.
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Gibt den für die [**MIB- \_ ipstats**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) -Struktur zugeordneten Arbeitsspeicher frei, auf den der *pStats* -Parameter verweist. Dies sollte erfolgen, wenn die Anwendung die Daten nicht mehr benötigt, die vom *pStats* -Parameter zurückgegeben werden.
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Nächster Schritt: [Abrufen von Informationen mithilfe von GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Vorheriger Schritt: [Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
