---
title: Allgemeine Steuerelement Parameter
description: Im folgenden wird die allgemeine Syntax für eine Control Resource-Definition-Anweisung beschrieben.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314913"
---
# <a name="common-control-parameters"></a><span data-ttu-id="6bba6-103">Allgemeine Steuerelement Parameter</span><span class="sxs-lookup"><span data-stu-id="6bba6-103">Common Control Parameters</span></span>

<span data-ttu-id="6bba6-104">Im folgenden wird die allgemeine Syntax für eine Control Resource-Definition-Anweisung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6bba6-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="6bba6-105">Die Bedeutung der einzelnen Parameter ist unten angegeben.</span><span class="sxs-lookup"><span data-stu-id="6bba6-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="6bba6-106">Gelegentlich verwendet eine-Anweisung einen-Parameter anders, oder es kann ein Parameter ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="6bba6-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="6bba6-107">Die Anweisungs spezifische Variation wird in der Dokumentation für die-Anweisung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6bba6-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="6bba6-108"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="6bba6-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-109">Text, der mit dem-Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6bba6-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="6bba6-110">Der Text wird im-Steuerelement oder neben dem-Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="6bba6-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="6bba6-111">Dieser Parameter muss NULL oder mehr Zeichen enthalten, die in doppelten Anführungszeichen (") eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="6bba6-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="6bba6-112">Zeichen folgen werden automatisch mit null-terminierter und in die resultierende Ressourcen Datei in Unicode konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6bba6-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="6bba6-113">Standardmäßig sind die zwischen den doppelten Anführungszeichen aufgelisteten Zeichen ANSI-Zeichen, und Escapesequenzen werden als Byte-Escapesequenzen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6bba6-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="6bba6-114">Wenn der Zeichenfolge das Präfix "L" vorangestellt ist, ist die Zeichenfolge eine Zeichenfolge mit breit Zeichen, und Escapesequenzen werden als 2-Byte-Escapesequenzen interpretiert, die Unicode-Zeichen angeben</span><span class="sxs-lookup"><span data-stu-id="6bba6-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="6bba6-115">Wenn im Text ein doppeltes Anführungszeichen erforderlich ist, müssen Sie das doppelte Anführungszeichen zweimal einschließen.</span><span class="sxs-lookup"><span data-stu-id="6bba6-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="6bba6-116">Ein kaufmännisches und-Zeichen (&) im Text gibt an, dass das folgende Zeichen als mnetmonisches Zeichen für das-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bba6-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="6bba6-117">Wenn das Steuerelement angezeigt wird, wird das kaufmännische und-Zeichen nicht angezeigt, aber das mnetmonische Zeichen wird unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="6bba6-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="6bba6-118">Der Benutzer kann das Steuerelement auswählen, indem er die Taste drückt, die dem unterstrichenen mnetmonischen Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6bba6-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="6bba6-119">Um das kaufmännische und-Zeichen als Zeichen in einer Zeichenfolge zu verwenden, fügen Sie zwei kaufmännische und-Zeichen (&&) ein.</span><span class="sxs-lookup"><span data-stu-id="6bba6-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-120"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="6bba6-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-121">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6bba6-121">Control identifier.</span></span> <span data-ttu-id="6bba6-122">Bei diesem Wert muss es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich 0 bis 65.535 oder um einen einfachen arithmetischen Ausdruck handeln, der zu einem Wert in diesem Bereich ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="6bba6-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-123"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="6bba6-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-124">X-Koordinate des linken Rands des Steuer Elements relativ zur linken Seite des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="6bba6-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="6bba6-125">Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 0 und 65.535 sein.</span><span class="sxs-lookup"><span data-stu-id="6bba6-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="6bba6-126">Die Koordinate befindet sich in Dialogfeld Einheiten und ist relativ zum Ursprung des Dialog Felds, Fensters oder Steuer Elements, das das angegebene Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="6bba6-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-127"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="6bba6-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-128">Y-Koordinate des oberen Rands des Steuer Elements relativ zum oberen Rand des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="6bba6-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="6bba6-129">Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 0 und 65.535 sein.</span><span class="sxs-lookup"><span data-stu-id="6bba6-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="6bba6-130">Die Koordinate befindet sich in Dialog Einheiten relativ zum Ursprung des Dialog Felds, Fensters oder Steuer Elements, das das angegebene Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="6bba6-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-131"><span id="width"></span><span id="WIDTH"></span>*Breite*</span><span class="sxs-lookup"><span data-stu-id="6bba6-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-132">Breite des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="6bba6-132">Width of the control.</span></span> <span data-ttu-id="6bba6-133">Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 1 und 65.535 sein.</span><span class="sxs-lookup"><span data-stu-id="6bba6-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="6bba6-134">Die Breite liegt bei Einheiten von 1/4 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6bba6-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-135"><span id="height"></span><span id="HEIGHT"></span>*Flugh*</span><span class="sxs-lookup"><span data-stu-id="6bba6-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-136">Die Höhe des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="6bba6-136">Height of the control.</span></span> <span data-ttu-id="6bba6-137">Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 1 und 65.535 sein.</span><span class="sxs-lookup"><span data-stu-id="6bba6-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="6bba6-138">Die Höhe ist in Einheiten von 1/8 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6bba6-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-139"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="6bba6-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-140">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="6bba6-140">Control styles.</span></span> <span data-ttu-id="6bba6-141">Verwenden Sie den bitweisen or ( \| )-Operator, um Stile zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="6bba6-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="6bba6-142">Weitere Informationen finden Sie unter [Fenster Stile](../winmsg/window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6bba6-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*Erweiterter Stil*</span><span class="sxs-lookup"><span data-stu-id="6bba6-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-144">Erweiterte Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="6bba6-144">Extended window styles.</span></span> <span data-ttu-id="6bba6-145">Sie müssen *Style* angeben, um den *erweiterten Stil* anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6bba6-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="6bba6-146">Weitere Informationen finden Sie unter [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6bba6-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*</span><span class="sxs-lookup"><span data-stu-id="6bba6-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-148">Numerischer Ausdruck, der die ID angibt, mit der das Steuerelement während der [**WM- \_ Hilfe**](../shell/wm-help.md) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6bba6-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="6bba6-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span><span class="sxs-lookup"><span data-stu-id="6bba6-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="6bba6-150">Steuerelement spezifische Daten für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6bba6-150">Control-specific data for the control.</span></span> <span data-ttu-id="6bba6-151">Wenn ein Dialogfeld erstellt wird und ein Steuerelement in diesem Dialogfeld, das Steuerelement spezifische Daten enthält, erstellt wird, wird ein Zeiger auf diese Daten über den *LPARAM* der [**WM \_ Create**](../winmsg/wm-create.md) -Meldung für dieses Steuerelement an die Fenster Prozedur des Steuer Elements übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6bba6-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bba6-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bba6-152">Remarks</span></span>

<span data-ttu-id="6bba6-153">Horizontale Dialog Einheiten sind 1/4 der Dialogfeld Basis-breiten Einheit.</span><span class="sxs-lookup"><span data-stu-id="6bba6-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="6bba6-154">Vertikale Einheiten sind 1/8 der Dialogfeld Basis-Höheneinheit.</span><span class="sxs-lookup"><span data-stu-id="6bba6-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="6bba6-155">Die aktuellen Dialogfeld Basiseinheiten werden aus der Höhe und Breite der aktuellen System Schriftart berechnet.</span><span class="sxs-lookup"><span data-stu-id="6bba6-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="6bba6-156">Die [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) -Funktion gibt die Dialog Basiseinheiten in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="6bba6-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="6bba6-157">Die Koordinaten sind relativ zum Ursprung des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="6bba6-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 