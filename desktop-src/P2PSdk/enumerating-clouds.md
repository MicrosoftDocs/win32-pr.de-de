---
description: Beim Aufzählen von Clouds muss eine Anwendung den Bereich der Suche nach Clouds bereitstellen. Nachdem der Bereich identifiziert wurde, kann die Anwendung den Enumerationsprozess starten.
ms.assetid: efd16cca-ac63-4bfa-bc6c-d7465cc374ee
title: Aufzählen von Clouds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c651fcfd003e4cafdf9b0f04c7cfc993a1e677b03630a61556523eed8c3aaece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011558"
---
# <a name="enumerating-clouds"></a>Aufzählen von Clouds

Beim Aufzählen von Clouds muss eine Anwendung den Bereich der Suche nach Clouds bereitstellen. Nachdem der Bereich identifiziert wurde, kann die Anwendung den Enumerationsprozess starten.

Im folgenden Verfahren werden die Aufrufe identifiziert, die zum Aufzählen von Clouds vorgenommen werden müssen.

**So aufzählen Sie Clouds**

1.  Rufen [**Sie WSALookupServiceBegin auf,**](pnrp-and-wsalookupservicebegin.md) um den Prozess zu starten und ein Handle zurück zu geben.
2.  Rufen [**Sie WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) auf, um eine Reihe von Clouds abzurufen, und rufen Sie dann diese Funktion auf, bis die Anwendung alle Clouds abgerufen hat.
3.  Rufen [**Sie WSALookupServiceEnd auf,**](pnrp-and-wsalookupserviceend.md) um die Enumeration fertig zu stellen.

## <a name="example-enumerating-and-printing-the-names-of-available-link-local-clouds"></a>Beispiel: Aufzählen und Drucken der Namen verfügbarer linker lokaler Clouds


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "ws2_32.lib")

DWORD PrintLinkLocalClouds()
{

    WSAQUERYSETW    qset;
    BLOB            Blob;
    PNRPCLOUDINFO   CloudInfo;
    HANDLE          hLookup = NULL;
    int             err;
    DWORD           dwErr = NO_ERROR;
    DWORD           dwSize;
    WSAQUERYSETW    *pResults = NULL;

    ZeroMemory(&qset, sizeof(qset));
    ZeroMemory(&CloudInfo, sizeof(CloudInfo));

    CloudInfo.dwSize = sizeof(PNRPCLOUDINFO);
    CloudInfo.Cloud.Scope = PNRP_LINK_LOCAL_SCOPE;

    Blob.cbSize = sizeof(PNRPCLOUDINFO);
    Blob.pBlobData = (LPBYTE)&CloudInfo;

    qset.dwSize = sizeof(WSAQUERYSET);
    qset.dwNameSpace = NS_PNRPCLOUD;
    qset.lpServiceClassId = (LPGUID)&SVCID_PNRPCLOUD;
    qset.lpBlob = &Blob;

    //
    // Start enumeration
    //
    err = WSALookupServiceBegin(
            &qset,
            LUP_RETURN_NAME,
            &hLookup);
                
    if(err !=0)
    {
        return WSAGetLastError();
    }

    // getting results
    while(TRUE)
    {

        //
        // Get size
        //
        ZeroMemory(&qset, sizeof(qset));
        dwSize = sizeof(qset);

        pResults = &qset;

        err = WSALookupServiceNext(
                hLookup,
                0,
                &dwSize,
                pResults
                );
        if(err != 0)
        {
            dwErr = WSAGetLastError();
        }

        if(dwErr != NO_ERROR)
        {
            if(dwErr == WSA_E_NO_MORE)
            {
                //
                // No more entries
                //
                dwErr = ERROR_SUCCESS;
                break;
            }
            else if (dwErr == WSAEFAULT)
            {
                //
                // This usually means result buffer too small. Allocate space
                //
                pResults = (WSAQUERYSET *)malloc(dwSize);
                if(pResults == NULL)
                {
                    dwErr = ERROR_OUTOFMEMORY;
                    break;
                }

                //
                // Get cloud name
                //
                err = WSALookupServiceNext(
                        hLookup,
                        0,
                        &dwSize,
                        pResults
                        );
                if(err == 0)
                {
                    wprintf(L"%s\n", pResults->lpszServiceInstanceName);

                    dwErr = NO_ERROR;
                }
                else
                {
                    dwErr = WSAGetLastError();
                }

                free(pResults);

                if(dwErr != NO_ERROR)
                {
                    break;
                }
            }
            else
            {
                //
                // Some other unexpected error
                //
                break;
            }
        }
        else
        {
            //
            // Should never happen
            //
            dwErr = ERROR_GEN_FAILURE;
            break;
        }
    }

    //
    // Close the enumeration
    //
    WSALookupServiceEnd(hLookup);
                
    return dwErr;
}
```



 

 



