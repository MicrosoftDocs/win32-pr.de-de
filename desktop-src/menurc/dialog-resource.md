---
title: Dialog Ressource
description: Definiert ein Dialogfeld. | Dialog Ressource
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Dialog Feld Ressourcen Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366397"
---
# <a name="dialog-resource"></a><span data-ttu-id="09da3-105">Dialog Ressource</span><span class="sxs-lookup"><span data-stu-id="09da3-105">DIALOG resource</span></span>

<span data-ttu-id="09da3-106">Definiert ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="09da3-106">Defines a dialog box.</span></span> <span data-ttu-id="09da3-107">Die-Anweisung definiert die Position und die Dimensionen des Dialog Felds auf dem Bildschirm sowie den Dialogfeld Stil.</span><span class="sxs-lookup"><span data-stu-id="09da3-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="09da3-108">**Dialog** ist eine veraltete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="09da3-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="09da3-109">Neue Anwendungen sollten [**DIALOGEX**](dialogex-resource.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="09da3-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="09da3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09da3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09da3-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="09da3-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="09da3-112">Eindeutiger Name oder ein eindeutiger ganzzahliger 16-Bit-Wert ohne Vorzeichen, der das Dialogfeld identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09da3-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="09da3-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="09da3-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="09da3-114">Optionen für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="09da3-114">Options for the dialog box.</span></span> <span data-ttu-id="09da3-115">Dies kann NULL oder mehr der folgenden-Anweisungen sein.</span><span class="sxs-lookup"><span data-stu-id="09da3-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="09da3-116">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="09da3-116">Statement</span></span>                                                        | <span data-ttu-id="09da3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09da3-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09da3-118">[**Beschriftung**](caption-statement.md) "*Text*"</span><span class="sxs-lookup"><span data-stu-id="09da3-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="09da3-119">Beschriftung des Dialog Felds, wenn es über eine Titelleiste verfügt.</span><span class="sxs-lookup"><span data-stu-id="09da3-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="09da3-120">Weitere Informationen finden Sie unter [**Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="09da3-121">[**Merkmale**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="09da3-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="09da3-122">Benutzerdefinierter **DWORD** -Wert, der von Ressourcen Tools verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09da3-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="09da3-123">Dieser Wert wird vom System nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="09da3-123">This value is not used by the system.</span></span> <span data-ttu-id="09da3-124">Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="09da3-125">[**Class**](class-statement.md) - *Klasse*</span><span class="sxs-lookup"><span data-stu-id="09da3-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="09da3-126">Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die die Klasse des Dialog Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="09da3-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="09da3-127">Weitere Informationen finden Sie unter- [**Klasse**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="09da3-128">**ExStyle =** *Erweiterte Stile*</span><span class="sxs-lookup"><span data-stu-id="09da3-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="09da3-129">Erweiterte Fenster Stil des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="09da3-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="09da3-130">Weitere Informationen finden Sie unter [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="09da3-131">**Schriftart** *pointsize*, *Schriftart*</span><span class="sxs-lookup"><span data-stu-id="09da3-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="09da3-132">Die Punktgröße und Schriftart für die Schriftart.</span><span class="sxs-lookup"><span data-stu-id="09da3-132">Point size and typeface for the font.</span></span> <span data-ttu-id="09da3-133">Weitere Informationen finden Sie unter [**Schriftart**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="09da3-134">[**Sprach**](language-statement.md) *Sprache*, *unter Sprache*</span><span class="sxs-lookup"><span data-stu-id="09da3-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="09da3-135">Sprache des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="09da3-135">Language of the dialog box.</span></span> <span data-ttu-id="09da3-136">Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="09da3-137"> *MENUNAME darf* -Menü</span><span class="sxs-lookup"><span data-stu-id="09da3-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="09da3-138">Das zu verwendende Menü.</span><span class="sxs-lookup"><span data-stu-id="09da3-138">Menu to be used.</span></span> <span data-ttu-id="09da3-139">Dieser Wert ist entweder der Name des Menüs oder der ganzzahlige Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="09da3-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="09da3-140">[**Stil**](style-statement.md) *Stile*</span><span class="sxs-lookup"><span data-stu-id="09da3-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="09da3-141">Stile des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="09da3-141">Styles of the dialog box.</span></span> <span data-ttu-id="09da3-142">Weitere Informationen finden Sie unter [**Style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="09da3-143">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="09da3-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="09da3-144">Benutzerdefinierter **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="09da3-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="09da3-145">Diese Anweisung ist für die Verwendung durch zusätzliche Ressourcen Tools vorgesehen und wird nicht vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="09da3-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="09da3-146">Weitere Informationen finden Sie unter [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="09da3-147">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09da3-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="09da3-148">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="09da3-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09da3-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09da3-149">Remarks</span></span>

<span data-ttu-id="09da3-150">Die [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) -Funktion gibt die Dialog Basiseinheiten in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="09da3-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="09da3-151">Die genaue Bedeutung der Koordinaten hängt von dem Stil ab, der von der [**Style**](style-statement.md) Option-Anweisung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="09da3-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="09da3-152">Bei Dialogfeldern im untergeordneten Stil sind die Koordinaten relativ zum Ursprung des übergeordneten Fensters, es sei denn, im Dialogfeld ist der Stil **DS \_ absalign** enthalten. in diesem Fall sind die Koordinaten relativ zum Ursprung des Anzeige Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="09da3-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="09da3-153">Verwenden Sie das unter **geordnete \_ WS** -Format nicht mit einem modalen Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="09da3-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="09da3-154">Die [**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) -Funktion deaktiviert immer das übergeordnete Element bzw. den Besitzer des neu erstellten Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="09da3-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="09da3-155">Wenn ein übergeordnetes Fenster deaktiviert wird, werden die untergeordneten Fenster implizit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="09da3-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="09da3-156">Da das übergeordnete Fenster des Dialog Felds untergeordneter Stil deaktiviert ist, ist das Dialogfeld untergeordnete Formate ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="09da3-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="09da3-157">Wenn ein Dialogfeld den Stil " **DS \_ absalign** " aufweist, sind die Dialog Koordinaten für die linke obere Ecke relativ zum Bildschirm Ursprung und nicht zur oberen linken Ecke des übergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="09da3-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="09da3-158">Normalerweise verwenden Sie diesen Stil, wenn das Dialogfeld in einem bestimmten Teil der Anzeige gestartet werden soll, unabhängig davon, wo sich das übergeordnete Fenster möglicherweise auf dem Bildschirm befindet.</span><span class="sxs-lookup"><span data-stu-id="09da3-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="09da3-159">Das **Dialog** Feld Name kann auch als Class-Name-Parameter für die Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " verwendet werden, um ein Fenster mit Dialog Feld Attributen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="09da3-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="09da3-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09da3-160">Examples</span></span>

<span data-ttu-id="09da3-161">Im folgenden Beispiel wird die Verwendung der **Dialog** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="09da3-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="09da3-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09da3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09da3-163">Verwenden von Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="09da3-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="09da3-164">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="09da3-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="09da3-165">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="09da3-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="09da3-166">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="09da3-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="09da3-167">**"Kreatedialog"**</span><span class="sxs-lookup"><span data-stu-id="09da3-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="09da3-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="09da3-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="09da3-169">**Dialogbox**</span><span class="sxs-lookup"><span data-stu-id="09da3-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="09da3-170">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="09da3-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="09da3-171">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="09da3-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="09da3-172">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="09da3-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="09da3-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="09da3-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="09da3-174">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="09da3-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="09da3-175">**Version**</span><span class="sxs-lookup"><span data-stu-id="09da3-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
