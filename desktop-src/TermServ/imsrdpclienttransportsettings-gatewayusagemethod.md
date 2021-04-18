---
title: Imsrdpclienttransportsettings (gatewayusagemethod-Eigenschaft)
description: Gibt an, wann ein Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Gatewayusagemethod-Eigenschaft Remotedesktopdienste
- Gatewayusagemethod-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayusagemethod-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340986"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="58060-106">Imsrdpclienttransportsettings:: gatewayusagemethod-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58060-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="58060-107">Gibt an, wann ein Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58060-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="58060-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="58060-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58060-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="58060-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="58060-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="58060-110">Property value</span></span>

<span data-ttu-id="58060-111">Eine **ulong** -Variable, die die RD-Gateway Server-Verwendungs Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="58060-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="58060-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="58060-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="58060-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ Proxy \_ Modus " \_ keine \_ direkt** " (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="58060-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="58060-114">Verwenden Sie keinen RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="58060-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="58060-115">In der Client Benutzeroberfläche des Remotedesktopverbindung (RDC) ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="58060-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="58060-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ Proxy \_ Modus \_ Direct** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="58060-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="58060-117">Verwenden Sie immer einen RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="58060-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="58060-118">In der RDC-Client-Benutzeroberfläche ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="58060-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="58060-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ Proxy \_ Modus- \_ Erkennung** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="58060-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="58060-120">Verwenden Sie einen RD-Gateway Server, wenn keine direkte Verbindung mit dem RD-Sitzungshost Server hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="58060-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="58060-121">Auf der RDC-Client Benutzeroberfläche ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58060-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="58060-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ Proxy \_ Modus \_ Standard** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="58060-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="58060-123">Standard RD-Gateway Servereinstellungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="58060-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="58060-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ Proxy \_ Modus \_ keine \_ Erkennung** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="58060-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="58060-125">Verwenden Sie keinen RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="58060-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="58060-126">Auf der RDC-Client Benutzeroberfläche ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58060-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="58060-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="58060-127">Error codes</span></span>

<span data-ttu-id="58060-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="58060-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="58060-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58060-129">Requirements</span></span>



| <span data-ttu-id="58060-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58060-130">Requirement</span></span> | <span data-ttu-id="58060-131">Wert</span><span class="sxs-lookup"><span data-stu-id="58060-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58060-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58060-132">Minimum supported client</span></span><br/> | <span data-ttu-id="58060-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58060-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="58060-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58060-134">Minimum supported server</span></span><br/> | <span data-ttu-id="58060-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58060-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="58060-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="58060-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="58060-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58060-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="58060-138">DLL</span><span class="sxs-lookup"><span data-stu-id="58060-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58060-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58060-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="58060-140">IID</span><span class="sxs-lookup"><span data-stu-id="58060-140">IID</span></span><br/>                      | <span data-ttu-id="58060-141">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="58060-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58060-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58060-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58060-143">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="58060-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





