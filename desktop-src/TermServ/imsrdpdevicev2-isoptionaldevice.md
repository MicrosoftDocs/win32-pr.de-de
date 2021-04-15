---
title: IMsRdpDeviceV2 isoptionaldevice (Eigenschaft)
description: Gibt an, ob das Gerät für die USB-Umleitung optional ist.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Isoptionaldevice-Eigenschaft Remotedesktopdienste
- Isoptionaldevice-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2 Interface Remotedesktopdienste, isoptionaldevice-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477742"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="6949b-106">IMsRdpDeviceV2:: isoptionaldevice-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6949b-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="6949b-107">Gibt an, ob das Gerät für die USB-Umleitung optional ist.</span><span class="sxs-lookup"><span data-stu-id="6949b-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="6949b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6949b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6949b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6949b-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="6949b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6949b-110">Property value</span></span>

<span data-ttu-id="6949b-111">**true** , wenn das Gerät optional ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6949b-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6949b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6949b-112">Requirements</span></span>



| <span data-ttu-id="6949b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6949b-113">Requirement</span></span> | <span data-ttu-id="6949b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6949b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6949b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6949b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6949b-116">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="6949b-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="6949b-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6949b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6949b-118">Windows Server 2008 R2 mit SP1</span><span class="sxs-lookup"><span data-stu-id="6949b-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="6949b-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6949b-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="6949b-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6949b-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6949b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6949b-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6949b-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6949b-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6949b-123">IID</span><span class="sxs-lookup"><span data-stu-id="6949b-123">IID</span></span><br/>                      | <span data-ttu-id="6949b-124">IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.</span><span class="sxs-lookup"><span data-stu-id="6949b-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="6949b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6949b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6949b-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="6949b-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





