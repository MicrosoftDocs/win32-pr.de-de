---
title: Imsrdpclienttransportsettings (gatewaydefaultusagemethod-Eigenschaft)
description: Die Standard Verwendungs Methode für Remotedesktop Gateway (RD-Gateway).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Gatewaydefaultusagemethod-Eigenschaft Remotedesktopdienste
- Gatewaydefaultusagemethod-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewaydefaultusagemethod-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338525"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="7c6ac-106">Imsrdpclienttransportsettings:: gatewaydefaultusagemethod (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7c6ac-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="7c6ac-107">Die Standard Verwendungs Methode für Remotedesktop Gateway (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="7c6ac-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="7c6ac-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7c6ac-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6ac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c6ac-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="7c6ac-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7c6ac-110">Property value</span></span>

<span data-ttu-id="7c6ac-111">Ein Zeiger auf die Standard Verwendungs Methode für RD-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c6ac-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="7c6ac-112">Gibt eine Union der Benutzereinstellungen zurück, die durch [**Put \_ gatewayusagemethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)und Gruppenrichtlinien Einstellungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7c6ac-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="7c6ac-113">Wenn keine Benutzereinstellungen durch **Put \_ gatewayusagemethod ()** festgelegt wurden, gibt **get \_ gatewaydefaultusagemethod ()** den Standardwert für die **Erkennung des TSC- \_ Proxy \_ Modus \_** zurück.</span><span class="sxs-lookup"><span data-stu-id="7c6ac-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c6ac-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7c6ac-114">Error codes</span></span>

<span data-ttu-id="7c6ac-115">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7c6ac-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6ac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c6ac-116">Requirements</span></span>



| <span data-ttu-id="7c6ac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c6ac-117">Requirement</span></span> | <span data-ttu-id="7c6ac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7c6ac-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6ac-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c6ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6ac-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c6ac-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="7c6ac-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c6ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6ac-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c6ac-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7c6ac-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7c6ac-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c6ac-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ac-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7c6ac-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7c6ac-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c6ac-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c6ac-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7c6ac-127">IID</span><span class="sxs-lookup"><span data-stu-id="7c6ac-127">IID</span></span><br/>                      | <span data-ttu-id="7c6ac-128">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="7c6ac-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c6ac-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c6ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6ac-130">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="7c6ac-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





