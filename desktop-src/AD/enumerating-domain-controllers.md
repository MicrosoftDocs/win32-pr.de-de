---
title: Auflisten von Domänen Controllern
description: In früheren Versionen von Windows konnte eine Anwendung nur einen einzigen Domänen Controller in einer Domäne abrufen, indem DsGetDcName aufgerufen wurde.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory das Auflisten von Domänen Controllern Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707697"
---
# <a name="enumerating-domain-controllers"></a>Auflisten von Domänen Controllern

In früheren Versionen von Windows konnte eine Anwendung nur einen einzigen Domänen Controller in einer Domäne abrufen, indem [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)aufgerufen wurde. Es gab keine Möglichkeit, vorherzusagen, welcher Domänen Controller abgerufen wird, oder eine Liste der Domänen Controller zu erhalten. Windows ermöglicht einer Anwendung die Enumeration der Domänen Controller in einer Domäne mithilfe der Funktionen [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)und [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Um einen Domänen Controller aufzulisten, nennen Sie [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena). Diese Funktion übernimmt Parameter, die die Domäne für die Aufzählung und andere Enumerationsoptionen definieren. **Dsgetdcopen** stellt ein domänenenumerationskontext-Handle bereit, das verwendet wird, um den Enumerationsvorgang zu identifizieren, wenn [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) und [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aufgerufen werden.

Die [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) -Funktion wird mit dem domänenaufzählungs-Kontext Handle aufgerufen, um den nächsten Domänen Controller in der-Enumeration abzurufen. Wenn diese Funktion zum ersten Mal aufgerufen wird, wird der erste Domänen Controller in der-Enumeration abgerufen. Wenn diese Funktion zum zweiten Mal aufgerufen wird, wird der zweite Domänen Controller in der-Enumeration abgerufen. Dieser Prozess wird wiederholt, bis **dsgetdcnext** **\_ einen Fehler ohne \_ Weitere \_ Elemente** zurückgibt, der das Ende der Enumeration angibt.

Die [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) -Funktion Listet die Domänen Controller in zwei Gruppen auf. Die erste Gruppe enthält die Domänen Controller, die den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird, und die zweite Gruppe enthält die Domänen Controller, die nicht den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird. Wenn im *optionflags* -Parameter in [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)das Flag **für die DS- \_ Benachrichtigung nach einem \_ \_ Standort \_ Daten** Satz angegeben ist, gibt die Funktion " **dsgetdcnext** " eine Fehlermeldung zurück, die **\_ \_ erkannt** wird, nachdem alle Site spezifischen Domänen Controller abgerufen wurden. **Dsgetdcnext** beginnt dann mit der Enumeration der zweiten Gruppe, die alle Domänen Controller in der Domäne enthält, einschließlich der standortspezifischen Domänen Controller, die in der ersten Gruppe enthalten sind.

Die Domänen Controller, die den Standort des Computers verarbeiten, auf dem die Funktion ausgeführt wird, werden zuerst aufgelistet, gefolgt von den Domänen Controllern, die nicht den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird. Ein Domänen Controller dient als Abdeckung für einen Standort, wenn der Domänen Controller so konfiguriert ist, dass er sich an diesem Standort befindet, oder wenn sich der Domänen Controller an einem Standort befindet, der in Bezug auf die konfigurierten standortübergreifenden Verknüpfungs Kosten am nächsten liegt. Wenn Domänen Controller sowohl in der Gruppe der Domänen Controller als auch in der Gruppe der Domänen Controller vorhanden sind, die den Computerstandort nicht abdecken, werden Domänen Controller innerhalb der Gruppe in der Reihenfolge ihrer konfigurierten Prioritäten und Gewichtungen zurückgegeben, die in DNS angegeben sind. Domänen Controller mit niedrigerer numerischer Priorität werden zuerst innerhalb einer Gruppe zurückgegeben. Wenn in einer Site bezogenen Gruppe eine Untergruppe von mehreren Domänen Controllern mit der gleichen Priorität vorhanden ist, werden Domänen Controller in einer gewichteten zufälligen Reihenfolge zurückgegeben, in der Domänen Controller mit höherer Gewichtung eine höhere Wahrscheinlichkeit haben, zuerst zurückgegeben zu werden. Die Standorte, Prioritäten und Gewichtungen werden vom Domänen Administrator konfiguriert, um eine effektive Leistung und einen effektiven Lastenausgleich zwischen mehreren Domänen Controllern in der Domäne zu erzielen. Aus diesem Grund nutzen Anwendungen, die die [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) -Funktionen verwenden, diese Optimierungen automatisch.

Wenn die Enumeration abgeschlossen ist oder nicht mehr erforderlich ist, muss die Enumeration durch Aufrufen von [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) mit dem domänenaufzählungs Kontext Handle geschlossen werden.

Zum Zurücksetzen der Enumeration ist es erforderlich, die aktuelle Enumeration durch Aufrufen von [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) zu schließen und die Enumeration dann erneut zu öffnen, indem Sie erneut [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) aufrufen.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird gezeigt, wie diese Funktionen verwendet werden, um die Domänen Controller in der lokalen Domäne aufzulisten.


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




