---
title: Imsrdpclienttransportsettings (gatewaykredssource-Eigenschaft)
description: Gibt die Authentifizierungsmethode für das Remotedesktop Gateway (RD-Gateway) an oder ruft Sie ab.
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Gatewaykredssource-Eigenschaft Remotedesktopdienste
- Gatewaykredssource-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewaykredssource-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391670"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="a8c65-106">Imsrdpclienttransportsettings:: gatewaykredssource-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8c65-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="a8c65-107">Gibt die Authentifizierungsmethode für das Remotedesktop Gateway (RD-Gateway) an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="a8c65-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="a8c65-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a8c65-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c65-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8c65-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="a8c65-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a8c65-110">Property value</span></span>

<span data-ttu-id="a8c65-111">Eine **ulong** -Variable, die die RD-Gateway Authentifizierungsmethode angibt.</span><span class="sxs-lookup"><span data-stu-id="a8c65-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="a8c65-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="a8c65-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="a8c65-113">Port für den TSC- \_ Proxy- \_ \_ \_ Benutzer Durchlauf (0)</span><span class="sxs-lookup"><span data-stu-id="a8c65-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="a8c65-114">Verwenden Sie ein Kennwort (NTLM) als Authentifizierungsmethode für RD-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a8c65-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="a8c65-115">Smartcard für den TSC-Proxy-Anmelde \_ \_ \_ Modus \_ (1)</span><span class="sxs-lookup"><span data-stu-id="a8c65-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="a8c65-116">Verwenden Sie eine Smartcard als Authentifizierungsmethode für RD-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a8c65-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="a8c65-117">Port für den TSC- \_ Proxy- \_ \_ Modus \_ Any (4)</span><span class="sxs-lookup"><span data-stu-id="a8c65-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="a8c65-118">Verwenden Sie für RD-Gateway eine beliebige Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="a8c65-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="a8c65-119">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a8c65-119">Error codes</span></span>

<span data-ttu-id="a8c65-120">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8c65-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c65-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8c65-121">Requirements</span></span>



| <span data-ttu-id="a8c65-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8c65-122">Requirement</span></span> | <span data-ttu-id="a8c65-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a8c65-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c65-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8c65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c65-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8c65-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a8c65-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8c65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c65-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8c65-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a8c65-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a8c65-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8c65-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c65-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a8c65-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a8c65-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8c65-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c65-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a8c65-132">IID</span><span class="sxs-lookup"><span data-stu-id="a8c65-132">IID</span></span><br/>                      | <span data-ttu-id="a8c65-133">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="a8c65-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8c65-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8c65-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c65-135">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="a8c65-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





