---
description: 'Um einen Peernamen zu registrieren, muss eine Anwendung die folgenden Informationen bereitstellen: IP-Adresse listPeer identityPeer nameWenn ein Peername unsicher ist, ist eine Identität optional.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrieren eines Peernamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcedbe3e405e21ec9709289e8a9237179703b1b8e81f40b449479373524beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011488"
---
# <a name="registering-a-peer-name"></a>Registrieren eines Peernamens

Um einen Peernamen zu registrieren, muss eine Anwendung die folgenden Informationen bereitstellen:

-   IP-Adressliste
-   [Peeridentität](creating-a-peer-identity.md)
-   [Peername](peer-names.md)

Wenn ein Peername nicht gesichert ist, ist eine Identität optional. Wenn eine Peeridentität als **NULL** angegeben wird, verwendet das PEER Name Resolution Protocol (PNRP) eine interne Standard-Peeridentität.

## <a name="registering-a-peer-name"></a>Registrieren eines Peernamens

Nachdem die IP-Adressliste, die Peeridentität und der Peername identifiziert wurden, kann die Anwendung einen Peernamen registrieren, indem [**sie WSASetService**](pnrp-and-wsasetservice.md)aufruft. Verwenden Sie die Richtlinien in den folgenden Abschnitten dieses Themas, um die erforderlichen Konfigurationen für die **WSASetService-Parameter** und die [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) vorzunehmen.

### <a name="configuring-wsasetservice"></a>Konfigurieren von WSASetService

Wenn eine Anwendung [**WSASetService aufruft,**](pnrp-and-wsasetservice.md)müssen die Parameter gemäß den folgenden Spezifikationen konfiguriert werden:

-   *essOperation* muss den Wert **RNRSERVICE \_ REGISTER aufweisen.**
-   *dwFlags* muss 0 (null) sein.
-   *lpqsRegInfo* muss auf eine [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) verweisen, die anhand der Richtlinien im folgenden Abschnitt Konfigurieren von **WSAQUERYSET** dieses Themas konfiguriert werden muss.

### <a name="configuring-wsaqueryset"></a>Konfigurieren von WSAQUERYSET

Die [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) muss gemäß den folgenden Spezifikationen konfiguriert werden:

-   **dwSize** muss die Größe der [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) angeben.
-   **lpszServiceInstanceName** muss auf den Peernamen verweisen, der registriert wird.
-   **lpBlob** muss auf eine [**PNRPINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) zeigen.
-   **lpcsaBuffer** muss auf die Adressliste verweisen.

> [!Note]  
> Die verbleibenden Member werden in [**PNRP und WSASetService**](pnrp-and-wsasetservice.md)beschrieben.

 

Nachdem ein Peername registriert wurde, sind die Informationen für die Peerinfrastruktur verfügbar. Es gibt jedoch eine Verzögerung zwischen der Registrierungszeit und der Weitergabe der Registrierungsinformationen an andere Knoten. Während dieser Zeit können andere Knoten den neu registrierten Peer möglicherweise nicht auflösen.

## <a name="example-of-registering-a-peer-name"></a>Beispiel für die Registrierung eines Peernamens

Der folgende Codeausschnitt zeigt, wie Sie einen Peernamen registrieren, indem Sie beim Aufrufen von [**WSASetService**](pnrp-and-wsasetservice.md) mithilfe der [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) die richtigen Informationen bereitstellen.


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



 

 



