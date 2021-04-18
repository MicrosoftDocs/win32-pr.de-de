---
title: IMsRdpClientAdvancedSettings5 redirectdevices (Eigenschaft)
description: Legt die Konfiguration für die Geräte Umleitung fest oder ruft Sie ab.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- Redirectdevices-Eigenschaft Remotedesktopdienste
- Redirectdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, redirectdevices (Eigenschaft)
- Redirectdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, redirectdevices (Eigenschaft)
- Redirectdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, redirectdevices (Eigenschaft)
- Redirectdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, redirectdevices (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341372"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="83df9-112">IMsRdpClientAdvancedSettings5:: redirectdevices (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="83df9-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="83df9-113">Legt die Konfiguration für die Geräte Umleitung fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="83df9-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="83df9-114">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="83df9-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="83df9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="83df9-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="83df9-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="83df9-116">Property value</span></span>

<span data-ttu-id="83df9-117">Legt den Geräte Umleitungs Modus auf **true** oder **false** fest.</span><span class="sxs-lookup"><span data-stu-id="83df9-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="83df9-118">Wenn dieser Wert auf **true** festgelegt ist, ist der Geräte Umleitungs Modus aktiviert</span><span class="sxs-lookup"><span data-stu-id="83df9-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="83df9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83df9-119">Requirements</span></span>



| <span data-ttu-id="83df9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83df9-120">Requirement</span></span> | <span data-ttu-id="83df9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="83df9-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83df9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83df9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="83df9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83df9-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="83df9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83df9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="83df9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83df9-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="83df9-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="83df9-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="83df9-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83df9-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="83df9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="83df9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83df9-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83df9-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="83df9-130">IID</span><span class="sxs-lookup"><span data-stu-id="83df9-130">IID</span></span><br/>                      | <span data-ttu-id="83df9-131">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="83df9-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83df9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83df9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83df9-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="83df9-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="83df9-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="83df9-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="83df9-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="83df9-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="83df9-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="83df9-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





