---
title: IMsRdpClientTransportSettings2 gatewayusername (Eigenschaft)
description: Gibt den Benutzernamen an, der für den Remotedesktop Gateway-Server (RD-Gateway) bereitgestellt wird, oder ruft ihn ab.
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Gatewayusername-Eigenschaft Remotedesktopdienste
- Gatewayusername-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewayusername (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342409"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a><span data-ttu-id="424b6-106">IMsRdpClientTransportSettings2:: gatewayusername-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="424b6-106">IMsRdpClientTransportSettings2::GatewayUserName property</span></span>

<span data-ttu-id="424b6-107">Gibt den Benutzernamen an, der für den Remotedesktop Gateway-Server (RD-Gateway) bereitgestellt wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="424b6-107">Specifies or retrieves the user name that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="424b6-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="424b6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="424b6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="424b6-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a><span data-ttu-id="424b6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="424b6-110">Property value</span></span>

<span data-ttu-id="424b6-111">Der Benutzername, der zum Herstellen der Verbindung mit dem RD-Gateway Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="424b6-111">The user name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="424b6-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="424b6-112">Error codes</span></span>

<span data-ttu-id="424b6-113">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="424b6-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="424b6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="424b6-114">Requirements</span></span>



| <span data-ttu-id="424b6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="424b6-115">Requirement</span></span> | <span data-ttu-id="424b6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="424b6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="424b6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="424b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="424b6-118">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="424b6-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="424b6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="424b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="424b6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="424b6-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="424b6-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="424b6-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="424b6-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="424b6-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="424b6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="424b6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="424b6-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="424b6-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="424b6-125">IID</span><span class="sxs-lookup"><span data-stu-id="424b6-125">IID</span></span><br/>                      | <span data-ttu-id="424b6-126">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="424b6-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="424b6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="424b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="424b6-128">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="424b6-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="424b6-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="424b6-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





