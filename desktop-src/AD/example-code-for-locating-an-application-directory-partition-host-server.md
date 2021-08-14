---
title: Beispielcode zum Suchen eines Anwendungsverzeichnispartitionshostservers
description: Dieses Thema enthält ein Codebeispiel, das einen Anwendungsverzeichnispartitionshostserver sucht.
ms.assetid: c161323b-13ce-4986-8b24-b459009ff53c
ms.tgt_platform: multiple
keywords:
- Beispielcode zum Suchen eines Anwendungsverzeichnispartitionshostservers AD
- Application Directory Partition AD , Beispielcode zum Suchen eines Application Directory-Partitionshostservers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d7a218acf3608c18587b7d9b9c82779f17fd6eb251608a86d99d8acb3b7bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693599"
---
# <a name="example-code-for-locating-an-application-directory-partition-host-server"></a>Beispielcode zum Suchen eines Anwendungsverzeichnispartitionshostservers

Dieses Thema enthält ein Codebeispiel, das einen Anwendungsverzeichnispartitionshostserver sucht.

Das folgende C/C++-Codebeispiel zeigt, wie sie die [**DsGetDcName-Funktion**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) verwendet, um einen Domänencontroller zu suchen, der ein Replikat einer Anwendungsverzeichnispartition hostet. Dieses Codebeispiel zeigt auch, wie sie die [**DsCrackNames-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa) verwendet, um den Distinguished Name einer Anwendungsverzeichnispartition in einen DNS-Namen zu konvertieren.


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



 

 




