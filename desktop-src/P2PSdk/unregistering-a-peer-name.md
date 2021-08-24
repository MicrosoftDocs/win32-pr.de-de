---
description: Wenn Sie die Registrierung eines Peernamens aufheben, wird ein registrierter Name aus einer PNRP-Cloud (Peer Name Resolution Protocol) entfernt.
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Aufheben der Registrierung eines Peernamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ee0bd03e881f93321c31dfccd03cc71459b323f1ed356a88f829489c578a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675010"
---
# <a name="unregistering-a-peer-name"></a>Aufheben der Registrierung eines Peernamens

Wenn Sie die Registrierung eines Peernamens aufheben, wird ein registrierter Name aus einer PNRP-Cloud (Peer Name Resolution Protocol) entfernt.

## <a name="unregistering-a-peer-name"></a>Aufheben der Registrierung eines Peernamens

Um die Registrierung eines Peernamens zu aufheben, rufen Sie [**WSASetService**](pnrp-and-wsasetservice.md)auf. Der *essOperation-Parameter* muss den Wert **RNRSERVICE \_ DELETE aufweisen.** Verwenden Sie die Richtlinien in den folgenden Abschnitten dieses Themas, um die erforderlichen Konfigurationen für die **WSASetService-Parameter** und die [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) vorzunehmen.

## <a name="configuring-wsasetservice"></a>Konfigurieren von WSASetService

Wenn eine Anwendung [**WSASetService aufruft,**](pnrp-and-wsasetservice.md)müssen die Parameter gemäß den folgenden Spezifikationen konfiguriert werden:

-   *essOperation* muss den Wert **RNRSERVICE \_ DELETE** aufweisen.
-   *dwFlags* muss null (0) sein.
-   *lpqsRegInfo* muss auf eine [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) verweisen, die mithilfe der Richtlinien im folgenden Abschnitt dieses Themas konfiguriert werden muss.

## <a name="configuring-wsaqueryset"></a>Konfigurieren von WSAQUERYSET

Die [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) muss gemäß den folgenden Spezifikationen konfiguriert werden:

-   **dwSize** muss die Größe der [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) angeben.
-   **lpszServiceInstanceName** muss auf den Peernamen verweisen, der nicht registriert wird.
-   **lpBlob** muss auf eine [**PNRPINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) zeigen.
-   **lpcsaBuffer** muss auf die Adressliste verweisen.

> [!Note]  
> Die verbleibenden Member werden in [**PNRP und WSASetService**](pnrp-and-wsasetservice.md)beschrieben.

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Beispiel für das Aufheben der Registrierung eines Peernamens

Der folgende Codeausschnitt zeigt, wie Sie die Registrierung eines Peernamens aufheben, indem Sie beim Aufrufen von [**WSASetService**](pnrp-and-wsasetservice.md) mithilfe der [**WSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) die richtigen Informationen bereitstellen.


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



 

 



