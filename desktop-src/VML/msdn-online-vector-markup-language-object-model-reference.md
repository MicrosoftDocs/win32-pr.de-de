---
title: VML-Objektmodell Referenz
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039513"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="a0ab9-104">VML-Objektmodell Referenz</span><span class="sxs-lookup"><span data-stu-id="a0ab9-104">VML Object Model Reference</span></span>

<span data-ttu-id="a0ab9-105">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a0ab9-106">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a0ab9-107">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a0ab9-108">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a0ab9-109">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a0ab9-110">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a0ab9-111">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-111">In this topic:</span></span>

-   [<span data-ttu-id="a0ab9-112">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="a0ab9-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0ab9-113">Example</span></span>](#example)
-   [<span data-ttu-id="a0ab9-114">Einrichten von VML</span><span class="sxs-lookup"><span data-stu-id="a0ab9-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="a0ab9-115">VML-OM-Referenz</span><span class="sxs-lookup"><span data-stu-id="a0ab9-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="a0ab9-116">Shape-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="a0ab9-117">Unter Elemente des Shape-Elements</span><span class="sxs-lookup"><span data-stu-id="a0ab9-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="a0ab9-118">Background-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="a0ab9-119">Extrusion-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="a0ab9-120">Fill-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="a0ab9-121">Group-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="a0ab9-122">Imagedata-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="a0ab9-123">Path-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="a0ab9-124">Shadow-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="a0ab9-125">Verzerrt-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="a0ab9-126">Stroke-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="a0ab9-127">TextPath-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="a0ab9-128">Im VML-Objektmodell verwendete Datentypen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="a0ab9-129">Einführung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-129">Introduction</span></span>

<span data-ttu-id="a0ab9-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) ist eine textbasierte Sprache, die [XML](https://www.w3.org/TR/REC-xml.mdl) verwendet, um HTML zu erweitern, um Vektorgrafik Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="a0ab9-131">Der VML-Dokumentobjektmodell (DOM) definiert eine programmgesteuerte Schnittstelle für die Bearbeitung der Dokument Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="a0ab9-132">Dies ermöglicht dem Benutzer das dynamische Erstellen und Ändern von Vektorgrafiken über eine Plattform-und sprachneutrale Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="a0ab9-133">Das VML-DOM entspricht der [Dokumentobjektmodell](https://www.w3.org/TR/REC-DOM-Level-1/) Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="a0ab9-134">VML verwendet das [Shape](#shape-element) -Element als grundlegenden Baustein für Vektorgrafik Bilder.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="a0ab9-135">Nachdem eine Form erstellt wurde, können Sie die Form durch Attribute oder angefügte unter Elemente ändern.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="a0ab9-136">Um z. b. die Farbe einer Form zu ändern, weisen Sie dem **FillColor** -Attribut einen Farbwert zu.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="a0ab9-137">Einige der Attribute einer Form [sind auch unter](/windows) Elemente und verfügen über eigene Attribute, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="a0ab9-138">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0ab9-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="a0ab9-139">Schläuche</span><span class="sxs-lookup"><span data-stu-id="a0ab9-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="a0ab9-140">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="a0ab9-141">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="a0ab9-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="a0ab9-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="a0ab9-143">Pfad</span><span class="sxs-lookup"><span data-stu-id="a0ab9-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="a0ab9-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="a0ab9-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="a0ab9-145">Neigen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="a0ab9-146">Stellung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="a0ab9-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="a0ab9-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="a0ab9-148">Das VML-OM verwendet mehrere [Datentypen](/windows) , um Parameter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="a0ab9-149">Datatypes, die "VG" als Präfix haben, sind Enumerationen, und die mit dem Präfix "IVG" sind Objekte.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="a0ab9-150">Klicken Sie hier, um eine Liste zu finden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-150">Click here for a list.</span></span> <span data-ttu-id="a0ab9-151">Kleinere Datentypen sind mit bestimmten Parametern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="a0ab9-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0ab9-152">Example</span></span>

<span data-ttu-id="a0ab9-153">Der folgende VBScript-Code zeigt, wie eine einfache Form erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="a0ab9-154">Im obigen Beispiel wird eine Form mithilfe der Dokumentobjektmodell-Methode " **kreateelement**" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="a0ab9-155">Die Form ist eine vordefinierte VML-Form "Rect".</span><span class="sxs-lookup"><span data-stu-id="a0ab9-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="a0ab9-156">Obwohl das Objekt vorhanden ist, kann es nicht Teil des Dokuments sein, bis es an das Dokument angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="a0ab9-157">Mithilfe der **AppendChild** -Methode wird das Rect als untergeordnetes Element eines **div** -Elements mit dem Namen mydiv festgestellt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="a0ab9-158">Einige minimale Stil Attribute (**Position**, **Breite**, **Höhe**, **oben**, **Links**) werden festgelegt, um der Form eine bestimmte Größe zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="a0ab9-159">Schließlich wird eine Farbe mit dem **FillColor** -Attribut zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="a0ab9-160">Beachten Sie, dass jede Skriptsprache oder jede beliebige Sprache verwendet werden kann, die mit Dokumentobjektmodell-Schnittstellen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="a0ab9-161">Einrichten von VML</span><span class="sxs-lookup"><span data-stu-id="a0ab9-161">Setting up VML</span></span>

<span data-ttu-id="a0ab9-162">Eine Implementierung von VML erfolgt über Microsoft Internet Explorer 5,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="a0ab9-163">Zum ordnungsgemäßen Einrichten des renderingobjekts auf einer Webseite müssen folgende Ergänzungen vorgenommen werden:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="a0ab9-164">Das Schema muss im ersten</span><span class="sxs-lookup"><span data-stu-id="a0ab9-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="a0ab9-165">Markieren Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="a0ab9-166">Das Renderingverhalten muss Teil des Dokument Stils sein:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="a0ab9-167">Im folgenden sehen Sie eine Beispiel-HTML-Webseite, die für VML ordnungsgemäß eingerichtet wurde und die dynamische Erstellung einer Form anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="a0ab9-168">Beachten Sie, dass in Beta Versionen ein ActiveX-Objekttag und ein anderes Verhaltens Format erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="a0ab9-169">VML-OM-Referenz</span><span class="sxs-lookup"><span data-stu-id="a0ab9-169">VML OM Reference</span></span>

<span data-ttu-id="a0ab9-170">Dieser Verweis definiert die [Shape](#shape-element) -Elemente [, unter](/windows)Elemente und [Datentypen](/windows) , die vom Objektmodell von VML verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="a0ab9-171">Shape-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-171">Shape element</span></span>

<span data-ttu-id="a0ab9-172">Formen sind die Bausteine grafischer Bilder, die durch Vector Markup Language (VML) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="a0ab9-173">Die Form ist das Element der obersten Ebene, und verschiedene unter Elemente helfen dabei, die Art der einzelnen Formen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="a0ab9-174">VML bietet vordefinierte Formen:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="a0ab9-175">**Shape-Attribute**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="a0ab9-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-176">**Arc**</span></span>
-   <span data-ttu-id="a0ab9-177">**FF**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-177">**Curve**</span></span>
-   <span data-ttu-id="a0ab9-178">**Line**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-178">**Line**</span></span>
-   <span data-ttu-id="a0ab9-179">**Polylinie**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-179">**PolyLine**</span></span>
-   <span data-ttu-id="a0ab9-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-180">**Rect**</span></span>
-   <span data-ttu-id="a0ab9-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-182">ADJ</span><span class="sxs-lookup"><span data-stu-id="a0ab9-182">Adj</span></span>          | <span data-ttu-id="a0ab9-183">[Ivganpassungen](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="a0ab9-184">Eine durch Trennzeichen getrennte Liste von Zahlen, die die Parameter für die Führungs Formeln sind, die den Pfad der Form definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="a0ab9-185">Werte werden möglicherweise weggelassen, um die Verwendung von Standardwerten zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="a0ab9-186">Es können bis zu 8 Anpassungs Werte vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="a0ab9-187">ALT</span><span class="sxs-lookup"><span data-stu-id="a0ab9-187">Alt</span></span>          | <span data-ttu-id="a0ab9-188">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-188">String.</span></span> <span data-ttu-id="a0ab9-189">Alternativer Text, der Shape zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-189">Alternative text associated with shape.</span></span> <span data-ttu-id="a0ab9-190">Wird für nicht-grafische Browser verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a0ab9-191">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a0ab9-191">Button</span></span>       | <span data-ttu-id="a0ab9-192">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-193">Zeigt das Schaltflächen Verhalten beim Klicken an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a0ab9-194">Bwmode</span><span class="sxs-lookup"><span data-stu-id="a0ab9-194">BWMode</span></span>       | <span data-ttu-id="a0ab9-195">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="a0ab9-196">Bestimmt, wie die Form in der schwarz-und weiß-Ansicht in-Apps oder bei der Druck auf schwarze und weiße Drucker dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="a0ab9-197">Folgende Werte sind enthalten: **Color**, **Auto**, **Grayscale**, **lightgrayscale**, **inversgray**, **grayoutline**, **blacktextandlines**, **HighContrast**, **Black**, **White**, **undrawn**.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="a0ab9-198">Standardwert: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="a0ab9-199">Bwnormal</span><span class="sxs-lookup"><span data-stu-id="a0ab9-199">BWNormal</span></span>     | <span data-ttu-id="a0ab9-200">Vgblackwhitemode.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="a0ab9-201">Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für die Art und Weise, wie die Form in normalem schwarz und weiß dargestellt wird, untersucht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="a0ab9-202">Folgende Werte sind enthalten: **Color**, **Auto**, **Grayscale**, **lightgrayscale**, **inversgray**, **grayoutline**, **blacktextandlines**, **HighContrast**, **Black**, **White**, **undrawn**.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="a0ab9-203">Standardwert: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="a0ab9-204">Bwpure</span><span class="sxs-lookup"><span data-stu-id="a0ab9-204">BWPure</span></span>       | <span data-ttu-id="a0ab9-205">Vgblackwhitemode.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="a0ab9-206">Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für das Renderingformat in reiner B/W.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="a0ab9-207">Folgende Werte sind enthalten: **Color**, **Auto**, **Grayscale**, **lightgrayscale**, **inversgray**, **grayoutline**, **blacktextandlines**, **HighContrast**, **Black**, **White**, **undrawn**.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="a0ab9-208">Standardwert: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="a0ab9-209">Childshapes</span><span class="sxs-lookup"><span data-stu-id="a0ab9-209">ChildShapes</span></span>  | <span data-ttu-id="a0ab9-210">Ivggroupshapes.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-210">IVgGroupShapes.</span></span> <span data-ttu-id="a0ab9-211">Eine Auflistung anderer Formen in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="a0ab9-212">Diese Auflistung unterstützt die standardmäßigen length-und Item-Methoden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a0ab9-213">Chromakey</span><span class="sxs-lookup"><span data-stu-id="a0ab9-213">Chromakey</span></span>    | <span data-ttu-id="a0ab9-214">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="a0ab9-215">Ein Farbwert, der transparent ist und alles hinter der Form anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a0ab9-216">Control1</span><span class="sxs-lookup"><span data-stu-id="a0ab9-216">Control1</span></span>     | <span data-ttu-id="a0ab9-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-218">Der Kontrollpunkt für die Kurve.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0ab9-219">Control2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-219">Control2</span></span>     | <span data-ttu-id="a0ab9-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-221">Der Kontrollpunkt für die Kurve.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0ab9-222">Coordorigin</span><span class="sxs-lookup"><span data-stu-id="a0ab9-222">CoordOrigin</span></span>  | <span data-ttu-id="a0ab9-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Die Koordinaten in der oberen linken Ecke des Container Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="a0ab9-224">Bereich von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a0ab9-225">Coordsize</span><span class="sxs-lookup"><span data-stu-id="a0ab9-225">CoordSize</span></span>    | <span data-ttu-id="a0ab9-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-227">Die Breite und Höhe des Koordinaten Raums innerhalb des Bezugs Rechtecks dieser Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="a0ab9-228">Wenn Sie nicht angegeben ist, entspricht Sie der Breite und Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="a0ab9-229">Bereich von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-229">Range from 0 to infinity.</span></span> <span data-ttu-id="a0ab9-230">Standardwert: "1000, 1000".</span><span class="sxs-lookup"><span data-stu-id="a0ab9-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="a0ab9-231">Umschließen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-231">EndAngle</span></span>     | <span data-ttu-id="a0ab9-232">[Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="a0ab9-233">Endwinkel der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a0ab9-234">Schläuche</span><span class="sxs-lookup"><span data-stu-id="a0ab9-234">Extrusion</span></span>    | <span data-ttu-id="a0ab9-235">Ivgextrusion.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-235">IVgExtrusion.</span></span> <span data-ttu-id="a0ab9-236">Gibt den Wert des extrusionsobjekt für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="a0ab9-237">Weitere Informationen finden Sie unter dem-Element " [Extrusion](msdn-online-vml-extrusion-element.md) ".</span><span class="sxs-lookup"><span data-stu-id="a0ab9-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a0ab9-238">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-238">Fill</span></span>         | <span data-ttu-id="a0ab9-239">Vgfillformat.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-239">VgFillFormat.</span></span> <span data-ttu-id="a0ab9-240">Gibt den Füll Wert für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="a0ab9-241">Weitere Informationen finden [Sie im Fill](msdn-online-vml-fill-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="a0ab9-242">FillColor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-242">FillColor</span></span>    | <span data-ttu-id="a0ab9-243">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="a0ab9-244">Die Primärfarbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0ab9-245">Füllen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-245">Filled</span></span>       | <span data-ttu-id="a0ab9-246">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-247">True gibt an, dass der Pfad, der die Form definiert, ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="a0ab9-248">Standardmäßig wird Sie mit einer voll Tonfarbe aufgefüllt, es sei denn, es gibt ein Füll Teilelement, das komplexere Fülleigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="a0ab9-249">Wenn der Wert false ist, ist die Füllung transparent.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="a0ab9-250">Kippen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-250">Flip</span></span>         | <span data-ttu-id="a0ab9-251">Vgfliporientation.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-251">VgFlipOrientation.</span></span> <span data-ttu-id="a0ab9-252">Werte: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="a0ab9-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a0ab9-253">Forcedash</span><span class="sxs-lookup"><span data-stu-id="a0ab9-253">ForceDash</span></span>    | <span data-ttu-id="a0ab9-254">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-255">Gibt an, dass ein gestrichelter Umriss gerendert werden soll, wenn keine Zeile und keine Füllung für eine Form vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="a0ab9-256">Dieses Verhalten ist in der Regel hilfreich, um unsichtbare Formen in der Bearbeitung von Anwendungen sichtbar zu machen, sodass Sie ausgewählt und verarbeitet werden können, z. b. in einer ImageMap.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="a0ab9-257">Formeln</span><span class="sxs-lookup"><span data-stu-id="a0ab9-257">Formulas</span></span>     | <span data-ttu-id="a0ab9-258">Ivgformeln.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-258">IVgFormulas.</span></span> <span data-ttu-id="a0ab9-259">Ein Array von Formeln, das eine Form definiert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a0ab9-260">From</span><span class="sxs-lookup"><span data-stu-id="a0ab9-260">From</span></span>         | <span data-ttu-id="a0ab9-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-262">Anfangspunkt der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a0ab9-263">HRef</span><span class="sxs-lookup"><span data-stu-id="a0ab9-263">HRef</span></span>         | <span data-ttu-id="a0ab9-264">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-265">Die URL, zu der gewechselt werden soll, wenn auf diese Form geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a0ab9-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="a0ab9-266">ImageData</span></span>    | <span data-ttu-id="a0ab9-267">Ivgimagedata.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-267">IVgImageData.</span></span> <span data-ttu-id="a0ab9-268">Bild Informationen, wenn die Form ein Bild ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="a0ab9-269">Weitere Informationen finden Sie unter dem imagedata-Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a0ab9-270">Geplant</span><span class="sxs-lookup"><span data-stu-id="a0ab9-270">OnEd</span></span>         | <span data-ttu-id="a0ab9-271">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-272">Blendet alle Handles außer der oberen linken und unteren rechten Ecke aus, wie in den Handles für ein gerades Liniensegment.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="a0ab9-273">Opacity</span><span class="sxs-lookup"><span data-stu-id="a0ab9-273">Opacity</span></span>      | <span data-ttu-id="a0ab9-274">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="a0ab9-275">Die Deckkraft der gesamten Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-275">The opacity of the entire shape.</span></span> <span data-ttu-id="a0ab9-276">Eine Zahl zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a0ab9-277">Pfad</span><span class="sxs-lookup"><span data-stu-id="a0ab9-277">Path</span></span>         | <span data-ttu-id="a0ab9-278">Ivgpath.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-278">IVgPath.</span></span> <span data-ttu-id="a0ab9-279">Eine Zeichenfolge, die die Befehle enthält, die den Pfad definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0ab9-280">Punkte</span><span class="sxs-lookup"><span data-stu-id="a0ab9-280">Points</span></span>       | <span data-ttu-id="a0ab9-281">[Ivgpoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="a0ab9-282">Eine Auflistung von Punkten, die eine Form definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a0ab9-283">Drucken</span><span class="sxs-lookup"><span data-stu-id="a0ab9-283">Print</span></span>        | <span data-ttu-id="a0ab9-284">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-285">True gibt an, dass diese Form gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a0ab9-286">Drehung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-286">Rotation</span></span>     | <span data-ttu-id="a0ab9-287">[Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="a0ab9-288">Legt die Drehung der Form fest.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-288">Sets rotation of shape.</span></span> <span data-ttu-id="a0ab9-289">Der Wert wird an den Shape-Stil weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="a0ab9-290">Skalieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-290">Scale</span></span>        | <span data-ttu-id="a0ab9-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-292">Skalierung der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a0ab9-293">Shadow</span><span class="sxs-lookup"><span data-stu-id="a0ab9-293">Shadow</span></span>       | <span data-ttu-id="a0ab9-294">Ivgshadow.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-294">IVgShadow.</span></span> <span data-ttu-id="a0ab9-295">Gibt den Schatten für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="a0ab9-296">Weitere Informationen finden Sie im [Schatten](msdn-online-vml-shadow-element.md) Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a0ab9-297">SPT</span><span class="sxs-lookup"><span data-stu-id="a0ab9-297">Spt</span></span>          | <span data-ttu-id="a0ab9-298">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a0ab9-299">Start Angle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-299">StartAngle</span></span>   | <span data-ttu-id="a0ab9-300">[Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="a0ab9-301">Der Start Winkel der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a0ab9-302">Stroke</span><span class="sxs-lookup"><span data-stu-id="a0ab9-302">Stroke</span></span>       | <span data-ttu-id="a0ab9-303">Vgstrokeformat.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-303">VgStrokeFormat.</span></span> <span data-ttu-id="a0ab9-304">Weitere Informationen finden Sie unter Stroke-Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0ab9-305">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-305">StrokeColor</span></span>  | <span data-ttu-id="a0ab9-306">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="a0ab9-307">Die Primärfarbe des Pinsels, der zum Zeichnen des Pfads dieser Form verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a0ab9-308">Strichen gezeichnet</span><span class="sxs-lookup"><span data-stu-id="a0ab9-308">Stroked</span></span>      | <span data-ttu-id="a0ab9-309">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-310">Wenn der Wert true ist, wird der Pfad, der die Form definiert, mit Strichen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a0ab9-311">Strokeweight</span><span class="sxs-lookup"><span data-stu-id="a0ab9-311">StrokeWeight</span></span> | <span data-ttu-id="a0ab9-312">[Vglength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="a0ab9-313">Die Breite des Pinsels, der zum Zeichnen des Pfads verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="a0ab9-314">Zwischen 0 und 1584.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a0ab9-315">TextPath</span><span class="sxs-lookup"><span data-stu-id="a0ab9-315">TextPath</span></span>     | <span data-ttu-id="a0ab9-316">Ivgtextpath.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-316">IVgTextPath.</span></span> <span data-ttu-id="a0ab9-317">Gibt das TextPath-Objekt der Form an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="a0ab9-318">Weitere Informationen finden Sie im [TextPath](msdn-online-vml-textpath-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="a0ab9-319">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-319">To</span></span>           | <span data-ttu-id="a0ab9-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-321">Endpunkt Ende.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a0ab9-322">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-322">Type</span></span>         | <span data-ttu-id="a0ab9-323">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-323">String.</span></span> <span data-ttu-id="a0ab9-324">Der Typ der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="a0ab9-325">Unter Elemente des Shape-Elements</span><span class="sxs-lookup"><span data-stu-id="a0ab9-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="a0ab9-326">Die folgenden unter Elemente sind Teil des VML-Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="a0ab9-327">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0ab9-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="a0ab9-328">Schläuche</span><span class="sxs-lookup"><span data-stu-id="a0ab9-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="a0ab9-329">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="a0ab9-330">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="a0ab9-331">Imagedata</span><span class="sxs-lookup"><span data-stu-id="a0ab9-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="a0ab9-332">Pfad</span><span class="sxs-lookup"><span data-stu-id="a0ab9-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="a0ab9-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="a0ab9-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="a0ab9-334">Neigen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="a0ab9-335">Stellung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="a0ab9-336">TextPath</span><span class="sxs-lookup"><span data-stu-id="a0ab9-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="a0ab9-337">Background-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-337">Background element</span></span>

<span data-ttu-id="a0ab9-338">Beschreibt die Füllung des Hintergrunds einer Seite mithilfe von VML-Füllungen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="a0ab9-339">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-340">Bwmode</span><span class="sxs-lookup"><span data-stu-id="a0ab9-340">BWMode</span></span>    | <span data-ttu-id="a0ab9-341">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="a0ab9-342">Bestimmt, wie die Form in der schwarzen und weißen Ansicht in Anwendungen oder gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="a0ab9-343">Bwnormal</span><span class="sxs-lookup"><span data-stu-id="a0ab9-343">BWNormal</span></span>  | <span data-ttu-id="a0ab9-344">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="a0ab9-345">Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für die Art und Weise, wie die Form in normalem schwarz und weiß dargestellt wird, untersucht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="a0ab9-346">Bwpure</span><span class="sxs-lookup"><span data-stu-id="a0ab9-346">BWPure</span></span>    | <span data-ttu-id="a0ab9-347">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="a0ab9-348">Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für das Renderingformat in reiner Schwarz-und weiß-Form abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="a0ab9-349">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-349">Fill</span></span>      | <span data-ttu-id="a0ab9-350">Vgfillformat.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-350">VgFillFormat.</span></span> <span data-ttu-id="a0ab9-351">Gibt die Füllung für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="a0ab9-352">Weitere Informationen finden [Sie unter Fill](msdn-online-vml-fill-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="a0ab9-353">FillColor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-353">FillColor</span></span> | <span data-ttu-id="a0ab9-354">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="a0ab9-355">Die Primärfarbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="a0ab9-356">Duplikat des Farbwerts im Fill-Element.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="a0ab9-357">Der Standardwert ist Weiß.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="a0ab9-358">Extrusion-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-358">Extrusion element</span></span>

<span data-ttu-id="a0ab9-359">Beschreibt eine 3D-Extrusion der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="a0ab9-360">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-361">Autorotationcenter</span><span class="sxs-lookup"><span data-stu-id="a0ab9-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="a0ab9-362"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-363">True gibt an, dass der Mittelpunkt der Drehung der Gruppe von 3D-Objekten (tatsächlich ist nur ein Objekt in der Gruppe vorhanden) automatisch als Mittelpunkt der Gruppe festgelegt wird. Andernfalls wird Sie durch die rotationCenter-Parameter bestimmt, bei denen es sich um einen Bruchteil der Form handelt, bei dem 0, 0, 0 die Mitte ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-364">Backtiefe</span><span class="sxs-lookup"><span data-stu-id="a0ab9-364">BackDepth</span></span></td>
<td><span data-ttu-id="a0ab9-365"><a href="msdn-online-vml-vglength.md"><strong>Vglength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="a0ab9-366">Menge der abwärts Extrusion.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-366">Amount of backward extrusion.</span></span> <span data-ttu-id="a0ab9-367">Liegt zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-368">Brightness</span><span class="sxs-lookup"><span data-stu-id="a0ab9-368">Brightness</span></span></td>
<td><span data-ttu-id="a0ab9-369"><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="a0ab9-370">Allgemeine Helligkeit der Szene.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-370">Overall brightness of the scene.</span></span> <span data-ttu-id="a0ab9-371">Der Standardwert ist &quot; 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-372">Color</span><span class="sxs-lookup"><span data-stu-id="a0ab9-372">Color</span></span></td>
<td><span data-ttu-id="a0ab9-373"><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="a0ab9-374">Die Farbe der-Extrusion.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-374">The color of the extrusion.</span></span> <span data-ttu-id="a0ab9-375">Wird nur verwendet, wenn ColorMode Benutzer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="a0ab9-376">Andernfalls wird die Farbe des Bild-und-Effekts automatisch auf den gleichen Wert wie FillColor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-377">ColorMode</span><span class="sxs-lookup"><span data-stu-id="a0ab9-377">ColorMode</span></span></td>
<td><span data-ttu-id="a0ab9-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-378">Vg3DColorMode.</span></span> <span data-ttu-id="a0ab9-379">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-380">Auto (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-380">Auto (default)</span></span></li>
<li><span data-ttu-id="a0ab9-381">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-382">Diffusity</span><span class="sxs-lookup"><span data-stu-id="a0ab9-382">Diffusity</span></span></td>
<td><span data-ttu-id="a0ab9-383"><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="a0ab9-384">Das Verhältnis zwischen Incident und diffus reflektiertem Licht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="a0ab9-385">Werte, die kleiner als 1,0 sind, sind normal, aber Werte, die größer als 1 sind, können interessante Effekte</span><span class="sxs-lookup"><span data-stu-id="a0ab9-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-386">Edge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-386">Edge</span></span></td>
<td><span data-ttu-id="a0ab9-387"><a href="msdn-online-vml-vglength.md">Vglength</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="a0ab9-388">Legt die Größe eines simulierten, gerundeten gepufferten Edge fest.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="a0ab9-389">Reicht zwischen 0 und 32767 in Gleit Komma-pts.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="a0ab9-390">Der Standardwert ist &quot; 1 pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-391">Facet</span><span class="sxs-lookup"><span data-stu-id="a0ab9-391">Facet</span></span></td>
<td><span data-ttu-id="a0ab9-392"><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="a0ab9-393">Legt die Facette der Szene fest.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-393">Sets the facet of the scene.</span></span> <span data-ttu-id="a0ab9-394">Der Standardwert ist &quot; 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-395">Foretiefe</span><span class="sxs-lookup"><span data-stu-id="a0ab9-395">ForeDepth</span></span></td>
<td><span data-ttu-id="a0ab9-396"><a href="msdn-online-vml-vglength.md">Vglength</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="a0ab9-397">Menge der vorwärts-Extrusion.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-397">Amount of forward extrusion.</span></span> <span data-ttu-id="a0ab9-398">Liegt zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-399">Lightface</span><span class="sxs-lookup"><span data-stu-id="a0ab9-399">LightFace</span></span></td>
<td><span data-ttu-id="a0ab9-400"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-401">Determinimt, ob die Vorderseite des Objekts auf Änderungen in der 3D-Beleuchtung antwortet, z. b. Wenn ein Objekt rotiert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-402">Lightharsh</span><span class="sxs-lookup"><span data-stu-id="a0ab9-402">LightHarsh</span></span></td>
<td><span data-ttu-id="a0ab9-403"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-404">Harte Beleuchtung für die primäre Light-Quelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="a0ab9-405">Der Standardwert lautet False.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="a0ab9-407"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-408">Harte Beleuchtung der sekundären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="a0ab9-409">Der Standardwert lautet False.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-410">Lightlevel</span><span class="sxs-lookup"><span data-stu-id="a0ab9-410">LightLevel</span></span></td>
<td><span data-ttu-id="a0ab9-411"><a href="#data-types-used-in-the-vml-object-model">Vgnumber</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="a0ab9-412">Intensität der primären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-412">Intensity of the primary light source.</span></span> <span data-ttu-id="a0ab9-413">Der Standardwert ist &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-414">LightLevel2</span></span></td>
<td><span data-ttu-id="a0ab9-415"><a href="#data-types-used-in-the-vml-object-model">Vgnumber</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="a0ab9-416">Intensität der sekundären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="a0ab9-417">Der Standardwert ist &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-418">Lightposition</span><span class="sxs-lookup"><span data-stu-id="a0ab9-418">LightPosition</span></span></td>
<td><span data-ttu-id="a0ab9-419">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-419">Vector3D.</span></span> <span data-ttu-id="a0ab9-420">Die Position der primären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-420">Position of the primary light source.</span></span> <span data-ttu-id="a0ab9-421">Der Standardwert ist &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-422">LightPosition2</span></span></td>
<td><span data-ttu-id="a0ab9-423">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-423">Vector3D.</span></span> <span data-ttu-id="a0ab9-424">Die Position der sekundären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-424">Position of the secondary light source.</span></span> <span data-ttu-id="a0ab9-425">Der Standardwert ist &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-426">Lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="a0ab9-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="a0ab9-427"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-428">&quot;Lockrotationcenter &quot; bedeutet, dass die Rotation der Gruppe so definiert ist, dass Sie durch den Drehwinkel [1] Grad um die y-Achse auf der Seite folgt, gefolgt von einem Drehwinkel [0] Grad zur x-Achse.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="a0ab9-429">Wenn lockrotationcenter auf false festgelegt ist, wird die Drehung so definiert, dass Sie durch die Ausrichtung auf den durch Ausrichtung definierten Vektor festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="a0ab9-430">Beispielsweise entspricht lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) dem lockrotationcenter = true RotationAngle = (0,0).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-431">Metallisch</span><span class="sxs-lookup"><span data-stu-id="a0ab9-431">Metal</span></span></td>
<td><span data-ttu-id="a0ab9-432"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-433">Bewirkt, dass das Licht mit dem reflektierten Licht anstelle der hellen Quellfarbe die Material Farbe ist, sodass das Objekt mehr Metallic erscheint.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-434">Ein</span><span class="sxs-lookup"><span data-stu-id="a0ab9-434">On</span></span></td>
<td><span data-ttu-id="a0ab9-435"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-436">Schaltet die Anzeige des extrusioneffekts ein bzw. aus.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-437">Orientation</span><span class="sxs-lookup"><span data-stu-id="a0ab9-437">Orientation</span></span></td>
<td><span data-ttu-id="a0ab9-438">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-438">Vector3D.</span></span> <span data-ttu-id="a0ab9-439">Die Ausrichtung der Kamera.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-440">Orientationangle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="a0ab9-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Vganglin Grad</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="a0ab9-442">Der Winkel zwischen der Ausrichtung der Kamera und der XY-Ebene.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-443">Wasser</span><span class="sxs-lookup"><span data-stu-id="a0ab9-443">Plane</span></span></td>
<td><span data-ttu-id="a0ab9-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="a0ab9-445">Ermöglicht die-Extrusion zwischen orthogonaler Ebene und der Bildschirm Ebene.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="a0ab9-446">Erfordert, dass foretiefe und backtiefe in Zeichnungs Einheiten anstelle von Emus angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="a0ab9-447">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-448">D</span><span class="sxs-lookup"><span data-stu-id="a0ab9-448">XY</span></span></li>
<li><span data-ttu-id="a0ab9-449">ZX</span><span class="sxs-lookup"><span data-stu-id="a0ab9-449">ZX</span></span></li>
<li><span data-ttu-id="a0ab9-450">YZ</span><span class="sxs-lookup"><span data-stu-id="a0ab9-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-451">Rendern</span><span class="sxs-lookup"><span data-stu-id="a0ab9-451">Render</span></span></td>
<td><span data-ttu-id="a0ab9-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-452">Vg3DRenderMode.</span></span> <span data-ttu-id="a0ab9-453">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-454">Solid (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-454">Solid (default)</span></span></li>
<li><span data-ttu-id="a0ab9-455">Draht Modell</span><span class="sxs-lookup"><span data-stu-id="a0ab9-455">WireFrame</span></span></li>
<li><span data-ttu-id="a0ab9-456">Boundingcube</span><span class="sxs-lookup"><span data-stu-id="a0ab9-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-457">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-457">RotationAngle</span></span></td>
<td><span data-ttu-id="a0ab9-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-459">AngleX, AngleY oder anglez wird durch das shaperotations-Attribut gesteuert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-460">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="a0ab9-460">RotationCenter</span></span></td>
<td><span data-ttu-id="a0ab9-461">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-461">Vector3D.</span></span> <span data-ttu-id="a0ab9-462">Mittelpunkt der Drehung.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-463">Glanz</span><span class="sxs-lookup"><span data-stu-id="a0ab9-463">Shininess</span></span></td>
<td><span data-ttu-id="a0ab9-464"><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="a0ab9-465">Bestimmt, wie sich die Glanz Reflektion konzentriert oder verteilt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="a0ab9-466">Ein hoher Wert wäre 8 bis 10 und würde eine Spiegelung angleichen, und ein niedriger Wert wäre 2 bis 3 und würde eine ungefähre Reihenfolge von Bekleidung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="a0ab9-467">Werte von 3 bis 7 werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="a0ab9-468">Hohe Werte werden PinPoint-Lichtquellen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-469">Schief</span><span class="sxs-lookup"><span data-stu-id="a0ab9-469">SkewAmt</span></span></td>
<td><span data-ttu-id="a0ab9-470"><a href="#data-types-used-in-the-vml-object-model">Vgprozentsatz</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="a0ab9-471">Wenn der Typ parallel ist, bestimmt das Attribut die Menge der Schiefe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="a0ab9-472">Liegt zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-473">Schief legen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-473">SkewAngle</span></span></td>
<td><span data-ttu-id="a0ab9-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Vganglin Grad</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="a0ab9-475">Wenn der Typ parallel ist, bestimmt das Attribut den Grad der Schiefe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="a0ab9-476">Der Standardwert ist &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-477">Spiegelung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-477">Specularity</span></span></td>
<td><span data-ttu-id="a0ab9-478"><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="a0ab9-479">Das Verhältnis zwischen Incident und spekulativ reflektiertem Licht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="a0ab9-480">Werte, die kleiner als 1,0 sind, sind normal, aber Werte, die größer als 1 sind, können interessante Effekte</span><span class="sxs-lookup"><span data-stu-id="a0ab9-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-481">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-481">Type</span></span></td>
<td><span data-ttu-id="a0ab9-482">Vgextrusiontype.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-482">VgExtrusionType.</span></span> <span data-ttu-id="a0ab9-483">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-484">Parallel (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="a0ab9-485">Perspektive</span><span class="sxs-lookup"><span data-stu-id="a0ab9-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-486">Standpunkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-486">Viewpoint</span></span></td>
<td><span data-ttu-id="a0ab9-487">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-487">Vector3D.</span></span> <span data-ttu-id="a0ab9-488">Der Punkt, von dem aus die Szene angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-489">Viewpointorigin</span><span class="sxs-lookup"><span data-stu-id="a0ab9-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="a0ab9-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-491">Kann über Werte von 0,5 bis-0,5 verfügen, um den Ursprung des Standpunkts innerhalb des umgebenden Felds der Form zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="a0ab9-492">Fill-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-492">Fill element</span></span>

<span data-ttu-id="a0ab9-493">Beschreibt, wie ein Pfad für Füllungen komplexer ist als eine voll Tonfarbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="a0ab9-494">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-495">Alignshape</span><span class="sxs-lookup"><span data-stu-id="a0ab9-495">AlignShape</span></span></td>
<td><span data-ttu-id="a0ab9-496"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-497">Richten Sie das Bild mit der Form aus.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-497">Align the image with the shape.</span></span> <span data-ttu-id="a0ab9-498">Wenn false, wird das Bild mit dem Fenster ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-499">Angle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-499">Angle</span></span></td>
<td><span data-ttu-id="a0ab9-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Vganglin Grad</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="a0ab9-501">Der Winkel, in dem der Farbverlauf verläuft.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="a0ab9-502">0 Grad liegt entlang der horizontalen Achse von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-503">Aspekt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-503">Aspect</span></span></td>
<td><span data-ttu-id="a0ab9-504"><strong>Vgaspecttype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="a0ab9-505">Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="a0ab9-506">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-507">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-507">Value</span></span></th>
<th><span data-ttu-id="a0ab9-508">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-509">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-509">Ignore</span></span></td>
<td><span data-ttu-id="a0ab9-510">Ignoriert Aspekte von Aspekten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-511">Mindestens</span><span class="sxs-lookup"><span data-stu-id="a0ab9-511">AtLeast</span></span></td>
<td><span data-ttu-id="a0ab9-512">Image ist mindestens so groß wie die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-513">Höchstens</span><span class="sxs-lookup"><span data-stu-id="a0ab9-513">AtMost</span></span></td>
<td><span data-ttu-id="a0ab9-514">Das Bild ist nicht größer als die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-515">Color</span><span class="sxs-lookup"><span data-stu-id="a0ab9-515">Color</span></span></td>
<td><span data-ttu-id="a0ab9-516"><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a> Die Haupt Füllfarbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="a0ab9-517">Identisch mit FillColor-Attribut in Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-518">Color2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-518">Color2</span></span></td>
<td><span data-ttu-id="a0ab9-519"><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="a0ab9-520">Die sekundäre Farbe für eine Füllung, wenn der Bildtyp ein Muster oder eine Farbverlaufsfüllung ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-521">Farben</span><span class="sxs-lookup"><span data-stu-id="a0ab9-521">Colors</span></span></td>
<td><span data-ttu-id="a0ab9-522"><a href="#data-types-used-in-the-vml-object-model">Ivggradientcolorarray</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="a0ab9-523">Zwischen Farben im Farbverlauf und ihre relativen Positionen entlang des Farbverlaufs, z. b. &quot; 30% rot, 70% blau, 90% grün &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="a0ab9-524">Die primäre Farbe (Farb Attribut in Form) ist 0%, und die sekundäre Farbe (color2-Attribut) ist 100%.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-525">Fokus</span><span class="sxs-lookup"><span data-stu-id="a0ab9-525">Focus</span></span></td>
<td><span data-ttu-id="a0ab9-526"><a href="#data-types-used-in-the-vml-object-model">Vgsignedprozentsatz</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="a0ab9-527">Der Fokuspunkt für die lineare Verlaufs Füllung.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="a0ab9-528">Werte werden von-100 bis + 100.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-529">Focusposition</span><span class="sxs-lookup"><span data-stu-id="a0ab9-529">FocusPosition</span></span></td>
<td><span data-ttu-id="a0ab9-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-531">Die Position des innersten Rechtecks für radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="a0ab9-532">Der Vektor ist ein Bruchteil (0,0-1,0) der Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-533">Focussize</span><span class="sxs-lookup"><span data-stu-id="a0ab9-533">FocusSize</span></span></td>
<td><span data-ttu-id="a0ab9-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Größe des innersten Rechtecks für radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="a0ab9-535">Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-536">Methode</span><span class="sxs-lookup"><span data-stu-id="a0ab9-536">Method</span></span></td>
<td><span data-ttu-id="a0ab9-537">Vgsigmatype.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-537">VgSigmaType.</span></span> <span data-ttu-id="a0ab9-538">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-539">Keine</span><span class="sxs-lookup"><span data-stu-id="a0ab9-539">None</span></span></li>
<li><span data-ttu-id="a0ab9-540">Linear</span><span class="sxs-lookup"><span data-stu-id="a0ab9-540">Linear</span></span></li>
<li><span data-ttu-id="a0ab9-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="a0ab9-541">Sigma</span></span></li>
<li><span data-ttu-id="a0ab9-542">Any</span><span class="sxs-lookup"><span data-stu-id="a0ab9-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="a0ab9-543">Der Standardwert ist Sigma.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-544">Ein</span><span class="sxs-lookup"><span data-stu-id="a0ab9-544">On</span></span></td>
<td><span data-ttu-id="a0ab9-545"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-546">Schaltet die Füll Anzeige ein.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-546">Turns fill display on.</span></span> <span data-ttu-id="a0ab9-547">Identisch mit Fill-Attribut in Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-548">Opacity</span><span class="sxs-lookup"><span data-stu-id="a0ab9-548">Opacity</span></span></td>
<td><span data-ttu-id="a0ab9-549"><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="a0ab9-550">Deckkraft der Füllung.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-551">Opacity2</span></span></td>
<td><span data-ttu-id="a0ab9-552"><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="a0ab9-553">Die sekundäre Deckkraft für Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-554">Origin</span><span class="sxs-lookup"><span data-stu-id="a0ab9-554">Origin</span></span></td>
<td><span data-ttu-id="a0ab9-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-556">Der Punkt ist relativ zur oberen linken Ecke des Bilds, das als Ursprung des Bilds behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="a0ab9-557">Der Standardwert ist der Mittelpunkt des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-557">Default is the center of the image.</span></span> <span data-ttu-id="a0ab9-558">Der Vektor ist ein Bruchteil (zwischen 0,0 und 1,0) der Breite und Höhe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-559">Position</span><span class="sxs-lookup"><span data-stu-id="a0ab9-559">Position</span></span></td>
<td><span data-ttu-id="a0ab9-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-561">Zeigen Sie im Verweis Rechteck der Form, um den Ursprung des Bilds zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="a0ab9-562">Der Standardwert ist die Mitte des Container Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="a0ab9-563">Der Vektor ist ein Bruchteil (0,0-1,0) der Breite und Höhe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-564">Size</span><span class="sxs-lookup"><span data-stu-id="a0ab9-564">Size</span></span></td>
<td><span data-ttu-id="a0ab9-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-566">Die Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-566">The size of the image.</span></span> <span data-ttu-id="a0ab9-567">Der Standardwert ist die Pixelgröße des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-567">Default is pixel size of the image.</span></span> <span data-ttu-id="a0ab9-568">Kann in absoluten Koordinaten oder in Prozent angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-569">Src</span><span class="sxs-lookup"><span data-stu-id="a0ab9-569">Src</span></span></td>
<td><span data-ttu-id="a0ab9-570"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="a0ab9-571">Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="a0ab9-572">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-573">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-573">Type</span></span></td>
<td><span data-ttu-id="a0ab9-574">Vgfilltype.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-574">VgFillType.</span></span> <span data-ttu-id="a0ab9-575">Es kann sich um einen der folgenden Typen handeln:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-576">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0ab9-576">Background</span></span></li>
<li><span data-ttu-id="a0ab9-577">Frame</span><span class="sxs-lookup"><span data-stu-id="a0ab9-577">Frame</span></span></li>
<li><span data-ttu-id="a0ab9-578">Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="a0ab9-578">Gradient</span></span></li>
<li><span data-ttu-id="a0ab9-579">Gradientcenter</span><span class="sxs-lookup"><span data-stu-id="a0ab9-579">GradientCenter</span></span></li>
<li><span data-ttu-id="a0ab9-580">Gradientradiale</span><span class="sxs-lookup"><span data-stu-id="a0ab9-580">GradientRadial</span></span></li>
<li><span data-ttu-id="a0ab9-581">Gradienttitle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-581">GradientTitle</span></span></li>
<li><span data-ttu-id="a0ab9-582">Gradientunskaliert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="a0ab9-583">Muster</span><span class="sxs-lookup"><span data-stu-id="a0ab9-583">Pattern</span></span></li>
<li><span data-ttu-id="a0ab9-584">Basis</span><span class="sxs-lookup"><span data-stu-id="a0ab9-584">Solid</span></span></li>
<li><span data-ttu-id="a0ab9-585">Tile</span><span class="sxs-lookup"><span data-stu-id="a0ab9-585">Tile</span></span></li>
</ul>
<span data-ttu-id="a0ab9-586">Kachel, Muster und Rahmen erfordern, dass die Bildattribute bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="a0ab9-587">Gradient und gradientradiale erfordern, dass die Farbverlaufs Attribute bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="a0ab9-588">Group-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-588">Group element</span></span>

<span data-ttu-id="a0ab9-589">Eine Gruppe ist eine Sammlung einzelner Formen, die als Einheit positioniert und transformiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-590">Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-590">Item</span></span>   | <span data-ttu-id="a0ab9-591">[Ivgshape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-592">Das angegebene Element im Array von Formen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="a0ab9-593">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-593">Length</span></span> | <span data-ttu-id="a0ab9-594">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-595">Anzahl der Formen in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="a0ab9-596">Imagedata-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-596">Imagedata element</span></span>

<span data-ttu-id="a0ab9-597">Beschreibt ein Bild, das oberhalb einer Form gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-598">BiLevel</span><span class="sxs-lookup"><span data-stu-id="a0ab9-598">BiLevel</span></span>     | <span data-ttu-id="a0ab9-599">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-600">Zeigt das Bild nur in zwei Farben an (normalerweise schwarz und weiß).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a0ab9-601">Blacklevel</span><span class="sxs-lookup"><span data-stu-id="a0ab9-601">BlackLevel</span></span>  | <span data-ttu-id="a0ab9-602">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="a0ab9-603">Ermöglicht die Anpassung, um die Ebene so festzulegen, dass schwarze als echte schwarze angezeigt werden und alle anderen Farben als Schattierungen über schwarz sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a0ab9-604">Chromakey</span><span class="sxs-lookup"><span data-stu-id="a0ab9-604">Chromakey</span></span>   | <span data-ttu-id="a0ab9-605">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="a0ab9-606">Transparente Farbe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a0ab9-607">CropBottom</span><span class="sxs-lookup"><span data-stu-id="a0ab9-607">CropBottom</span></span>  | <span data-ttu-id="a0ab9-608">[Vgnumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-609">Der Abstand von der unteren Seite des Bilds wird als Prozentsatz der Bildgröße ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="a0ab9-610">Durchforsten</span><span class="sxs-lookup"><span data-stu-id="a0ab9-610">CropLeft</span></span>    | <span data-ttu-id="a0ab9-611">[Vgnumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-612">Die Entfernung von der linken Kante des Bilds wird als Bruchteil der Bildgröße ausgedrückt (von 0,0 bis 1,0).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="a0ab9-613">"Out-Zuschneiden" wird jedoch unterstützt. Daher werden Werte kleiner als 0 und größer als 1 unterstützt. Beispielsweise würde-5, 20 die Begrenzungen 25 x der Bildgröße mit 4/5 auf einer Seite des Bilds überschneiden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="a0ab9-614">Durchschnitt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-614">CropRight</span></span>   | <span data-ttu-id="a0ab9-615">[Vgnumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-616">Der Entfernungs Abstand von der rechten Seite des Bilds, ausgedrückt als Prozentsatz der Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="a0ab9-617">CropTop</span><span class="sxs-lookup"><span data-stu-id="a0ab9-617">CropTop</span></span>     | <span data-ttu-id="a0ab9-618">[Vgnumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-619">Die Entfernung von der Oberkante des Bilds wird als Prozentsatz der Bildgröße ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="a0ab9-620">Embosscolor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-620">EmbossColor</span></span> | <span data-ttu-id="a0ab9-621">[Ivgcolor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="a0ab9-622">Dies wird auf einen Prozentsatz der Schatten Farbe festgelegt, um einen geprägten Bildeffekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="a0ab9-623">Erzielen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-623">Gain</span></span>        | <span data-ttu-id="a0ab9-624">[Vgpositivenumschlag](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-625">Passt die Intensität aller Farben an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="a0ab9-626">Legt im Grunde fest, wie hell weiß sein wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="a0ab9-627">Liegt zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="a0ab9-628">Gamma</span><span class="sxs-lookup"><span data-stu-id="a0ab9-628">Gamma</span></span>       | <span data-ttu-id="a0ab9-629">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="a0ab9-630">Gamma Korrektur.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-630">Gamma correction.</span></span> <span data-ttu-id="a0ab9-631">Das Erhöhen des Bilds bietet einem Bild einen größeren Kontrast.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="a0ab9-632">GrayScale</span><span class="sxs-lookup"><span data-stu-id="a0ab9-632">GrayScale</span></span>   | <span data-ttu-id="a0ab9-633">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-634">Bild in Graustufen Farben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a0ab9-635">Src</span><span class="sxs-lookup"><span data-stu-id="a0ab9-635">Src</span></span>         | <span data-ttu-id="a0ab9-636">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-637">Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="a0ab9-638">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="a0ab9-639">Path-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-639">Path element</span></span>

<span data-ttu-id="a0ab9-640">Definiert den Pfad, der die Form bildet, mithilfe einer Zeichenfolge, die einen umfangreichen Satz von "Pen Movement"-Befehlen enthält.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-641">Limo</span><span class="sxs-lookup"><span data-stu-id="a0ab9-641">Limo</span></span></td>
<td><span data-ttu-id="a0ab9-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="a0ab9-643">Definiert den Punkt, an dem die Form gestreckt wird. Beispielsweise würde sich der Limo-Punkt für eine Giraffen-Form auf dem Hals befinden, sodass bei der Größenänderung der Form der Hals gestreckt wird und der Rest der Form seine Dimensionen beibehält.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-644">Textboxrect</span><span class="sxs-lookup"><span data-stu-id="a0ab9-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="a0ab9-645"><a href="#data-types-used-in-the-vml-object-model">Ivgfixedrechglearray</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="a0ab9-646">Ein Array mit den Rechtecke, die definieren, wohin Text wechseln soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-647">V</span><span class="sxs-lookup"><span data-stu-id="a0ab9-647">V</span></span></td>
<td><span data-ttu-id="a0ab9-648"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="a0ab9-649">Entspricht dem v-Attribut des Path-Tags.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="a0ab9-650">Beachten Sie, dass path möglicherweise dem Pfad Attribut oder dem Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-651">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-651">Value</span></span></td>
<td><span data-ttu-id="a0ab9-652"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="a0ab9-653">Eine Textdarstellung der Befehle, die den Pfad definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="a0ab9-654">X-oder y-Koordinaten Werte können ein Verweis auf eine Formel in der Form sein &quot; @# &quot; , wobei # die Ordinalzahl der Formel (z. b.) ist &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="a0ab9-655">Diese Attribut Zeichenfolge besteht aus einem umfangreichen Satz von Befehlen, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-656">Get-Help</span><span class="sxs-lookup"><span data-stu-id="a0ab9-656">Command</span></span></th>
<th><span data-ttu-id="a0ab9-657">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-658">AE (angleelliponto)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="a0ab9-659"><strong>Mittelpunkt</strong>(x, y) <strong>Größe</strong>(w, h) <strong>anfangs Winkel</strong>, <strong>Endwinkel</strong></span><span class="sxs-lookup"><span data-stu-id="a0ab9-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="a0ab9-660">Zeichnen Sie ein Segment einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="a0ab9-661">Eine gerade Linie wird vom aktuellen Punkt bis zum Startpunkt des Segments gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-662">Al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="a0ab9-663">Identisch mit AE, mit dem Unterschied, dass es ein implizites m bis zum Ausgangspunkt des Segments gibt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-664">AR (Bogen)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-664">ar (arc)</span></span></td>
<td><span data-ttu-id="a0ab9-665">Identisch mit.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-665">Same as at.</span></span> <span data-ttu-id="a0ab9-666">Ein neuer Unterpfad wird jedoch von einem impliziten m bis zum Anfangspunkt des Bogens gestartet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-667">at (ArcTo)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-667">at (arcto)</span></span></td>
<td><span data-ttu-id="a0ab9-668"><strong>left</strong>, <strong>Top</strong>, <strong>right</strong>, <strong>Bottom</strong>, <strong>Start</strong>(x, y) <strong>End</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="a0ab9-669">Die ersten vier Werte definieren das umgebende Feld einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="a0ab9-670">Die letzten vier definieren zwei radiale Vektoren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-670">The last four define two radial vectors.</span></span> <span data-ttu-id="a0ab9-671">Ein Segment der Ellipse wird gezeichnet, das mit dem durch den Start RADIUS-Vektor definierten Winkel beginnt und mit dem durch den endvektor definierten Winkel endet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="a0ab9-672">Eine gerade Linie wird vom aktuellen Punkt bis zum Anfang des Bogens gezeichnet. Der Bogen wird immer in der Richtung gegen den Uhrzeigersinn gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-673">c (Cursor)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-673">c (curveto)</span></span></td>
<td><span data-ttu-id="a0ab9-674"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>bis</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="a0ab9-675">Zeichnen Sie eine kubische Bézier-Kurve vom aktuellen Punkt bis zur Koordinate, die von den letzten beiden Parametern angegeben wird, und die von den ersten vier Parametern angegebenen Steuerungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="a0ab9-676">Der aktuelle Punkt wird zum Endpunkt des bezierers.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-677">e (Ende)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-677">e (end)</span></span></td>
<td><span data-ttu-id="a0ab9-678">Beendet den aktuellen Satz von unter Pfaden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-678">End the current set of subpaths.</span></span> <span data-ttu-id="a0ab9-679">Ein angegebener Satz von unter Pfaden (wie durch Ende getrennt) wird mithilfe von eofill gefüllt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="a0ab9-680">Nachfolgende Sätze von unter Pfaden werden unabhängig voneinander aufgefüllt und für vorhandene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-681">l (LineTo)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-681">l (lineto)</span></span></td>
<td><span data-ttu-id="a0ab9-682">x, y</span><span class="sxs-lookup"><span data-stu-id="a0ab9-682">x,y</span></span><br/> <span data-ttu-id="a0ab9-683">Zeichnen Sie eine Linie vom aktuellen Punkt bis zur angegebenen x-, y-Koordinate, die zum neuen aktuellen Punkt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="a0ab9-684">Es können zusätzliche Koordinatenpaare angegeben werden, um eine Polylinie zu bilden, z. b. &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-685">m (muveto)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-685">m (moveto)</span></span></td>
<td><span data-ttu-id="a0ab9-686">x, y</span><span class="sxs-lookup"><span data-stu-id="a0ab9-686">x,y</span></span><br/> <span data-ttu-id="a0ab9-687">Startet einen neuen unter Pfad an der angegebenen x-, y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-688">NF (nofill)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="a0ab9-689">Der aktuelle Satz von unter Pfaden (durch Ende getrennt) wird nicht ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-690">NS (noStroke)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="a0ab9-691">Der aktuelle Satz von unter Pfaden (durch Ende getrennt) wird nicht mit Strichen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-692">QB (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="a0ab9-693">(<strong>ControlPoint</strong>(x, y)) \*,<strong>Ende</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="a0ab9-694">Definiert eine oder mehrere Quadratische Bézier-Kurven mithilfe von Steuerungs Punkten und einem Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="a0ab9-695">Intermediate (On-Curve)-Punkte werden durch Interpolationen zwischen aufeinander folgenden Steuerungs Punkten abgerufen, ähnlich wie TrueType-Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="a0ab9-696">Der Unterpfad muss kein Start sein. in diesem Fall wird der Unterpfad geschlossen, und der letzte Punkt definiert den Startpunkt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-697">QX (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="a0ab9-698"><strong>Ende</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="a0ab9-699">Eine Quartals Ellipse wird vom aktuellen Punkt zum angegebenen Endpunkt gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="a0ab9-700">Das elliptische Segment ist anfänglich tangential zu einer Zeile parallel zur x-Achse. Das Segment wird also horizontal gestartet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-701">Qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="a0ab9-702"><strong>Ende</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="a0ab9-703">Identisch mit QX, mit dem Unterschied, dass das elliptische Segment anfänglich tangential zu einer Zeile parallel zur y-Achse ist. Dies bedeutet, dass das Segment vertikal beginnt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-704">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="a0ab9-705">x, y</span><span class="sxs-lookup"><span data-stu-id="a0ab9-705">x,y</span></span> <br/> <span data-ttu-id="a0ab9-706">Zeichnen Sie eine Linie vom aktuellen Punkt bis zur relativen Koordinate (CPX + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="a0ab9-707">Wenn zusätzliche Koordinatenpaare angegeben werden, wird jeder neue Punkt relativ zum letzten Wert berechnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-708">t (rmuveto)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="a0ab9-709">x, y</span><span class="sxs-lookup"><span data-stu-id="a0ab9-709">x,y</span></span><br/> <span data-ttu-id="a0ab9-710">Starten Sie einen neuen untergeordneten Pfad an den relativen Koordinaten (CPX + x, cpy + y), wobei CPX, cpy die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-711">v (Cursor)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-711">v (curveto)</span></span></td>
<td><span data-ttu-id="a0ab9-712"><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>bis</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="a0ab9-713">Eine kubische Bézier-Kurve, die die angegebenen Koordinaten relativ zum aktuellen Punkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="a0ab9-714">Alle Punkte werden relativ zum gleichen Ausgangspunkt berechnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-715">WA (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="a0ab9-716">Identisch mit, aber der Bogen wird in Richtung im Uhrzeigersinn gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-717">WR (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="a0ab9-718">Identisch mit AR, wird aber in Richtung des Uhrzeigersinn gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-719">x (schließen)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-719">x (close)</span></span></td>
<td><span data-ttu-id="a0ab9-720">Schließen Sie den aktuellen untergeordneten Pfad, indem Sie eine gerade Linie von der aktuellen Punkt-zum ursprünglichen muvepoint zeichnen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="a0ab9-721">Shadow-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-721">Shadow element</span></span>

<span data-ttu-id="a0ab9-722">Beschreibt einen Schatteneffekt für eine Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-723">Color</span><span class="sxs-lookup"><span data-stu-id="a0ab9-723">Color</span></span></td>
<td><span data-ttu-id="a0ab9-724"><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="a0ab9-725">Farbe des primär Schattens.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-725">Color of the primary shadow.</span></span> <span data-ttu-id="a0ab9-726">Der Standardwert ist RGB (128128128).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-727">Color2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-727">Color2</span></span></td>
<td><span data-ttu-id="a0ab9-728"><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="a0ab9-729">Farbe des zweiten Schattens oder hervorheben in einem geprägten oder einschenden Schatten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="a0ab9-730">Der Standardwert ist RGB (203203203).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-731">Matrix</span><span class="sxs-lookup"><span data-stu-id="a0ab9-731">Matrix</span></span></td>
<td><span data-ttu-id="a0ab9-732"><a href="#data-types-used-in-the-vml-object-model">Ivgskewmatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="a0ab9-733">Eine perspektivische Transformationsmatrix in Form von &quot; Sxx, sxy, syx, SYY, px, PY &quot; [s = Scale, p = Perspective].</span><span class="sxs-lookup"><span data-stu-id="a0ab9-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="a0ab9-734">Die s-Elemente geben an, wie der Schatten in Bezug auf die Form skaliert werden soll, und die p-Elemente geben an, wie der Schatten in Bezug auf die Form verzerrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="a0ab9-735">In der folgenden Matrix wird z. b. die Form um den Faktor 2 angepasst und um den Faktor 4 in alle Richtungen geneigt:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="a0ab9-736">&quot;2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="a0ab9-737">Diese Matrix wird nur verwendet, wenn der Typ des Schattens auf Perspective festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-738">Verdeckt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-738">Obscured</span></span></td>
<td><span data-ttu-id="a0ab9-739"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-740">Der Schatten kann durchsucht werden, wenn die Form nicht ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="a0ab9-741">Der Standardwert lautet False.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-742">Offset</span><span class="sxs-lookup"><span data-stu-id="a0ab9-742">Offset</span></span></td>
<td><span data-ttu-id="a0ab9-743"><a href="#data-types-used-in-the-vml-object-model">Ivgskewoffset</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="a0ab9-744">Die Menge des x-, y-Offsets vom Speicherort der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="a0ab9-745">Der Standardwert ist &quot; 2pt, 2pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-746">Offset2</span></span></td>
<td><span data-ttu-id="a0ab9-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-748">Die Menge des x, y Sekunden Offsets von der Form? s.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="a0ab9-749">Werte sind entweder eine absolute Messung oder ein Bruchteil der Form (-0,5 bis + 0,5).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-750">Ein</span><span class="sxs-lookup"><span data-stu-id="a0ab9-750">On</span></span></td>
<td><span data-ttu-id="a0ab9-751"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-752">Schaltet die Anzeige des Schattens ein und aus.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-753">Opacity</span><span class="sxs-lookup"><span data-stu-id="a0ab9-753">Opacity</span></span></td>
<td><span data-ttu-id="a0ab9-754"><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="a0ab9-755">Deckkraft des Schatten Effekts.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-756">Origin</span><span class="sxs-lookup"><span data-stu-id="a0ab9-756">Origin</span></span></td>
<td><span data-ttu-id="a0ab9-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Ein paar von Bruchteil-Werten von-0,5 bis + 0,5.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-758">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-758">Type</span></span></td>
<td><span data-ttu-id="a0ab9-759"><a href="#data-types-used-in-the-vml-object-model">Vgshadowtype</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="a0ab9-760">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-761">Single (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-761">Single (default)</span></span></li>
<li><span data-ttu-id="a0ab9-762">Double</span><span class="sxs-lookup"><span data-stu-id="a0ab9-762">Double</span></span></li>
<li><span data-ttu-id="a0ab9-763">Perspektive</span><span class="sxs-lookup"><span data-stu-id="a0ab9-763">Perspective</span></span></li>
<li><span data-ttu-id="a0ab9-764">Shaperelative</span><span class="sxs-lookup"><span data-stu-id="a0ab9-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="a0ab9-765">Drawingrelative</span><span class="sxs-lookup"><span data-stu-id="a0ab9-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="a0ab9-766">Emboss</span><span class="sxs-lookup"><span data-stu-id="a0ab9-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="a0ab9-767">Verzerrt-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-767">Skew element</span></span>

<span data-ttu-id="a0ab9-768">Beschreibt einen perspektivischen perspektivischen Effekt auf eine Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="a0ab9-769">Die Schiefe wird auf Vektorgrafik Daten, nicht auf Bilddaten angewendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-770">Matrix</span><span class="sxs-lookup"><span data-stu-id="a0ab9-770">Matrix</span></span> | <span data-ttu-id="a0ab9-771">[Ivgskewmatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-772">Eine perspektivische Transformationsmatrix in der Form "Sxx, sxy, syx, SYY, px, py" \[ s = Scale, p = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="a0ab9-773">Wenn Offset in absoluten Einheiten ist, befinden sich px und py in den Einheiten "EMU ^-1". andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="a0ab9-774">Offset</span><span class="sxs-lookup"><span data-stu-id="a0ab9-774">Offset</span></span> | <span data-ttu-id="a0ab9-775">[Ivgskewoffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-776">Die Menge des x-, y-Offsets vom Speicherort der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="a0ab9-777">Der Standardwert ist "2pt, 2pt".</span><span class="sxs-lookup"><span data-stu-id="a0ab9-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="a0ab9-778">Ein</span><span class="sxs-lookup"><span data-stu-id="a0ab9-778">On</span></span>     | <span data-ttu-id="a0ab9-779">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-780">Schaltet die Anzeige der Schiefe ein bzw. aus.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a0ab9-781">Origin</span><span class="sxs-lookup"><span data-stu-id="a0ab9-781">Origin</span></span> | <span data-ttu-id="a0ab9-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-783">Ein paar von Bruchteil-Werten von-0,5 bis + 0,5.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="a0ab9-784">Stroke-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-784">Stroke element</span></span>

<span data-ttu-id="a0ab9-785">Beschreibt das Zeichnen des Pfads, wenn etwas über eine voll tonlinie hinaus mit einer voll Tonfarbe gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-786">Color</span><span class="sxs-lookup"><span data-stu-id="a0ab9-786">Color</span></span></td>
<td><span data-ttu-id="a0ab9-787"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-788">Die Farbe der Linie.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-788">The color of the line.</span></span> <span data-ttu-id="a0ab9-789">Identisch mit dem Attribut "strokeColor" in Form, überschreibt es jedoch.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-790">Color2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-790">Color2</span></span></td>
<td><span data-ttu-id="a0ab9-791"><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="a0ab9-792">Sekundärfarbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-792">Secondary color.</span></span> <span data-ttu-id="a0ab9-793">Wird verwendet, wenn FillType den Wert Pattern hat.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-794">DashStyle</span></span></td>
<td><span data-ttu-id="a0ab9-795"><strong>Vglinedashstyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="a0ab9-796">Stil Format für Strich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-796">Dash style format.</span></span> <span data-ttu-id="a0ab9-797">Kann ein bestimmter Wert oder eine Sequenz von Zahlen mit einem benutzerdefinierten Bindestrich Muster sein.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="a0ab9-798">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-799">Solid (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-799">Solid (default)</span></span></li>
<li><span data-ttu-id="a0ab9-800">Shortdash</span><span class="sxs-lookup"><span data-stu-id="a0ab9-800">ShortDash</span></span></li>
<li><span data-ttu-id="a0ab9-801">Kurzpunkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-801">ShortDot</span></span></li>
<li><span data-ttu-id="a0ab9-802">Shortdashdot</span><span class="sxs-lookup"><span data-stu-id="a0ab9-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="a0ab9-803">Shortdashdotdot</span><span class="sxs-lookup"><span data-stu-id="a0ab9-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="a0ab9-804">Punkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-804">Dot</span></span></li>
<li><span data-ttu-id="a0ab9-805">Strich</span><span class="sxs-lookup"><span data-stu-id="a0ab9-805">Dash</span></span></li>
<li><span data-ttu-id="a0ab9-806">DashDot</span><span class="sxs-lookup"><span data-stu-id="a0ab9-806">DashDot</span></span></li>
<li><span data-ttu-id="a0ab9-807">Longdash</span><span class="sxs-lookup"><span data-stu-id="a0ab9-807">LongDash</span></span></li>
<li><span data-ttu-id="a0ab9-808">Longdashdot</span><span class="sxs-lookup"><span data-stu-id="a0ab9-808">LongDashDot</span></span></li>
<li><span data-ttu-id="a0ab9-809">Longdashdotdot</span><span class="sxs-lookup"><span data-stu-id="a0ab9-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-810">Umdarrow</span><span class="sxs-lookup"><span data-stu-id="a0ab9-810">EndArrow</span></span></td>
<td><span data-ttu-id="a0ab9-811"><strong>Vgarrowheadstyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="a0ab9-812">Arrowhead für das Ende der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="a0ab9-813">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-814">Keine (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-814">None (default)</span></span></li>
<li><span data-ttu-id="a0ab9-815">Blockieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-815">Block</span></span></li>
<li><span data-ttu-id="a0ab9-816">Klassisch</span><span class="sxs-lookup"><span data-stu-id="a0ab9-816">Classic</span></span></li>
<li><span data-ttu-id="a0ab9-817">Diamond</span><span class="sxs-lookup"><span data-stu-id="a0ab9-817">Diamond</span></span></li>
<li><span data-ttu-id="a0ab9-818">Oval</span><span class="sxs-lookup"><span data-stu-id="a0ab9-818">Oval</span></span></li>
<li><span data-ttu-id="a0ab9-819">Öffnen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-819">Open</span></span></li>
<li><span data-ttu-id="a0ab9-820">Chevron</span><span class="sxs-lookup"><span data-stu-id="a0ab9-820">Chevron</span></span></li>
<li><span data-ttu-id="a0ab9-821">Doublechevron</span><span class="sxs-lookup"><span data-stu-id="a0ab9-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-822">"Tdarrowlength"</span><span class="sxs-lookup"><span data-stu-id="a0ab9-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="a0ab9-823"><strong>Vgarrowheadlength</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="a0ab9-824">Pfeilspitzen Länge für das Ende der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="a0ab9-825">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-826">Short</span><span class="sxs-lookup"><span data-stu-id="a0ab9-826">Short</span></span></li>
<li><span data-ttu-id="a0ab9-827">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-827">Medium (default)</span></span></li>
<li><span data-ttu-id="a0ab9-828">Long</span><span class="sxs-lookup"><span data-stu-id="a0ab9-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-829">"-Rowwidth"</span><span class="sxs-lookup"><span data-stu-id="a0ab9-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="a0ab9-830"><strong>Vgarrowheadwidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="a0ab9-831">Pfeilspitze Breite für das Ende der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="a0ab9-832">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-833">Verringern</span><span class="sxs-lookup"><span data-stu-id="a0ab9-833">Narrow</span></span></li>
<li><span data-ttu-id="a0ab9-834">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-834">Medium (default)</span></span></li>
<li><span data-ttu-id="a0ab9-835">Breite</span><span class="sxs-lookup"><span data-stu-id="a0ab9-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-836">EndCap</span><span class="sxs-lookup"><span data-stu-id="a0ab9-836">EndCap</span></span></td>
<td><span data-ttu-id="a0ab9-837"><strong>Vglineendcapstyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="a0ab9-838">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-839">Flach</span><span class="sxs-lookup"><span data-stu-id="a0ab9-839">Flat</span></span></li>
<li><span data-ttu-id="a0ab9-840">Square</span><span class="sxs-lookup"><span data-stu-id="a0ab9-840">Square</span></span></li>
<li><span data-ttu-id="a0ab9-841">Round</span><span class="sxs-lookup"><span data-stu-id="a0ab9-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-842">FillType</span><span class="sxs-lookup"><span data-stu-id="a0ab9-842">FillType</span></span></td>
<td><span data-ttu-id="a0ab9-843"><strong>Vglinefilltype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="a0ab9-844">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-845">Solid (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-845">Solid (default)</span></span></li>
<li><span data-ttu-id="a0ab9-846">Tile</span><span class="sxs-lookup"><span data-stu-id="a0ab9-846">Tile</span></span></li>
<li><span data-ttu-id="a0ab9-847">Muster</span><span class="sxs-lookup"><span data-stu-id="a0ab9-847">Pattern</span></span></li>
<li><span data-ttu-id="a0ab9-848">Frame</span><span class="sxs-lookup"><span data-stu-id="a0ab9-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-849">Imagealignshape</span><span class="sxs-lookup"><span data-stu-id="a0ab9-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="a0ab9-850"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-851">Richten Sie das Bild mit der Form aus.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-851">Align the image with the shape.</span></span> <span data-ttu-id="a0ab9-852">Wenn false, wird das Bild mit dem Fenster ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-853">Imageaspekt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-853">ImageAspect</span></span></td>
<td><span data-ttu-id="a0ab9-854"><strong>Vgaspecttype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="a0ab9-855">Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="a0ab9-856">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-857">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-857">Value</span></span></th>
<th><span data-ttu-id="a0ab9-858">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-859">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-859">Ignore</span></span></td>
<td><span data-ttu-id="a0ab9-860">Ignoriert Aspekte von Aspekten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-861">Mindestens</span><span class="sxs-lookup"><span data-stu-id="a0ab9-861">AtLeast</span></span></td>
<td><span data-ttu-id="a0ab9-862">Image ist mindestens so groß wie die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-863">Höchstens</span><span class="sxs-lookup"><span data-stu-id="a0ab9-863">AtMost</span></span></td>
<td><span data-ttu-id="a0ab9-864">Das Bild ist nicht größer als die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="a0ab9-865">ImageSize</span></span></td>
<td><span data-ttu-id="a0ab9-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="a0ab9-867">Größe des Bilds, mit dem der Pinsel gebildet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="a0ab9-868">Der Standardwert ist die Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-869">JOINSTYLE</span><span class="sxs-lookup"><span data-stu-id="a0ab9-869">JoinStyle</span></span></td>
<td><span data-ttu-id="a0ab9-870"><strong>Vglinejoinstyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="a0ab9-871">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-872">Round (abgerundetes gemeinsames)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="a0ab9-873">Abgeschrägte (abgeschrägte Verbindung)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="a0ab9-874">Miter (Miter Joint)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-875">LineStyle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-875">LineStyle</span></span></td>
<td><span data-ttu-id="a0ab9-876"><strong>Vglinestyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="a0ab9-877">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-878">Single</span><span class="sxs-lookup"><span data-stu-id="a0ab9-878">Single</span></span></li>
<li><span data-ttu-id="a0ab9-879">Thin Thin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="a0ab9-880">Thin Thick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="a0ab9-881">Dickdünn (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="a0ab9-882">Thickbetweenthin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-883">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="a0ab9-883">MiterLimit</span></span></td>
<td><span data-ttu-id="a0ab9-884"><a href="msdn-online-vml-vglength.md">Länge</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="a0ab9-885">Der maximale Abstand zwischen dem inneren und dem äußeren Punkt eines gemeinsamen Punkts.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="a0ab9-886">Diese Zahl ist ein Vielfaches der Linienstärke.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="a0ab9-887">Liegt zwischen 0 und 32.767.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-888">Ein</span><span class="sxs-lookup"><span data-stu-id="a0ab9-888">On</span></span></td>
<td><span data-ttu-id="a0ab9-889"><a href="msdn-online-vml-vgtristate.md">Vgder State</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="a0ab9-890">Schaltet die Anzeige der Zeile ein und aus.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="a0ab9-891">Identisch mit dem Stroke-Attribut in Form, überschreibt es jedoch.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-892">Opacity</span><span class="sxs-lookup"><span data-stu-id="a0ab9-892">Opacity</span></span></td>
<td><span data-ttu-id="a0ab9-893"><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="a0ab9-894">Deckkraft des Strichs.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-895">Src</span><span class="sxs-lookup"><span data-stu-id="a0ab9-895">Src</span></span></td>
<td><span data-ttu-id="a0ab9-896">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-896">String.</span></span> <span data-ttu-id="a0ab9-897">Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="a0ab9-898">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-899">Startarrow</span><span class="sxs-lookup"><span data-stu-id="a0ab9-899">StartArrow</span></span></td>
<td><span data-ttu-id="a0ab9-900"><strong>Vgarrowheadstyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="a0ab9-901">Pfeilspitze für den Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="a0ab9-902">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-903">Keine (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-903">None (default)</span></span></li>
<li><span data-ttu-id="a0ab9-904">Blockieren</span><span class="sxs-lookup"><span data-stu-id="a0ab9-904">Block</span></span></li>
<li><span data-ttu-id="a0ab9-905">Klassisch</span><span class="sxs-lookup"><span data-stu-id="a0ab9-905">Classic</span></span></li>
<li><span data-ttu-id="a0ab9-906">Diamond</span><span class="sxs-lookup"><span data-stu-id="a0ab9-906">Diamond</span></span></li>
<li><span data-ttu-id="a0ab9-907">Oval</span><span class="sxs-lookup"><span data-stu-id="a0ab9-907">Oval</span></span></li>
<li><span data-ttu-id="a0ab9-908">Öffnen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-908">Open</span></span></li>
<li><span data-ttu-id="a0ab9-909">Chevron</span><span class="sxs-lookup"><span data-stu-id="a0ab9-909">Chevron</span></span></li>
<li><span data-ttu-id="a0ab9-910">Doublechevron</span><span class="sxs-lookup"><span data-stu-id="a0ab9-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-911">Startarrowlength</span><span class="sxs-lookup"><span data-stu-id="a0ab9-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="a0ab9-912">Vgarrowheadlength.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-912">VgArrowHeadLength.</span></span> <span data-ttu-id="a0ab9-913">Pfeilspitzen Länge für den Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="a0ab9-914">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-915">Short</span><span class="sxs-lookup"><span data-stu-id="a0ab9-915">Short</span></span></li>
<li><span data-ttu-id="a0ab9-916">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-916">Medium (default)</span></span></li>
<li><span data-ttu-id="a0ab9-917">Long</span><span class="sxs-lookup"><span data-stu-id="a0ab9-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-918">Startarrowwidth</span><span class="sxs-lookup"><span data-stu-id="a0ab9-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="a0ab9-919">Vgarrowheadwidth.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-919">VgArrowheadWidth.</span></span> <span data-ttu-id="a0ab9-920">Pfeilspitzen Breite für den Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="a0ab9-921">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-922">Schmale mittlere Breite (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-923">Weight</span><span class="sxs-lookup"><span data-stu-id="a0ab9-923">Weight</span></span></td>
<td><span data-ttu-id="a0ab9-924"><a href="msdn-online-vml-vglength.md">Vglength</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="a0ab9-925">Breite der Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-925">Width of line.</span></span> <span data-ttu-id="a0ab9-926">Liegt zwischen 0 und 1584.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="a0ab9-927">Mit dem Attribut "Dashboard" kann der Benutzer ein benutzerdefiniertes Bindestrich Muster angeben.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="a0ab9-928">Dies erfolgt mithilfe einer Reihe von Zahlen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-928">This is done using a series of numbers.</span></span> <span data-ttu-id="a0ab9-929">Dash-Stile werden in Bezug auf die Länge des Bindestrichs (der gezeichnete Teil des Strichs) und die Länge des leer Zeichens zwischen den Bindestrichen definiert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="a0ab9-930">Die Längen sind relativ zur Linienstärke. &quot;die Länge 1 &quot; ist gleich der Linienstärke.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="a0ab9-931">Der EndCap-Stil wird auf jeden Bindestrich angewendet, Pfeil Stile nicht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="a0ab9-932">Die Zeichenfolge definiert zuerst die Länge des Bindestrichs und dann die Länge des Leerraums.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="a0ab9-933">Dies wird möglicherweise wiederholt, um komplexe Dash-Stile zu bilden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="a0ab9-934">Die Zeichenfolge sollte immer ein Zahlenpaar enthalten. Wenn Sie eine ungerade Anzahl von Zahlen enthält, werden die letzten möglicherweise ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="a0ab9-935">In der folgenden Tabelle sind einige typische Werte und eine Beschreibung des beabsichtigten Effekts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="a0ab9-936">&quot;0 &quot; impliziert einen Punkt, der vierfache symmetrisch sein sollte (bei roundendpunkten sollte er ein Kreis sein).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="a0ab9-937">Wenn das Zeilen endlimit flach ist, sollte ein Viewer, sofern möglich, einen integrierten Betriebssystem-Dash auswählen (d.h. etwas, das schnell gezeichnet werden kann).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="a0ab9-938">Im folgenden finden Sie einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-940">kurzstriche (jeder Bindestrich und der zwischen Raum in der Zwischenzeit ist die doppelte Breite der Linie)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-942">Punkt (jeder Bindestrich ist die Breite der Linie, während jeder Leerraum doppelt so breit ist wie die Linie)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-944">Dash (jeder Bindestrich ist viermal so breit wie die Breite der Linie)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-946">langer Bindestrich</span><span class="sxs-lookup"><span data-stu-id="a0ab9-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-948">Bindestrich Punkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-950">Long-Dash-Punkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="a0ab9-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="a0ab9-952">Long-Dash-Punkt Punkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="a0ab9-953">TextPath-Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-953">TextPath element</span></span>

<span data-ttu-id="a0ab9-954">Beschreibt einen Vektor Pfad basierend auf den angegebenen Textdaten, Schriftart und Stilen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="a0ab9-955">Wenn ein Pfad Element angegeben wird, wird der Textpfad nach der Angabe an ein **Pfad** Element geleitet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-956">Fitpath</span><span class="sxs-lookup"><span data-stu-id="a0ab9-956">FitPath</span></span>  | <span data-ttu-id="a0ab9-957">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-958">Gibt den Text an, um den Pfad auszufüllen, in dem er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="a0ab9-959">Fitshape</span><span class="sxs-lookup"><span data-stu-id="a0ab9-959">FitShape</span></span> | <span data-ttu-id="a0ab9-960">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-961">Streckt den Textpfad auf die Ränder des Form Felds.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="a0ab9-962">Ein</span><span class="sxs-lookup"><span data-stu-id="a0ab9-962">On</span></span>       | <span data-ttu-id="a0ab9-963">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-964">Bestimmt, ob die Zeichen Pfade angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="a0ab9-965">String</span><span class="sxs-lookup"><span data-stu-id="a0ab9-965">String</span></span>   | <span data-ttu-id="a0ab9-966">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-966">String.</span></span> <span data-ttu-id="a0ab9-967">Der Text, der als Textpfad dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="a0ab9-968">Glätten</span><span class="sxs-lookup"><span data-stu-id="a0ab9-968">Trim</span></span>     | <span data-ttu-id="a0ab9-969">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-970">Entfernt alle zusätzlichen Speicherplatz, die für Vorgänger und Nachfolger reserviert sind, wenn Sie nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="a0ab9-971">XScale</span><span class="sxs-lookup"><span data-stu-id="a0ab9-971">XScale</span></span>   | <span data-ttu-id="a0ab9-972">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-973">Verwenden Sie die gerade x-Messung anstelle des Pfads.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="a0ab9-974">Im VML-Objektmodell verwendete Datentypen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="a0ab9-975">Die folgenden Datentypen werden vom VML-Objektmodell verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="a0ab9-976">Double</span><span class="sxs-lookup"><span data-stu-id="a0ab9-976">Double</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-977">Fest</span><span class="sxs-lookup"><span data-stu-id="a0ab9-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-978">Integer</span><span class="sxs-lookup"><span data-stu-id="a0ab9-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-979">Ivganpassungen</span><span class="sxs-lookup"><span data-stu-id="a0ab9-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-980">Ivgcolor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-981">Ivgequation</span><span class="sxs-lookup"><span data-stu-id="a0ab9-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-982">Ivgfixedrechteck</span><span class="sxs-lookup"><span data-stu-id="a0ab9-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-983">Ivgfixedrechglearray</span><span class="sxs-lookup"><span data-stu-id="a0ab9-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-984">Ivgformula</span><span class="sxs-lookup"><span data-stu-id="a0ab9-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-985">Ivgformeln</span><span class="sxs-lookup"><span data-stu-id="a0ab9-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-986">Ivggradientcolorarray</span><span class="sxs-lookup"><span data-stu-id="a0ab9-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-987">Ivgpoints</span><span class="sxs-lookup"><span data-stu-id="a0ab9-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-988">Ivgskewmatrix</span><span class="sxs-lookup"><span data-stu-id="a0ab9-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-989">Ivgskewoffset</span><span class="sxs-lookup"><span data-stu-id="a0ab9-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="a0ab9-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="a0ab9-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-992">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-992">Length</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-993">Measure</span><span class="sxs-lookup"><span data-stu-id="a0ab9-993">Measure</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-994">String</span><span class="sxs-lookup"><span data-stu-id="a0ab9-994">String</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-995">Vgblackwhitemode</span><span class="sxs-lookup"><span data-stu-id="a0ab9-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-996">Vgbruchteile</span><span class="sxs-lookup"><span data-stu-id="a0ab9-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="a0ab9-997">Vgvstate</span><span class="sxs-lookup"><span data-stu-id="a0ab9-997">VgTriState</span></span>](/windows)

<span data-ttu-id="a0ab9-998">**Double-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-998">**Double data type**</span></span>

<span data-ttu-id="a0ab9-999">Eine ganze Zahl mit doppelter Genauigkeit mit einem Bereich von-unendlich bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="a0ab9-1000">**Fester Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1000">**Fixed data type**</span></span>

<span data-ttu-id="a0ab9-1001">Gleit Komma Zahl mit einem Bereich von-32.766,0 bis 32.766,0.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="a0ab9-1002">**Integer-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1002">**Integer data type**</span></span>

<span data-ttu-id="a0ab9-1003">Eine ganze Zahl mit einem Bereich von-unendlich bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="a0ab9-1004">**Ivganpassungen-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="a0ab9-1005">Sammlung von Anpassungen einer Form, die zum Ändern der Abmessungen einer Form verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="a0ab9-1006">Anpassungen können als temporäre Platzhalter verwendet werden, oder Sie können aus irgendeinem Grund Variablen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="a0ab9-1007">Es gibt nur 8 Anpassungen in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="a0ab9-1008">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1008">Attributes</span></span> | <span data-ttu-id="a0ab9-1009">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1010">Exists</span></span>     | <span data-ttu-id="a0ab9-1011">[Ivgtrstate](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="a0ab9-1012">Bestimmt, ob eine angegebene Anpassung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="a0ab9-1013">Beachten Sie, dass ein Index verwendet werden muss. Das heißt, "vorhanden" (Element) muss verwendet werden, um das vorhanden sein eines Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a0ab9-1014">Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1014">Item</span></span>       | <span data-ttu-id="a0ab9-1015">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1016">Ein Array von Anpassungen, die von 0 bis 7 indiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="a0ab9-1017">Beachten Sie, dass die Anpassungen möglicherweise sparsam angegeben werden. Das heißt, zwischen Array Werte können nicht immer ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="a0ab9-1018">Beispielsweise können Element 1, 3 und 5 Werte für eine Länge von 3 aufweisen, wobei Item (0), Item (2) und Item (4) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="a0ab9-1019">Um festzustellen, ob ein Element vorhanden ist, verwenden Sie das vorhanden sein-Attribut.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="a0ab9-1020">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1020">Length</span></span>     | <span data-ttu-id="a0ab9-1021">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1022">Anzahl der Anpassungen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1022">Number of adjustments.</span></span> <span data-ttu-id="a0ab9-1023">Darf nicht größer als 8 sein.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a0ab9-1024">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1024">Value</span></span>      | <span data-ttu-id="a0ab9-1025">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1026">Text Darstellung numerischer Werte mit Kommas zwischen den einzelnen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="a0ab9-1027">**Ivgcolor**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1027">**IVgColor**</span></span>

<span data-ttu-id="a0ab9-1028">Gibt eine Farbe an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-1029">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1029">Attributes</span></span></th>
<th><span data-ttu-id="a0ab9-1030">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1031">RGB</span></span></td>
<td><span data-ttu-id="a0ab9-1032"><strong>Vgrgbtype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="a0ab9-1033">RGB-Wert (Long) der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="a0ab9-1034">Nur gültig, wenn der Typ RGB ist.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1035">R</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1035">R</span></span></td>
<td><span data-ttu-id="a0ab9-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="a0ab9-1037">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1037">Red component of the color.</span></span> <span data-ttu-id="a0ab9-1038">Kann zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1039">G</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1039">G</span></span></td>
<td><span data-ttu-id="a0ab9-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="a0ab9-1041">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1041">Green component of the color.</span></span> <span data-ttu-id="a0ab9-1042">Kann zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1043">B</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1043">B</span></span></td>
<td><span data-ttu-id="a0ab9-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="a0ab9-1045">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1045">Blue component of the color.</span></span> <span data-ttu-id="a0ab9-1046">Kann zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1047">String</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1047">String</span></span></td>
<td><span data-ttu-id="a0ab9-1048"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="a0ab9-1049">Text Darstellung der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1049">Text representation of the color.</span></span> <span data-ttu-id="a0ab9-1050">Die folgenden benannten Farb Typen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-1051">Schwarz (#000000)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="a0ab9-1052">Silber (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="a0ab9-1053">Grau (#808080)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="a0ab9-1054">Weiß (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="a0ab9-1055">Maroon (#800000)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="a0ab9-1056">Rot (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="a0ab9-1057">Lila (#800080)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="a0ab9-1058">Fuchsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="a0ab9-1059">Grün (#008000)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="a0ab9-1060">Kalk (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="a0ab9-1061">Oliv (#808000)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="a0ab9-1062">Gelb (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="a0ab9-1063">Navy (#000080)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="a0ab9-1064">Blau (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="a0ab9-1065">Teal (#008080)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="a0ab9-1066">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1067">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1067">Type</span></span></td>
<td><span data-ttu-id="a0ab9-1068"><strong>Vgcolortype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="a0ab9-1069">Der Typ der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1069">Type of color.</span></span> <span data-ttu-id="a0ab9-1070">Einer der folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-1071">Mixed</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1071">Mixed</span></span></li>
<li><span data-ttu-id="a0ab9-1072">benannt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1072">Named</span></span></li>
<li><span data-ttu-id="a0ab9-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1073">RGB</span></span></li>
<li><span data-ttu-id="a0ab9-1074">Schema</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0ab9-1075">**Ivgequation**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1075">**IVgEquation**</span></span>

<span data-ttu-id="a0ab9-1076">Für Formeln verwendete Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1077">Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1077">Operation</span></span></td>
<td><span data-ttu-id="a0ab9-1078"><strong>Vgequationoperationtype</strong> Der Name des Vorgangs, der für die Parameter durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="a0ab9-1079">Die folgenden Vorgänge können in einer Gleichung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-1080">Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1080">Operation</span></span></th>
<th><span data-ttu-id="a0ab9-1081">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1082">Abs</span></span></td>
<td><span data-ttu-id="a0ab9-1083">Absoluter Wert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1083">Absolute value.</span></span> <br/> <span data-ttu-id="a0ab9-1084"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1085">Atan2</span></span></td>
<td><span data-ttu-id="a0ab9-1086">Polar Arithmetik: führt zu FD-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="a0ab9-1087"><strong>atan2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1088">Cos</span></span></td>
<td><span data-ttu-id="a0ab9-1089">Kosinus, Argument in FD-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="a0ab9-1090">v \* <strong>cos</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="a0ab9-1092">Behält die vollständige Genauigkeit in der zwischen Berechnung bei.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="a0ab9-1093">v \* <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="a0ab9-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1094">Ellipse</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1094">Ellipse</span></span></td>
<td><span data-ttu-id="a0ab9-1095">Ellipse</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1096">Wenn</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1096">If</span></span></td>
<td><span data-ttu-id="a0ab9-1097">Bei Bedingungs Test.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1097">If Condition test.</span></span> <span data-ttu-id="a0ab9-1098">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="a0ab9-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="a0ab9-1099">P1: P2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1100">Max.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1100">Max</span></span></td>
<td><span data-ttu-id="a0ab9-1101">Der größere von zwei-Werten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="a0ab9-1102"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1103">Mid</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1103">Mid</span></span></td>
<td><span data-ttu-id="a0ab9-1104">Durchschnitt (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1105">Min</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1105">Min</span></span></td>
<td><span data-ttu-id="a0ab9-1106">Der kleinere von zwei-Werten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1106">The lesser of two values.</span></span> <span data-ttu-id="a0ab9-1107"><strong>Min</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1108">Mod</span></span></td>
<td><span data-ttu-id="a0ab9-1109">Modulo</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1110">Produkt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1110">Product</span></span></td>
<td><span data-ttu-id="a0ab9-1111">Wird für Multiplikation und Division verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1111">Used for multiplication and division.</span></span> <span data-ttu-id="a0ab9-1112">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1113">Sin</span></span></td>
<td><span data-ttu-id="a0ab9-1114">Sinus, Argument in FD-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="a0ab9-1115">v \* <strong>Sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="a0ab9-1117">Behält die vollständige Genauigkeit in der zwischen Berechnung bei.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="a0ab9-1118">v \* <strong>Sin</strong>(<strong>atan2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1119">Sqrt</span></span></td>
<td><span data-ttu-id="a0ab9-1120">Das Ergebnis ist positiv und wird abgerundet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="a0ab9-1121"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1122">SUM</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1122">Sum</span></span></td>
<td><span data-ttu-id="a0ab9-1123">Wird für Addition und Subtraktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="a0ab9-1124">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1125">Sumangle</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1125">Sumangle</span></span></td>
<td><span data-ttu-id="a0ab9-1126">Vorhandener Winkel (skaliert durch 65536), wobei P1 und P2 in Grad liegen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="a0ab9-1127">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1128">Tan</span></span></td>
<td><span data-ttu-id="a0ab9-1129">Tangens, Argument in FD-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="a0ab9-1130">v \* Tan (P1)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1131">Val</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1131">Val</span></span></td>
<td><span data-ttu-id="a0ab9-1132">Definiert einen Führungs Wert aus einem anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1133">Param1</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1133">Param1</span></span></td>
<td><span data-ttu-id="a0ab9-1134"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="a0ab9-1135">Der erste Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="a0ab9-1137"><strong>Vgformulaparamtype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="a0ab9-1138">Der Typ des ersten Parameters.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1138">The type of the first parameter.</span></span> <span data-ttu-id="a0ab9-1139">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-1140">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1140">Type</span></span></th>
<th><span data-ttu-id="a0ab9-1141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1142">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1142">Value</span></span></td>
<td><span data-ttu-id="a0ab9-1143">Der Parameter ist ein einfacher Wert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1144">"Anpassungen Reference"</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="a0ab9-1145">Der-Parameter ist ein Verweis auf eine-Anpassung.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="a0ab9-1146">Wenn der erste Parameter z. b. 1 ist, wird der Wert der ersten Anpassung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1147">Formulareferenzierung</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="a0ab9-1148">Der-Parameter ist das Ergebnis eines Verweises auf das Ergebnis einer vorherigen Formel.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="a0ab9-1149">Wenn der erste Parameter z. b. 2 ist, wird das Ergebnis von Formel 2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1150">Param2</span></span></td>
<td><span data-ttu-id="a0ab9-1151"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="a0ab9-1152">Der zweite Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="a0ab9-1154"><strong>Vgformulaparamtype</strong> Der Typ des Parameters 2.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1155">Val</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1155">Val</span></span></td>
<td><span data-ttu-id="a0ab9-1156"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="a0ab9-1157">Das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1158">Valtype2</span></span></td>
<td><span data-ttu-id="a0ab9-1159"><strong>Vgformulaparamtype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="a0ab9-1160">Der Typ des Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0ab9-1161">**Ivgfixedrechteck**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="a0ab9-1162">Gibt ein festes Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="a0ab9-1163">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1163">Attributes</span></span> | <span data-ttu-id="a0ab9-1164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1165">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1165">Value</span></span>      | <span data-ttu-id="a0ab9-1166">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1167">Textwert, der den Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="a0ab9-1168">Links</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1168">Left</span></span>       | <span data-ttu-id="a0ab9-1169">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1170">Ganz links-Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="a0ab9-1171">Oben</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1171">Top</span></span>        | <span data-ttu-id="a0ab9-1172">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1173">Oberste Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="a0ab9-1174">Rechts</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1174">Right</span></span>      | <span data-ttu-id="a0ab9-1175">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1176">Rechte Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="a0ab9-1177">bottom</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1177">Bottom</span></span>     | <span data-ttu-id="a0ab9-1178">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1179">Die untersten Koordinaten des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="a0ab9-1180">**Ivgfixedrechglearray**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="a0ab9-1181">Array fester Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="a0ab9-1182">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1182">Attributes</span></span> | <span data-ttu-id="a0ab9-1183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1184">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1184">Value</span></span>      | <span data-ttu-id="a0ab9-1185">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1186">Text Darstellung des Arrays.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="a0ab9-1187">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1187">Length</span></span>     | <span data-ttu-id="a0ab9-1188">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1189">Anzahl der Rechtecke in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="a0ab9-1190">Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1190">Item</span></span>       | <span data-ttu-id="a0ab9-1191">[Ivgfixedrechteck](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1192">Das Rechteck Objekt am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="a0ab9-1193">**Ivgformula-** Datentyp</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="a0ab9-1194">Definitionen für Formeln, die den Pfad einer Form variieren oder zu anderen Berechnungs Zwecken verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="a0ab9-1195">Formeln können auf dem **ADJ** -Attribut einer Form basieren, die sich ändern kann.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="a0ab9-1196">Formeln können auch auf andere Formeln verweisen.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="a0ab9-1197">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1197">Attributes</span></span> | <span data-ttu-id="a0ab9-1198">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1199">Eqn</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1199">Eqn</span></span>        | <span data-ttu-id="a0ab9-1200">[Ivgequation.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1201">Jede Formel definiert einen einzelnen Wert als Ergebnis der Auswertung des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="a0ab9-1202">Der Ausdruck wird durch dieses Attribut definiert und verfügt über die allgemeine Form eines Vorgangs, gefolgt von bis zu drei Argumenten, bei denen es sich um Anpassungs Werte (z. b. \# 2), die Ergebnisse früherer Formeln (z. b. @2 ), festgelegte Zahlen oder vordefinierte Werte handeln kann.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="a0ab9-1203">**Ivgformeln-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="a0ab9-1204">Eine Auflistung von Formel Objekten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="a0ab9-1205">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1205">Attributes</span></span> | <span data-ttu-id="a0ab9-1206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1207">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1207">Length</span></span>     | <span data-ttu-id="a0ab9-1208">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1209">Anzahl der Formel Objekte in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="a0ab9-1210">Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1210">Item</span></span>       | <span data-ttu-id="a0ab9-1211">[Ivgformula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1212">Eine bestimmte Formel.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1212">A specific formula.</span></span> <span data-ttu-id="a0ab9-1213">Beachten Sie, dass das Formel Array den Shape-Typ als Abbildung vererbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="a0ab9-1214">**Ivggradientcolorarray**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="a0ab9-1215">Ein Array von Farben, die einen Farbverlauf (gemischter Bereich von Farben) definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="a0ab9-1216">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1216">Attributes</span></span> | <span data-ttu-id="a0ab9-1217">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1218">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1218">Value</span></span>      | <span data-ttu-id="a0ab9-1219">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1220">Gibt das Array von Farben an. Beispiel: "Red. 2; grün. 4; schwarz. 7 "</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="a0ab9-1221">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1221">Length</span></span>     | <span data-ttu-id="a0ab9-1222">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1223">Anzahl der Farben im Array.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="a0ab9-1224">Methoden</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1224">Methods</span></span>     | <span data-ttu-id="a0ab9-1225">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1226">Addcolor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1226">AddColor</span></span>    | <span data-ttu-id="a0ab9-1227">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="a0ab9-1228">Fügt eine neue Farbe an dem Durchbruch angegebenen Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="a0ab9-1229">Die neue Farbe ist standardmäßig weiß und ist der Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="a0ab9-1230">Die Farbe kann dann als Verweis geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="a0ab9-1231">Removecolor</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1231">RemoveColor</span></span> | <span data-ttu-id="a0ab9-1232">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="a0ab9-1233">Entfernt eine Farbe an einem Endpunkt, der durch einen Bruchteil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="a0ab9-1234">Hinweis: Wenn 0,0 oder 1,0 nicht vorhanden ist, wird dies impliziert und die Farbe weiß an diesem Punkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="a0ab9-1235">**Ivgpoints-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="a0ab9-1236">Ein Array von Punkten, die eine Form definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="a0ab9-1237">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1237">Attributes</span></span> | <span data-ttu-id="a0ab9-1238">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab9-1239">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1239">Value</span></span>      | <span data-ttu-id="a0ab9-1240">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1241">Text Darstellung des Arrays.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="a0ab9-1242">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1242">Length</span></span>     | <span data-ttu-id="a0ab9-1243">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="a0ab9-1244">Anzahl der Punkte in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="a0ab9-1245">Element</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1245">Item</span></span>       | <span data-ttu-id="a0ab9-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="a0ab9-1247">Der Punkt am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="a0ab9-1248">**Ivgskewmatrix-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="a0ab9-1249">Eine Matrix, die für verzerrende Formen verwendet wird, eine perspektivische Transformationsmatrix in der Form "*Sxx, sxy, syx, SYY, px, PY* " \[ *s* = Scale, *p* = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="a0ab9-1250">Wenn Offset in absoluten Einheiten ist, befinden sich *px und py* in den Einheiten "EMU ^-1". andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="a0ab9-1251">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1251">Attributes</span></span>   | <span data-ttu-id="a0ab9-1252">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="a0ab9-1253">Xtox</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1253">XtoX</span></span>         | <span data-ttu-id="a0ab9-1254">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="a0ab9-1255">Ytox</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1255">YtoX</span></span>         | <span data-ttu-id="a0ab9-1256">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="a0ab9-1257">Xtoy</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1257">XtoY</span></span>         | <span data-ttu-id="a0ab9-1258">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="a0ab9-1259">Ytoy</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1259">YtoY</span></span>         | <span data-ttu-id="a0ab9-1260">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="a0ab9-1261">Perspectivex</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1261">PerspectiveX</span></span> | <span data-ttu-id="a0ab9-1262">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="a0ab9-1263">Perspectivey</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1263">PerspectiveY</span></span> | <span data-ttu-id="a0ab9-1264">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="a0ab9-1265">**Ivgskewoffset**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="a0ab9-1266">Gibt den Offset der Schiefe an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-1267">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1267">Attributes</span></span></th>
<th><span data-ttu-id="a0ab9-1268">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1269">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1269">Value</span></span></td>
<td><span data-ttu-id="a0ab9-1270"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="a0ab9-1271">Text Darstellung des Offsets.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1272">X</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1272">X</span></span></td>
<td><span data-ttu-id="a0ab9-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1274">X-Komponente.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1274">X component.</span></span> <span data-ttu-id="a0ab9-1275">Prozentsatz oder Measure.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1275">Percentage or measure.</span></span> <span data-ttu-id="a0ab9-1276">Wenn keine Einheiten enthalten sind, wird der shaperelative Typ impliziert. Andernfalls wird der absolute Typ impliziert.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1277">J</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1277">Y</span></span></td>
<td><span data-ttu-id="a0ab9-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1279">Y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1280">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1280">Type</span></span></td>
<td><span data-ttu-id="a0ab9-1281"><strong>Vgskewtransformtype</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="a0ab9-1282">Gibt den Typ der Transformation an.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="a0ab9-1283">Gültige Werte sind ganzzahlige Punkte im Bereich von-unendlich und unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-1284">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1284">Type</span></span></th>
<th><span data-ttu-id="a0ab9-1285">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1286">Shaperelative</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="a0ab9-1287">Die Werte des Offsets sind Prozentsätze (Verhältnisse) der Größe der ursprünglichen Form. der Wert 0,5 bedeutet z. b. einen Offset der Hälfte der Form.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1288">Absolut</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1288">Absolute</span></span></td>
<td><span data-ttu-id="a0ab9-1289">Die Werte sind absolute Einheiten.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0ab9-1290">**IVgVector2D-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="a0ab9-1291">Gibt einen zweidimensionalen Vektor an, der aus zwei **doppelten** Zahlen besteht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ab9-1292">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1292">Attributes</span></span></th>
<th><span data-ttu-id="a0ab9-1293">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1294">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1294">Value</span></span></td>
<td><span data-ttu-id="a0ab9-1295"><strong>Zeichenfolge</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1295"><strong>String</strong>.</span></span> <span data-ttu-id="a0ab9-1296">Eine Text Darstellung beider Vektor Zahlen, die durch ein Leerzeichen voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1297">X</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1297">X</span></span></td>
<td><span data-ttu-id="a0ab9-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1299">X-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1300">J</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1300">Y</span></span></td>
<td><span data-ttu-id="a0ab9-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1302">Y-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1303">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1303">Type</span></span></td>
<td><span data-ttu-id="a0ab9-1304"><strong>Vgvector Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="a0ab9-1305">Erwartete Einheiten für diesen Vektor.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1305">Expected units for this vector.</span></span> <span data-ttu-id="a0ab9-1306">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-1307">Measure</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1307">Measure</span></span></li>
<li><span data-ttu-id="a0ab9-1308">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1308">Length</span></span></li>
<li><span data-ttu-id="a0ab9-1309">Angler</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="a0ab9-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1310">Fraction</span></span></li>
<li><span data-ttu-id="a0ab9-1311">Ganzzahl in Prozent</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0ab9-1312">**IVgVector3D-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="a0ab9-1313">Gibt einen dreidimensionalen Vektor an, der aus drei **doppelten** Zahlen besteht.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1314">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1314">Value</span></span></td>
<td><span data-ttu-id="a0ab9-1315"><strong>Zeichenfolge</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1315"><strong>String</strong>.</span></span> <span data-ttu-id="a0ab9-1316">Text Darstellung von drei Vektor Zahlen, die durch ein Leerzeichen voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1317">X</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1317">X</span></span></td>
<td><span data-ttu-id="a0ab9-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1319">X-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1320">J</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1320">Y</span></span></td>
<td><span data-ttu-id="a0ab9-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1322">Y-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0ab9-1323">Z</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1323">Z</span></span></td>
<td><span data-ttu-id="a0ab9-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="a0ab9-1325">Z-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0ab9-1326">type</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1326">Type</span></span></td>
<td><span data-ttu-id="a0ab9-1327"><strong>Vgvector Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="a0ab9-1328">Erwartete Einheiten für diesen Vektor.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1328">Expected units for this vector.</span></span> <span data-ttu-id="a0ab9-1329">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="a0ab9-1330">Measure</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1330">Measure</span></span></li>
<li><span data-ttu-id="a0ab9-1331">Länge</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1331">Length</span></span></li>
<li><span data-ttu-id="a0ab9-1332">Angler</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="a0ab9-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1333">Fraction</span></span></li>
<li><span data-ttu-id="a0ab9-1334">Zahl</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1334">Number</span></span></li>
<li><span data-ttu-id="a0ab9-1335">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1335">Percentage</span></span></li>
<li><span data-ttu-id="a0ab9-1336">Integer</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0ab9-1337">**Length-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1337">**Length data type**</span></span>

<span data-ttu-id="a0ab9-1338">Eine Gleit Komma Zahl mit einem Bereich von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="a0ab9-1339">**Measure-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1339">**Measure data type**</span></span>

<span data-ttu-id="a0ab9-1340">Eine Gleit Komma Zahl von-unendlich bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="a0ab9-1341">**String-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1341">**String data type**</span></span>

<span data-ttu-id="a0ab9-1342">Zeichendaten beliebiger Länge.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1342">Character data of any length.</span></span>

<span data-ttu-id="a0ab9-1343">**Vgblackwhitemode**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="a0ab9-1344">Renderingmodus für schwarz und weiß.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="a0ab9-1345">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1345">Possible values are:</span></span>

-   <span data-ttu-id="a0ab9-1346">**Farbe**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1346">**Color**</span></span>
-   <span data-ttu-id="a0ab9-1347">**Automatisch**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1347">**Auto**</span></span>
-   <span data-ttu-id="a0ab9-1348">**Graustufen**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1348">**GrayScale**</span></span>
-   <span data-ttu-id="a0ab9-1349">**Lightgrayscale**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="a0ab9-1350">**Inverton**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1350">**InverseGray**</span></span>
-   <span data-ttu-id="a0ab9-1351">**Grayoutline**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="a0ab9-1352">**Blacktextandlines**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="a0ab9-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1353">**HighContrast**</span></span>
-   <span data-ttu-id="a0ab9-1354">**Schwarz**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1354">**Black**</span></span>
-   <span data-ttu-id="a0ab9-1355">**Weiß**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1355">**White**</span></span>
-   <span data-ttu-id="a0ab9-1356">**Rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1356">**Undrawn**</span></span>

<span data-ttu-id="a0ab9-1357">**Vgbruchdatentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1357">**VgFraction data type**</span></span>

<span data-ttu-id="a0ab9-1358">Gleit Komma Zahl mit einem Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="a0ab9-1359">Bruchzahlen können auch als Prozentsatz angegeben werden. z. b. "50%".</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="a0ab9-1360">**Vgvstate-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="a0ab9-1361">Enumeration, die für Werte verwendet wird, die einen von drei Zuständen haben können:</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="a0ab9-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1362">**TRUE**</span></span>
-   <span data-ttu-id="a0ab9-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1363">**FALSE**</span></span>
-   <span data-ttu-id="a0ab9-1364">**GEMISCHT**</span><span class="sxs-lookup"><span data-stu-id="a0ab9-1364">**MIXED**</span></span>