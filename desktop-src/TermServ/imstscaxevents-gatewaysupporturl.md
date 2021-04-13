---
title: IMsRdpClientTransportSettings2 gatewaysupporturl (Eigenschaft)
description: Gibt die Webadresse der Website an, die technischen Support für diesen Remotedesktop Gateway-Server (RD-Gateway) bereitstellt, oder ruft diese ab.
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Gatewaysupporturl-Eigenschaft Remotedesktopdienste
- Gatewaysupporturl-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaysupporturl (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391664"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="43b61-106">IMsRdpClientTransportSettings2:: gatewaysupporturl (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43b61-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="43b61-107">Gibt die Webadresse der Website an, die technischen Support für diesen Remotedesktop Gateway-Server (RD-Gateway) bereitstellt, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="43b61-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="43b61-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="43b61-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b61-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b61-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="43b61-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="43b61-110">Property value</span></span>

<span data-ttu-id="43b61-111">Gibt die Webadresse der Website an, die technischen Support für diesen RD-Gateway Server bereitstellt, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="43b61-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="43b61-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43b61-112">Requirements</span></span>



| <span data-ttu-id="43b61-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43b61-113">Requirement</span></span> | <span data-ttu-id="43b61-114">Wert</span><span class="sxs-lookup"><span data-stu-id="43b61-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b61-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43b61-115">Minimum supported client</span></span><br/> | <span data-ttu-id="43b61-116">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="43b61-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="43b61-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43b61-117">Minimum supported server</span></span><br/> | <span data-ttu-id="43b61-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43b61-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="43b61-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="43b61-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="43b61-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43b61-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="43b61-121">DLL</span><span class="sxs-lookup"><span data-stu-id="43b61-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43b61-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43b61-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="43b61-123">IID</span><span class="sxs-lookup"><span data-stu-id="43b61-123">IID</span></span><br/>                      | <span data-ttu-id="43b61-124">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="43b61-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43b61-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43b61-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b61-126">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="43b61-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="43b61-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="43b61-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





