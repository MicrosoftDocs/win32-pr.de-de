---
title: PUSHBUTTON-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Push-Button-Steuerelement. Das-Steuerelement ist ein Rechteck mit runden Kurven, das den angegebenen Text enthält. Der Text wird im-Steuerelement zentriert. Das-Steuerelement sendet eine Meldung an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menüs für PUSHBUTTON-Steuerelemente und andere Ressourcen
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315129"
---
# <a name="pushbutton-control"></a><span data-ttu-id="b9c66-107">PUSHBUTTON-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b9c66-107">PUSHBUTTON control</span></span>

<span data-ttu-id="b9c66-108">Definiert ein Push-Button-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="b9c66-108">Defines a push-button control.</span></span> <span data-ttu-id="b9c66-109">Das-Steuerelement ist ein Rechteck mit runden Kurven, das den angegebenen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="b9c66-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="b9c66-110">Der Text wird im-Steuerelement zentriert.</span><span class="sxs-lookup"><span data-stu-id="b9c66-110">The text is centered in the control.</span></span> <span data-ttu-id="b9c66-111">Das-Steuerelement sendet eine Meldung an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.</span><span class="sxs-lookup"><span data-stu-id="b9c66-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b9c66-112"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="b9c66-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b9c66-113">Stile für die PUSHBUTTON-Datei, bei der es sich um eine Kombination aus der Art der Karten **Schaltfläche \_** und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ deaktiviert** und **WS- \_ Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="b9c66-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="b9c66-114">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_PUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="b9c66-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="b9c66-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b9c66-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9c66-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9c66-116">Examples</span></span>

<span data-ttu-id="b9c66-117">Im folgenden Beispiel wird die Verwendung der **PUSHBUTTON** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b9c66-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="b9c66-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9c66-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c66-119">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="b9c66-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="b9c66-120">Pushschaltflächen</span><span class="sxs-lookup"><span data-stu-id="b9c66-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 