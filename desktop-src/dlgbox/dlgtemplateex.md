---
title: Dlgtemplateex-Struktur
description: Eine erweiterte Dialogfeld Vorlage beginnt mit einem dlgtemplateex-Header, der das Dialogfeld beschreibt und die Anzahl der Steuerelemente im Dialogfeld angibt.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Dialog Felder der dlgtemplateex-Struktur
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518353"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="9ccfb-104">Dlgtemplateex-Struktur</span><span class="sxs-lookup"><span data-stu-id="9ccfb-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="9ccfb-105">Eine erweiterte Dialogfeld Vorlage beginnt mit einem **dlgtemplateex** -Header, der das Dialogfeld beschreibt und die Anzahl der Steuerelemente im Dialogfeld angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="9ccfb-106">Für jedes Steuerelement in einem Dialogfeld verfügt eine erweiterte Dialogfeld Vorlage über einen Datenblock, der das [**dlgitemtemplateex**](dlgitemtemplateex.md) -Format verwendet, um das Steuerelement zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="9ccfb-107">Die **dlgtemplateex** -Struktur ist in keiner Standard Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="9ccfb-108">Die Struktur Definition wird hier bereitgestellt, um das Format einer erweiterten Vorlage für ein Dialogfeld zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ccfb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ccfb-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="9ccfb-110">Member</span><span class="sxs-lookup"><span data-stu-id="9ccfb-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ccfb-111">**dlgver**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-112">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-113">Die Versionsnummer der erweiterten Dialogfeld Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="9ccfb-114">Dieser Member muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-115">**Signatur**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-116">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-117">Gibt an, ob eine Vorlage eine erweiterte Dialogfeld Vorlage ist.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="9ccfb-118">Wenn die **Signatur** "0xFFFF" ist, handelt es sich um eine erweiterte Dialogfeld Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="9ccfb-119">In diesem Fall gibt das **dlgver** -Mitglied die Versionsnummer der Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="9ccfb-120">Wenn **Signature** ein anderer Wert als 0xFFFF ist, handelt es sich hierbei um eine Standard Dialogfeld Vorlage, die die [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) -Struktur und die [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-121">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-122">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-123">Der Hilfe Kontext Bezeichner für das Dialogfeld Fenster.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="9ccfb-124">Wenn das System eine [**WM- \_ Hilfe**](../shell/wm-help.md) Nachricht sendet, übergibt es diesen Wert an den **wcontextid** -Member der [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-125">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-126">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-127">Die erweiterten Windows-Stile.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-127">The extended windows styles.</span></span> <span data-ttu-id="9ccfb-128">Dieser Member wird nicht zum Erstellen von Dialogfeldern verwendet, aber Anwendungen, die Dialogfeld Vorlagen verwenden, können ihn verwenden, um andere Fenstertypen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="9ccfb-129">Eine Liste der Werte finden Sie unter [**Erweiterte Fenster Stile**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="9ccfb-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-130">**style**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-131">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-132">Der Stil des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-132">The style of the dialog box.</span></span> <span data-ttu-id="9ccfb-133">Dieser Member kann eine Kombination aus [Fenster Stil Werten](/windows/desktop/winmsg/window-styles) und [Dialogfeld-Stil Werten](dialog-box-styles.md)sein.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="9ccfb-134">Wenn **Style** den Formatvorlagen Stil **DS \_ setFont** oder **DS \_ shellfont** enthält, enthält der **dlgtemplateex** -Header der erweiterten Dialogfeld Vorlage vier zusätzliche Member ( **pointsize**, **Weight**, **kursiv** und Font **),** die die Schriftart beschreiben, die für den Text im Client Bereich und die Steuerelemente des Dialog Felds verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="9ccfb-135">Wenn möglich, erstellt das System eine Schriftart entsprechend den Werten, die in diesen Membern angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="9ccfb-136">Anschließend sendet das System eine [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht an das Dialogfeld und an jedes Steuerelement, um ein Handle für die Schriftart bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="9ccfb-137">Weitere Informationen finden Sie unter [Dialog Feld Schriftarten](about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="9ccfb-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-138">**cdlgitems**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-139">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-140">Die Anzahl der Steuerelemente im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-141">**x**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-142">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-143">Die x-Koordinate der oberen linken Ecke des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-144">**y**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-145">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-146">Die y-Koordinate der oberen linken Ecke des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-147">**verschoben**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-148">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-149">Die Breite des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-150">**CY**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-151">Typ: **Short**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-152">Die Höhe des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-153">**stehen**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-154">Typ: **SZ \_ oder \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-155">Ein Array variabler Länge mit 16-Bit-Elementen, das eine Menü Ressource für das Dialogfeld angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="9ccfb-156">Wenn das erste Element dieses Arrays 0x0000 ist, enthält das Dialogfeld kein Menü, und das Array enthält keine anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="9ccfb-157">Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer Menü Ressource in einer ausführbaren Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="9ccfb-158">Wenn das erste Element einen anderen Wert aufweist, behandelt das System das Array als eine NULL-terminierte Unicode-Zeichenfolge, die den Namen einer Menü Ressource in einer ausführbaren Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-159">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-160">Typ: **SZ \_ oder \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-161">Ein Array variabler Länge mit 16-Bit-Elementen, das die Fenster Klasse des Dialog Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="9ccfb-162">Wenn das erste Element des Arrays 0x0000 ist, verwendet das System die vordefinierte Dialogfeld Klasse für das Dialogfeld, und das Array enthält keine anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="9ccfb-163">Wenn das erste Element 0xFFFF ist, verfügt das Array über ein zusätzliches Element, das den Ordinalwert einer vordefinierten System Fenster Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="9ccfb-164">Wenn das erste Element einen anderen Wert aufweist, behandelt das System das Array als eine NULL-terminierte Unicode-Zeichenfolge, die den Namen einer registrierten Fenster Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-165">**title**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-166">Typ: **WCHAR \[ titlelen \]**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-167">Der Titel des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-167">The title of the dialog box.</span></span> <span data-ttu-id="9ccfb-168">Wenn das erste Element dieses Arrays 0x0000 ist, enthält das Dialogfeld keinen Titel, und das Array enthält keine anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-169">**pointsize**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-170">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-171">Die Punktgröße der Schriftart, die für den Text im Dialogfeld und dessen Steuerelemente verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="9ccfb-172">Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-174">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-175">Die Gewichtung der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-175">The weight of the font.</span></span> <span data-ttu-id="9ccfb-176">Beachten Sie, dass die Werte, die für den **lfWeight** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur aufgeführt sind, zwar alle Werte sein können **\_**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="9ccfb-177">Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-178">**Kursiv**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-179">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-180">Gibt an, ob die Schriftart kursiv formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="9ccfb-181">Wenn dieser Wert **true** ist, wird die Schriftart kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="9ccfb-182">Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-183">**charset**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-184">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-185">Der zu verwendende Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-185">The character set to be used.</span></span> <span data-ttu-id="9ccfb-186">Weitere Informationen finden Sie unter dem **lfCharSet** -Member von [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span><span class="sxs-lookup"><span data-stu-id="9ccfb-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="9ccfb-187">Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="9ccfb-188">**Gotik**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="9ccfb-189">Typ: **WCHAR \[ stringlen \]**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="9ccfb-190">Der Name der Schriftart für die Schriftart.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="9ccfb-191">Dieser Member ist nur vorhanden, wenn der **stilmember** **DS \_ setFont** oder **DS \_ shellfont** angibt.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ccfb-192">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ccfb-192">Remarks</span></span>

<span data-ttu-id="9ccfb-193">Sie können eine erweiterte Dialogfeld Vorlage anstelle einer Standard Dialogfeld Vorlage [**in den Funktionen**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)"" von "", "", " [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)", "-param", "Funktionen [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)" und " [**dialogboxindirekte**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="9ccfb-194">Im Anschluss an den **dlgtemplateex** -Header in einer erweiterten Dialogfeld Vorlage handelt es sich um eine oder mehrere [**dlgitemtemplateex**](dlgitemtemplateex.md) -Strukturen, die die Steuerelemente des Dialog Felds beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="9ccfb-195">Der **cdlgitems** -Member der **dlgitemtemplateex** -Struktur gibt die Anzahl der **dlgitemtemplateex** -Strukturen an, die in der Vorlage befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="9ccfb-196">Jede [**dlgitemtemplateex**](dlgitemtemplateex.md) -Struktur in der Vorlage muss an einer **DWORD** -Grenze ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="9ccfb-197">Wenn der **stilmember** den **DS- \_ setFont** - **oder DS- \_ shellfont** -Stil angibt, beginnt die erste **dlgitemtemplateex** -Struktur an der ersten **DWORD** -Grenze hinter der **Schriftart** Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="9ccfb-198">Wenn diese Stile nicht angegeben werden, beginnt die erste Struktur an der ersten **DWORD** -Grenze hinter der **Titel** Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="9ccfb-199">Die Arrays " **Menu**", " **WindowClass**", " **Title**" und " **Schriftart** " müssen an **Wort** Grenzen ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="9ccfb-200">Wenn Sie Zeichen folgen in den Feldern " **Menü**", " **WindowClass**", " **Title**" und " **Schriftart** " angeben, müssen Sie Unicode-Zeichen folgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="9ccfb-201">Verwenden Sie die [**Multibyte-**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) Funktion, um diese Unicode-Zeichen folgen aus ANSI-Zeichen folgen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="9ccfb-202">Die Member **x**, **y**, **CX** und **CY** geben Werte in Dialogfeld Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="9ccfb-203">Sie können diese Werte mithilfe der [**mapdialogrect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) -Funktion in Bildschirm Einheiten (Pixel) konvertieren.</span><span class="sxs-lookup"><span data-stu-id="9ccfb-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ccfb-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ccfb-204">Requirements</span></span>



| <span data-ttu-id="9ccfb-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ccfb-205">Requirement</span></span> | <span data-ttu-id="9ccfb-206">Wert</span><span class="sxs-lookup"><span data-stu-id="9ccfb-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9ccfb-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ccfb-207">Minimum supported client</span></span><br/> | <span data-ttu-id="9ccfb-208">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ccfb-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ccfb-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ccfb-209">Minimum supported server</span></span><br/> | <span data-ttu-id="9ccfb-210">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ccfb-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9ccfb-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ccfb-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ccfb-212">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ccfb-213">**"Kreatedialogindirect"**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="9ccfb-214">**"Kreatedialogindirectparam"**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="9ccfb-215">**Dialogboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="9ccfb-216">**Dialogboxderedereparam**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="9ccfb-217">**Dlgitemtemplateex**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="9ccfb-218">**Mapdialogrect**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="9ccfb-219">**WM- \_ setFont**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="9ccfb-220">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ccfb-221">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="9ccfb-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="9ccfb-222">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9ccfb-223">**"LogFont"**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="9ccfb-224">**MultiByteToWideChar muss**</span><span class="sxs-lookup"><span data-stu-id="9ccfb-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

