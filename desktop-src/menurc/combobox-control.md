---
title: ComboBox-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Kombinations Feld-Steuerelement (ein Kombinations Feld).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menüs für ComboBox-Steuerelemente und andere Ressourcen
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390209"
---
# <a name="combobox-control"></a><span data-ttu-id="d88ea-104">ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d88ea-104">COMBOBOX control</span></span>

<span data-ttu-id="d88ea-105">Definiert ein Kombinations Feld-Steuerelement (ein Kombinations Feld).</span><span class="sxs-lookup"><span data-stu-id="d88ea-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="d88ea-106">Ein Kombinations Feld besteht aus einem statischen Textfeld oder einem Bearbeitungsfeld, das mit einem Listenfeld kombiniert ist.</span><span class="sxs-lookup"><span data-stu-id="d88ea-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="d88ea-107">Das Listenfeld kann jederzeit angezeigt oder vom Benutzer abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d88ea-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="d88ea-108">Wenn das Kombinations Feld ein statisches Textfeld enthält, zeigt das Textfeld immer die Auswahl (sofern vorhanden) im Listenfeld Bereich des Kombinations Felds an.</span><span class="sxs-lookup"><span data-stu-id="d88ea-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="d88ea-109">Wenn ein Bearbeitungsfeld verwendet wird, kann der Benutzer die gewünschte Auswahl eingeben. im Listenfeld wird das erste Element (sofern vorhanden) hervorgehoben, das dem entspricht, was der Benutzer im Bearbeitungsfeld eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d88ea-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="d88ea-110">Der Benutzer kann dann das im Listenfeld hervorgehobene Element auswählen, um die Auswahl abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d88ea-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="d88ea-111">Außerdem kann das Kombinations Feld vom Besitzer gezeichnet werden und eine Höhe mit fester oder variabler Höhe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d88ea-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="d88ea-112"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="d88ea-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="d88ea-113">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="d88ea-113">Control styles.</span></span> <span data-ttu-id="d88ea-114">Bei diesem Wert kann es sich um eine Kombination der ComboBox-Klassen Stile und eines der folgenden Stile handeln: " **WS \_ Tabstopps**", " **WS \_ Group**", " **WS \_ VScroll**" und " **WS \_ deaktiviert**".</span><span class="sxs-lookup"><span data-stu-id="d88ea-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="d88ea-115">Wenn Sie keinen Stil angeben, ist der Standardstil `CBS_SIMPLE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="d88ea-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="d88ea-116">Der *height* -Parameter gilt für die Höhe eines Kombinations Felds, in dem eine Dropdown Liste vollständig erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="d88ea-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="d88ea-117">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d88ea-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d88ea-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d88ea-118">Examples</span></span>

<span data-ttu-id="d88ea-119">In diesem Beispiel wird ein Kombinations Feld-Steuerelement mit einer vertikalen Scrollleiste definiert:</span><span class="sxs-lookup"><span data-stu-id="d88ea-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="d88ea-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d88ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88ea-121">Kombinations Felder</span><span class="sxs-lookup"><span data-stu-id="d88ea-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 