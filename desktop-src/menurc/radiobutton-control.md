---
title: RadioButton-Steuerelement
description: Definiert ein Optionsfeld-Steuerelement.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- RadioButton-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038989"
---
# <a name="radiobutton-control"></a><span data-ttu-id="e4494-104">RadioButton-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e4494-104">RADIOBUTTON control</span></span>

<span data-ttu-id="e4494-105">Definiert ein Optionsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e4494-105">Defines a radio-button control.</span></span> <span data-ttu-id="e4494-106">Das-Steuerelement ist ein kleiner Kreis, in dem der angegebene Text daneben in der Regel rechts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e4494-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="e4494-107">Das-Steuerelement hebt den Kreis hervor und sendet eine Meldung an das übergeordnete Fenster, wenn der Benutzer die Schaltfläche auswählt.</span><span class="sxs-lookup"><span data-stu-id="e4494-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="e4494-108">Das-Steuerelement entfernt die Hervorhebung und sendet eine Meldung, wenn die Schaltfläche das nächste Mal ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e4494-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="e4494-109"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="e4494-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="e4494-110">Stile für das Optionsfeld, bei dem es sich um eine Kombination aus Schaltflächen Klassen Formaten und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ Deaktivierte** und **WS- \_ Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="e4494-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="e4494-111">Wenn Sie keinen Stil angeben, ist der Standardstil `BS_RADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="e4494-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="e4494-112">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e4494-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e4494-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4494-113">Examples</span></span>

<span data-ttu-id="e4494-114">Im folgenden Beispiel wird die Verwendung der **RadioButton** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="e4494-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="e4494-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4494-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4494-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="e4494-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="e4494-117">Options Felder</span><span class="sxs-lookup"><span data-stu-id="e4494-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 