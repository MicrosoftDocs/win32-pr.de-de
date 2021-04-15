---
title: Imsrdpentvicecollection devicebyindex (Eigenschaft)
description: Ruft das Gerät am angegebenen Index ab.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Devicebyindex-Eigenschaft Remotedesktopdienste
- Devicebyindex-Eigenschaft Remotedesktopdienste, imsrdpentvicecollection-Schnittstelle
- Imsrdpentvicecollection-Schnittstelle Remotedesktopdienste, devicebyindex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479281"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a><span data-ttu-id="a91ad-106">Imsrdpentvicecollection::D Eigenschaft "evicebyindex"</span><span class="sxs-lookup"><span data-stu-id="a91ad-106">IMsRdpDeviceCollection::DeviceByIndex property</span></span>

<span data-ttu-id="a91ad-107">Ruft das Gerät am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="a91ad-107">Retrieves the device at the specified index.</span></span>

<span data-ttu-id="a91ad-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a91ad-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91ad-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a91ad-109">Syntax</span></span>


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="a91ad-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a91ad-110">Property value</span></span>

<span data-ttu-id="a91ad-111">Ein [**imsrdpdevice**](imsrdpdevice.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a91ad-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a91ad-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a91ad-112">Error codes</span></span>

<span data-ttu-id="a91ad-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a91ad-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="a91ad-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a91ad-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a91ad-115">Requirements</span></span>



| <span data-ttu-id="a91ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a91ad-116">Requirement</span></span> | <span data-ttu-id="a91ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a91ad-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a91ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a91ad-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a91ad-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="a91ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a91ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a91ad-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a91ad-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a91ad-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a91ad-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="a91ad-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a91ad-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a91ad-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a91ad-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a91ad-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a91ad-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a91ad-126">IID</span><span class="sxs-lookup"><span data-stu-id="a91ad-126">IID</span></span><br/>                      | <span data-ttu-id="a91ad-127">IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.</span><span class="sxs-lookup"><span data-stu-id="a91ad-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a91ad-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a91ad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91ad-129">**Imsrdpde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="a91ad-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





