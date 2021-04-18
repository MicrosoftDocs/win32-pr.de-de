---
title: Imsrdpdevicecollection-Methode "rescandevices"
description: Aktualisiert die Liste der-Objekte in der Auflistung. | Imsrdpdevicecollection-Methode "rescandevices"
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Methode zum erneuten Hinzufügen der Geräte Remotedesktopdienste
- Methode "rescandevices" Remotedesktopdienste "imsrdpdevicecollection"-Schnittstelle
- Imsrdpdevicecollection-Schnittstelle Remotedesktopdienste, Methode zum erneuten konvertieren
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354326"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="3e531-107">Imsrdpdevicecollection:: rescandevices-Methode</span><span class="sxs-lookup"><span data-stu-id="3e531-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="3e531-108">Aktualisiert die Liste der-Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3e531-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e531-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e531-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="3e531-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e531-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e531-111">*vbooldynredir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e531-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e531-112">Der Standard Umleitungs Status, der auf alle neu ermittelten Geräte oder Laufwerke angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e531-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e531-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e531-113">Return value</span></span>

<span data-ttu-id="3e531-114">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e531-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="3e531-115">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3e531-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e531-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e531-116">Requirements</span></span>



| <span data-ttu-id="3e531-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e531-117">Requirement</span></span> | <span data-ttu-id="3e531-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3e531-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e531-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e531-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e531-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e531-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="3e531-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e531-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e531-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e531-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3e531-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3e531-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e531-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e531-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="3e531-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e531-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e531-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e531-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="3e531-127">IID</span><span class="sxs-lookup"><span data-stu-id="3e531-127">IID</span></span><br/>                      | <span data-ttu-id="3e531-128">IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.</span><span class="sxs-lookup"><span data-stu-id="3e531-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e531-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e531-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e531-130">**Imsrdpde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="3e531-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





