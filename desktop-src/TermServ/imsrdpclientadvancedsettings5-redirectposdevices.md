---
title: IMsRdpClientAdvancedSettings5 redirectposdevices (Eigenschaft)
description: Legt die Konfiguration für eine Point-of-Service-Geräte Umleitung fest oder ruft Sie ab.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- Redirectposdevices-Eigenschaft Remotedesktopdienste
- Redirectposdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, Eigenschaft redirectposdevices
- Redirectposdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, Eigenschaft redirectposdevices
- Redirectposdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, Eigenschaft redirectposdevices
- Redirectposdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, Eigenschaft redirectposdevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104625"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="c09b3-112">IMsRdpClientAdvancedSettings5:: redirectposdevices (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c09b3-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="c09b3-113">Legt die Konfiguration für eine Point-of-Service-Geräte Umleitung fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="c09b3-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="c09b3-114">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c09b3-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09b3-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c09b3-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="c09b3-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c09b3-116">Property value</span></span>

<span data-ttu-id="c09b3-117">Legt den Point of Service-Geräte Umleitungs Modus auf **true** oder **false** fest.</span><span class="sxs-lookup"><span data-stu-id="c09b3-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="c09b3-118">Wenn der Wert auf **true** festgelegt ist, wird der Geräte Umleitungs Modus für den Dienst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c09b3-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="c09b3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c09b3-119">Requirements</span></span>



| <span data-ttu-id="c09b3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c09b3-120">Requirement</span></span> | <span data-ttu-id="c09b3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c09b3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c09b3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c09b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c09b3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c09b3-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c09b3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c09b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c09b3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c09b3-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c09b3-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c09b3-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="c09b3-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c09b3-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c09b3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c09b3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c09b3-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c09b3-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c09b3-130">IID</span><span class="sxs-lookup"><span data-stu-id="c09b3-130">IID</span></span><br/>                      | <span data-ttu-id="c09b3-131">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="c09b3-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c09b3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c09b3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09b3-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c09b3-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c09b3-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c09b3-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c09b3-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c09b3-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c09b3-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c09b3-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





