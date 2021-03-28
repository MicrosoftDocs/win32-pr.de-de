---
description: Stellt Optionen dar, die beim Anzeigen eines Popup Menüs verfügbar sind.
title: MP_POPUPFLAGS Konstanten (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130084"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="3ca5f-103">MP- \_ popupflags-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3ca5f-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="3ca5f-104">Stellt Optionen dar, die beim Anzeigen eines Popup Menüs verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="3ca5f-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="3ca5f-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="3ca5f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ca5f-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="3ca5f-107"><dt>**Mppf \_ SetFocus**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="3ca5f-108">Legen Sie dem Popupmenü den Fokus.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="3ca5f-109"><dt>**Mppf \_ Initialselect**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="3ca5f-110">Wählen Sie das erste Element im Popup Menü aus.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="3ca5f-111"><dt>**Mppf \_ Noanimieren**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="3ca5f-112">Verwenden Sie beim Anzeigen des Menüs nicht die Standard systemanimationen, z. b. "ausblenden".</span><span class="sxs-lookup"><span data-stu-id="3ca5f-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="3ca5f-113"><dt>**Mppf \_ Tastatur**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="3ca5f-114">Aktivieren Sie das Menü mit einer Tastenkombination.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="3ca5f-115"><dt>**Mppf \_ Neupositionieren**</dt> von <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="3ca5f-116">Zeigt die Leiste auf der Grundlage von Änderungen am Menü an einer anderen Position an.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="3ca5f-117"><dt>**Mppf \_ Forcezorder**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="3ca5f-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-118">Reserved.</span></span> <span data-ttu-id="3ca5f-119">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="3ca5f-120"><dt>**Mppf \_ Finalselect**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="3ca5f-121">Wählen Sie das letzte Element im Menü aus.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="3ca5f-122"><dt>**Mppf \_ \_Left**</dt> <dt>0x02000000</dt> ausrichten</span><span class="sxs-lookup"><span data-stu-id="3ca5f-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="3ca5f-123">**Windows Vista oder** höher: richten Sie das Popup Menü links neben dem Bereich ein, der im *prcexclude* -Parameter von [**itrackshellmenu angegeben ist::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**imenupopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="3ca5f-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="3ca5f-124">Dies ist die Standardausrichtung.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="3ca5f-125"><dt>**Mppf \_ \_Rechts**</dt> bündig ausrichten <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="3ca5f-126">**Windows Vista oder** höher: richten Sie das Popup Menü rechts neben dem im *prcexclude* -Parameter von [**itrackshellmenu angegebenen Bereich ein::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**imenupopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="3ca5f-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="3ca5f-127"><dt>**Mppf \_ Top**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="3ca5f-128">Positionieren Sie das Popup Menü oberhalb des Anfangs Punkts, der im *PPT* -Parameter von [**itrackshellmenu angegeben ist::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) oder [**imenupopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="3ca5f-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="3ca5f-129"><dt>**Mppf \_ Left**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="3ca5f-130">Positionieren Sie das Popup Menü auf der linken Seite des Anfangs Punkts.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="3ca5f-131"><dt>**Mppf \_ Right**</dt> <dt>0x60000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="3ca5f-132">Positionieren Sie das Popup Menü rechts neben dem Anfangspunkt.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="3ca5f-133"><dt>**Mppf \_ Bottom**</dt> <dt>(int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="3ca5f-134">Positionieren Sie das Popup Menü unterhalb des Anfangs Punkts.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="3ca5f-135"><dt>**Mppf \_ POS \_ Mask**</dt> <dt>(int) 0xE0000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="3ca5f-136">Die Menü Positions Maske.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="3ca5f-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ca5f-137">Remarks</span></span>

<span data-ttu-id="3ca5f-138">Diese Konstanten werden in der Datei "shobjidl. h" ab Windows XP Service Pack 1 (SP1) und Windows Server 2003 definiert.</span><span class="sxs-lookup"><span data-stu-id="3ca5f-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca5f-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3ca5f-139">Requirements</span></span>



| <span data-ttu-id="3ca5f-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ca5f-140">Requirement</span></span> | <span data-ttu-id="3ca5f-141">Wert</span><span class="sxs-lookup"><span data-stu-id="3ca5f-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca5f-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ca5f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca5f-143">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ca5f-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ca5f-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ca5f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca5f-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ca5f-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ca5f-146">Header</span><span class="sxs-lookup"><span data-stu-id="3ca5f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca5f-147"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ca5f-148">IDL</span><span class="sxs-lookup"><span data-stu-id="3ca5f-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ca5f-149"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5f-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca5f-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3ca5f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca5f-151">**Imeinupopup::P-opup**</span><span class="sxs-lookup"><span data-stu-id="3ca5f-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="3ca5f-152">**Itrackshellmenu::P-opup**</span><span class="sxs-lookup"><span data-stu-id="3ca5f-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




