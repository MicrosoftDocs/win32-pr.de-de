---
title: Aufzählen von Domänencontrollern
description: In früheren Versionen von Windows konnte eine Anwendung nur einen einzelnen Domänencontroller in einer Domäne abrufen, indem DsGetDcName aufgerufen wurde.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Auflisten von Domänencontrollern in Active Directory'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54234301ad843708fd4e9b20e38f2b4fd8391e1134a78cea8b0d45a001d701d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695148"
---
# <a name="enumerating-domain-controllers"></a>Aufzählen von Domänencontrollern

In früheren Versionen von Windows konnte eine Anwendung nur einen einzelnen Domänencontroller in einer Domäne durch Aufrufen von [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)abrufen. Es gab keine Möglichkeit, vorherzusagen, welcher Domänencontroller abgerufen wird, oder eine Liste der Domänencontroller abzurufen. Windows ermöglicht einer Anwendung das Aufzählen der Domänencontroller in einer Domäne mithilfe der Funktionen [**DsGetDcOpen,**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)und [**DsGetDcClose.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)

Um einen Domänencontroller aufzuzählen, rufen [**Sie DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)auf. Diese Funktion verwendet Parameter, die die aufzuzählende Domäne und andere Enumerationsoptionen definieren. **DsGetDcOpen** stellt ein Domänenenumerationskontexthandle bereit, das verwendet wird, um den Enumerationsvorgang zu identifizieren, wenn [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) und [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aufgerufen werden.

Die [**DsGetDcNext-Funktion**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) wird mit dem Domänenenumerationskontexthandle aufgerufen, um den nächsten Domänencontroller in der Enumeration abzurufen. Beim ersten Aufruf dieser Funktion wird der erste Domänencontroller in der Enumeration abgerufen. Beim zweiten Aufruf dieser Funktion wird der zweite Domänencontroller in der -Enumeration abgerufen. Dieser Vorgang wird wiederholt, bis **DsGetDcNext** **ERROR NO MORE \_ \_ \_ ITEMS** zurückgibt, der das Ende der Enumeration angibt.

Die [**DsGetDcNext-Funktion**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) führt die Domänencontroller in zwei Gruppen auf. Die erste Gruppe enthält die Domänencontroller, die den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird, und die zweite Gruppe enthält die Domänencontroller, die nicht den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird. Wenn das **Flag DS \_ NOTIFY AFTER \_ SITE \_ \_ RECORDS** im *Parameter OptionFlags* in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)angegeben ist, gibt die **DsGetDcNext-Funktion** **ERROR \_ FILEMARK \_ DETECTED** zurück, nachdem alle standortspezifischen Domänencontroller abgerufen wurden. **DsGetDcNext** beginnt dann mit dem Aufzählen der zweiten Gruppe, die alle Domänencontroller in der Domäne enthält, einschließlich der standortspezifischen Domänencontroller, die in der ersten Gruppe enthalten sind.

Domänencontroller, die den Standort des Computers behandeln, auf dem die Funktion ausgeführt wird, werden zuerst aufgeführt, gefolgt von den Domänencontrollern, die den Standort des Computers, auf dem die Funktion ausgeführt wird, nicht abdecken. Ein Domänencontroller deckt einen Standort ab, wenn der Domänencontroller so konfiguriert ist, dass er sich an diesem Standort befindet, oder wenn sich der Domänencontroller an einem Standort befindet, der dem betreffenden Standort im Hinblick auf die konfigurierten Kosten für standortübergreifende Verbindungen am nächsten liegt. Wenn sich Domänencontroller sowohl in der Domänencontrollergruppe, die abdecken, als auch in der Gruppe der Domänencontroller befinden, die den Computerstandort nicht abdecken, werden Domänencontroller innerhalb der Gruppe in der Reihenfolge ihrer konfigurierten Prioritäten und Gewichtungen zurückgegeben, die in DNS angegeben sind. Domänencontroller mit einer niedrigeren numerischen Priorität werden zuerst innerhalb einer Gruppe zurückgegeben. Wenn innerhalb einer standortbezogenen Gruppe eine Untergruppe von mehreren Domänencontrollern mit der gleichen Priorität vorhanden ist, werden Domänencontroller in einer gewichteten zufälligen Reihenfolge zurückgegeben, wobei Domänencontroller mit höherer Gewichtung eine höhere Wahrscheinlichkeit haben, zuerst zurückgegeben zu werden. Die Standorte, Prioritäten und Gewichtungen werden vom Domänenadministrator konfiguriert, um einen effektiven Leistungs- und Lastenausgleich zwischen mehreren in der Domäne verfügbaren Domänencontrollern zu erzielen. Aus diesem Grund nutzen Anwendungen, die die [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose-Funktionen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) verwenden, diese Optimierungen automatisch.

Wenn die Enumeration abgeschlossen ist oder nicht mehr erforderlich ist, muss die Enumeration geschlossen werden, indem [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) mit dem Domänenenumerationskontexthandle aufgerufen wird.

Um die Enumeration zurückzusetzen, müssen Sie die aktuelle Enumeration schließen, indem [**Sie DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aufrufen und dann die Enumeration erneut öffnen, indem [**Sie DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) erneut aufrufen.

## <a name="example"></a>Beispiel

Das folgende Codebeispiel zeigt, wie diese Funktionen verwendet werden, um die Domänencontroller in der lokalen Domäne aufzuzählen.


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



 

 




