---
title: Selflag-Konstanten (Oleacc. h)
description: In diesem Thema werden die Konstanten Werte beschrieben, die verwendet werden, um anzugeben, wie ein Barrierefreies Objekt ausgewählt wird oder den Fokus erhält.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364691"
---
# <a name="selflag-constants"></a><span data-ttu-id="778a1-103">Selflag-Konstanten</span><span class="sxs-lookup"><span data-stu-id="778a1-103">SELFLAG Constants</span></span>

<span data-ttu-id="778a1-104">In diesem Thema werden die Konstanten Werte beschrieben, die verwendet werden, um anzugeben, wie ein Barrierefreies Objekt ausgewählt wird oder den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="778a1-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="778a1-105">Die Konstanten werden in Oleacc. h definiert und mit der [**ibarrierefreie:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="778a1-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="778a1-106">Die folgenden Kombinationen sind nicht zulässig:</span><span class="sxs-lookup"><span data-stu-id="778a1-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="778a1-107">selflag \_ AddSelection \| selflag \_ RemoveSelection</span><span class="sxs-lookup"><span data-stu-id="778a1-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="778a1-108">selflag \_ AddSelection \| selflag \_ TakeSelection</span><span class="sxs-lookup"><span data-stu-id="778a1-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="778a1-109">selflag \_ RemoveSelection \| selflag \_ TakeSelection</span><span class="sxs-lookup"><span data-stu-id="778a1-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="778a1-110">selflag \_ ExtendSelection \| selflag \_ TakeSelection</span><span class="sxs-lookup"><span data-stu-id="778a1-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="778a1-111">**Hinweis für Clients:** Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Edit-und Rich Edit-Steuerelementen enthalten ist, da der Text als Zeichenfolge in der [Value-Eigenschaft](value-property.md)des Objekts verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="778a1-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="778a1-112">Informationen zum Ausführen komplexer Auswahl Vorgänge finden Sie unter Auswählen von untergeordneten [Objekten](selecting-child-objects.md).</span><span class="sxs-lookup"><span data-stu-id="778a1-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="778a1-113">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="778a1-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="778a1-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="778a1-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="778a1-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="778a1-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="778a1-116">Führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="778a1-116">Performs no action.</span></span> <span data-ttu-id="778a1-117">Die Auswahl oder der Fokus wird von Microsoft Active Accessibility nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="778a1-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="778a1-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="778a1-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="778a1-119">Legt den Fokus auf das-Objekt fest und macht ihn zum Auswahl Anker.</span><span class="sxs-lookup"><span data-stu-id="778a1-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="778a1-120">Mit diesem Flag wird die Auswahl nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="778a1-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="778a1-121">Der Effekt ähnelt dem manuellen Verschieben des Fokus durch Drücken einer Pfeiltaste, während die STRG-Taste in Windows-Explorer oder in einem Listenfeld mit mehreren Auswahl Punkten gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="778a1-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="778a1-122">Bei Objekten, die über die <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>verfügen, wird SELFLAG_TAKEFOCUS mit den folgenden Werten kombiniert:</span><span class="sxs-lookup"><span data-stu-id="778a1-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="778a1-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="778a1-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="778a1-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="778a1-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="778a1-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="778a1-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="778a1-129">Wenn Sie <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> mit dem SELFLAG_TAKEFOCUS-Flag für ein Objekt mit einem <strong>HWND</strong>aufgerufen haben, wird das Flag nur wirksam, wenn das übergeordnete Objekt bereits den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="778a1-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="778a1-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span><span class="sxs-lookup"><span data-stu-id="778a1-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="778a1-131">Wählt das-Objekt aus und entfernt die Auswahl aus allen anderen Objekten im Container.</span><span class="sxs-lookup"><span data-stu-id="778a1-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="778a1-132">Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht.</span><span class="sxs-lookup"><span data-stu-id="778a1-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="778a1-133">Der SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem einfachen Klicken auf ein Element in Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="778a1-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="778a1-134">Dieses Flag darf nicht mit den folgenden Flags kombiniert werden:</span><span class="sxs-lookup"><span data-stu-id="778a1-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="778a1-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="778a1-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="778a1-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="778a1-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="778a1-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="778a1-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="778a1-139">Ändert die Auswahl, sodass alle Objekte zwischen dem Auswahl Anker und diesem Objekt den Auswahl Zustand des Anker Objekts übernehmen.</span><span class="sxs-lookup"><span data-stu-id="778a1-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="778a1-140">Wenn das Ankerobjekt nicht ausgewählt ist, werden die Objekte aus der Auswahl entfernt.</span><span class="sxs-lookup"><span data-stu-id="778a1-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="778a1-141">Wenn das Anker Objekt ausgewählt ist, wird die Auswahl so erweitert, dass Sie dieses Objekt und alle Objekte dazwischen enthält.</span><span class="sxs-lookup"><span data-stu-id="778a1-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="778a1-142">Legen Sie den Auswahl Zustand fest, indem Sie dieses Flag mit SELFLAG_ADDSELECTION oder SELFLAG_REMOVESELECTION kombinieren.</span><span class="sxs-lookup"><span data-stu-id="778a1-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="778a1-143">Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht.</span><span class="sxs-lookup"><span data-stu-id="778a1-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="778a1-144">Der SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Hinzufügen eines Elements zu einer Auswahl, indem die UMSCHALTTASTE gedrückt gehalten und in Windows-Explorer auf ein nicht ausgewähltes Objekt geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="778a1-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="778a1-145">Dieses Flag wird nicht mit SELFLAG_TAKESELECTION kombiniert.</span><span class="sxs-lookup"><span data-stu-id="778a1-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="778a1-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="778a1-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="778a1-147">Fügt das-Objekt der aktuellen Auswahl hinzu. das mögliche Ergebnis ist eine nicht zusammenhängende Auswahl.</span><span class="sxs-lookup"><span data-stu-id="778a1-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="778a1-148">Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht.</span><span class="sxs-lookup"><span data-stu-id="778a1-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="778a1-149">Der SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Hinzufügen eines Elements zu einer Auswahl, indem Sie die STRG-Taste gedrückt halten und in Windows-Explorer auf ein nicht ausgewähltes Objekt klicken.</span><span class="sxs-lookup"><span data-stu-id="778a1-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="778a1-150">Dieses Flag wird nicht mit SELFLAG_REMOVESELECTION oder SELFLAG_TAKESELECTION kombiniert.</span><span class="sxs-lookup"><span data-stu-id="778a1-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="778a1-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="778a1-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="778a1-152">Entfernt das-Objekt aus der aktuellen Auswahl. das mögliche Ergebnis ist eine nicht zusammenhängende Auswahl.</span><span class="sxs-lookup"><span data-stu-id="778a1-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="778a1-153">Wenn Sie nicht mit SELFLAG_TAKEFOCUS kombiniert wird, ändert dieses Flag den Fokus oder den Auswahl Anker nicht.</span><span class="sxs-lookup"><span data-stu-id="778a1-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="778a1-154">Der SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Entfernen eines Elements aus einer Auswahl, indem Sie die STRG-Taste gedrückt halten, während Sie auf ein ausgewähltes Objekt in Windows-Explorer klicken.</span><span class="sxs-lookup"><span data-stu-id="778a1-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="778a1-155">Dieses Flag wird nicht mit SELFLAG_ADDSELECTION oder SELFLAG_TAKESELECTION kombiniert.</span><span class="sxs-lookup"><span data-stu-id="778a1-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="778a1-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="778a1-156">Requirements</span></span>



| <span data-ttu-id="778a1-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="778a1-157">Requirement</span></span> | <span data-ttu-id="778a1-158">Wert</span><span class="sxs-lookup"><span data-stu-id="778a1-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="778a1-159">Header</span><span class="sxs-lookup"><span data-stu-id="778a1-159">Header</span></span><br/> | <dl> <span data-ttu-id="778a1-160"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="778a1-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778a1-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="778a1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="778a1-162">**IAccessible:: accSelect**</span><span class="sxs-lookup"><span data-stu-id="778a1-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="778a1-163">Auswählen von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="778a1-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 





