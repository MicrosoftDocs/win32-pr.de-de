---
title: VML-Klassen Attribut
description: VML-Klassen Attribut
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948905"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="d2aad-103">VML-Klassen Attribut</span><span class="sxs-lookup"><span data-stu-id="d2aad-103">VML Class Attribute</span></span>

<span data-ttu-id="d2aad-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d2aad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d2aad-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d2aad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d2aad-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d2aad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d2aad-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d2aad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d2aad-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d2aad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d2aad-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d2aad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d2aad-110">Verweist auf eine Definition eines CSS-Stils.</span><span class="sxs-lookup"><span data-stu-id="d2aad-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="d2aad-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d2aad-111">Read/write.</span></span> <span data-ttu-id="d2aad-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="d2aad-112">**String**.</span></span>

<span data-ttu-id="d2aad-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="d2aad-113">**Applies To**</span></span>

[<span data-ttu-id="d2aad-114">Form</span><span class="sxs-lookup"><span data-stu-id="d2aad-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d2aad-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="d2aad-115">**Tag Syntax**</span></span>

<span data-ttu-id="d2aad-116"><v: *Element* Class = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d2aad-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="d2aad-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="d2aad-117">**Script Syntax**</span></span>

<span data-ttu-id="d2aad-118">*Element* . ClassName = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="d2aad-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="d2aad-119">*Ausdruck* = *Element*. ClassName</span><span class="sxs-lookup"><span data-stu-id="d2aad-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="d2aad-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="d2aad-120">**Remarks**</span></span>

<span data-ttu-id="d2aad-121">Das **Class** -Attribut ähnelt dem Standard-HTML- **Klassen** Attribut, das mit CSS-Stylesheets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2aad-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="d2aad-122">Beachten Sie, dass **className** anstelle der- **Klasse** für die Skripterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2aad-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="d2aad-123">Beachten Sie außerdem, dass für die Skripterstellung nur der **Klassenname** gelesen werden kann. Wenn Sie den Wert von **className** ändern, wird das Rendering der Form nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d2aad-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="d2aad-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="d2aad-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d2aad-125">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="d2aad-125">**See Also**</span></span>

[<span data-ttu-id="d2aad-126">Form</span><span class="sxs-lookup"><span data-stu-id="d2aad-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d2aad-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="d2aad-127">**Example**</span></span>

<span data-ttu-id="d2aad-128">Eine Klasse für die **Breite** wird mit dem Stil erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2aad-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="d2aad-129">Dann wird auf die Breite durch Einschließen des Stils verwiesen.</span><span class="sxs-lookup"><span data-stu-id="d2aad-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="d2aad-130">Beachten Sie, dass die Width-und Height-Eigenschaft nicht im **Style** -Attribut definiert ist, sondern durch den-Stil definiert wird.</span><span class="sxs-lookup"><span data-stu-id="d2aad-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="d2aad-131">Beachten Sie, dass die **Klasse** nur auf CSS-Type-Attribute angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2aad-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 