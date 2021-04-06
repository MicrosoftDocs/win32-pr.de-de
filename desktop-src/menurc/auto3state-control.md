---
title: AUTO3STATE-Steuerelement
description: Definiert ein automatisches Kontrollkästchen mit drei Zuständen.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- AUTO3STATE-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101558"
---
# <a name="auto3state-control"></a><span data-ttu-id="d1c73-104">AUTO3STATE-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d1c73-104">AUTO3STATE control</span></span>

<span data-ttu-id="d1c73-105">Definiert ein automatisches Kontrollkästchen mit drei Zuständen.</span><span class="sxs-lookup"><span data-stu-id="d1c73-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="d1c73-106">Das-Steuerelement ist ein geöffnetes Feld mit dem angegebenen Text, der rechts neben dem Feld positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="d1c73-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="d1c73-107">Wenn diese Option ausgewählt ist, wechselt das Feld automatisch zwischen drei Zuständen: aktiviert, deaktiviert und deaktiviert (grau).</span><span class="sxs-lookup"><span data-stu-id="d1c73-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="d1c73-108">Das-Steuerelement sendet eine Meldung an das übergeordnete Element, wenn der Benutzer das Steuerelement auswählt.</span><span class="sxs-lookup"><span data-stu-id="d1c73-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="d1c73-109"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="d1c73-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="d1c73-110">Stile für das-Steuerelement, bei dem es sich um eine Kombination aus dem **\_ AUTO3STATE** -Format und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ Deaktivierte** und **WS- \_ Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="d1c73-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="d1c73-111">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTO3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="d1c73-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="d1c73-112">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d1c73-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d1c73-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1c73-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c73-114">**AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="d1c73-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="d1c73-115">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="d1c73-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="d1c73-116">**Markieren**</span><span class="sxs-lookup"><span data-stu-id="d1c73-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="d1c73-117">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="d1c73-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="d1c73-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="d1c73-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="d1c73-119">Fensterstile</span><span class="sxs-lookup"><span data-stu-id="d1c73-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 