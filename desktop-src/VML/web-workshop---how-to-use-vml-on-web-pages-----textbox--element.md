---
title: Verwenden des TextBox-Elements
description: Verwenden des TextBox-Elements
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Webworkshop, TextBox-Element
- Entwerfen von Webseiten, TextBox-Element
- Vector Markup Language (VML), TextBox-Element
- VML (Vector Markup Language), TextBox-Element
- Vektorgrafiken, TextBox-Element
- Textfeld-Element
- VML-Elemente, TextBox
- VML-Formen, TextBox-Element
- Vector Markup Language (VML), Anfügen von Text
- VML (Vector Markup Language), Anfügen von Text
- Vektorgrafiken, Anfügen von Text
- VML-Formen, Anfügen von Text
- Anfügen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474124"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="c5a4b-116">Verwenden des TextBox-Elements</span><span class="sxs-lookup"><span data-stu-id="c5a4b-116">Using the Textbox Element</span></span>

<span data-ttu-id="c5a4b-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c5a4b-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5a4b-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c5a4b-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5a4b-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c5a4b-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5a4b-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c5a4b-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5a4b-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5a4b-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5a4b-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5a4b-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="c5a4b-123">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="c5a4b-123">Examples:</span></span>

<span data-ttu-id="c5a4b-124">Um Text an ein Rechteck anzufügen, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:</span><span class="sxs-lookup"><span data-stu-id="c5a4b-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="c5a4b-125">Um einen Hyperlink an ein abgerundetes Rechteck anzufügen, das mit einem Farbverlauf gefüllt ist, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:</span><span class="sxs-lookup"><span data-stu-id="c5a4b-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![textbox2.gif (1147 Bytes)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





<span data-ttu-id="c5a4b-127">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span><span class="sxs-lookup"><span data-stu-id="c5a4b-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 