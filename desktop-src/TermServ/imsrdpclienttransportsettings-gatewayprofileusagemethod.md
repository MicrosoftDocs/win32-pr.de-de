---
title: Imsrdpclienttransportsettings (gatewayprofileusagemethod-Eigenschaft)
description: Gibt an, ob die Standardeinstellungen für Remotedesktop Gateway (RD-Gateway) verwendet werden sollen.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Gatewayprofileusagemethod-Eigenschaft Remotedesktopdienste
- Gatewayprofileusagemethod-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayprofileusagemethod-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391875"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="07790-106">Imsrdpclienttransportsettings:: gatewayprofileusagemethod-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07790-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="07790-107">Gibt an, ob die Standardeinstellungen für Remotedesktop Gateway (RD-Gateway) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07790-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="07790-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="07790-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="07790-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07790-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="07790-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="07790-110">Property value</span></span>

<span data-ttu-id="07790-111">Die RD-Gateway Profil Verwendungs Methode.</span><span class="sxs-lookup"><span data-stu-id="07790-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="07790-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="07790-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="07790-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ \_ \_ \_ Standardmodus für Proxy Profil Modus** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="07790-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="07790-114">Verwenden Sie den Standardprofil Modus, wie vom Administrator angegeben.</span><span class="sxs-lookup"><span data-stu-id="07790-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="07790-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ Proxy \_ Profil \_ Modus \_ explizit** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="07790-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="07790-116">Verwenden Sie die vom Benutzer angegebenen expliziten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="07790-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="07790-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="07790-117">Error codes</span></span>

<span data-ttu-id="07790-118">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="07790-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="07790-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07790-119">Requirements</span></span>



| <span data-ttu-id="07790-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07790-120">Requirement</span></span> | <span data-ttu-id="07790-121">Wert</span><span class="sxs-lookup"><span data-stu-id="07790-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07790-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07790-122">Minimum supported client</span></span><br/> | <span data-ttu-id="07790-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07790-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="07790-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07790-124">Minimum supported server</span></span><br/> | <span data-ttu-id="07790-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07790-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="07790-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="07790-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="07790-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07790-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="07790-128">DLL</span><span class="sxs-lookup"><span data-stu-id="07790-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07790-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07790-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="07790-130">IID</span><span class="sxs-lookup"><span data-stu-id="07790-130">IID</span></span><br/>                      | <span data-ttu-id="07790-131">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="07790-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07790-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07790-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07790-133">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="07790-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





