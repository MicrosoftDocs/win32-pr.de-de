---
title: Normalmenuitem-Struktur
description: Enthält Informationen zu jedem Element in einer Menü Ressource, die kein Menü oder Untermenü öffnet. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Normmenuitem-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340517"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="b1392-105">Normalmenuitem-Struktur</span><span class="sxs-lookup"><span data-stu-id="b1392-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="b1392-106">Enthält Informationen zu jedem Element in einer Menü Ressource, die kein Menü oder Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="b1392-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="b1392-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b1392-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1392-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1392-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="b1392-109">Member</span><span class="sxs-lookup"><span data-stu-id="b1392-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1392-110">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="b1392-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="b1392-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="b1392-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b1392-112">Der Typ des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="b1392-112">The type of menu item.</span></span> <span data-ttu-id="b1392-113">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b1392-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="b1392-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b1392-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="b1392-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b1392-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="b1392-116"><dt>**MFR \_ Ende**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="b1392-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="b1392-117">Das Menü Element ist das letzte in diesem Untermenü oder in der Menü Ressource. Dieses Flag wird intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1392-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="b1392-118"><dt>**MFR \_ Popup**</dt> - <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="b1392-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="b1392-119">Das Menü Element öffnet ein Menü oder ein Untermenü. das-Flag wird intern vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1392-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="b1392-120">**MenuText**</span><span class="sxs-lookup"><span data-stu-id="b1392-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="b1392-121">Typ: **szorord**</span><span class="sxs-lookup"><span data-stu-id="b1392-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="b1392-122">Eine NULL-terminierte Unicode-Zeichenfolge, die den Text für dieses Menü Element enthält.</span><span class="sxs-lookup"><span data-stu-id="b1392-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="b1392-123">Es gibt keine Beschränkung für die Größe dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b1392-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1392-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1392-124">Remarks</span></span>

<span data-ttu-id="b1392-125">Es gibt eine **Normal MenuItem** -Struktur für jedes Menü Element, das kein Menü oder Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="b1392-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="b1392-126">Geben Sie das letzte Menü Element in einem Menü an, indem Sie das **ResInfo** -Element auf **MFR- \_ Ende** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b1392-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="b1392-127">Ein Menü Trennzeichen ist ein spezieller Typ von Menü Element, das inaktiv ist, aber als Trennleiste zwischen zwei aktiven Menü Elementen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b1392-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="b1392-128">Geben Sie ein Menü Trennzeichen an, indem Sie den **MenuText** -Member leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="b1392-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1392-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1392-129">Requirements</span></span>



| <span data-ttu-id="b1392-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1392-130">Requirement</span></span> | <span data-ttu-id="b1392-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b1392-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b1392-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1392-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b1392-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1392-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1392-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1392-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b1392-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1392-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b1392-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1392-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1392-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b1392-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1392-138">**Menuheader**</span><span class="sxs-lookup"><span data-stu-id="b1392-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="b1392-139">**Menuiteminfo zuordnet**</span><span class="sxs-lookup"><span data-stu-id="b1392-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="b1392-140">**Popupmenuitem**</span><span class="sxs-lookup"><span data-stu-id="b1392-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="b1392-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b1392-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1392-142">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1392-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





