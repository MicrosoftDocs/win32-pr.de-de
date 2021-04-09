---
title: ListBox-Steuerelement (Menüs und andere Ressourcen)
description: Definiert häufig verwendete Steuerelemente für ein Dialogfeld oder Fenster. Das-Steuerelement ist ein Rechteck, das eine Liste von Zeichen folgen enthält (z. b. Dateinamen), aus denen der Benutzer auswählen kann.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- ListBox-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101607"
---
# <a name="listbox-control"></a><span data-ttu-id="5c26e-105">ListBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5c26e-105">LISTBOX control</span></span>

<span data-ttu-id="5c26e-106">Definiert häufig verwendete Steuerelemente für ein Dialogfeld oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="5c26e-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="5c26e-107">Das-Steuerelement ist ein Rechteck, das eine Liste von Zeichen folgen enthält (z. b. Dateinamen), aus denen der Benutzer auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="5c26e-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="5c26e-108">Die **ListBox** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -oder **Window** -Anweisung verwendet werden kann, definiert den Bezeichner, die Dimensionen und die Attribute eines Steuerelement Fensters.</span><span class="sxs-lookup"><span data-stu-id="5c26e-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="5c26e-109"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="5c26e-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="5c26e-110">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="5c26e-110">Control styles.</span></span> <span data-ttu-id="5c26e-111">Bei diesem Wert kann es sich um eine Kombination der Listenfeld Klassen Stile und eines der folgenden Stile handeln: **WS \_ Border** und **WS \_ VScroll**.</span><span class="sxs-lookup"><span data-stu-id="5c26e-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="5c26e-112">Wenn Sie keinen Stil angeben, ist der Standardstil `LBS_NOTIFY | WS_BORDER` .</span><span class="sxs-lookup"><span data-stu-id="5c26e-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="5c26e-113">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5c26e-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c26e-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c26e-114">Examples</span></span>

<span data-ttu-id="5c26e-115">In diesem Beispiel wird ein Listenfeld-Steuerelement definiert, dessen Bezeichner 101 ist:</span><span class="sxs-lookup"><span data-stu-id="5c26e-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="5c26e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c26e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c26e-117">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="5c26e-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="5c26e-118">Listenfelder</span><span class="sxs-lookup"><span data-stu-id="5c26e-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 