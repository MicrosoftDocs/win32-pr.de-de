---
title: CTEXT-Steuerelement
description: Definiert ein zentriertes Text Steuerelement.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- CTEXT-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101554"
---
# <a name="ctext-control"></a><span data-ttu-id="43128-104">CTEXT-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="43128-104">CTEXT control</span></span>

<span data-ttu-id="43128-105">Definiert ein zentriertes Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="43128-105">Defines a centered-text control.</span></span> <span data-ttu-id="43128-106">Das-Steuerelement ist ein einfaches Rechteck, das den angegebenen Text anzeigt, der im Rechteck zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="43128-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="43128-107">Der Text wird formatiert, bevor er angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="43128-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="43128-108">Wörter, die über das Ende einer Linie hinaus erweitert werden, werden automatisch an den Anfang der nächsten Zeile umschließt.</span><span class="sxs-lookup"><span data-stu-id="43128-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="43128-109">Wörter, die länger als die Breite des Steuer Elements sind, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="43128-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="43128-110">Die [**LTEXT**](ltext-control.md) -Anweisung, die nur in einer Rep-Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="43128-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="43128-111"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="43128-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="43128-112">Text, der im rechteckigen Bereich des-Steuer Elements zentriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="43128-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="43128-113"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="43128-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="43128-114">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="43128-114">Control styles.</span></span> <span data-ttu-id="43128-115">Bei diesem Wert kann es sich um eine beliebige Kombination der folgenden Stile handeln: **SS \_ Center**, **WS \_ Tabstopps** und **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="43128-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="43128-116">Wenn Sie keinen Stil angeben, ist der Standardstil `SS_CENTER | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="43128-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="43128-117">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="43128-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="43128-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43128-118">Examples</span></span>

<span data-ttu-id="43128-119">In diesem Beispiel wird ein zentriert-Text-Steuerelement mit der Bezeichnung "filename" definiert:</span><span class="sxs-lookup"><span data-stu-id="43128-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="43128-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43128-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43128-121">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="43128-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="43128-122">Steuerelemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="43128-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="43128-123">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="43128-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="43128-124">**Rtext**</span><span class="sxs-lookup"><span data-stu-id="43128-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 