---
title: AUTOCHECKBOX-Steuerelement
description: Definiert ein automatisches Kontrollkästchen-Steuerelement.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menüs für AUTOCHECKBOX-Steuerelemente und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725560"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="c208e-104">AUTOCHECKBOX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c208e-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="c208e-105">Definiert ein automatisches Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c208e-105">Defines an automatic check box control.</span></span> <span data-ttu-id="c208e-106">Das-Steuerelement ist ein kleines Rechteck (Kontrollkästchen), das neben dem angegebenen Text angezeigt wird (in der Regel rechts).</span><span class="sxs-lookup"><span data-stu-id="c208e-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="c208e-107">Wenn der Benutzer das Steuerelement auswählt, hebt das-Steuerelement das Rechteck hervor und sendet eine Meldung an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="c208e-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="c208e-108">Die **AUTOCHECKBOX** -Anweisung kann nur im Text einer [**Dialog**](dialog-resource.md) -oder [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c208e-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="c208e-109"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="c208e-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="c208e-110">Stile des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c208e-110">Styles of the control.</span></span> <span data-ttu-id="c208e-111">Bei diesem Wert kann es sich um eine Kombination aus der Schaltfläche "Button" der Schaltfläche " **\_ AUTOCHECKBOX** " und " **WS \_ Tabstopps** " und " **WS \_**</span><span class="sxs-lookup"><span data-stu-id="c208e-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="c208e-112">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTOCHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="c208e-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="c208e-113">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c208e-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c208e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c208e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c208e-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="c208e-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="c208e-116">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="c208e-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="c208e-117">**Markieren**</span><span class="sxs-lookup"><span data-stu-id="c208e-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="c208e-118">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="c208e-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="c208e-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="c208e-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 