---
description: In diesem Thema werden Methoden zum Auflösen eines Peer namens mithilfe der PNRP-Namespace Anbieter-APIs erläutert.
ms.assetid: 7b21ec52-bc29-447e-9c46-34b9115574e0
title: Auflösen eines Peernamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7f3aa59d3dc3be89f35ce9d6eca58bed1ce137
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867004"
---
# <a name="resolving-a-peer-name"></a>Auflösen eines Peernamens

In diesem Thema werden Methoden zum Auflösen eines Peer namens mithilfe der PNRP-Namespace Anbieter-APIs erläutert.

Wenn Sie einen Peernamen auflösen, müssen Sie die folgenden Informationen angeben:

-   [PeerName](peer-names.md)
-   [Kriterien auflösen](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)
-   Der cloudName, in dem der Peername aufgelöst werden soll.
-   Die IP-Adresse, die optional ist und als Hinweis verwendet wird.

## <a name="resolving-a-peer-name"></a>Auflösen eines Peernamens

Nachdem Sie einen Peernamen, das Auflösungs Kriterium, den cloudnamen und die optionale IP-Adresse bereitgestellt haben, müssen die folgenden Schritte ausgeführt werden, um die Auflösung eines Peer namens abzuschließen:

-   [**Wsalookupservicebegin**](pnrp-and-wsalookupservicebegin.md) aufrufen, um den Prozess zu starten und ein Handle zurückzugeben.
-   [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) zum Auflösen des Peer namens abrufen.
-   Aufrufen von [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) , um den Vorgang abzuschließen.

## <a name="an-example-of-resolving-a-peer-name"></a>Ein Beispiel für das Auflösen eines Peer namens

Der folgende Code Ausschnitt zeigt, wie Sie einen Peernamen auflösen. Im Beispiel wird davon ausgegangen, dass eine TCP/IP-Adresse zurückgegeben wird.


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment( lib, "ws2_32.lib")

// Function: PnrpResolve
//
// Purpose:  Resolve the given name within a PNRP cloud
//
// Arguments:
//   pwzName  : name to resolve in PNRP, generally the graph id
//   pwzCloud : name of cloud to resolve in, NULL = global cloud
//   pAddr    : pointer to result buffer
//
// Returns:  HRESULT
//
HRESULT PnrpResolve(PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddr)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    WSAQUERYSET*    pResults = NULL;
    WSAQUERYSET     tempResultSet = {0};
    HANDLE          hLookup = NULL;
    BOOL            fFound = FALSE;
    DWORD           dwError;
    INT             iRet;
    ULONG           i;
    DWORD           dwSize = 0;

    //
    // fill in the WSAQUERYSET
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.nMaxResolve = 1;
    pnrpInfo.dwTimeout = 30;
    pnrpInfo.enResolveCriteria = PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;
    // start resolve
    iRet = WSALookupServiceBegin(
            &querySet,
            LUP_RETURN_NAME | LUP_RETURN_ADDR | LUP_RETURN_COMMENT,
            &hLookup);


    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    if (SUCCEEDED(hr))
    {
        dwSize = sizeof(tempResultSet);

        // retrieve the required size
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, &tempResultSet);
        dwError = WSAGetLastError();

        if (dwError == WSAEFAULT)
        {
            // allocate space for the results
            pResults = (WSAQUERYSET*)malloc(dwSize);
            if (pResults == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }
        else
        {
            hr = HRESULT_FROM_WIN32(dwError);
        }
    }

    if (SUCCEEDED(hr))
    {
        // retrieve the addresses
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, pResults);
        if (iRet != 0)
        {
            hr = HRESULT_FROM_WIN32(WSAGetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // return the first IPv6 address found
        for (i = 0; i < pResults->dwNumberOfCsAddrs; i++)
        {
            if (pResults->lpcsaBuffer[i].iProtocol == IPPROTO_TCP &&
                pResults->lpcsaBuffer[i].RemoteAddr.iSockaddrLength == sizeof(SOCKADDR_IN6))
            {
                CopyMemory(pAddr, pResults->lpcsaBuffer[i].RemoteAddr.lpSockaddr, sizeof(SOCKADDR_IN6));
                fFound = TRUE;
                break;
            }
        }

        if (!fFound)
        {
            // unable to find an IPv6 address
            hr = HRESULT_FROM_WIN32(WSA_E_NO_MORE);
        }
    }

    if (hLookup != NULL)
    {
        WSALookupServiceEnd(hLookup);
    }

    if (pResults != NULL)
    {
        free(pResults);
    }

    return hr;
}
```



 

 



