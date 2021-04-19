---
description: 'Um einen Peernamen zu registrieren, muss eine Anwendung die folgenden Informationen bereitstellen: IP-Adresse listpeer identitypeer nameif ein PeerName ist nicht gesichert, eine Identität ist optional.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrieren eines Peer namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364094"
---
# <a name="registering-a-peer-name"></a>Registrieren eines Peer namens

Zum Registrieren eines Peer namens muss eine Anwendung die folgenden Informationen bereitstellen:

-   IP-Adressliste
-   [Peer Identität](creating-a-peer-identity.md)
-   [PeerName](peer-names.md)

Wenn ein PeerName nicht gesichert ist, ist eine Identität optional. Wenn eine Peer Identität als **null** angegeben ist, verwendet das Peer Name Resolution-Protokoll (PNRP) eine interne Standard-Peer Identität.

## <a name="registering-a-peer-name"></a>Registrieren eines Peer namens

Nachdem die IP-Adressliste, die Peer Identität und der PeerName identifiziert wurden, kann die Anwendung einen Peernamen registrieren, indem [**wsasetservice**](pnrp-and-wsasetservice.md)aufgerufen wird. Verwenden Sie die Richtlinien in den folgenden Abschnitten dieses Themas, um die erforderlichen Konfigurationen für die **wsasetservice** -Parameter und die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur vorzunehmen.

### <a name="configuring-wsasetservice"></a>Konfigurieren von wsasetservice

Wenn eine Anwendung [**wsasetservice**](pnrp-and-wsasetservice.md)aufruft, müssen die Parameter entsprechend den folgenden Spezifikationen konfiguriert werden:

-   " *ESS Operation* " muss den Wert " **rnrservice \_ Register**" aufweisen.
-   *dwFlags* muss NULL (0) sein.
-   *lpqsreginfo* muss auf eine [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur verweisen, die mithilfe der Richtlinien im folgenden Abschnitt Konfigurieren von **wsaqueryset** in diesem Thema konfiguriert werden muss.

### <a name="configuring-wsaqueryset"></a>Konfigurieren von wsaqueryset

Die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur muss entsprechend den folgenden Spezifikationen konfiguriert werden:

-   **dwSize** muss die Größe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur angeben.
-   " **lpszserviceinstancename** " muss auf den Peernamen verweisen, der registriert wird.
-   **lpblob** muss auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigen.
-   **lpcsabuffer** muss auf die Adressliste zeigen.

> [!Note]  
> Die übrigen Elemente werden in [**PNRP und wsasetservice**](pnrp-and-wsasetservice.md)beschrieben.

 

Nachdem ein Peername registriert wurde, sind die Informationen für die Peer Infrastruktur verfügbar. Allerdings gibt es eine Verzögerung zwischen der Registrierungs Zeit und der Weitergabe der Registrierungsinformationen an andere Knoten. Während dieser Zeit sind andere Knoten möglicherweise nicht in der Lage, den neu registrierten Peer aufzulösen.

## <a name="example-of-registering-a-peer-name"></a>Beispiel für das Registrieren eines Peer namens

Der folgende Code Ausschnitt zeigt, wie Sie einen Peer Namen registrieren, indem Sie beim Aufrufen von [**wsasetservice**](pnrp-and-wsasetservice.md) mithilfe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die korrekten Informationen bereitstellen.


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



