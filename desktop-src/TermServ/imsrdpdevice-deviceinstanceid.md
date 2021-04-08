---
title: Imsrdpdevice-Eigenschaft "tviceinstanceid"
description: Ruft den geräteinstanzbezeichner des Geräts ab.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Eigenschaften von "tviceingestanceid" Remotedesktopdienste
- Eigenschaften von "tviceinstanceid" Remotedesktopdienste, imsrdpdevice-Schnittstelle
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, Eigenschaft "de viceinstanceid"
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957223"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a><span data-ttu-id="97f1f-106">Imsrdpdevice::D eviceinstanceid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="97f1f-106">IMsRdpDevice::DeviceInstanceId property</span></span>

<span data-ttu-id="97f1f-107">Ruft den geräteinstanzbezeichner des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="97f1f-107">Retrieves the device instance identifier of the device.</span></span>

<span data-ttu-id="97f1f-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="97f1f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f1f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="97f1f-109">Syntax</span></span>


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a><span data-ttu-id="97f1f-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="97f1f-110">Property value</span></span>

<span data-ttu-id="97f1f-111">Der Bezeichner der Geräte Instanz.</span><span class="sxs-lookup"><span data-stu-id="97f1f-111">The device instance identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97f1f-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="97f1f-112">Error codes</span></span>

<span data-ttu-id="97f1f-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97f1f-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="97f1f-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="97f1f-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f1f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97f1f-115">Requirements</span></span>



| <span data-ttu-id="97f1f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97f1f-116">Requirement</span></span> | <span data-ttu-id="97f1f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="97f1f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97f1f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97f1f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97f1f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97f1f-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="97f1f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97f1f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97f1f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97f1f-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="97f1f-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="97f1f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="97f1f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97f1f-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="97f1f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="97f1f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97f1f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97f1f-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="97f1f-126">IID</span><span class="sxs-lookup"><span data-stu-id="97f1f-126">IID</span></span><br/>                      | <span data-ttu-id="97f1f-127">IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.</span><span class="sxs-lookup"><span data-stu-id="97f1f-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="97f1f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97f1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f1f-129">**Imsrdpdevice**</span><span class="sxs-lookup"><span data-stu-id="97f1f-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





