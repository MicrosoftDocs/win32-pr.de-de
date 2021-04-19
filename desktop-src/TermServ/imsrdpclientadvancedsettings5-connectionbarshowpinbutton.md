---
title: IMsRdpClientAdvancedSettings5 connectionbarshowpinbutton-Eigenschaft
description: Legt die Konfiguration für die PIN-Schaltfläche in der Verbindungs Leiste fest oder ruft Sie ab.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Connectionbarshowpinbutton-Eigenschaft Remotedesktopdienste
- Connectionbarshowpinbutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, connectionbarshowpinbutton-Eigenschaft
- Connectionbarshowpinbutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, connectionbarshowpinbutton-Eigenschaft
- Connectionbarshowpinbutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, connectionbarshowpinbutton-Eigenschaft
- Connectionbarshowpinbutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, connectionbarshowpinbutton-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341593"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="3687c-112">IMsRdpClientAdvancedSettings5:: connectionbarshowpinbutton-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3687c-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="3687c-113">Legt die Konfiguration für die PIN-Schaltfläche in der Verbindungs Leiste fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="3687c-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="3687c-114">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3687c-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3687c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3687c-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="3687c-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3687c-116">Property value</span></span>

<span data-ttu-id="3687c-117">Der boolesche Wert **true** oder **false**.</span><span class="sxs-lookup"><span data-stu-id="3687c-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="3687c-118">Mit dem Wert **true** wird die PIN-Schaltfläche in der Verbindungs Leiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3687c-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="3687c-119">Mit dem Wert **false** wird die PIN-Schaltfläche in der Verbindungs Leiste ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="3687c-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="3687c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3687c-120">Requirements</span></span>



| <span data-ttu-id="3687c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3687c-121">Requirement</span></span> | <span data-ttu-id="3687c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3687c-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3687c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3687c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3687c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3687c-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="3687c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3687c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3687c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3687c-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="3687c-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3687c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="3687c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3687c-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3687c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3687c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3687c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3687c-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3687c-131">IID</span><span class="sxs-lookup"><span data-stu-id="3687c-131">IID</span></span><br/>                      | <span data-ttu-id="3687c-132">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="3687c-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3687c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3687c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3687c-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3687c-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3687c-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3687c-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3687c-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3687c-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3687c-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3687c-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





