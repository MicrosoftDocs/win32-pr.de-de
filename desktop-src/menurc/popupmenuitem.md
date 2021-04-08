---
title: Popupmenuitem-Struktur
description: Enthält Informationen zu den Menü Elementen in einer Menü Ressource, mit der ein Menü oder ein Untermenü geöffnet wird. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Popupmenuitem-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949552"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="3c309-105">Popupmenuitem-Struktur</span><span class="sxs-lookup"><span data-stu-id="3c309-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="3c309-106">Enthält Informationen zu den Menü Elementen in einer Menü Ressource, mit der ein Menü oder ein Untermenü geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3c309-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="3c309-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3c309-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c309-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c309-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="3c309-109">Member</span><span class="sxs-lookup"><span data-stu-id="3c309-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c309-110">**type**</span><span class="sxs-lookup"><span data-stu-id="3c309-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="3c309-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3c309-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3c309-112">Beschreibt das Menü Element.</span><span class="sxs-lookup"><span data-stu-id="3c309-112">Describes the menu item.</span></span> <span data-ttu-id="3c309-113">Einige der Werte, die dieser Member enthalten kann, sind die in der folgenden Liste aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="3c309-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="3c309-114">Zusätzlich zu den angezeigten Werten kann dieser Member auch eine Kombination der Typwerte sein, die mit dem **ftype** -Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3c309-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="3c309-115">Die Typwerte sind diejenigen, die mit MFT beginnen \_ .</span><span class="sxs-lookup"><span data-stu-id="3c309-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="3c309-116">Um diese vordefinierten MFT- \_ \* Typwerte zu verwenden, fügen Sie die folgende Anweisung in die RC-Datei ein:</span><span class="sxs-lookup"><span data-stu-id="3c309-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="3c309-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3c309-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="3c309-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3c309-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="3c309-119"><dt>**MF \_ Ende**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="3c309-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="3c309-120">Das Menü Element ist das letzte im Menü. das-Flag wird intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c309-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="3c309-121"><dt>**MF \_ Popup**</dt> - <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3c309-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="3c309-122">Das Menü Element öffnet ein Menü oder ein Untermenü. das-Flag wird intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c309-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="3c309-123">**state**</span><span class="sxs-lookup"><span data-stu-id="3c309-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="3c309-124">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3c309-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3c309-125">Beschreibt das Menü Element.</span><span class="sxs-lookup"><span data-stu-id="3c309-125">Describes the menu item.</span></span> <span data-ttu-id="3c309-126">Dieser Member kann eine Kombination der Zustands Werte sein, die mit dem **dwstate** -Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="3c309-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="3c309-127">Die Statuswerte sind diejenigen, die mit MFS beginnen \_ .</span><span class="sxs-lookup"><span data-stu-id="3c309-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="3c309-128">Um diese vordefinierten MFS- \_ \* Zustands Werte zu verwenden, fügen Sie die folgende Anweisung in die RC-Datei ein:</span><span class="sxs-lookup"><span data-stu-id="3c309-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="3c309-129">**id**</span><span class="sxs-lookup"><span data-stu-id="3c309-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="3c309-130">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3c309-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3c309-131">Ein numerischer Ausdruck, der das Menü Element identifiziert, das in der [**WM- \_ Befehls**](wm-command.md) Meldung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3c309-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="3c309-132">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="3c309-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3c309-133">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="3c309-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3c309-134">Ein Satz von Bitflags, die den Typ des Menü Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="3c309-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="3c309-135">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3c309-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="3c309-136">Wert</span><span class="sxs-lookup"><span data-stu-id="3c309-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="3c309-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3c309-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="3c309-138"><dt>**MFR \_ Ende**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="3c309-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="3c309-139">Das Menü Element ist das letzte in diesem Untermenü oder in der Menü Ressource. Dieses Flag wird intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c309-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="3c309-140"><dt>**MFR \_ Popup**</dt> - <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3c309-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="3c309-141">Das Menü Element öffnet ein Menü oder ein Untermenü. das-Flag wird intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c309-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="3c309-142">**MenuText**</span><span class="sxs-lookup"><span data-stu-id="3c309-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="3c309-143">Typ: **szorord**</span><span class="sxs-lookup"><span data-stu-id="3c309-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="3c309-144">Eine NULL-terminierte Unicode-Zeichenfolge, die den Text für dieses Menü Element enthält.</span><span class="sxs-lookup"><span data-stu-id="3c309-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="3c309-145">Es gibt keine Beschränkung für die Größe dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3c309-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c309-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c309-146">Remarks</span></span>

