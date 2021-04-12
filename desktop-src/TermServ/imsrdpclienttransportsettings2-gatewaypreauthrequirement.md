---
title: IMsRdpClientTransportSettings2 gatewaypreauthrequirement (Eigenschaft)
description: Gibt die Einstellung für das einmalige Kennwort (One-time password, OTP) des Remotedesktop Gateway-Gateways (RD-Gateway) an oder ruft diese ab.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Gatewaypreauthrequirement-Eigenschaft Remotedesktopdienste
- Gatewaypreauthrequirement-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaypreauthrequirement (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518941"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="ba2ad-106">IMsRdpClientTransportSettings2:: gatewaypreauthrequirement (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ba2ad-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="ba2ad-107">Gibt die Einstellung für das einmalige Kennwort (One-time password, OTP) des Remotedesktop Gateway-Gateways (RD-Gateway) an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="ba2ad-108">Wenn OTP aktiviert ist, versucht **gatewaypreauthrequirement** , das OTP-Cookie mithilfe der [**gatewaypreauthserveraddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) -Eigenschaft aus dem Internet Cookie-Speicher abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="ba2ad-109">Bei erfolgreicher Ausführung sendet **gatewaypreauthrequirement** das OTP-Cookie für die Vorauthentifizierung an den Firewallserver (z. b. Microsoft Internet Security und Acceleration \[ ISA \] Server).</span><span class="sxs-lookup"><span data-stu-id="ba2ad-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="ba2ad-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba2ad-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba2ad-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="ba2ad-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ba2ad-112">Property value</span></span>

<span data-ttu-id="ba2ad-113">Wenn der Wert auf 1 festgelegt ist, ist die OTP-Funktion aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="ba2ad-114">Wenn der Wert auf 0 festgelegt ist, ist die OTP-Funktion deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba2ad-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ba2ad-115">Error codes</span></span>

<span data-ttu-id="ba2ad-116">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba2ad-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba2ad-117">Requirements</span></span>



| <span data-ttu-id="ba2ad-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba2ad-118">Requirement</span></span> | <span data-ttu-id="ba2ad-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ba2ad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba2ad-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba2ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ba2ad-121">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ba2ad-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="ba2ad-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba2ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ba2ad-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba2ad-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="ba2ad-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ba2ad-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba2ad-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba2ad-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="ba2ad-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ba2ad-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba2ad-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba2ad-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="ba2ad-128">IID</span><span class="sxs-lookup"><span data-stu-id="ba2ad-128">IID</span></span><br/>                      | <span data-ttu-id="ba2ad-129">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="ba2ad-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba2ad-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba2ad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba2ad-131">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="ba2ad-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="ba2ad-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="ba2ad-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





