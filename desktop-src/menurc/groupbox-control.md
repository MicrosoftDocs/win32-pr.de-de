---
title: GroupBox-Steuerelement (Menüs und andere Ressourcen)
description: Definiert ein Gruppenfeld-Steuerelement. Das-Steuerelement ist ein Rechteck, in dem andere Steuerelemente gruppiert werden. Die Steuerelemente werden gruppiert, indem Sie einen Rahmen herum zeichnen und den angegebenen Text in der oberen linken Ecke anzeigen.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- GroupBox-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104038301"
---
# <a name="groupbox-control"></a><span data-ttu-id="22827-106">GroupBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="22827-106">GROUPBOX control</span></span>

<span data-ttu-id="22827-107">Definiert ein Gruppenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="22827-107">Defines a group box control.</span></span> <span data-ttu-id="22827-108">Das-Steuerelement ist ein Rechteck, in dem andere Steuerelemente gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="22827-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="22827-109">Die Steuerelemente werden gruppiert, indem Sie einen Rahmen herum zeichnen und den angegebenen Text in der oberen linken Ecke anzeigen.</span><span class="sxs-lookup"><span data-stu-id="22827-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="22827-110">Die **GroupBox** -Anweisung, die Sie nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwenden können, definiert den Text, den Bezeichner, die Dimensionen und die Attribute eines Steuerelement Fensters.</span><span class="sxs-lookup"><span data-stu-id="22827-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="22827-111"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="22827-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="22827-112">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="22827-112">Control styles.</span></span> <span data-ttu-id="22827-113">Bei diesem Wert kann es sich um eine Kombination aus der Schaltfläche "Class Style" der Schaltfläche " **\_ GroupBox** **" und den Stilen " \_** **WS \_ Tabstopps** "</span><span class="sxs-lookup"><span data-stu-id="22827-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="22827-114">Wenn Sie keinen Stil angeben, ist der Standardstil " **SB \_ GroupBox**".</span><span class="sxs-lookup"><span data-stu-id="22827-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="22827-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="22827-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22827-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22827-116">Remarks</span></span>

<span data-ttu-id="22827-117">Wenn der Stil **WS \_ Tabstopps** enthält oder der Text eine Zugriffstaste angibt, verschiebt die Tab-Taste oder das Drücken der Tastenkombination den Fokus auf das erste Steuerelement in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="22827-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="22827-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22827-118">Examples</span></span>

<span data-ttu-id="22827-119">In diesem Beispiel wird ein Gruppenfeld-Steuerelement mit der Bezeichnung "Options" definiert:</span><span class="sxs-lookup"><span data-stu-id="22827-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="22827-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22827-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22827-121">Gruppenfelder</span><span class="sxs-lookup"><span data-stu-id="22827-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




