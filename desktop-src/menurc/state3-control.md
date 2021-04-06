---
title: STATE3-Steuerelement
description: Definiert ein Kontrollkästchen-Steuerelement mit drei Zuständen. Das Steuerelement ist mit einem Kontrollkästchen identisch, mit dem Unterschied, dass drei Zustände aktiviert, deaktiviert und deaktiviert (grau) sind.
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- STATE3-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718131"
---
# <a name="state3-control"></a><span data-ttu-id="2445f-105">STATE3-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2445f-105">STATE3 control</span></span>

<span data-ttu-id="2445f-106">Definiert ein Kontrollkästchen-Steuerelement mit drei Zuständen.</span><span class="sxs-lookup"><span data-stu-id="2445f-106">Defines a three-state check box control.</span></span> <span data-ttu-id="2445f-107">Das Steuerelement ist mit einem [**Kontrollkästchen**](checkbox-control.md)identisch, mit dem Unterschied, dass es drei Zustände aufweist: aktiviert, deaktiviert und deaktiviert (grau).</span><span class="sxs-lookup"><span data-stu-id="2445f-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="2445f-108"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="2445f-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="2445f-109">Text, der auf der rechten Seite des-Steuer Elements angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2445f-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2445f-110"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="2445f-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="2445f-111">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="2445f-111">Control styles.</span></span> <span data-ttu-id="2445f-112">Bei diesem Wert kann es sich um eine Kombination der Schaltflächen Klassen Style **SB \_ 3STATE** und **WS \_ Tabstopps** und **WS- \_ Gruppen** Stile handeln.</span><span class="sxs-lookup"><span data-stu-id="2445f-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="2445f-113">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="2445f-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="2445f-114">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2445f-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2445f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2445f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2445f-116">**AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="2445f-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="2445f-117">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="2445f-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="2445f-118">**Markieren**</span><span class="sxs-lookup"><span data-stu-id="2445f-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="2445f-119">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="2445f-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




