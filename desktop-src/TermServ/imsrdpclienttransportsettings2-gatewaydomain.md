---
title: IMsRdpClientTransportSettings2 gatewaydomain (Eigenschaft)
description: Gibt den Domänen Namen eines Benutzers an, der für den Remotedesktop Gateway-Server (RD-Gateway) bereitgestellt wird, oder ruft ihn ab.
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- Gatewaydomain-Eigenschaft Remotedesktopdienste
- Gatewaydomain-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaydomain (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391666"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="c6d8a-106">IMsRdpClientTransportSettings2:: gatewaydomain (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6d8a-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="c6d8a-107">Gibt den Domänen Namen eines Benutzers an, der für den Remotedesktop Gateway-Server (RD-Gateway) bereitgestellt wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c6d8a-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="c6d8a-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c6d8a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d8a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6d8a-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="c6d8a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c6d8a-110">Property value</span></span>

<span data-ttu-id="c6d8a-111">Der Domänen Name, der zum Herstellen der Verbindung mit dem RD-Gateway Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6d8a-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6d8a-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c6d8a-112">Error codes</span></span>

<span data-ttu-id="c6d8a-113">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c6d8a-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d8a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6d8a-114">Requirements</span></span>



| <span data-ttu-id="c6d8a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6d8a-115">Requirement</span></span> | <span data-ttu-id="c6d8a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c6d8a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d8a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6d8a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d8a-118">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="c6d8a-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="c6d8a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6d8a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d8a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6d8a-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="c6d8a-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c6d8a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6d8a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d8a-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="c6d8a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c6d8a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6d8a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d8a-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="c6d8a-125">IID</span><span class="sxs-lookup"><span data-stu-id="c6d8a-125">IID</span></span><br/>                      | <span data-ttu-id="c6d8a-126">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="c6d8a-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6d8a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6d8a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d8a-128">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="c6d8a-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="c6d8a-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="c6d8a-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





