---
title: Imsrdpdecovicecollection devicecount (Eigenschaft)
description: Ruft die Anzahl der-Objekte in der-Auflistung ab. | Imsrdpdecovicecollection devicecount (Eigenschaft)
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Devicecount-Eigenschaft Remotedesktopdienste
- Devicecount-Eigenschaft Remotedesktopdienste, imsrdpentvicecollection-Schnittstelle
- Imsrdpentvicecollection-Schnittstelle Remotedesktopdienste, devicecount-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354956"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="ecc90-107">Imsrdpenvicecollection::D evicecount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ecc90-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="ecc90-108">Ruft die Anzahl der-Objekte in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="ecc90-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="ecc90-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ecc90-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc90-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecc90-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="ecc90-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ecc90-111">Property value</span></span>

<span data-ttu-id="ecc90-112">Die Objekt Anzahl.</span><span class="sxs-lookup"><span data-stu-id="ecc90-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ecc90-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ecc90-113">Error codes</span></span>

<span data-ttu-id="ecc90-114">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ecc90-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ecc90-115">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ecc90-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc90-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecc90-116">Requirements</span></span>



| <span data-ttu-id="ecc90-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecc90-117">Requirement</span></span> | <span data-ttu-id="ecc90-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ecc90-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc90-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecc90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc90-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecc90-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ecc90-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecc90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc90-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecc90-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ecc90-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ecc90-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ecc90-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc90-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ecc90-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ecc90-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecc90-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc90-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ecc90-127">IID</span><span class="sxs-lookup"><span data-stu-id="ecc90-127">IID</span></span><br/>                      | <span data-ttu-id="ecc90-128">IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.</span><span class="sxs-lookup"><span data-stu-id="ecc90-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecc90-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecc90-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc90-130">**Imsrdpde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="ecc90-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





