---
title: ScrollBar-Steuerelement
description: Definiert ein ScrollBar-Steuerelement.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- ScrollBar-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101635"
---
# <a name="scrollbar-control"></a><span data-ttu-id="65989-104">ScrollBar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="65989-104">SCROLLBAR control</span></span>

<span data-ttu-id="65989-105">Definiert ein ScrollBar-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="65989-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="65989-106">Das-Steuerelement ist ein Rechteck, das ein Bild Lauf Feld mit Richtungs Pfeilen an beiden Enden enthält.</span><span class="sxs-lookup"><span data-stu-id="65989-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="65989-107">Das Bild Lauf leisten-Steuerelement sendet eine Benachrichtigungs Meldung an das übergeordnete Element, wenn der Benutzer im Steuerelement auf die Maus klickt.</span><span class="sxs-lookup"><span data-stu-id="65989-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="65989-108">Das übergeordnete Element ist für das Aktualisieren der scrollfeldposition verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="65989-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="65989-109">Bild Lauf leisten-Steuerelemente können an beliebiger Stelle in einem Fenster positioniert und bei Bedarf verwendet werden, um scrolleingaben bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="65989-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="65989-110"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="65989-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="65989-111">NULL oder eine Kombination der folgenden Stile: **WS \_ Tabstopps**, **WS \_ Group** und **WS \_ deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="65989-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="65989-112">Zusätzlich zu diesen Stilen kann der *Style* -Parameter eine Kombination (oder keine) der ScrollBar-Klassen Stile enthalten.</span><span class="sxs-lookup"><span data-stu-id="65989-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="65989-113">Wenn Sie keinen Stil angeben, ist der Standardstil **SSB \_ Horz**.</span><span class="sxs-lookup"><span data-stu-id="65989-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="65989-114">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="65989-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="65989-115">Beachten Sie, dass Sie für dieses Steuerelement keinen Text angeben können.</span><span class="sxs-lookup"><span data-stu-id="65989-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="65989-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65989-116">Examples</span></span>

<span data-ttu-id="65989-117">Im folgenden Beispiel wird die Verwendung der **ScrollBar** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="65989-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="65989-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65989-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65989-119">Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="65989-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 