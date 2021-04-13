---
title: IMsRdpClientTransportSettings2 gatewaykredsharing (Eigenschaft)
description: Gibt die Einstellung an, ob das Feature für die Freigabe von Anmelde Informationen für das Remotedesktop Gateway (RD-Gateway) aktiviert ist, oder ruft Sie ab.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Gatewaykredsharing-Eigenschaft Remotedesktopdienste
- Gatewaykredsharing-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaykredsharing (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475627"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="de416-106">IMsRdpClientTransportSettings2:: gatewaykredsharing (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de416-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="de416-107">Gibt die Einstellung an, ob das Feature für die Freigabe von Anmelde Informationen für das Remotedesktop Gateway (RD-Gateway) aktiviert ist, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="de416-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="de416-108">Wenn das Feature aktiviert ist, versucht das Remotedesktop ActiveX-Steuerelement, die gleichen Anmelde Informationen für die Authentifizierung beim Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server und beim RD-Gateway Server zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="de416-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="de416-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="de416-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de416-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="de416-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="de416-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="de416-111">Property value</span></span>

<span data-ttu-id="de416-112">Wenn Sie auf 1 festgelegt ist, ist die Freigabe von Anmelde Informationen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="de416-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="de416-113">Wenn der Wert auf NULL festgelegt ist, ist die Freigabe von Anmelde Informationen deaktiviert</span><span class="sxs-lookup"><span data-stu-id="de416-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de416-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="de416-114">Error codes</span></span>

<span data-ttu-id="de416-115">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="de416-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="de416-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de416-116">Remarks</span></span>

<span data-ttu-id="de416-117">Diese Eigenschaft wird vom ActiveX-Steuerelement verwendet, um eine einzelne Eingabeaufforderung für die Freigabe von Anmelde Informationen zwischen dem RD-Sitzungshost Server und dem RD-Gateway Server zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="de416-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="de416-118">Die Freigabe von Anmelde Informationen unterstützt keine webbasierte Kenn Wort Freigabe mit [**gatewaypassword**](imsrdpclienttransportsettings2-gatewaypassword.md) oder [**cleartextpassword**](imstscnonscriptable-cleartextpassword.md).</span><span class="sxs-lookup"><span data-stu-id="de416-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de416-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de416-119">Requirements</span></span>



| <span data-ttu-id="de416-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de416-120">Requirement</span></span> | <span data-ttu-id="de416-121">Wert</span><span class="sxs-lookup"><span data-stu-id="de416-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de416-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de416-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de416-123">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="de416-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="de416-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de416-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de416-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de416-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="de416-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="de416-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="de416-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de416-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="de416-128">DLL</span><span class="sxs-lookup"><span data-stu-id="de416-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de416-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de416-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="de416-130">IID</span><span class="sxs-lookup"><span data-stu-id="de416-130">IID</span></span><br/>                      | <span data-ttu-id="de416-131">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="de416-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de416-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de416-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de416-133">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="de416-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="de416-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="de416-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