<span data-ttu-id="3c309-147">Es gibt eine **popupmenuitem** -Struktur für jedes Menü Element, das ein Menü oder ein Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="3c309-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="3c309-148">Identifizieren Sie diesen Typ von Menü Element durch Festlegen des **Typmembers** auf das **MF- \_ Popup** und durch Festlegen des **MFR- \_ Popup** Bits im **ResInfo** -Member auf 0x0001.</span><span class="sxs-lookup"><span data-stu-id="3c309-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="3c309-149">In diesem Fall handelt es sich bei den letzten Daten, die in die [**RT- \_ Menü**](/windows/desktop/menurc/resource-types) Ressource für das Menü oder Untermenü geschrieben werden, um die [**menuhelpid**](menuhelpid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3c309-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="3c309-150">**Menuhelpid** enthält einen numerischen Ausdruck, der das Menü während der [**WM- \_ Hilfe**](../shell/wm-help.md) Verarbeitung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3c309-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="3c309-151">Außerdem folgt jede **popupmenuitem** -Struktur, der das **MFR- \_ Popup** -Bit im **ResInfo** -Member festgelegt ist, eine [**menuhelpid**](menuhelpid.md) -Struktur plus eine zusätzliche Anzahl von **popupmenuitem** -Strukturen, eine für jedes Menü Element in diesem Untermenü.</span><span class="sxs-lookup"><span data-stu-id="3c309-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="3c309-152">In der letzten **popupmenuitem** -Struktur im Untermenü wird das **MFR- \_ Endbit** im **ResInfo** -Member festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3c309-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="3c309-153">Um das Ende der Ressource zu ermitteln, suchen Sie nach einem passenden **MFR- \_ Ende** für jedes **MFR- \_ Popup** plus ein zusätzliches **MFR- \_ Ende** , das mit dem äußersten Satz von Menü Elementen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3c309-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="3c309-154">Geben Sie das letzte Menü Element an, indem Sie das **Typelement** auf das **\_ Ende von MF** festlegen.</span><span class="sxs-lookup"><span data-stu-id="3c309-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="3c309-155">Da Untermenüs geschachtelt werden können, können mehrere Ebenen von **MF \_ enden**.</span><span class="sxs-lookup"><span data-stu-id="3c309-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="3c309-156">In diesen Fällen sind die Menü Elemente sequenziell.</span><span class="sxs-lookup"><span data-stu-id="3c309-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c309-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c309-157">Requirements</span></span>



| <span data-ttu-id="3c309-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c309-158">Requirement</span></span> | <span data-ttu-id="3c309-159">Wert</span><span class="sxs-lookup"><span data-stu-id="3c309-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c309-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c309-160">Minimum supported client</span></span><br/> | <span data-ttu-id="3c309-161">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c309-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3c309-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c309-162">Minimum supported server</span></span><br/> | <span data-ttu-id="3c309-163">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c309-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3c309-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c309-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c309-165">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3c309-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c309-166">**Menuheader**</span><span class="sxs-lookup"><span data-stu-id="3c309-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="3c309-167">**Menuhelpid**</span><span class="sxs-lookup"><span data-stu-id="3c309-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="3c309-168">**Menuiteminfo zuordnet**</span><span class="sxs-lookup"><span data-stu-id="3c309-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="3c309-169">**Normalmenuitem**</span><span class="sxs-lookup"><span data-stu-id="3c309-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="3c309-170">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3c309-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3c309-171">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3c309-171">Resources</span></span>](resources.md)
</dt> </dl>

 

