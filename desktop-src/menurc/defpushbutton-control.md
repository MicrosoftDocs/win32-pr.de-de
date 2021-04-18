---
title: DEFPUSHBUTTON-Steuerelement
description: Definiert ein Standardmäßiges Push-Button-Steuerelement.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- DEFPUSHBUTTON-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338233"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="a6b8f-104">DEFPUSHBUTTON-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a6b8f-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="a6b8f-105">Definiert ein Standardmäßiges Push-Button-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a6b8f-105">Defines a default push-button control.</span></span> <span data-ttu-id="a6b8f-106">Das-Steuerelement ist ein kleines Rechteck mit einem fetten Umriss, der die Standardantwort für den Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6b8f-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="a6b8f-107">Der angegebene Text wird in der Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6b8f-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="a6b8f-108">Das-Steuerelement hebt die Schaltfläche auf die übliche Weise hervor, wenn der Benutzer mit der Maus darauf klickt und eine Meldung an das übergeordnete Fenster sendet.</span><span class="sxs-lookup"><span data-stu-id="a6b8f-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a6b8f-109"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="a6b8f-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="a6b8f-110">Text, der im rechteckigen Bereich des-Steuer Elements zentriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6b8f-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="a6b8f-111"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="a6b8f-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a6b8f-112">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="a6b8f-112">Control styles.</span></span> <span data-ttu-id="a6b8f-113">Bei diesem Wert kann es sich um eine Kombination der folgenden Stile handeln: " **SB \_ DEFPUSHBUTTON**", " **WS \_ Tabstopps**", " **WS \_ Group**" und " **WS \_**"</span><span class="sxs-lookup"><span data-stu-id="a6b8f-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="a6b8f-114">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_DEFPUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="a6b8f-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="a6b8f-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a6b8f-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a6b8f-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6b8f-116">Examples</span></span>

<span data-ttu-id="a6b8f-117">In diesem Beispiel wird ein Standardmäßiges Push-Button-Steuerelement mit der Bezeichnung Abbrechen definiert:</span><span class="sxs-lookup"><span data-stu-id="a6b8f-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="a6b8f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6b8f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b8f-119">Pushschaltflächen</span><span class="sxs-lookup"><span data-stu-id="a6b8f-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="a6b8f-120">**PUSHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="a6b8f-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="a6b8f-121">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="a6b8f-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




