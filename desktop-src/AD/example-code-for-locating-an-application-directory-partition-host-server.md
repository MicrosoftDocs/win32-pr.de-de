---
title: Beispiel Code für die Suche eines Anwendungsverzeichnis-Partitions Host Servers
description: Dieses Thema enthält ein Codebeispiel, das einen Anwendungsverzeichnis-Partitions Host Server findet.
ms.assetid: c161323b-13ce-4986-8b24-b459009ff53c
ms.tgt_platform: multiple
keywords:
- Beispiel Code für die Suche nach einem Anwendungsverzeichnis-Partitions Host Server AD
- Anwendungsverzeichnis-Partitions Anzeige, Beispiel Code für die Suche eines Anwendungsverzeichnis-Partitions Host Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa82c91573e0ce00017fe93b8e8713f50ab7b26c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309287"
---
# <a name="example-code-for-locating-an-application-directory-partition-host-server"></a>Beispiel Code für die Suche eines Anwendungsverzeichnis-Partitions Host Servers

Dieses Thema enthält ein Codebeispiel, das einen Anwendungsverzeichnis-Partitions Host Server findet.

Im folgenden C/C++-Codebeispiel wird veranschaulicht, wie die [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) -Funktion verwendet wird, um einen Domänen Controller zu suchen, der ein Replikat einer Anwendungsverzeichnis Partition hostet. Dieses Codebeispiel zeigt auch, wie Sie die [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa) -Funktion verwenden, um den Distinguished Name einer Anwendungsverzeichnis Partition in einen DNS-Namen zu konvertieren.


```C++
/***************************************************************************

    AppPartitionDNToDNS()

    Converts the distinguished name of an application directory partition to 
    a DNS name for the partition.

    The caller must free the memory allocated to ppszDNS by calling 
    FreeADsMem when it is no longer required.

***************************************************************************/

DWORD AppPartitionDNToDNS(LPCTSTR pszDN, LPTSTR *ppszDNS)
{   
    DWORD dwRet;
    LPCTSTR rgpszNames[] = {pszDN};
    PDS_NAME_RESULT pResults;

    /*
    Convert the distinguished name to a DNS name using only syntactic 
    mapping. The DS_NAME_FLAG_SYNTACTICAL_ONLY flag allows DsCrackNames to 
    be called without binding.
    */
    dwRet = DsCrackNames(NULL, 
        DS_NAME_FLAG_SYNTACTICAL_ONLY,
        DS_FQDN_1779_NAME,
        DS_CANONICAL_NAME,
        1,
        rgpszNames,
        &pResults);

    if(NO_ERROR == dwRet)
    {
        /*
        Allocate the memory and copy the DNS name of the partition.
        */
        DWORD dwBytes = (lstrlen(pResults->rItems[0].pDomain) + 1) * sizeof(TCHAR);
        *ppszDNS = (LPTSTR)AllocADsMem(dwBytes);
        if(*ppszDNS)
        {
            wcsncpy_s(*ppszDNS, pResults->rItems[0].pDomain, dwBytes);

            dwRet = NO_ERROR;
        }
        else
        {
            dwRet = ERROR_NOT_ENOUGH_MEMORY;
        }
        
        // Free the result set.
        DsFreeNameResult(pResults);
    }
    
    return dwRet;
}

/***************************************************************************

    PrintDCFromAppPartition()

    Given the distinguished name of an application directory partition, 
    prints to the console the DNS name of a domain controller that hosts a 
    replica of the application directory partition.

***************************************************************************/

DWORD PrintDCFromAppPartition(LPCTSTR pszAppPartitionDN)
{
    DWORD dwRet;

    /*
    Convert the distinguished name of the partition to a DNS name so that 
    the DNS name can be passed to DsGetDcName.
    */
    LPTSTR pszDNS;
    dwRet = AppPartitionDNToDNS(pszAppPartitionDN, &pszDNS);
    if(NO_ERROR == dwRet)
    {
        PDOMAIN_CONTROLLER_INFO pdci;

        /*
        Get the name of a domain controller that hosts a replica of the 
        application directory partition.
        */
        dwRet = DsGetDcName(NULL, 
            pszDNS, 
            NULL, 
            NULL, 
            DS_ONLY_LDAP_NEEDED, 
            &pdci);

        if(NO_ERROR == dwRet)
        {
            // Print the DNS name of the domain controller.
            _tprintf(pdci->DomainControllerName);
            
            NetApiBufferFree(pdci);
        }

        FreeADsMem(pszDNS);
    }

    return dwRet;
}
```



 

 




