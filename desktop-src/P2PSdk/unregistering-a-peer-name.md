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
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="a8ba8-103">Aufheben der Registrierung eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="a8ba8-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="a8ba8-104">Wenn Sie die Registrierung eines Peer namens aufheben, wird ein registrierter Name aus einer PNRP-Cloud (Peer Name Resolution Protocol) entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="a8ba8-105">Aufheben der Registrierung eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="a8ba8-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="a8ba8-106">Um die Registrierung eines Peer namens aufzuheben, wenden Sie [**wsasetservice**](pnrp-and-wsasetservice.md)an.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="a8ba8-107">Der *ESS Operation* -Parameter muss den Wert **rnrservice \_ Delete** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="a8ba8-108">Verwenden Sie die Richtlinien in den folgenden Abschnitten dieses Themas, um die erforderlichen Konfigurationen für die **wsasetservice** -Parameter und die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="a8ba8-109">Konfigurieren von wsasetservice</span><span class="sxs-lookup"><span data-stu-id="a8ba8-109">Configuring WSASetService</span></span>

<span data-ttu-id="a8ba8-110">Wenn eine Anwendung [**wsasetservice**](pnrp-and-wsasetservice.md)aufruft, müssen die Parameter entsprechend den folgenden Spezifikationen konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="a8ba8-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="a8ba8-111">" *ESS Operation* " muss den Wert " **rnrservice \_ Delete**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="a8ba8-112">*dwFlags* muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="a8ba8-113">*lpqsreginfo* muss auf eine [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur verweisen, die mithilfe der Richtlinien im folgenden Abschnitt dieses Themas konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="a8ba8-114">Konfigurieren von wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="a8ba8-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="a8ba8-115">Die [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur muss entsprechend den folgenden Spezifikationen konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="a8ba8-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="a8ba8-116">**dwSize** muss die Größe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="a8ba8-117">**lpszserviceinstancename** muss auf den Peernamen verweisen, für den die Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="a8ba8-118">**lpblob** muss auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="a8ba8-119">**lpcsabuffer** muss auf die Adressliste zeigen.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="a8ba8-120">Die übrigen Elemente werden in [**PNRP und wsasetservice**](pnrp-and-wsasetservice.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="a8ba8-121">Ein Beispiel für die Aufhebung der Registrierung eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="a8ba8-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="a8ba8-122">Der folgende Code Ausschnitt zeigt, wie Sie die Registrierung eines Peer namens aufheben, indem Sie beim Aufrufen von [**wsasetservice**](pnrp-and-wsasetservice.md) mithilfe der [**wsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die korrekten Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a8ba8-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



