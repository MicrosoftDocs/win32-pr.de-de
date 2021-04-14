---
title: Imsrdptovicecollection devicebyid (Eigenschaft)
description: Ruft das Gerät mit dem angegebenen Bezeichner ab.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Devicebyid-Eigenschaft Remotedesktopdienste
- Devicebyid-Eigenschaft Remotedesktopdienste, imsrdpentvicecollection-Schnittstelle
- Imsrdpentvicecollection-Schnittstelle Remotedesktopdienste, devicebyid-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476449"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="23afb-106">Imsrdptovicecollection::D Eigenschaft "evicebyid"</span><span class="sxs-lookup"><span data-stu-id="23afb-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="23afb-107">Ruft das Gerät mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="23afb-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="23afb-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="23afb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="23afb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="23afb-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="23afb-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="23afb-110">Property value</span></span>

<span data-ttu-id="23afb-111">Ein [**imsrdpdevice**](imsrdpdevice.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="23afb-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23afb-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="23afb-112">Error codes</span></span>

<span data-ttu-id="23afb-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23afb-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="23afb-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="23afb-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="23afb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23afb-115">Requirements</span></span>



| <span data-ttu-id="23afb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23afb-116">Requirement</span></span> | <span data-ttu-id="23afb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="23afb-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="23afb-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23afb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23afb-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23afb-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="23afb-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23afb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23afb-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23afb-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="23afb-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="23afb-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="23afb-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23afb-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="23afb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="23afb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23afb-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23afb-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="23afb-126">IID</span><span class="sxs-lookup"><span data-stu-id="23afb-126">IID</span></span><br/>                      | <span data-ttu-id="23afb-127">IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.</span><span class="sxs-lookup"><span data-stu-id="23afb-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23afb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23afb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23afb-129">**Imsrdpde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="23afb-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





