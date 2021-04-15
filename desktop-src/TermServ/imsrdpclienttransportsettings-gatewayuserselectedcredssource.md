---
title: Imsrdpclienttransportsettings gatewayuserselectedkredssource-Eigenschaft
description: Legt die benutzerdefinierte Remotedesktop Gateway-Anmelde Informationsquelle (RD-Gateway) fest oder ruft Sie ab.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Gatewayuserselectedkredssource-Eigenschaft Remotedesktopdienste
- Gatewayuserselectedkredssource-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayuserselectedkredssource-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517489"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="d9dcd-106">Imsrdpclienttransportsettings:: gatewayuserselectedkredssource-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9dcd-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="d9dcd-107">Legt die benutzerdefinierte Remotedesktop Gateway-Anmelde Informationsquelle (RD-Gateway) fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="d9dcd-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9dcd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9dcd-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="d9dcd-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d9dcd-110">Property value</span></span>

<span data-ttu-id="d9dcd-111">Eine **ulong** -Variable, die die RD-Gateway Authentifizierungsmethode angibt.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="d9dcd-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="d9dcd-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ Proxys des Proxys im Proxy \_ \_ Modus \_** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d9dcd-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d9dcd-114">Verwenden Sie ein Kennwort (NTLM) als Authentifizierungsmethode für RD-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="d9dcd-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ Proxy-Anmelde \_ \_ Modus- \_ Smartcard** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d9dcd-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d9dcd-116">Verwenden Sie eine Smartcard als Authentifizierungsmethode für RD-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="d9dcd-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ Proxys im Proxy \_ \_ Modus \_ any** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="d9dcd-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="d9dcd-118">Verwenden Sie für RD-Gateway eine beliebige Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="d9dcd-119">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d9dcd-119">Error codes</span></span>

<span data-ttu-id="d9dcd-120">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9dcd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9dcd-121">Requirements</span></span>



| <span data-ttu-id="d9dcd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9dcd-122">Requirement</span></span> | <span data-ttu-id="d9dcd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d9dcd-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dcd-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9dcd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9dcd-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9dcd-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="d9dcd-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9dcd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9dcd-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9dcd-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="d9dcd-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d9dcd-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9dcd-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9dcd-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d9dcd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d9dcd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9dcd-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9dcd-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d9dcd-132">IID</span><span class="sxs-lookup"><span data-stu-id="d9dcd-132">IID</span></span><br/>                      | <span data-ttu-id="d9dcd-133">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="d9dcd-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9dcd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9dcd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9dcd-135">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="d9dcd-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





