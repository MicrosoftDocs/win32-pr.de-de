---
title: Skin-Definitionsdatei
description: Skin-Definitionsdatei
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Windows Media Player Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340635"
---
# <a name="skin-definition-file"></a><span data-ttu-id="9309f-107">Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="9309f-107">Skin Definition File</span></span>

<span data-ttu-id="9309f-108">Skin-Definitions Dateien enthalten die grundlegenden Anweisungen, wie die Skin funktioniert und welche anderen von der Skin verwendeten Dateien gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="9309f-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="9309f-109">Es kann nur eine Skin-Definitionsdatei für einen Skin vorhanden sein, die die Dateinamenerweiterung. WMS enthält.</span><span class="sxs-lookup"><span data-stu-id="9309f-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="9309f-110">Die Anweisungen in der Skin-Definitionsdatei werden in Extensible Markup Language (XML) geschrieben, die HTML ähnelt.</span><span class="sxs-lookup"><span data-stu-id="9309f-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="9309f-111">Wenn Sie zum Erstellen von Webseiten HTML verwendet haben, werden Sie feststellen, dass XML vertraut ist.</span><span class="sxs-lookup"><span data-stu-id="9309f-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="9309f-112">Der XML-Code in der Skin-Definitionsdatei verwendet einen Satz von speziellen Element Tags, um Teile der Skin-Benutzeroberfläche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9309f-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="9309f-113">Beispielsweise definiert das [Button](button-element.md) -Element, wie sich eine Schaltfläche verhält, wo Sie angezeigt wird und wie Sie aussehen soll.</span><span class="sxs-lookup"><span data-stu-id="9309f-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="9309f-114">Jedes Elementtag weist bestimmte Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="9309f-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="9309f-115">Beispielsweise verfügt das [Button](button-element.md) -Element über ein **Image** -Attribut, das definiert, wo das Bild für die Schaltfläche gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="9309f-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="9309f-116">Dies ähnelt HTML, wobei das Body-Element über ein **BgColor** -Attribut verfügt, das die Hintergrundfarbe der HTML-Seite definiert.</span><span class="sxs-lookup"><span data-stu-id="9309f-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="9309f-117">Ausführliche Informationen zu allen Skin-Elementen und deren Attributen finden Sie im Abschnitt zur Design- [Programmier Referenz](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9309f-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="9309f-118">XML hat einige einfache Regeln, die Sie zum Erstellen von Skins kennen müssen.</span><span class="sxs-lookup"><span data-stu-id="9309f-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="9309f-119">Im Gegensatz zu HTML erfordert XML, dass Sie die Regeln genau befolgen.</span><span class="sxs-lookup"><span data-stu-id="9309f-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="9309f-120">Einschließen von Elementen mit spitzen Klammern</span><span class="sxs-lookup"><span data-stu-id="9309f-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="9309f-121">Alle Elemente werden in spitzen Klammern eingeschlossen. Beispielsweise ist das **Button** -Element wie folgt typisiert:</span><span class="sxs-lookup"><span data-stu-id="9309f-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="9309f-122">Sie müssen das Wort "Button" nicht in Großbuchstaben eingeben, aber die Konvention zum Eingeben von Elementnamen in Großbuchstaben wird im Beispielcode dieses SDK verwendet.</span><span class="sxs-lookup"><span data-stu-id="9309f-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="9309f-123">Attribute vor der schließenden Klammer platzieren</span><span class="sxs-lookup"><span data-stu-id="9309f-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="9309f-124">Alle Attribute für ein bestimmtes Element müssen vor der schließenden Spitze Klammer eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9309f-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="9309f-125">Ein Attribut besteht aus dem Attributnamen, gefolgt von einem Gleichheitszeichen (=) und dem Wert des Attributs in Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="9309f-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="9309f-126">Sie müssen das Wort "Image" nicht in Kleinbuchstaben eingeben, aber die Konvention der Typisierung von Attributnamen in Kleinbuchstaben wird im Beispielcode dieses SDK verwendet.</span><span class="sxs-lookup"><span data-stu-id="9309f-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="9309f-127">Beachten Sie außerdem, dass der Wert des-Attributs in Anführungszeichen eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9309f-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="9309f-128">Öffnende und schließende Elemente</span><span class="sxs-lookup"><span data-stu-id="9309f-128">Opening and Closing Elements</span></span>

<span data-ttu-id="9309f-129">Einige Elemente werden in einem anderen Element gruppiert.</span><span class="sxs-lookup"><span data-stu-id="9309f-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="9309f-130">Beispielsweise ist das **ButtonGroup** -Element nicht sehr sinnvoll, es sei denn, Sie verwenden ein oder mehrere **ButtonElement** -Elemente.</span><span class="sxs-lookup"><span data-stu-id="9309f-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="9309f-131">Um die Gruppierung klar zu machen, müssen Sie für jedes Element über ein öffnendes und ein Schließ Endes Tag verfügen.</span><span class="sxs-lookup"><span data-stu-id="9309f-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="9309f-132">Das öffnende Tag ist nur der Elementname und alle zugehörigen Attribute in spitzen Klammern.</span><span class="sxs-lookup"><span data-stu-id="9309f-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="9309f-133">Das schließende Tag ist der Elementname, dem ein Schrägstrich (/) vorangestellt und dann durch spitzen Klammern eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9309f-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="9309f-134">Beispielsweise sieht das öffnende Tag des **ButtonGroup** -Elements wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9309f-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="9309f-135">Das schließende **ButtonGroup** -Tag sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9309f-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="9309f-136">Sie würden die **ButtonElement** -Tags zwischen den öffnenden und schließenden **ButtonGroup** -Element Tags platzieren.</span><span class="sxs-lookup"><span data-stu-id="9309f-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="9309f-137">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9309f-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="9309f-138">Schließen von Elementen</span><span class="sxs-lookup"><span data-stu-id="9309f-138">Closing Off Elements</span></span>

<span data-ttu-id="9309f-139">Wenn ein Element keine anderen Elemente enthält, müssen Sie einen Schrägstrich am Ende des Element namens direkt vor der schließenden Spitze Klammer platzieren.</span><span class="sxs-lookup"><span data-stu-id="9309f-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="9309f-140">Im obigen Code hat jedes **ButtonElement** -Element z. b. einen Schrägstrich, um anzugeben, dass keine anderen Elemente geschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="9309f-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="9309f-141">Mit anderen Worten, Sie müssen entweder ein Schließ Endes Elementtag haben oder das Element mit einem Schrägstrich schließen.</span><span class="sxs-lookup"><span data-stu-id="9309f-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="9309f-142">Dies ist richtig:</span><span class="sxs-lookup"><span data-stu-id="9309f-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="9309f-143">Dies ist nicht korrekt:</span><span class="sxs-lookup"><span data-stu-id="9309f-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="9309f-144">Dies ist auch nicht korrekt:</span><span class="sxs-lookup"><span data-stu-id="9309f-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="9309f-145">Der folgende Abschnitt enthält weitere Informationen zu Skin-Definitions Dateien:</span><span class="sxs-lookup"><span data-stu-id="9309f-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="9309f-146">Struktur der Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="9309f-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="9309f-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9309f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9309f-148">**Skin-Dateien**</span><span class="sxs-lookup"><span data-stu-id="9309f-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




