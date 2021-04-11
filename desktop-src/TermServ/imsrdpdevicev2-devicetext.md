---
title: IMsRdpDeviceV2 devicetext-Eigenschaft
description: Enthält den Geräte Text.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Devicetext-Eigenschaft Remotedesktopdienste
- Devicetext-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2 Interface Remotedesktopdienste, devicetext-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213706"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="d4b05-106">IMsRdpDeviceV2::D der Eigenschaft "evicetext"</span><span class="sxs-lookup"><span data-stu-id="d4b05-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="d4b05-107">Enthält den Geräte Text.</span><span class="sxs-lookup"><span data-stu-id="d4b05-107">Contains the device text.</span></span> <span data-ttu-id="d4b05-108">Dies ist der Name, den Windows dem Benutzer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d4b05-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="d4b05-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4b05-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b05-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4b05-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="d4b05-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d4b05-111">Property value</span></span>

<span data-ttu-id="d4b05-112">Der Anzeigename für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="d4b05-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b05-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4b05-113">Requirements</span></span>



| <span data-ttu-id="d4b05-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4b05-114">Requirement</span></span> | <span data-ttu-id="d4b05-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d4b05-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b05-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4b05-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b05-117">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="d4b05-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="d4b05-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4b05-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b05-119">Windows Server 2008 R2 mit SP1</span><span class="sxs-lookup"><span data-stu-id="d4b05-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="d4b05-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d4b05-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4b05-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b05-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4b05-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d4b05-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4b05-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b05-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4b05-124">IID</span><span class="sxs-lookup"><span data-stu-id="d4b05-124">IID</span></span><br/>                      | <span data-ttu-id="d4b05-125">IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.</span><span class="sxs-lookup"><span data-stu-id="d4b05-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d4b05-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4b05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b05-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="d4b05-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





