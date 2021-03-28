---
description: In diesem Abschnitt werden die von iactivedesktop-Schnittstellen Methoden verwendeten Flags beschrieben.
title: Iactivedesktop-Flags (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982932"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="ef54f-103">Iactivedesktop-Flags</span><span class="sxs-lookup"><span data-stu-id="ef54f-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="ef54f-104">In diesem Abschnitt werden die von [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstellen Methoden verwendeten Flags beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef54f-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="ef54f-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ \_ alle anwenden**</span><span class="sxs-lookup"><span data-stu-id="ef54f-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-106">Aggregat der \* \* \* \* AD Apply \_ \_ Save \* \* \* \*, \* \* \* \* AD Apply \_ \_ htmlgen \* \* \* \* und \* \* \* \* AD \_ Apply \_ Refresh \* \* \* \*-Werte.</span><span class="sxs-lookup"><span data-stu-id="ef54f-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ - \_ gepufferte \_ Aktualisierung anwenden**</span><span class="sxs-lookup"><span data-stu-id="ef54f-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-108">Startet einen Timer und aggregiert alle Aktualisierungs Anforderungen, die während dieses Zeitintervalls mit diesem Flag durchgeführt werden, in eine einzelne Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="ef54f-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="ef54f-109">Dieses Intervall ist auf fünf Sekunden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef54f-109">This interval is set at five seconds.</span></span> <span data-ttu-id="ef54f-110">Am Ende des Intervalls oder wenn eine Aktualisierung während des Intervalls ohne das Flag "\* \* \* \* AD \_ Apply \_ Buffered Refresh \* \* \* \*" angefordert wird \_ , wird die Aktualisierung durchgeführt, und der Timer wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="ef54f-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="ef54f-111">Dieses Flag muss mit dem Flag \* \* \* \* AD \_ Apply \_ Refresh \* \* \* \* kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ef54f-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ Apply \_ dynamikrefresh**</span><span class="sxs-lookup"><span data-stu-id="ef54f-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-113">[Version 5,0](versions.md).</span><span class="sxs-lookup"><span data-stu-id="ef54f-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="ef54f-114">Verwenden Sie Dynamic HTML, um nur die Elemente zu aktualisieren, die sich seit der letzten Aktualisierung geändert haben, nicht den gesamten Desktop.</span><span class="sxs-lookup"><span data-stu-id="ef54f-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ Apply \_ Force**</span><span class="sxs-lookup"><span data-stu-id="ef54f-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-116">Erzwingen einer aktiven Desktop Änderung</span><span class="sxs-lookup"><span data-stu-id="ef54f-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ Anwenden von \_ htmlgen**</span><span class="sxs-lookup"><span data-stu-id="ef54f-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-118">Generieren Sie die HTML-Desktop Datei erneut.</span><span class="sxs-lookup"><span data-stu-id="ef54f-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ - \_ Aktualisierung anwenden**</span><span class="sxs-lookup"><span data-stu-id="ef54f-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-120">Aktualisieren Sie das Desktop Element.</span><span class="sxs-lookup"><span data-stu-id="ef54f-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ Apply \_ Save**</span><span class="sxs-lookup"><span data-stu-id="ef54f-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-122">Speichern Sie das Desktop Element.</span><span class="sxs-lookup"><span data-stu-id="ef54f-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**Alle Comp- \_ Elem \_**</span><span class="sxs-lookup"><span data-stu-id="ef54f-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-124">Aggregat der Comp- \_ Elem- \_ \* Werte.</span><span class="sxs-lookup"><span data-stu-id="ef54f-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**Comp- \_ Elem \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="ef54f-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-126">Das Element wurde geprüft.</span><span class="sxs-lookup"><span data-stu-id="ef54f-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**Comp \_ Elem \_ curitemstate**</span><span class="sxs-lookup"><span data-stu-id="ef54f-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-128">Der aktuelle Zustand des Desktop Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**Comp \_ Elem \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="ef54f-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-130">Der Anzeige Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**Comp \_ Elem \_ NoScroll**</span><span class="sxs-lookup"><span data-stu-id="ef54f-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-132">Das Element kann nicht Bild lauffähigen.</span><span class="sxs-lookup"><span data-stu-id="ef54f-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**Comp \_ Elem- \_ ursprünglicher \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="ef54f-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-134">Die ursprünglichen Zustandsinformationen des Desktop Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**Comp-Elem Torys Verb \_ \_ \_ leiben**</span><span class="sxs-lookup"><span data-stu-id="ef54f-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-136">Die horizontale Position des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**Comp- \_ Elem \_ \_ tortop**</span><span class="sxs-lookup"><span data-stu-id="ef54f-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-138">Die vertikale Position des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**Comp \_ Elem \_ POS \_ ZIndex**</span><span class="sxs-lookup"><span data-stu-id="ef54f-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-140">Der z-Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**Comp- \_ \_ wiederhergestellte \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="ef54f-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-142">Die Statusinformationen des wiederhergestellten Desktop Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**Größe der Comp \_ Elem- \_ Größe \_**</span><span class="sxs-lookup"><span data-stu-id="ef54f-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-144">Die Höhe des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**Breite der Comp \_ Elem- \_ Größe \_**</span><span class="sxs-lookup"><span data-stu-id="ef54f-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-146">Die Breite des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**Comp- \_ Elem- \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="ef54f-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-148">Die ursprüngliche Quelle des Elements.</span><span class="sxs-lookup"><span data-stu-id="ef54f-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**Comp- \_ Elem- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="ef54f-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-150">Der Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="ef54f-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**Comp- \_ Typ \_ cfhtml**</span><span class="sxs-lookup"><span data-stu-id="ef54f-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-152">Komprimiertes HTML-Format.</span><span class="sxs-lookup"><span data-stu-id="ef54f-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**Comp \_ - \_ typsteuerelement**</span><span class="sxs-lookup"><span data-stu-id="ef54f-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-154">Das Element ist ein Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ef54f-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**Comp- \_ Typ \_ htmldoc**</span><span class="sxs-lookup"><span data-stu-id="ef54f-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-156">Das Element ist ein HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="ef54f-156">The item is an HTML document.</span></span> <span data-ttu-id="ef54f-157">Dieses Flag sollte nur verwendet werden, wenn es absolut notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="ef54f-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="ef54f-158">Es bewirkt, dass ein HTML-Dokument wörtlich in die Datei "Desktop. htt" eingefügt wird, die zum Steuern des Layouts des Desktops verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef54f-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="ef54f-159">In den meisten Fällen sollten Sie den \* \* \* \* Comp \_ Type \_ Website-Flag \* \* \* \* verwenden, um dem Desktop Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ef54f-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**Comp- \_ Typ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="ef54f-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-161">Der Höchstwert eines Comp \_ Type- \_ \* Flags.</span><span class="sxs-lookup"><span data-stu-id="ef54f-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**Bild des Comp- \_ Typs \_**</span><span class="sxs-lookup"><span data-stu-id="ef54f-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-163">Das Element ist ein Bild.</span><span class="sxs-lookup"><span data-stu-id="ef54f-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**Comp \_ Type- \_ Website**</span><span class="sxs-lookup"><span data-stu-id="ef54f-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-165">Das Element ist eine Website.</span><span class="sxs-lookup"><span data-stu-id="ef54f-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**\_obere Komponente**</span><span class="sxs-lookup"><span data-stu-id="ef54f-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-167">Ein z-Reihen folgen Wert, der angibt, dass sich das Element am oberen Rand befindet.</span><span class="sxs-lookup"><span data-stu-id="ef54f-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**wpstyle- \_ Center**</span><span class="sxs-lookup"><span data-stu-id="ef54f-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-169">Das Hintergrundbild wird zentriert.</span><span class="sxs-lookup"><span data-stu-id="ef54f-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**wpstyle \_ Max**</span><span class="sxs-lookup"><span data-stu-id="ef54f-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-171">Der Höchstwert eines wpstyle- \_ \* Flags.</span><span class="sxs-lookup"><span data-stu-id="ef54f-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**wpstyle- \_ Streckung**</span><span class="sxs-lookup"><span data-stu-id="ef54f-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-173">Das Hintergrundbild wird gestreckt, um den gesamten Bildschirm anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ef54f-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**wpstyle- \_ Kachel**</span><span class="sxs-lookup"><span data-stu-id="ef54f-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-175">Das Hintergrundbild wird gekachelt.</span><span class="sxs-lookup"><span data-stu-id="ef54f-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef54f-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**wpstyle- \_ Spanne**</span><span class="sxs-lookup"><span data-stu-id="ef54f-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef54f-177">**Windows 8 und** höher: das Hintergrundbild umfasst mehrere Monitore.</span><span class="sxs-lookup"><span data-stu-id="ef54f-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef54f-178">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ef54f-178">Requirements</span></span>



| <span data-ttu-id="ef54f-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef54f-179">Requirement</span></span> | <span data-ttu-id="ef54f-180">Wert</span><span class="sxs-lookup"><span data-stu-id="ef54f-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ef54f-181">Header</span><span class="sxs-lookup"><span data-stu-id="ef54f-181">Header</span></span><br/> | <dl> <span data-ttu-id="ef54f-182"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef54f-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
