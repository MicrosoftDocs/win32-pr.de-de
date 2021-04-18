---
title: IMsRdpDeviceV2 cmdeaktiviert (Eigenschaft)
description: Enthält die Configuration Manager-Geräte Instanz des Geräts.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Cmdebug-Eigenschaft Remotedesktopdienste
- Cmdebug-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2 Interface Remotedesktopdienste, cmdebug-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339311"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="83b1a-106">IMsRdpDeviceV2:: cmdebug-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83b1a-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="83b1a-107">Enthält die Configuration Manager-Geräte Instanz des Geräts.</span><span class="sxs-lookup"><span data-stu-id="83b1a-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="83b1a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83b1a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b1a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="83b1a-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="83b1a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="83b1a-110">Property value</span></span>

<span data-ttu-id="83b1a-111">Die Configuration Manager-Geräte Instanz des Geräts.</span><span class="sxs-lookup"><span data-stu-id="83b1a-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b1a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83b1a-112">Requirements</span></span>



| <span data-ttu-id="83b1a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83b1a-113">Requirement</span></span> | <span data-ttu-id="83b1a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="83b1a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83b1a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83b1a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="83b1a-116">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="83b1a-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="83b1a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83b1a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="83b1a-118">Windows Server 2008 R2 mit SP1</span><span class="sxs-lookup"><span data-stu-id="83b1a-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="83b1a-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="83b1a-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="83b1a-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83b1a-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="83b1a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="83b1a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83b1a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83b1a-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="83b1a-123">IID</span><span class="sxs-lookup"><span data-stu-id="83b1a-123">IID</span></span><br/>                      | <span data-ttu-id="83b1a-124">IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.</span><span class="sxs-lookup"><span data-stu-id="83b1a-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="83b1a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83b1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b1a-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="83b1a-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





