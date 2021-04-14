---
title: IMsRdpClientTransportSettings2 gatewaypreauthserveraddr (Eigenschaft)
description: Gibt die Webadresse des Servers für die Vorauthentifizierung an, der für das einmalige Kennwort (RD-Gateway) von Remotedesktop Gateway verwendet wird, oder ruft Sie ab.
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Gatewaypreauthserveraddr-Eigenschaft Remotedesktopdienste
- Gatewaypreauthserveraddr-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaypreauthserveraddr (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391665"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="4e413-106">IMsRdpClientTransportSettings2:: gatewaypreauthserveraddr (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4e413-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="4e413-107">Gibt die Webadresse des Servers für die Vorauthentifizierung an, der für das einmalige Kennwort (RD-Gateway) von Remotedesktop Gateway verwendet wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="4e413-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="4e413-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4e413-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e413-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e413-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="4e413-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4e413-110">Property value</span></span>

<span data-ttu-id="4e413-111">Die Webadresse des Servers, der vor der Authentifizierung verwendet wird. beispielsweise die Webadresse des Microsoft Internet Security and Acceleration (ISA)-Servers.</span><span class="sxs-lookup"><span data-stu-id="4e413-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="4e413-112">Geben Sie die Webadresse im Format "https://*Hostname*" an. *Domain Name*. com/*Websitename*"oder" https://*Hostname*. *Domain Name*. com/*Websitename*".</span><span class="sxs-lookup"><span data-stu-id="4e413-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e413-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4e413-113">Error codes</span></span>

<span data-ttu-id="4e413-114">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e413-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e413-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e413-115">Requirements</span></span>



| <span data-ttu-id="4e413-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e413-116">Requirement</span></span> | <span data-ttu-id="4e413-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4e413-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e413-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e413-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4e413-119">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="4e413-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="4e413-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e413-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4e413-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e413-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="4e413-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4e413-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e413-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e413-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4e413-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4e413-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e413-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e413-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4e413-126">IID</span><span class="sxs-lookup"><span data-stu-id="4e413-126">IID</span></span><br/>                      | <span data-ttu-id="4e413-127">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="4e413-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e413-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e413-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e413-129">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="4e413-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="4e413-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="4e413-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





