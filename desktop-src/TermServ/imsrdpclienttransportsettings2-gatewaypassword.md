---
title: IMsRdpClientTransportSettings2 gatewaypassword (Eigenschaft)
description: Gibt das Kennwort an, das ein Benutzer zum Herstellen einer Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) bereitstellt.
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Gatewaypassword-Eigenschaft Remotedesktopdienste
- Gatewaypassword-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaypassword (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517486"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="035c7-106">IMsRdpClientTransportSettings2:: gatewaypassword (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="035c7-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="035c7-107">Gibt das Kennwort an, das ein Benutzer zum Herstellen einer Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="035c7-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="035c7-108">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="035c7-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="035c7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="035c7-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="035c7-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="035c7-110">Property value</span></span>

<span data-ttu-id="035c7-111">Das Kennwort, das ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="035c7-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="035c7-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="035c7-112">Error codes</span></span>

<span data-ttu-id="035c7-113">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="035c7-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="035c7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="035c7-114">Requirements</span></span>



| <span data-ttu-id="035c7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="035c7-115">Requirement</span></span> | <span data-ttu-id="035c7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="035c7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="035c7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="035c7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="035c7-118">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="035c7-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="035c7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="035c7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="035c7-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="035c7-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="035c7-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="035c7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="035c7-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="035c7-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="035c7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="035c7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="035c7-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="035c7-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="035c7-125">IID</span><span class="sxs-lookup"><span data-stu-id="035c7-125">IID</span></span><br/>                      | <span data-ttu-id="035c7-126">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="035c7-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="035c7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="035c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="035c7-128">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="035c7-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="035c7-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="035c7-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





