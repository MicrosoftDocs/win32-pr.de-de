---
title: IMsRdpClientTransportSettings3 gatewayauthcookieserveraddr (Eigenschaft)
description: Die Server Adresse für die cookiebasierte Authentifizierung.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Gatewayauthcookieserveraddr-Eigenschaft Remotedesktopdienste
- Gatewayauthcookieserveraddr-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, gatewayauthcookieserveraddr (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479041"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="629f5-106">IMsRdpClientTransportSettings3:: gatewayauthcookieserveraddr (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="629f5-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="629f5-107">Die Server Adresse für die cookiebasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="629f5-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="629f5-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="629f5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="629f5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="629f5-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="629f5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="629f5-110">Property value</span></span>

<span data-ttu-id="629f5-111">Die neue Server Adresse für die cookiebasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="629f5-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="629f5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="629f5-112">Requirements</span></span>



| <span data-ttu-id="629f5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="629f5-113">Requirement</span></span> | <span data-ttu-id="629f5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="629f5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="629f5-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="629f5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="629f5-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="629f5-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="629f5-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="629f5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="629f5-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="629f5-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="629f5-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="629f5-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="629f5-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="629f5-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="629f5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="629f5-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="629f5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="629f5-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629f5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="629f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629f5-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="629f5-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





