---
title: IMsRdpClientAdvancedSettings5 publicmode (Eigenschaft)
description: Legt die Konfiguration für den öffentlichen Modus fest oder ruft Sie ab. Der öffentliche Modus verhindert, dass der Client Benutzerdaten auf dem lokalen System zwischenspeichert.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Publicmode-Eigenschaft Remotedesktopdienste
- Publicmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, publicmode (Eigenschaft)
- Publicmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, publicmode (Eigenschaft)
- Publicmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, publicmode (Eigenschaft)
- Publicmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, publicmode (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337917"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="3fb4d-113">IMsRdpClientAdvancedSettings5::P ublicmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3fb4d-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="3fb4d-114">Legt die Konfiguration für den öffentlichen Modus fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="3fb4d-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="3fb4d-115">Der öffentliche Modus verhindert, dass der Client Benutzerdaten auf dem lokalen System zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="3fb4d-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="3fb4d-116">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3fb4d-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb4d-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fb4d-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="3fb4d-118">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3fb4d-118">Property value</span></span>

<span data-ttu-id="3fb4d-119">Legt die Einstellung für den öffentlichen Modus auf **Variant \_ true** oder **Variant \_ false** fest.</span><span class="sxs-lookup"><span data-stu-id="3fb4d-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="3fb4d-120">Wenn der Wert auf **Variant \_ true** festgelegt ist, wird die Einstellung öffentlicher Modus aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3fb4d-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb4d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fb4d-121">Requirements</span></span>



| <span data-ttu-id="3fb4d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fb4d-122">Requirement</span></span> | <span data-ttu-id="3fb4d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3fb4d-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb4d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fb4d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb4d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fb4d-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="3fb4d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fb4d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb4d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fb4d-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="3fb4d-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3fb4d-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="3fb4d-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fb4d-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3fb4d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3fb4d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb4d-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fb4d-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3fb4d-132">IID</span><span class="sxs-lookup"><span data-stu-id="3fb4d-132">IID</span></span><br/>                      | <span data-ttu-id="3fb4d-133">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="3fb4d-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fb4d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fb4d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb4d-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3fb4d-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3fb4d-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3fb4d-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3fb4d-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3fb4d-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3fb4d-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3fb4d-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





