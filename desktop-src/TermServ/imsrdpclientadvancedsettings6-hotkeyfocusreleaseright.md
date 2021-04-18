---
title: IMsRdpClientAdvancedSettings6 hotkeyfocus releaseright (Eigenschaft)
description: Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-rechts zu bestimmen.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Hotkeyfocwayreleaseright-Eigenschaft Remotedesktopdienste
- Hotkeyfocwayreleaseright-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyfocwereleaseright (Eigenschaft)
- Hotkeyfocwayreleaseright-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyfocwereleaseright (Eigenschaft)
- Hotkeyfocwayreleaseright-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyfocwereleaseright (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344505"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="bd871-110">IMsRdpClientAdvancedSettings6:: hotkeyfocwayreleaseright (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bd871-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="bd871-111">Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-rechts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bd871-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="bd871-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bd871-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd871-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd871-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="bd871-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bd871-114">Property value</span></span>

<span data-ttu-id="bd871-115">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="bd871-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd871-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd871-116">Remarks</span></span>

<span data-ttu-id="bd871-117">Diese Eigenschaft wird nur von Remotedesktopverbindung 6,1-und 7,0-Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd871-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd871-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd871-118">Requirements</span></span>



| <span data-ttu-id="bd871-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd871-119">Requirement</span></span> | <span data-ttu-id="bd871-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bd871-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd871-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd871-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd871-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd871-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bd871-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd871-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd871-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd871-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bd871-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bd871-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd871-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd871-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd871-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bd871-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd871-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd871-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd871-129">IID</span><span class="sxs-lookup"><span data-stu-id="bd871-129">IID</span></span><br/>                      | <span data-ttu-id="bd871-130">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="bd871-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd871-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd871-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd871-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bd871-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bd871-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bd871-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bd871-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bd871-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





