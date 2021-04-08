---
title: IMsRdpClientAdvancedSettings6 hotkeyfocenreleaseleft (Eigenschaft)
description: Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-Links zu bestimmen.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Hotkeyfocupreleaseleft-Eigenschaft Remotedesktopdienste
- Hotkeyfocus releaseleft-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyfocwereleaseleft-Eigenschaft
- Hotkeyfocus releaseleft-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyfocwereleaseleft-Eigenschaft
- Hotkeyfocus releaseleft-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyfocwereleaseleft-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740008"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="1ce31-110">IMsRdpClientAdvancedSettings6:: hotkeyfocaufreleaseleft-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ce31-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="1ce31-111">Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-Links zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1ce31-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="1ce31-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1ce31-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce31-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ce31-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="1ce31-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1ce31-114">Property value</span></span>

<span data-ttu-id="1ce31-115">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="1ce31-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ce31-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ce31-116">Remarks</span></span>

<span data-ttu-id="1ce31-117">Diese Eigenschaft wird nur von Remotedesktopverbindung 6,1-und 7,0-Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ce31-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce31-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ce31-118">Requirements</span></span>



| <span data-ttu-id="1ce31-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ce31-119">Requirement</span></span> | <span data-ttu-id="1ce31-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1ce31-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce31-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ce31-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce31-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ce31-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1ce31-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ce31-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce31-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ce31-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1ce31-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1ce31-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1ce31-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce31-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1ce31-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce31-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ce31-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce31-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1ce31-129">IID</span><span class="sxs-lookup"><span data-stu-id="1ce31-129">IID</span></span><br/>                      | <span data-ttu-id="1ce31-130">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="1ce31-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ce31-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ce31-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce31-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1ce31-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1ce31-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1ce31-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1ce31-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1ce31-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





