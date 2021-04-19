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
# <a name="registering-a-peer-name"></a><span data-ttu-id="f9d9a-103">Registrieren eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="f9d9a-103">Registering a Peer Name</span></span>

<span data-ttu-id="f9d9a-104">Zum Registrieren eines Peer namens muss eine Anwendung die folgenden Informationen bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="f9d9a-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="f9d9a-105">IP-Adressliste</span><span class="sxs-lookup"><span data-stu-id="f9d9a-105">IP address list</span></span>
-   [<span data-ttu-id="f9d9a-106">Peer Identität</span><span class="sxs-lookup"><span data-stu-id="f9d9a-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="f9d9a-107">PeerName</span><span class="sxs-lookup"><span data-stu-id="f9d9a-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="f9d9a-108">Wenn ein PeerName nicht gesichert ist, ist eine Identität optional.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="f9d9a-109">Wenn eine Peer Identität als **null** angegeben ist, verwendet das Peer Name Resolution-Protokoll (PNRP) eine interne Standard-Peer Identität.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="f9d9a-110">Registrieren eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="f9d9a-110">Registering a Peer Name</span></span>

<span data-ttu-id="f9d9a-111">Nachdem die IP-Adressliste, die Peer Identität und der PeerName identifiziert wurden, kann die Anwendung einen Peernamen registrieren, indem [**wsasetservice**](pnrp-and-wsasetservice.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="f9d9a-112">Verwenden Sie die Richtlinien in den folgenden Abschnitten dieses Themas, um die erforderlichen Konfigurationen für die **wsasetservice** -Parameter und die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="f9d9a-113">Konfigurieren von wsasetservice</span><span class="sxs-lookup"><span data-stu-id="f9d9a-113">Configuring WSASetService</span></span>

<span data-ttu-id="f9d9a-114">Wenn eine Anwendung [**wsasetservice**](pnrp-and-wsasetservice.md)aufruft, müssen die Parameter entsprechend den folgenden Spezifikationen konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="f9d9a-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="f9d9a-115">" *ESS Operation* " muss den Wert " **rnrservice \_ Register**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="f9d9a-116">*dwFlags* muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="f9d9a-117">*lpqsreginfo* muss auf eine [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur verweisen, die mithilfe der Richtlinien im folgenden Abschnitt Konfigurieren von **wsaqueryset** in diesem Thema konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="f9d9a-118">Konfigurieren von wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="f9d9a-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="f9d9a-119">Die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur muss entsprechend den folgenden Spezifikationen konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="f9d9a-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="f9d9a-120">**dwSize** muss die Größe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="f9d9a-121">" **lpszserviceinstancename** " muss auf den Peernamen verweisen, der registriert wird.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="f9d9a-122">**lpblob** muss auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="f9d9a-123">**lpcsabuffer** muss auf die Adressliste zeigen.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="f9d9a-124">Die übrigen Elemente werden in [**PNRP und wsasetservice**](pnrp-and-wsasetservice.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="f9d9a-125">Nachdem ein Peername registriert wurde, sind die Informationen für die Peer Infrastruktur verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="f9d9a-126">Allerdings gibt es eine Verzögerung zwischen der Registrierungs Zeit und der Weitergabe der Registrierungsinformationen an andere Knoten.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="f9d9a-127">Während dieser Zeit sind andere Knoten möglicherweise nicht in der Lage, den neu registrierten Peer aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="f9d9a-128">Beispiel für das Registrieren eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="f9d9a-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="f9d9a-129">Der folgende Code Ausschnitt zeigt, wie Sie einen Peer Namen registrieren, indem Sie beim Aufrufen von [**wsasetservice**](pnrp-and-wsasetservice.md) mithilfe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die korrekten Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



