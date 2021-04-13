---
title: IMsRdpClientTransportSettings3 gatewayverschlüsseltedauthcookie (Eigenschaft)
description: Das verschlüsselte Authentifizierungs Cookie.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Gatewayverschlüsseltedauthcookie-Eigenschaft Remotedesktopdienste
- Gatewayverschlüsseltedauthcookie-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, gatewayverschlüsseltedauthcookie (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340687"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="ce91c-106">IMsRdpClientTransportSettings3:: gatewayverschlüsseltedauthcookie (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce91c-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="ce91c-107">Das verschlüsselte Authentifizierungs Cookie.</span><span class="sxs-lookup"><span data-stu-id="ce91c-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="ce91c-108">Die Größe der Eigenschaft wird durch die [**gatewayverschlüsseltedauthcookiesize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce91c-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="ce91c-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ce91c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce91c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce91c-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="ce91c-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ce91c-111">Property value</span></span>

<span data-ttu-id="ce91c-112">Das neue verschlüsselte Authentifizierungs Cookie.</span><span class="sxs-lookup"><span data-stu-id="ce91c-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce91c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce91c-113">Requirements</span></span>



| <span data-ttu-id="ce91c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce91c-114">Requirement</span></span> | <span data-ttu-id="ce91c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ce91c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce91c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce91c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce91c-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce91c-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="ce91c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce91c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce91c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce91c-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ce91c-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ce91c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce91c-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce91c-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ce91c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ce91c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce91c-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce91c-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce91c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce91c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce91c-125">**Gatewayverschlüsseltedauthcookiesize**</span><span class="sxs-lookup"><span data-stu-id="ce91c-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="ce91c-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="ce91c-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





