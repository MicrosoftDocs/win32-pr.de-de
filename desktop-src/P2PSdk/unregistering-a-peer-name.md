---
description: Wenn Sie die Registrierung eines Peer namens aufheben, wird ein registrierter Name aus einer PNRP-Cloud (Peer Name Resolution Protocol) entfernt.
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Aufheben der Registrierung eines Peer namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959778"
---
# <a name="unregistering-a-peer-name"></a>Aufheben der Registrierung eines Peer namens

Wenn Sie die Registrierung eines Peer namens aufheben, wird ein registrierter Name aus einer PNRP-Cloud (Peer Name Resolution Protocol) entfernt.

## <a name="unregistering-a-peer-name"></a>Aufheben der Registrierung eines Peer namens

Um die Registrierung eines Peer namens aufzuheben, wenden Sie [**wsasetservice**](pnrp-and-wsasetservice.md)an. Der *ESS Operation* -Parameter muss den Wert **rnrservice \_ Delete** aufweisen. Verwenden Sie die Richtlinien in den folgenden Abschnitten dieses Themas, um die erforderlichen Konfigurationen für die **wsasetservice** -Parameter und die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur vorzunehmen.

## <a name="configuring-wsasetservice"></a>Konfigurieren von wsasetservice

Wenn eine Anwendung [**wsasetservice**](pnrp-and-wsasetservice.md)aufruft, müssen die Parameter entsprechend den folgenden Spezifikationen konfiguriert werden:

-   " *ESS Operation* " muss den Wert " **rnrservice \_ Delete**" aufweisen.
-   *dwFlags* muss NULL (0) sein.
-   *lpqsreginfo* muss auf eine [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur verweisen, die mithilfe der Richtlinien im folgenden Abschnitt dieses Themas konfiguriert werden muss.

## <a name="configuring-wsaqueryset"></a>Konfigurieren von wsaqueryset

Die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur muss entsprechend den folgenden Spezifikationen konfiguriert werden:

-   **dwSize** muss die Größe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur angeben.
-   **lpszserviceinstancename** muss auf den Peernamen verweisen, für den die Registrierung aufgehoben wird.
-   **lpblob** muss auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigen.
-   **lpcsabuffer** muss auf die Adressliste zeigen.

> [!Note]  
> Die übrigen Elemente werden in [**PNRP und wsasetservice**](pnrp-and-wsasetservice.md)beschrieben.

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Ein Beispiel für die Aufhebung der Registrierung eines Peer namens

Der folgende Code Ausschnitt zeigt, wie Sie die Registrierung eines Peer namens aufheben, indem Sie beim Aufrufen von [**wsasetservice**](pnrp-and-wsasetservice.md) mithilfe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die korrekten Informationen bereitstellen.


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



