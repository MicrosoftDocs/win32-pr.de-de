---
title: CheckBox-Steuerelement (Ressourcen Compiler)
description: Definiert ein Kontrollkästchen-Steuerelement.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- CheckBox-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337648"
---
# <a name="checkbox-control"></a><span data-ttu-id="76bda-104">CheckBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="76bda-104">CHECKBOX control</span></span>

<span data-ttu-id="76bda-105">Definiert ein Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="76bda-105">Defines a check box control.</span></span> <span data-ttu-id="76bda-106">Das-Steuerelement ist ein kleines Rechteck (Kontrollkästchen), das neben dem angegebenen Text angezeigt wird (in der Regel rechts).</span><span class="sxs-lookup"><span data-stu-id="76bda-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="76bda-107">Wenn der Benutzer das Steuerelement auswählt, hebt das-Steuerelement das Rechteck hervor und sendet eine Meldung an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="76bda-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="76bda-108">Die **CheckBox** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="76bda-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="76bda-109"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="76bda-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="76bda-110">Text, der auf der rechten Seite des-Steuer Elements angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76bda-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="76bda-111"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="76bda-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="76bda-112">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="76bda-112">Control styles.</span></span> <span data-ttu-id="76bda-113">Bei diesem Wert kann es sich um eine Kombination aus **dem \_ Kontrollkästchen** "Schaltfläche für Schaltflächen Klassen" und " **WS \_ Tabstopps** " und " **WS \_** "</span><span class="sxs-lookup"><span data-stu-id="76bda-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="76bda-114">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_CHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="76bda-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="76bda-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="76bda-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="76bda-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76bda-116">Examples</span></span>

<span data-ttu-id="76bda-117">In diesem Beispiel wird ein Kontrollkästchen-Steuerelement mit der Bezeichnung "Kursiv" definiert:</span><span class="sxs-lookup"><span data-stu-id="76bda-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="76bda-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76bda-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76bda-119">**AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="76bda-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="76bda-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="76bda-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="76bda-121">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="76bda-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="76bda-122">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="76bda-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="76bda-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="76bda-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 