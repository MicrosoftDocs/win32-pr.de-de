---
title: IMsRdpDeviceV2 isusbdevice (Eigenschaft)
description: Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- Isusbdevice-Eigenschaft Remotedesktopdienste
- Isusbdevice-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste, isusbdevice-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391521"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a><span data-ttu-id="f5390-106">IMsRdpDeviceV2:: isusbdevice-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f5390-106">IMsRdpDeviceV2::IsUSBDevice property</span></span>

<span data-ttu-id="f5390-107">Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f5390-107">Specifies if the device is for USB redirection.</span></span>

<span data-ttu-id="f5390-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f5390-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5390-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5390-109">Syntax</span></span>


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a><span data-ttu-id="f5390-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f5390-110">Property value</span></span>

<span data-ttu-id="f5390-111">**true** , wenn das Gerät für die USB-Umleitung vorgesehen ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f5390-111">**true** if the device is for USB redirection; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5390-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5390-112">Requirements</span></span>



| <span data-ttu-id="f5390-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5390-113">Requirement</span></span> | <span data-ttu-id="f5390-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f5390-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5390-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5390-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f5390-116">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="f5390-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="f5390-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5390-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f5390-118">Windows Server 2008 R2 mit SP1</span><span class="sxs-lookup"><span data-stu-id="f5390-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="f5390-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f5390-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5390-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5390-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5390-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f5390-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5390-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5390-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5390-123">IID</span><span class="sxs-lookup"><span data-stu-id="f5390-123">IID</span></span><br/>                      | <span data-ttu-id="f5390-124">IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.</span><span class="sxs-lookup"><span data-stu-id="f5390-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="f5390-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5390-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5390-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="f5390-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





