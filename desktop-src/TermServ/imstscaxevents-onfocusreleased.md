---
title: Imstscaxevents onfocus Released-Methode
description: Wird aufgerufen, wenn die Tastenkombination für den releasefokus gedrückt wird. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste drückt.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Onfocus Released-Methode Remotedesktopdienste
- Onfocus Released-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onfocus Released-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337938"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="5227e-107">Imstscaxevents:: onfocus Released-Methode</span><span class="sxs-lookup"><span data-stu-id="5227e-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="5227e-108">Wird aufgerufen, wenn die Tastenkombination für den releasefokus gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="5227e-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="5227e-109">Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="5227e-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="5227e-110">Dieses Ereignis ermöglicht dem ActiveX-Steuerelement Container, die Steuerung des ActiveX-Steuer Elements zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5227e-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="5227e-111">Dies ist beispielsweise in einem Szenario hilfreich, in dem Sie keine Maus haben und spezielle Tastenkombinationen wie Alt + Tab an den Server umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5227e-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="5227e-112">In diesem Fall haben Sie keine Möglichkeit, den Tastaturfokus zurück zum lokalen Desktop zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5227e-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="5227e-113">Mit der Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste kann der ActiveX-Container jedoch auf dieses Ereignis lauschen und reagieren, indem der Fokus vom ActiveX-Steuerelement entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5227e-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="5227e-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="5227e-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="5227e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5227e-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5227e-116">*idirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5227e-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5227e-117">Der Richtungs Parameter 1 (STRG + ALT + nach-rechts-Taste) oder 1 (STRG + ALT + nach-links-Taste).</span><span class="sxs-lookup"><span data-stu-id="5227e-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5227e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5227e-118">Return value</span></span>

<span data-ttu-id="5227e-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5227e-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5227e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5227e-120">Remarks</span></span>

<span data-ttu-id="5227e-121">Dieses Ereignis ist verfügbar, wenn Remotedesktopverbindung 6,0 auf dem Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5227e-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="5227e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5227e-122">Requirements</span></span>



| <span data-ttu-id="5227e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5227e-123">Requirement</span></span> | <span data-ttu-id="5227e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5227e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5227e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5227e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5227e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5227e-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5227e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5227e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5227e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5227e-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5227e-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5227e-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="5227e-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5227e-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5227e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5227e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5227e-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5227e-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5227e-133">IID</span><span class="sxs-lookup"><span data-stu-id="5227e-133">IID</span></span><br/>                      | <span data-ttu-id="5227e-134">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="5227e-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5227e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5227e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5227e-136">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="5227e-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





