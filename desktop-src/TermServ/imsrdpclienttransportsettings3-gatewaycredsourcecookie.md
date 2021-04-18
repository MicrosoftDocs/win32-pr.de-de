---
title: IMsRdpClientTransportSettings3 gatewaykredsourcecookie (Eigenschaft)
description: Gibt an, ob die Anmelde Informationsquelle cookiebasiert ist.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Gatewaykredsourcecookie-Eigenschaft Remotedesktopdienste
- Gatewaykredsourcecookie-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings3-Schnittstelle
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, gatewaykredsourcecookie (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345333"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="f2ca4-106">IMsRdpClientTransportSettings3:: gatewaykredsourcecookie (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f2ca4-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="f2ca4-107">Gibt an, ob die Anmelde Informationsquelle cookiebasiert ist.</span><span class="sxs-lookup"><span data-stu-id="f2ca4-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="f2ca4-108">Enthält eine, wenn die Anmelde Informationsquelle cookiebasiert ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="f2ca4-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="f2ca4-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f2ca4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ca4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2ca4-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="f2ca4-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f2ca4-111">Property value</span></span>

<span data-ttu-id="f2ca4-112">Ein **ulong** -Wert, der angibt, ob die Anmelde Informationsquelle cookiebasiert ist.</span><span class="sxs-lookup"><span data-stu-id="f2ca4-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ca4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2ca4-113">Requirements</span></span>



| <span data-ttu-id="f2ca4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2ca4-114">Requirement</span></span> | <span data-ttu-id="f2ca4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f2ca4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ca4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2ca4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ca4-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2ca4-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="f2ca4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2ca4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ca4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2ca4-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f2ca4-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f2ca4-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2ca4-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2ca4-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2ca4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f2ca4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2ca4-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2ca4-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ca4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2ca4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ca4-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="f2ca4-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





