---
title: IMsRdpClient9 TransportSettings4-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientTransportSettings4-Schnittstelle unterstützt.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- TransportSettings4-Eigenschaft Remotedesktopdienste
- TransportSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings4-Eigenschaft
- TransportSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings4-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340378"
---
# <a name="imsrdpclient9transportsettings4-property"></a><span data-ttu-id="5491f-108">IMsRdpClient9:: TransportSettings4-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5491f-108">IMsRdpClient9::TransportSettings4 property</span></span>

<span data-ttu-id="5491f-109">Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5491f-109">Retrieves an object that supports the [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface.</span></span>

<span data-ttu-id="5491f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5491f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5491f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5491f-111">Syntax</span></span>


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a><span data-ttu-id="5491f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5491f-112">Property value</span></span>

<span data-ttu-id="5491f-113">Gibt einen [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="5491f-113">Returns an [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5491f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5491f-114">Requirements</span></span>



| <span data-ttu-id="5491f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5491f-115">Requirement</span></span> | <span data-ttu-id="5491f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5491f-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5491f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5491f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5491f-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5491f-118">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5491f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5491f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5491f-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5491f-120">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="5491f-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5491f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5491f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5491f-122"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="5491f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5491f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5491f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5491f-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="5491f-125">IID</span><span class="sxs-lookup"><span data-stu-id="5491f-125">IID</span></span><br/>                      | <span data-ttu-id="5491f-126">CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert</span><span class="sxs-lookup"><span data-stu-id="5491f-126">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="5491f-127">CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.</span><span class="sxs-lookup"><span data-stu-id="5491f-127">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="5491f-128">IID \_ IMsRdpClient9 ist als 28904001-04b6-436C-a55b-0af1a0883dc9 definiert.</span><span class="sxs-lookup"><span data-stu-id="5491f-128">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5491f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5491f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5491f-130">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5491f-130">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5491f-131">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="5491f-131">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





