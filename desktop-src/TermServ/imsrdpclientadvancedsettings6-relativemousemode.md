---
title: IMsRdpClientAdvancedSettings6 relativemousmode (Eigenschaft)
description: Gibt an, ob die Maus den relativen Modus verwenden soll.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Relativemousmode-Eigenschaft Remotedesktopdienste
- Relativemousmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, relativemousmode (Eigenschaft)
- Relativemousmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, relativemousmode (Eigenschaft)
- Relativemousmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, relativemousmode (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346726"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="7a05c-110">IMsRdpClientAdvancedSettings6:: relativemousmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7a05c-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="7a05c-111">Gibt an, ob die Maus den relativen Modus verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="7a05c-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="7a05c-112">Enthält **Variant \_ true** , wenn sich der Mauszeiger im relativen Modus befindet, oder **Variant \_ false** , wenn sich der Mauszeiger im absoluten Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="7a05c-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="7a05c-113">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7a05c-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a05c-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a05c-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="7a05c-115">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7a05c-115">Property value</span></span>

<span data-ttu-id="7a05c-116">Enthält den neuen Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="7a05c-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a05c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a05c-117">Remarks</span></span>

<span data-ttu-id="7a05c-118">Der Mausmodus gibt an, wie das ActiveX-Steuerelement die Maus Koordinaten berechnet, die es an den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) sendet.</span><span class="sxs-lookup"><span data-stu-id="7a05c-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="7a05c-119">Wenn sich der Mauszeiger im relativen Modus befindet, berechnet das ActiveX-Steuerelement Maus Koordinaten in Bezug auf die letzte Position der Maus.</span><span class="sxs-lookup"><span data-stu-id="7a05c-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="7a05c-120">Wenn sich der Mauszeiger im absoluten Modus befindet, berechnet das ActiveX-Steuerelement die Maus Koordinaten relativ zum Desktop des RD-Sitzungshost Servers.</span><span class="sxs-lookup"><span data-stu-id="7a05c-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a05c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a05c-121">Requirements</span></span>



| <span data-ttu-id="7a05c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a05c-122">Requirement</span></span> | <span data-ttu-id="7a05c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7a05c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a05c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a05c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7a05c-125">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="7a05c-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="7a05c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a05c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7a05c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a05c-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7a05c-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7a05c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a05c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a05c-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7a05c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a05c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a05c-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a05c-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7a05c-132">IID</span><span class="sxs-lookup"><span data-stu-id="7a05c-132">IID</span></span><br/>                      | <span data-ttu-id="7a05c-133">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="7a05c-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a05c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a05c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a05c-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7a05c-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7a05c-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7a05c-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7a05c-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7a05c-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





