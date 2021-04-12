---
title: Symbol Steuerelement
description: Definiert ein Symbol Steuerelement. Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Symbol Steuerungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471917"
---
# <a name="icon-control"></a><span data-ttu-id="a85d5-105">Symbol Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a85d5-105">ICON control</span></span>

<span data-ttu-id="a85d5-106">Definiert ein Symbol Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a85d5-106">Defines an icon control.</span></span> <span data-ttu-id="a85d5-107">Dieses Steuerelement ist ein Symbol, das in einem Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a85d5-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="a85d5-108">Die **Symbol** Steuerungs Anweisung, die Sie nur in einer [**DIALOGEX**](dialogex-resource.md) -Anweisung verwenden können, definiert den Symbol Ressourcen Bezeichner, den Symbol Steuerelement Bezeichner, die Position und die Attribute eines Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="a85d5-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a85d5-109"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="a85d5-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="a85d5-110">Der Name eines Symbols (kein Dateiname), der an anderer Stelle in der Ressourcen Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a85d5-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="a85d5-111"><span id="width"></span><span id="WIDTH"></span>*Breite*</span><span class="sxs-lookup"><span data-stu-id="a85d5-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="a85d5-112">Dieser Wert wird ignoriert und sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a85d5-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a85d5-113"><span id="height"></span><span id="HEIGHT"></span>*Flugh*</span><span class="sxs-lookup"><span data-stu-id="a85d5-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="a85d5-114">Dieser Wert wird ignoriert und sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a85d5-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a85d5-115"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="a85d5-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a85d5-116">Steuerelement Stil.</span><span class="sxs-lookup"><span data-stu-id="a85d5-116">Control style.</span></span> <span data-ttu-id="a85d5-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a85d5-117">This parameter is optional.</span></span> <span data-ttu-id="a85d5-118">Der einzige Wert, der angegeben werden kann, ist der **SS- \_** Symbolstil.</span><span class="sxs-lookup"><span data-stu-id="a85d5-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="a85d5-119">Dies ist der Standardstil, unabhängig davon, ob dieser Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a85d5-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="a85d5-120">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a85d5-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a85d5-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a85d5-121">Examples</span></span>

<span data-ttu-id="a85d5-122">In diesem Beispiel wird ein Symbol Steuerelement definiert, dessen Symbol Bezeichner 901 und dessen Name "myIcon" lautet:</span><span class="sxs-lookup"><span data-stu-id="a85d5-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="a85d5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a85d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85d5-124">**Angezeigt**</span><span class="sxs-lookup"><span data-stu-id="a85d5-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 




