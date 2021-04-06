---
title: Erstellen der SPNs für einen Dienst mit einem SCP
description: Im folgenden Codebeispiel wird ein SPN für einen Dienst verfasst, der einen Dienst Verbindungspunkt (Service Connection Point, SCP) verwendet.
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- Erstellen der SPNs für einen Dienst mit einem SCP-AD
- Dienst Prinzipal Name AD, Verfassen von SPNs für einen Dienst mit einem SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a9c44bc603372af35e874acfea4c1e12a2433d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036257"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a>Erstellen der SPNs für einen Dienst mit einem SCP

Im folgenden Codebeispiel wird ein SPN für einen Dienst verfasst, der einen Dienst Verbindungspunkt (Service Connection Point, SCP) verwendet. Der zurückgegebene SPN weist das folgende Format auf.


```C++
<service class>/<host>/<service name>
```



" &lt; Dienstklasse &gt; " und " &lt; Dienst Name &gt; " entsprechen den Parametern *pszdnofscp* und *pszserviceclass* . " &lt; Host &gt; " ist standardmäßig der DNS-Name des lokalen Computers.


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




