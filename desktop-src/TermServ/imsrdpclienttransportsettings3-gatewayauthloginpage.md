---
title: IMsRdpClientTransportSettings3 gatewayauthloginpage (Eigenschaft)
description: Die Adresse der Anmelde Webseite, die zum Authentifizieren eines Benutzers verwendet werden soll.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Gatewayauthloginpage-Eigenschaft Remotedesktopdienste
- Gatewayauthloginpage-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, gatewayauthloginpage (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106089"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="ac437-106">IMsRdpClientTransportSettings3:: gatewayauthloginpage (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ac437-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="ac437-107">Die Adresse der Anmelde Webseite, die zum Authentifizieren eines Benutzers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac437-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="ac437-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ac437-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac437-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac437-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="ac437-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ac437-110">Property value</span></span>

<span data-ttu-id="ac437-111">Die Adresse der neuen Anmelde Webseite.</span><span class="sxs-lookup"><span data-stu-id="ac437-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac437-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac437-112">Requirements</span></span>



| <span data-ttu-id="ac437-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac437-113">Requirement</span></span> | <span data-ttu-id="ac437-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ac437-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac437-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac437-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ac437-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac437-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="ac437-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac437-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ac437-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac437-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ac437-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ac437-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ac437-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ac437-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ac437-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac437-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac437-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac437-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac437-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="ac437-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





