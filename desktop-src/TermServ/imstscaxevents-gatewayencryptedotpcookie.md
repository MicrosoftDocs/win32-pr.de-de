---
title: IMsRdpClientTransportSettings2 gatewayverschlüsseltedotpcookie (Eigenschaft)
description: Gibt das verschlüsselte einmal Kennwort (One-time password, OTP) an oder ruft es ab.
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- Gatewayverschlüsseltedotpcookie-Eigenschaft Remotedesktopdienste
- Gatewayverschlüsseltedotpcookie-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewayverschlüsseltedotpcookie (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519223"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="0fd8c-106">IMsRdpClientTransportSettings2:: gatewayverschlüsseltedotpcookie-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0fd8c-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="0fd8c-107">Gibt das verschlüsselte einmal Kennwort (One-time password, OTP) an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="0fd8c-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd8c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd8c-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="0fd8c-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0fd8c-110">Property value</span></span>

<span data-ttu-id="0fd8c-111">Gibt das verschlüsselte OTP-Cookie an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd8c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fd8c-112">Requirements</span></span>



| <span data-ttu-id="0fd8c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fd8c-113">Requirement</span></span> | <span data-ttu-id="0fd8c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0fd8c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd8c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fd8c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd8c-116">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="0fd8c-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="0fd8c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fd8c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd8c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fd8c-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="0fd8c-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0fd8c-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0fd8c-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8c-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0fd8c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd8c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd8c-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8c-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0fd8c-123">IID</span><span class="sxs-lookup"><span data-stu-id="0fd8c-123">IID</span></span><br/>                      | <span data-ttu-id="0fd8c-124">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fd8c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd8c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd8c-126">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="0fd8c-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





