---
title: IMsRdpClientTransportSettings2 gatewayverschlüsseltedotpcookiesize (Eigenschaft)
description: Gibt die Größe des verschlüsselten Kennworts für einmal Kennwort (One-time password, OTP) an oder ruft diese ab.
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- Die gatewayverschlüsseltedotpcookiesize-Eigenschaft Remotedesktopdienste
- Gatewayverschlüsseltedotpcookiesize-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewayverschlüsseltedotpcookiesize (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741337"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="4bfa6-106">IMsRdpClientTransportSettings2:: gatewayverschlüsseltedotpcookiesize (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4bfa6-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="4bfa6-107">Gibt die Größe des verschlüsselten Kennworts für einmal Kennwort (One-time password, OTP) an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="4bfa6-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="4bfa6-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4bfa6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bfa6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bfa6-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="4bfa6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4bfa6-110">Property value</span></span>

<span data-ttu-id="4bfa6-111">Gibt die Größe des verschlüsselten Kennworts für einmal Kennwort (One-time password, OTP) an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="4bfa6-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfa6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bfa6-112">Requirements</span></span>



| <span data-ttu-id="4bfa6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bfa6-113">Requirement</span></span> | <span data-ttu-id="4bfa6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4bfa6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfa6-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bfa6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfa6-116">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="4bfa6-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="4bfa6-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bfa6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfa6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bfa6-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="4bfa6-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4bfa6-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4bfa6-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa6-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4bfa6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4bfa6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bfa6-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa6-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4bfa6-123">IID</span><span class="sxs-lookup"><span data-stu-id="4bfa6-123">IID</span></span><br/>                      | <span data-ttu-id="4bfa6-124">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="4bfa6-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bfa6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bfa6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfa6-126">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="4bfa6-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="4bfa6-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="4bfa6-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





