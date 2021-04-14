---
title: Dlgitemtemplateex-Struktur
description: Ein TextBlock, der von einer erweiterten Dialogfeld Vorlage verwendet wird, um das erweiterte Dialogfeld zu beschreiben. Eine Beschreibung des Formats einer erweiterten Dialogfeld Vorlage finden Sie unter dlgtemplateex.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Dialog Felder der dlgitemtemplateex-Struktur
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392190"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="11b72-105">Dlgitemtemplateex-Struktur</span><span class="sxs-lookup"><span data-stu-id="11b72-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="11b72-106">Ein TextBlock, der von einer erweiterten Dialogfeld Vorlage verwendet wird, um das erweiterte Dialogfeld zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="11b72-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="11b72-107">Eine Beschreibung des Formats einer erweiterten Dialogfeld Vorlage finden Sie unter [**dlgtemplateex**](dlgtemplateex.md).</span><span class="sxs-lookup"><span data-stu-id="11b72-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="11b72-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="11b72-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="11b72-109">Member</span><span class="sxs-lookup"><span data-stu-id="11b72-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="11b72-110">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="11b72-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11b72-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-112">Der Hilfe Kontext Bezeichner für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="11b72-112">The help context identifier for the control.</span></span> <span data-ttu-id="11b72-113">Wenn das System eine [**WM- \_ Hilfe**](../shell/wm-help.md) Nachricht sendet, übergibt es **den HelpID** -Wert im **dwcontextid** -Member der [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="11b72-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-114">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="11b72-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11b72-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-116">Die erweiterten Stile für ein Fenster.</span><span class="sxs-lookup"><span data-stu-id="11b72-116">The extended styles for a window.</span></span> <span data-ttu-id="11b72-117">Dieser Member wird nicht zum Erstellen von Steuerelementen in Dialogfeldern verwendet, aber Anwendungen, die Dialogfeld Vorlagen verwenden, können ihn verwenden, um andere Fenstertypen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11b72-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="11b72-118">Eine Liste der Werte finden Sie unter [**Erweiterte Fenster Stile**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="11b72-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="11b72-119">**style**</span><span class="sxs-lookup"><span data-stu-id="11b72-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-120">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11b72-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-121">Das Format des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="11b72-121">The style of the control.</span></span> <span data-ttu-id="11b72-122">Dieser Member kann eine Kombination aus [Fenster Stil Werten](/windows/desktop/winmsg/window-styles) (z. b. WS-Rahmen) und einem oder mehreren der Steuerelement-Format [Werten](/windows/desktop/Controls/common-control-styles) (z. b. "bin **\_ Push Button** " und " **es \_ left**") sein. **\_**</span><span class="sxs-lookup"><span data-stu-id="11b72-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="11b72-123">**x**</span><span class="sxs-lookup"><span data-stu-id="11b72-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-124">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="11b72-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-125">Die x-Koordinate der oberen linken Ecke des Steuer Elements in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="11b72-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="11b72-126">Diese Koordinate ist immer relativ zur oberen linken Ecke des Client Bereichs des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="11b72-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-127">**y**</span><span class="sxs-lookup"><span data-stu-id="11b72-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-128">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="11b72-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-129">Die y-Koordinate der oberen linken Ecke des Steuer Elements in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="11b72-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="11b72-130">Diese Koordinate ist immer relativ zur oberen linken Ecke des Client Bereichs des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="11b72-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-131">**verschoben**</span><span class="sxs-lookup"><span data-stu-id="11b72-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-132">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="11b72-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-133">Die Breite des Steuer Elements in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="11b72-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-134">**CY**</span><span class="sxs-lookup"><span data-stu-id="11b72-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-135">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="11b72-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-136">Die Höhe des Steuer Elements in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="11b72-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-137">**id**</span><span class="sxs-lookup"><span data-stu-id="11b72-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-138">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11b72-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-139">Der Steuerelement Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="11b72-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-140">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="11b72-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-141">Typ: **SZ \_ oder \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="11b72-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-142">Ein Array variabler Länge mit 16-Bit-Elementen, das die Fenster Klasse des Steuer Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="11b72-143">Wenn das erste Element dieses Arrays ein anderer Wert als 0xFFFF ist, behandelt das System das Array als eine mit NULL endenden Unicode-Zeichenfolge, die den Namen einer registrierten Fenster Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="11b72-144">Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer vordefinierten System Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="11b72-145">Die Ordinalzahl kann einen der folgenden Atom-Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="11b72-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="11b72-146">Wert</span><span class="sxs-lookup"><span data-stu-id="11b72-146">Value</span></span>                                                                             | <span data-ttu-id="11b72-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="11b72-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="11b72-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="11b72-149">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="11b72-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="11b72-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="11b72-151">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="11b72-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="11b72-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="11b72-153">statischen</span><span class="sxs-lookup"><span data-stu-id="11b72-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="11b72-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="11b72-155">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="11b72-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="11b72-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="11b72-157">Bildlaufleiste</span><span class="sxs-lookup"><span data-stu-id="11b72-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="11b72-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="11b72-159">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="11b72-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="11b72-160">**title**</span><span class="sxs-lookup"><span data-stu-id="11b72-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-161">Typ: **SZ \_ oder \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="11b72-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-162">Ein Array variabler Länge mit 16-Bit-Elementen, das den Anfangstext oder Ressourcen Bezeichner des Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="11b72-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="11b72-163">Wenn das erste Element dieses Arrays 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer Ressource (z. b. ein Symbol) in einer ausführbaren Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="11b72-164">Sie können einen Ressourcen Bezeichner für Steuerelemente verwenden, z. b. statische Symbol Steuerelemente, die ein Symbol oder eine andere Ressource anstelle von Text laden und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="11b72-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="11b72-165">Wenn das erste Element ein anderer Wert als 0xFFFF ist, behandelt das System das Array als eine mit NULL endenden Unicode-Zeichenfolge, die den Anfangstext angibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="11b72-166">**extracount**</span><span class="sxs-lookup"><span data-stu-id="11b72-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="11b72-167">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="11b72-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="11b72-168">Die Anzahl der Bytes der Erstellungs Daten, die diesem Element folgen.</span><span class="sxs-lookup"><span data-stu-id="11b72-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="11b72-169">Wenn dieser Wert größer als 0 (null) ist, beginnt die Erstellungs Daten an der nächsten **Wort** Grenze.</span><span class="sxs-lookup"><span data-stu-id="11b72-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="11b72-170">Diese Erstellungs Daten können eine beliebige Größe und ein beliebiges Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="11b72-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="11b72-171">Die Fenster Prozedur des Steuer Elements muss in der Lage sein, die Daten zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="11b72-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="11b72-172">Wenn das System das Steuerelement erstellt, übergibt es einen Zeiger auf diese Daten im *LPARAM* -Parameter der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, die an das Steuerelement gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="11b72-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11b72-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11b72-173">Remarks</span></span>

