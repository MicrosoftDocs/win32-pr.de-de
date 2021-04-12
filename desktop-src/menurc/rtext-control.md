---
title: Rtext-Steuerelement
description: Definiert ein rechts Bündiges Text Steuerelement.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Rtext-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473093"
---
# <a name="rtext-control"></a><span data-ttu-id="a0b9b-104">Rtext-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a0b9b-104">RTEXT control</span></span>

<span data-ttu-id="a0b9b-105">Definiert ein rechts Bündiges Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="a0b9b-106">Das-Steuerelement ist ein einfaches Rechteck, das den angegebenen Text rechtsbündig im Rechteck anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="a0b9b-107">Der Text wird formatiert, bevor er angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="a0b9b-108">Wörter, die über das Ende einer Linie hinaus erweitert werden, werden automatisch an den Anfang der nächsten Zeile umschließt.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="a0b9b-109">Wörter, die länger als die Breite des Steuer Elements sind, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="a0b9b-110">Die **rtext** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a0b9b-111"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="a0b9b-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a0b9b-112">Stile für das Text Steuerelement, bei denen es sich um eine beliebige Kombination der folgenden Typen handeln kann: **WS \_ Tabstopps** und **WS- \_ Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="a0b9b-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="a0b9b-113">Wenn Sie keinen Stil angeben, ist der Standardstil `SS_RIGHT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="a0b9b-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="a0b9b-114">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a0b9b-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a0b9b-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0b9b-115">Examples</span></span>

<span data-ttu-id="a0b9b-116">Im folgenden Beispiel wird die Verwendung der **rtext** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="a0b9b-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="a0b9b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0b9b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b9b-118">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="a0b9b-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="a0b9b-119">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="a0b9b-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="a0b9b-120">Steuerelemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="a0b9b-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="a0b9b-121">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="a0b9b-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 