---
title: Imsrdpclienttransportsettings (gatewayissupported-Eigenschaft)
description: Gibt an, ob Remotedesktop Gateway (RD-Gateway) unterstützt wird.
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Gatewayissupported-Eigenschaft Remotedesktopdienste
- Gatewayissupported-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayissupported-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391525"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="01790-106">Imsrdpclienttransportsettings:: gatewayissupported-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01790-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="01790-107">Gibt an, ob Remotedesktop Gateway (RD-Gateway) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="01790-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="01790-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="01790-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01790-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="01790-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="01790-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="01790-110">Property value</span></span>

<span data-ttu-id="01790-111">Gibt an, ob RD-Gateway unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="01790-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01790-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="01790-112">Error codes</span></span>

<span data-ttu-id="01790-113">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="01790-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="01790-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01790-114">Requirements</span></span>



| <span data-ttu-id="01790-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01790-115">Requirement</span></span> | <span data-ttu-id="01790-116">Wert</span><span class="sxs-lookup"><span data-stu-id="01790-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01790-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01790-117">Minimum supported client</span></span><br/> | <span data-ttu-id="01790-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01790-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="01790-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01790-119">Minimum supported server</span></span><br/> | <span data-ttu-id="01790-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01790-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="01790-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="01790-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="01790-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01790-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="01790-123">DLL</span><span class="sxs-lookup"><span data-stu-id="01790-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01790-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01790-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="01790-125">IID</span><span class="sxs-lookup"><span data-stu-id="01790-125">IID</span></span><br/>                      | <span data-ttu-id="01790-126">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="01790-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01790-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01790-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01790-128">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="01790-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





