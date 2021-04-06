---
title: Überprüfen der Abfrage Filter Syntax
description: Die LDAP-API stellt eine einfache Syntax Überprüfungs Funktion bereit. Beachten Sie, dass nur die Syntax und nicht das vorhanden sein der im Filter angegebenen Eigenschaften überprüft wird.
ms.assetid: 4e564cd9-2f8b-4e70-928c-3a8bd804aeba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da2c15052309bc2acbcff9d6bdabea95337db1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036261"
---
# <a name="checking-the-query-filter-syntax"></a><span data-ttu-id="2cc15-104">Überprüfen der Abfrage Filter Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc15-104">Checking the Query Filter Syntax</span></span>

<span data-ttu-id="2cc15-105">Die LDAP-API stellt eine einfache Syntax Überprüfungs Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="2cc15-105">The LDAP API provides a simple syntax-verification function.</span></span> <span data-ttu-id="2cc15-106">Beachten Sie, dass nur die Syntax und nicht das vorhanden sein der im Filter angegebenen Eigenschaften überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="2cc15-106">Be aware that it only verifies the syntax and not the existence of the properties specified in the filter.</span></span>

<span data-ttu-id="2cc15-107">Die folgende Funktion überprüft die Syntax des Abfrage Filters und gibt " **s \_ OK** " zurück, wenn der Filter gültig ist, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="2cc15-107">The following function verifies the syntax of the query filter and returns **S\_OK** if the filter is valid or S\_FALSE if it is not.</span></span>


```C++
HRESULT CheckFilterSyntax(
    LPOLESTR szServer, // NULL binds to a DC in the current domain.
    LPOLESTR szFilter) // Filter to check.
{
HRESULT hr = S_OK;
DWORD dwReturn;
LDAP *hConnect = NULL;  // Connection handle
 
if (!szFilter)
  return E_POINTER;
 
// LDAP_PORT is the default port, 389
 
hConnect  = ldap_open(szServer,  LDAP_PORT);
 
// Bind using the preferred authentication method on Windows 2000
// and the calling thread's security context.
 
dwReturn = ldap_bind_s( hConnect, NULL, NULL, LDAP_AUTH_NEGOTIATE );
if (dwReturn==LDAP_SUCCESS) {
    dwReturn = ldap_check_filter(hConnect, szFilter);
    if (dwReturn==LDAP_SUCCESS)
        hr = S_OK;
    else
        hr = S_FALSE;
}
 
// Unbind to free the connection.
 
ldap_unbind( hConnect );
 
return hr;
}
```



 

 




