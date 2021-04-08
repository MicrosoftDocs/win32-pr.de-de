---
title: IMsRdpClientAdvancedSettings5 redirectclipboard (Eigenschaft)
description: Legt die Konfiguration für die Umleitung der Zwischenablage fest oder ruft Sie ab.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Redirectclipboard-Eigenschaft Remotedesktopdienste
- Redirectclipboard-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, redirectclipboard (Eigenschaft)
- Redirectclipboard-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, redirectclipboard (Eigenschaft)
- Redirectclipboard-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, redirectclipboard (Eigenschaft)
- Redirectclipboard-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, redirectclipboard (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949629"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="a3645-112">IMsRdpClientAdvancedSettings5:: redirectclipboard (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a3645-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="a3645-113">Legt die Konfiguration für die Umleitung der Zwischenablage fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="a3645-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="a3645-114">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a3645-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3645-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3645-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="a3645-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a3645-116">Property value</span></span>

<span data-ttu-id="a3645-117">Legt den Umleitungs Modus für die Zwischenablage auf **true** oder **false** fest.</span><span class="sxs-lookup"><span data-stu-id="a3645-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="a3645-118">Wenn diese Option auf **true** festgelegt ist, ist der Umleitungs Modus der zwischen</span><span class="sxs-lookup"><span data-stu-id="a3645-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3645-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3645-119">Requirements</span></span>



| <span data-ttu-id="a3645-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3645-120">Requirement</span></span> | <span data-ttu-id="a3645-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a3645-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3645-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3645-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a3645-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3645-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a3645-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3645-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a3645-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3645-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a3645-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a3645-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3645-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3645-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a3645-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a3645-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3645-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3645-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a3645-130">IID</span><span class="sxs-lookup"><span data-stu-id="a3645-130">IID</span></span><br/>                      | <span data-ttu-id="a3645-131">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="a3645-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3645-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3645-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3645-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a3645-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a3645-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a3645-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a3645-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a3645-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a3645-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a3645-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