<span data-ttu-id="11b72-174">Eine erweiterte Vorlage für ein Dialogfeld besteht aus einem [**dlgtemplateex**](dlgtemplateex.md) -Header, gefolgt von einer **dlgitemtemplateex** -Struktur für jedes Steuerelement im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="11b72-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="11b72-175">Jede **dlgitemtemplateex** -Struktur muss an einer **DWORD** -Grenze ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="11b72-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="11b72-176">Die **WindowClass** -und **Title** -Arrays variabler Länge müssen an **Wort** Grenzen ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="11b72-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="11b72-177">Das Erstellungs Daten Array muss, falls vorhanden, an einer **Wort** Grenze ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="11b72-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="11b72-178">Wenn Sie Zeichen folgen in den **WindowClass** -und **Title** -Arrays angeben, müssen Sie Unicode-Zeichen folgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="11b72-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="11b72-179">Verwenden Sie die [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion zum Generieren von Unicode-Zeichen folgen aus ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="11b72-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="11b72-180">Die Member **x**, **y**, **CX** und **CY** geben Werte in Dialogfeld Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="11b72-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="11b72-181">Sie können diese Werte mithilfe der [**mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) -Funktion in Bildschirm Einheiten (Pixel) konvertieren.</span><span class="sxs-lookup"><span data-stu-id="11b72-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="11b72-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11b72-182">Requirements</span></span>



| <span data-ttu-id="11b72-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11b72-183">Requirement</span></span> | <span data-ttu-id="11b72-184">Wert</span><span class="sxs-lookup"><span data-stu-id="11b72-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="11b72-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11b72-185">Minimum supported client</span></span><br/> | <span data-ttu-id="11b72-186">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11b72-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="11b72-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11b72-187">Minimum supported server</span></span><br/> | <span data-ttu-id="11b72-188">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11b72-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="11b72-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11b72-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="11b72-190">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="11b72-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="11b72-191">**"Kreatedialogindirect"**</span><span class="sxs-lookup"><span data-stu-id="11b72-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="11b72-192">**"Kreatedialogindirectparam"**</span><span class="sxs-lookup"><span data-stu-id="11b72-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="11b72-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="11b72-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="11b72-194">**Dialogboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="11b72-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="11b72-195">**Dialogboxderedereparam**</span><span class="sxs-lookup"><span data-stu-id="11b72-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="11b72-196">**Dlgtemplateex**</span><span class="sxs-lookup"><span data-stu-id="11b72-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="11b72-197">**Mapdialogrect**</span><span class="sxs-lookup"><span data-stu-id="11b72-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="11b72-198">**WM \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="11b72-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="11b72-199">**Licher**</span><span class="sxs-lookup"><span data-stu-id="11b72-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11b72-200">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="11b72-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="11b72-201">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="11b72-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="11b72-202">**MultiByteToWideChar muss**</span><span class="sxs-lookup"><span data-stu-id="11b72-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="11b72-203">**WM- \_ Hilfe**</span><span class="sxs-lookup"><span data-stu-id="11b72-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

