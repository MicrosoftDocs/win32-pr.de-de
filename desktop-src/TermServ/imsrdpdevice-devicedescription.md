---
title: Imsrdpdevice devicedescription (Eigenschaft)
description: Ruft die Geräte Beschreibung ab, die dem Benutzer angezeigt werden soll, wenn der Anzeige Name nicht verfügbar ist.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Devicedescription-Eigenschaft Remotedesktopdienste
- Devicedescription-Eigenschaft Remotedesktopdienste, imsrdpdevice-Schnittstelle
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, devicedescription-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104613"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="cbfa0-106">Imsrdpdevice::D evicedescription-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cbfa0-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="cbfa0-107">Ruft die Geräte Beschreibung ab, die dem Benutzer angezeigt werden soll, wenn der Anzeige Name nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cbfa0-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="cbfa0-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cbfa0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfa0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbfa0-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="cbfa0-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cbfa0-110">Property value</span></span>

<span data-ttu-id="cbfa0-111">Die Geräte Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="cbfa0-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbfa0-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cbfa0-112">Error codes</span></span>

<span data-ttu-id="cbfa0-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbfa0-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="cbfa0-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cbfa0-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfa0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbfa0-115">Requirements</span></span>



| <span data-ttu-id="cbfa0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbfa0-116">Requirement</span></span> | <span data-ttu-id="cbfa0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cbfa0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfa0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbfa0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfa0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbfa0-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cbfa0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbfa0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfa0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbfa0-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cbfa0-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cbfa0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbfa0-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbfa0-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbfa0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cbfa0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbfa0-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbfa0-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbfa0-126">IID</span><span class="sxs-lookup"><span data-stu-id="cbfa0-126">IID</span></span><br/>                      | <span data-ttu-id="cbfa0-127">IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.</span><span class="sxs-lookup"><span data-stu-id="cbfa0-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="cbfa0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbfa0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfa0-129">**Imsrdpdevice**</span><span class="sxs-lookup"><span data-stu-id="cbfa0-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





