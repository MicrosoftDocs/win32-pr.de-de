---
title: LTEXT-Steuerelement
description: Definiert ein Links Bündiges Text Steuerelement.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- LTEXT-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340702"
---
# <a name="ltext-control"></a><span data-ttu-id="843ec-104">LTEXT-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="843ec-104">LTEXT control</span></span>

<span data-ttu-id="843ec-105">Definiert ein Links Bündiges Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="843ec-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="843ec-106">Das-Steuerelement ist ein einfaches Rechteck, das den angegebenen Text linksbündig im Rechteck anzeigt.</span><span class="sxs-lookup"><span data-stu-id="843ec-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="843ec-107">Der Text wird formatiert, bevor er angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="843ec-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="843ec-108">Wörter, die über das Ende einer Linie hinaus erweitert werden, werden automatisch an den Anfang der nächsten Zeile umschließt.</span><span class="sxs-lookup"><span data-stu-id="843ec-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="843ec-109">Wörter, die länger als die Breite des Steuer Elements sind, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="843ec-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="843ec-110">Die **LTEXT** -Anweisung, die nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwendet werden kann, definiert den Text, den Bezeichner, die Dimensionen und die Attribute des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="843ec-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="843ec-111"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="843ec-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="843ec-112">Steuerelement Stile.</span><span class="sxs-lookup"><span data-stu-id="843ec-112">Control styles.</span></span> <span data-ttu-id="843ec-113">Bei diesem Wert kann es sich um eine beliebige Kombination aus dem **\_ RadioButton** -Stil von "SB" und den folgenden Stilen handeln: **SS \_ left**, **WS \_ Tabstopps** und **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="843ec-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="843ec-114">Wenn Sie keinen Stil angeben, ist der Standardstil `SS_LEFT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="843ec-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="843ec-115">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="843ec-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="843ec-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="843ec-116">Examples</span></span>

<span data-ttu-id="843ec-117">In diesem Beispiel wird ein Links Bündiges Text Steuerelement mit der Bezeichnung "filename" definiert:</span><span class="sxs-lookup"><span data-stu-id="843ec-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="843ec-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="843ec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843ec-119">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="843ec-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="843ec-120">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="843ec-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="843ec-121">Steuerelemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="843ec-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="843ec-122">**Rtext**</span><span class="sxs-lookup"><span data-stu-id="843ec-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 