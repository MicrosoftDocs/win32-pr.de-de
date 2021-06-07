---
title: VML-Objektmodellreferenz
description: In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444821"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="9b5f6-104">VML-Objektmodellreferenz</span><span class="sxs-lookup"><span data-stu-id="9b5f6-104">VML Object Model Reference</span></span>

<span data-ttu-id="9b5f6-105">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9b5f6-106">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9b5f6-107">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9b5f6-108">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9b5f6-109">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9b5f6-110">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9b5f6-111">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-111">In this topic:</span></span>

-   [<span data-ttu-id="9b5f6-112">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9b5f6-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9b5f6-113">Example</span></span>](#example)
-   [<span data-ttu-id="9b5f6-114">Einrichten von VML</span><span class="sxs-lookup"><span data-stu-id="9b5f6-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="9b5f6-115">VML OM-Referenz</span><span class="sxs-lookup"><span data-stu-id="9b5f6-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="9b5f6-116">Shape-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="9b5f6-117">Unterelemente des Shape-Elements</span><span class="sxs-lookup"><span data-stu-id="9b5f6-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="9b5f6-118">Background-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="9b5f6-119">Element "Extrusion"</span><span class="sxs-lookup"><span data-stu-id="9b5f6-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="9b5f6-120">Fill-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="9b5f6-121">Group-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="9b5f6-122">Imagedata-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="9b5f6-123">Path-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="9b5f6-124">Shadow-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="9b5f6-125">Skew-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="9b5f6-126">Stroke-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="9b5f6-127">TextPath-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="9b5f6-128">Im VML-Objektmodell verwendete Datentypen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="9b5f6-129">Einführung</span><span class="sxs-lookup"><span data-stu-id="9b5f6-129">Introduction</span></span>

<span data-ttu-id="9b5f6-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) ist eine textbasierte Sprache, die [XML](https://www.w3.org/TR/REC-xml.mdl) verwendet, um HTML zum Anzeigen von Vektorgrafikinformationen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="9b5f6-131">Der VML-Dokumentobjektmodell (DOM) definiert eine programmgesteuerte Schnittstelle für die Bearbeitung der Dokumentelemente.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="9b5f6-132">Dadurch kann der Benutzer Vektorgrafiken dynamisch über eine plattform- und sprachneutrale Schnittstelle erstellen und ändern.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="9b5f6-133">Das VML-DOM entspricht der [Dokumentobjektmodell](https://www.w3.org/TR/REC-DOM-Level-1/) Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="9b5f6-134">VML verwendet das [Shape-Element](#shape-element) als grundlegenden Baustein für Vektorgrafikbilder.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="9b5f6-135">Nachdem eine Form erstellt wurde, können Sie die Form über Attribute oder angefügte Unterelemente ändern.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="9b5f6-136">Um beispielsweise die Farbe einer Form zu ändern, weisen Sie dem **FillColor-Attribut** einen Farbwert zu.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="9b5f6-137">Einige der Attribute einer Form sind ebenfalls [Unterelemente](/windows) und verfügen über eigene Attribute, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="9b5f6-138">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9b5f6-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="9b5f6-139">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9b5f6-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="9b5f6-140">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="9b5f6-141">Gruppe</span><span class="sxs-lookup"><span data-stu-id="9b5f6-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="9b5f6-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="9b5f6-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="9b5f6-143">Pfad</span><span class="sxs-lookup"><span data-stu-id="9b5f6-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="9b5f6-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="9b5f6-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="9b5f6-145">Neigen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="9b5f6-146">Takt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="9b5f6-147">Textpath</span><span class="sxs-lookup"><span data-stu-id="9b5f6-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="9b5f6-148">Die VML OM verwendet mehrere [Datentypen,](/windows) um Parameter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="9b5f6-149">Datentypen mit dem Präfix "Vg" sind Enumerationen, und solche mit dem Präfix "IVg" sind Objekte.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="9b5f6-150">Klicken Sie hier, um eine Liste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-150">Click here for a list.</span></span> <span data-ttu-id="9b5f6-151">Kleinere Datentypen werden mit bestimmten Parametern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="9b5f6-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9b5f6-152">Example</span></span>

<span data-ttu-id="9b5f6-153">Der folgende VBScript-Code zeigt, wie Sie eine einfache Form erstellen:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="9b5f6-154">Im obigen Beispiel wird eine Form mithilfe der Dokumentobjektmodell Methode **CreateElement** erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="9b5f6-155">Die Form ist eine vordefinierte VML-Rect-Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="9b5f6-156">Obwohl das Objekt vorhanden ist, kann es nicht Teil des Dokuments sein, bis es an das Dokument angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="9b5f6-157">Mithilfe der **AppendChild-Methode** wird rect zu einem untergeordneten Element eines **DIV-Elements** namens MyDiv.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="9b5f6-158">Einige minimale Stilattribute (**Position**, **Breite**, **Höhe**, **Top**, **Links**) werden festgelegt, um der Form eine bestimmte Größe zu geben.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="9b5f6-159">Schließlich wird eine Farbe mit dem **FillColor-Attribut** zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="9b5f6-160">Beachten Sie, dass jede Skriptsprache oder jede Sprache verwendet werden kann, die mit Dokumentobjektmodell Schnittstellen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="9b5f6-161">Einrichten von VML</span><span class="sxs-lookup"><span data-stu-id="9b5f6-161">Setting up VML</span></span>

<span data-ttu-id="9b5f6-162">Eine Implementierung von VML erfolgt über Microsoft Internet Explorer 5.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="9b5f6-163">Um das Renderingobjekt auf einer Webseite ordnungsgemäß einzurichten, müssen die folgenden Ergänzungen vorgenommen werden:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="9b5f6-164">Das Schema muss in der anfänglichen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="9b5f6-165">tag wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="9b5f6-166">Das Renderingverhalten muss Teil des Dokumentstils sein:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="9b5f6-167">Das folgende Beispiel zeigt eine HTML-Beispielwebseite, die ordnungsgemäß für VML eingerichtet wurde und die dynamische Erstellung einer Form zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="9b5f6-168">Beachten Sie, dass in Betaversionen ein ActiveX-Objekttag und ein anderes Verhalten erforderlich waren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="9b5f6-169">VML OM-Referenz</span><span class="sxs-lookup"><span data-stu-id="9b5f6-169">VML OM Reference</span></span>

<span data-ttu-id="9b5f6-170">Dieser Verweis definiert das [Shape-Element,](#shape-element) die Unterelemente und [die](/windows) [Datentypen,](/windows)die vom Objektmodell von VML verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="9b5f6-171">Shape-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-171">Shape element</span></span>

<span data-ttu-id="9b5f6-172">Formen sind die Bausteine grafischer Bilder, die von Vector Markup Language (VML) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="9b5f6-173">Die Form ist das Element der obersten Ebene, und mehrere Unterelemente helfen dabei, die Art der einzelnen Formen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="9b5f6-174">VML stellt vordefinierte Formen bereit:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="9b5f6-175">**Shape-Attribute**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="9b5f6-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-176">**Arc**</span></span>
-   <span data-ttu-id="9b5f6-177">**Kurve**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-177">**Curve**</span></span>
-   <span data-ttu-id="9b5f6-178">**Line**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-178">**Line**</span></span>
-   <span data-ttu-id="9b5f6-179">**Polylinie**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-179">**PolyLine**</span></span>
-   <span data-ttu-id="9b5f6-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-180">**Rect**</span></span>
-   <span data-ttu-id="9b5f6-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-181">**RoundRect**</span></span>



|   <span data-ttu-id="9b5f6-182">Unterelement</span><span class="sxs-lookup"><span data-stu-id="9b5f6-182">Subelement</span></span>           |    <span data-ttu-id="9b5f6-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-184">Adj</span><span class="sxs-lookup"><span data-stu-id="9b5f6-184">Adj</span></span>          | <span data-ttu-id="9b5f6-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="9b5f6-186">Eine durch Trennzeichen getrennte Liste von Zahlen, die die Parameter für die Führungsformeln sind, die den Pfad der Form definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="9b5f6-187">Werte können weggelassen werden, um die Verwendung von Standardwerten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="9b5f6-188">Es können bis zu 8 Anpassungswerte vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="9b5f6-189">ALT</span><span class="sxs-lookup"><span data-stu-id="9b5f6-189">Alt</span></span>          | <span data-ttu-id="9b5f6-190">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-190">String.</span></span> <span data-ttu-id="9b5f6-191">Alternativer Text, der der Form zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-191">Alternative text associated with shape.</span></span> <span data-ttu-id="9b5f6-192">Wird für das nicht grafische Durchsuchen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9b5f6-193">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9b5f6-193">Button</span></span>       | <span data-ttu-id="9b5f6-194">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-195">Zeigt das Schaltflächenverhalten beim Klicken an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9b5f6-196">BWMode</span><span class="sxs-lookup"><span data-stu-id="9b5f6-196">BWMode</span></span>       | <span data-ttu-id="9b5f6-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9b5f6-198">Bestimmt, wie die Form in der Schwarz-Weiß-Ansicht in Apps oder auf Schwarz-Weiß-Druckern gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="9b5f6-199">Zu den Werten gehören: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9b5f6-200">Standard: **Automatisch.**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="9b5f6-201">BWNormal</span><span class="sxs-lookup"><span data-stu-id="9b5f6-201">BWNormal</span></span>     | <span data-ttu-id="9b5f6-202">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="9b5f6-203">Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in normalem Schwarz/Weiß verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="9b5f6-204">Zu den Werten zählen: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9b5f6-205">Standardeinstellung: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="9b5f6-206">BWPure</span><span class="sxs-lookup"><span data-stu-id="9b5f6-206">BWPure</span></span>       | <span data-ttu-id="9b5f6-207">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="9b5f6-208">Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in reinen B/W-Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="9b5f6-209">Zu den Werten zählen: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="9b5f6-210">Standardeinstellung: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="9b5f6-211">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="9b5f6-211">ChildShapes</span></span>  | <span data-ttu-id="9b5f6-212">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-212">IVgGroupShapes.</span></span> <span data-ttu-id="9b5f6-213">Eine Auflistung anderer Formen in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="9b5f6-214">Diese Auflistung unterstützt die Standardmethoden Length und Item.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9b5f6-215">Key</span><span class="sxs-lookup"><span data-stu-id="9b5f6-215">Chromakey</span></span>    | <span data-ttu-id="9b5f6-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9b5f6-217">Ein Farbwert, der transparent ist und alles hinter der Form zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9b5f6-218">Control1</span><span class="sxs-lookup"><span data-stu-id="9b5f6-218">Control1</span></span>     | <span data-ttu-id="9b5f6-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-220">Kontrollpunkt für die Kurve.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b5f6-221">Control2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-221">Control2</span></span>     | <span data-ttu-id="9b5f6-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-223">Kontrollpunkt für die Kurve.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b5f6-224">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="9b5f6-224">CoordOrigin</span></span>  | <span data-ttu-id="9b5f6-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Die Koordinaten in der oberen linken Ecke des Containerrechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="9b5f6-226">Bereich von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9b5f6-227">CoordSize</span><span class="sxs-lookup"><span data-stu-id="9b5f6-227">CoordSize</span></span>    | <span data-ttu-id="9b5f6-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-229">Die Breite und Höhe des Koordinatenraums innerhalb des Verweisrechtecks dieser Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="9b5f6-230">Wenn er nicht angegeben wird, ist er identisch mit der Breite und Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="9b5f6-231">Bereich von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-231">Range from 0 to infinity.</span></span> <span data-ttu-id="9b5f6-232">Standardwert: "1000,1000".</span><span class="sxs-lookup"><span data-stu-id="9b5f6-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="9b5f6-233">EndAngle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-233">EndAngle</span></span>     | <span data-ttu-id="9b5f6-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9b5f6-235">Endwinkel der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9b5f6-236">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9b5f6-236">Extrusion</span></span>    | <span data-ttu-id="9b5f6-237">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-237">IVgExtrusion.</span></span> <span data-ttu-id="9b5f6-238">Gibt den Wert desExtrusionsobjekts für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="9b5f6-239">Weitere Informationen finden Sie im [Element "Extrusion".](msdn-online-vml-extrusion-element.md)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9b5f6-240">Füllung</span><span class="sxs-lookup"><span data-stu-id="9b5f6-240">Fill</span></span>         | <span data-ttu-id="9b5f6-241">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-241">VgFillFormat.</span></span> <span data-ttu-id="9b5f6-242">Gibt den Füllwert für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="9b5f6-243">Weitere Informationen [finden Sie](msdn-online-vml-fill-element.md) unter Fill-Element.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="9b5f6-244">Fillcolor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-244">FillColor</span></span>    | <span data-ttu-id="9b5f6-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9b5f6-246">Die Primäre Farbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b5f6-247">Gefüllt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-247">Filled</span></span>       | <span data-ttu-id="9b5f6-248">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-249">True gibt an, dass der Pfad, der die Form definiert, ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="9b5f6-250">Standardmäßig wird sie mit einer Volltonfarbe aufgefüllt, es sei denn, es gibt ein Fill-Unterelement, das komplexere Fülleigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="9b5f6-251">False gibt an, dass die Füllung transparent ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="9b5f6-252">Kippen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-252">Flip</span></span>         | <span data-ttu-id="9b5f6-253">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-253">VgFlipOrientation.</span></span> <span data-ttu-id="9b5f6-254">Werte sind: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="9b5f6-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9b5f6-255">ForceDash</span><span class="sxs-lookup"><span data-stu-id="9b5f6-255">ForceDash</span></span>    | <span data-ttu-id="9b5f6-256">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-257">Gibt an, dass eine gestrichelte Kontur gerendert werden soll, wenn es keine Linie und keine Füllung für eine Form gibt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="9b5f6-258">Dieses Verhalten ist im Allgemeinen nützlich, um unsichtbare Formen in Bearbeitungsanwendungen sichtbar zu machen, damit sie ausgewählt und bearbeitet werden können, z. B. in einer Bildkarte.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="9b5f6-259">Formeln</span><span class="sxs-lookup"><span data-stu-id="9b5f6-259">Formulas</span></span>     | <span data-ttu-id="9b5f6-260">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-260">IVgFormulas.</span></span> <span data-ttu-id="9b5f6-261">Ein Array von Formeln, das eine Form definiert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9b5f6-262">Von</span><span class="sxs-lookup"><span data-stu-id="9b5f6-262">From</span></span>         | <span data-ttu-id="9b5f6-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-264">Startpunkt der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9b5f6-265">Href</span><span class="sxs-lookup"><span data-stu-id="9b5f6-265">HRef</span></span>         | <span data-ttu-id="9b5f6-266">[Zeichenfolge.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-267">Die URL, zu der gesprungen werden soll, wenn auf diese Form geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9b5f6-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="9b5f6-268">ImageData</span></span>    | <span data-ttu-id="9b5f6-269">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-269">IVgImageData.</span></span> <span data-ttu-id="9b5f6-270">Bildinformationen, wenn die Form ein Bild ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="9b5f6-271">Weitere Informationen finden Sie im ImageData-Element.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9b5f6-272">OnEd</span><span class="sxs-lookup"><span data-stu-id="9b5f6-272">OnEd</span></span>         | <span data-ttu-id="9b5f6-273">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-274">Blendet alle Handles außer der oberen linken und unteren rechten Ecke aus, wie in den Ziehpunkten für ein gerades Liniensegment.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="9b5f6-275">Opacity</span><span class="sxs-lookup"><span data-stu-id="9b5f6-275">Opacity</span></span>      | <span data-ttu-id="9b5f6-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9b5f6-277">Die Deckkraft der gesamten Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-277">The opacity of the entire shape.</span></span> <span data-ttu-id="9b5f6-278">Eine Zahl zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b5f6-279">Pfad</span><span class="sxs-lookup"><span data-stu-id="9b5f6-279">Path</span></span>         | <span data-ttu-id="9b5f6-280">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-280">IVgPath.</span></span> <span data-ttu-id="9b5f6-281">Eine Zeichenfolge, die die Befehle enthält, die den Pfad definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b5f6-282">Punkte</span><span class="sxs-lookup"><span data-stu-id="9b5f6-282">Points</span></span>       | <span data-ttu-id="9b5f6-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="9b5f6-284">Eine Auflistung von Punkten, die eine Form definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9b5f6-285">Drucken</span><span class="sxs-lookup"><span data-stu-id="9b5f6-285">Print</span></span>        | <span data-ttu-id="9b5f6-286">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-287">True gibt an, dass diese Form gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b5f6-288">Drehung</span><span class="sxs-lookup"><span data-stu-id="9b5f6-288">Rotation</span></span>     | <span data-ttu-id="9b5f6-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9b5f6-290">Legt die Drehung der Form fest.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-290">Sets rotation of shape.</span></span> <span data-ttu-id="9b5f6-291">Der Wert wird an den Formstil propagiert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9b5f6-292">Skalieren</span><span class="sxs-lookup"><span data-stu-id="9b5f6-292">Scale</span></span>        | <span data-ttu-id="9b5f6-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-294">Formskala.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b5f6-295">Shadow</span><span class="sxs-lookup"><span data-stu-id="9b5f6-295">Shadow</span></span>       | <span data-ttu-id="9b5f6-296">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-296">IVgShadow.</span></span> <span data-ttu-id="9b5f6-297">Gibt den Schatten für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="9b5f6-298">Weitere Informationen [finden Sie](msdn-online-vml-shadow-element.md) im Shadow-Element.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b5f6-299">Spt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-299">Spt</span></span>          | <span data-ttu-id="9b5f6-300">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b5f6-301">Startangle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-301">StartAngle</span></span>   | <span data-ttu-id="9b5f6-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="9b5f6-303">Startwinkel der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b5f6-304">Stroke</span><span class="sxs-lookup"><span data-stu-id="9b5f6-304">Stroke</span></span>       | <span data-ttu-id="9b5f6-305">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-305">VgStrokeFormat.</span></span> <span data-ttu-id="9b5f6-306">Weitere Informationen finden Sie unter Stroke-Element.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b5f6-307">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-307">StrokeColor</span></span>  | <span data-ttu-id="9b5f6-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9b5f6-309">Die Primäre Farbe des Pinsels, der zum Strichen des Pfads dieser Form verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9b5f6-310">Streichelte</span><span class="sxs-lookup"><span data-stu-id="9b5f6-310">Stroked</span></span>      | <span data-ttu-id="9b5f6-311">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-312">True gibt an, dass der Pfad, der die Form definiert, stricht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9b5f6-313">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="9b5f6-313">StrokeWeight</span></span> | <span data-ttu-id="9b5f6-314">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="9b5f6-315">Die Breite des Pinsels, der zum Strichen des Pfads verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="9b5f6-316">Liegt zwischen 0 und 1584.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b5f6-317">Textpath</span><span class="sxs-lookup"><span data-stu-id="9b5f6-317">TextPath</span></span>     | <span data-ttu-id="9b5f6-318">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-318">IVgTextPath.</span></span> <span data-ttu-id="9b5f6-319">Gibt das TextPath-Objekt der Form an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="9b5f6-320">Weitere Informationen finden Sie im [TextPath-Element.](msdn-online-vml-textpath-element.md)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b5f6-321">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b5f6-321">To</span></span>           | <span data-ttu-id="9b5f6-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-323">Endpunkt der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b5f6-324">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-324">Type</span></span>         | <span data-ttu-id="9b5f6-325">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-325">String.</span></span> <span data-ttu-id="9b5f6-326">Typ der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="9b5f6-327">Unterelemente des Shape-Elements</span><span class="sxs-lookup"><span data-stu-id="9b5f6-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="9b5f6-328">Die folgenden Unterelemente sind Teil des VML-Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="9b5f6-329">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9b5f6-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="9b5f6-330">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9b5f6-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="9b5f6-331">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="9b5f6-332">Gruppe</span><span class="sxs-lookup"><span data-stu-id="9b5f6-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="9b5f6-333">Imagedata</span><span class="sxs-lookup"><span data-stu-id="9b5f6-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="9b5f6-334">Pfad</span><span class="sxs-lookup"><span data-stu-id="9b5f6-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="9b5f6-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="9b5f6-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="9b5f6-336">Neigen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="9b5f6-337">Takt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="9b5f6-338">Textpath</span><span class="sxs-lookup"><span data-stu-id="9b5f6-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="9b5f6-339">Background-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-339">Background element</span></span>

<span data-ttu-id="9b5f6-340">Beschreibt die Füllung des Hintergrunds einer Seite mithilfe von VML-Füllungen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="9b5f6-341">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-341">Attribute</span></span>        |   <span data-ttu-id="9b5f6-342">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-343">BWMode</span><span class="sxs-lookup"><span data-stu-id="9b5f6-343">BWMode</span></span>    | <span data-ttu-id="9b5f6-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9b5f6-345">Bestimmt, wie die Form in der Schwarz-Weiß-Ansicht in Anwendungen oder beim Drucken gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="9b5f6-346">BWNormal</span><span class="sxs-lookup"><span data-stu-id="9b5f6-346">BWNormal</span></span>  | <span data-ttu-id="9b5f6-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9b5f6-348">Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in normalem Schwarz-Weiß-Modus herangezogen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="9b5f6-349">BWPure</span><span class="sxs-lookup"><span data-stu-id="9b5f6-349">BWPure</span></span>    | <span data-ttu-id="9b5f6-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="9b5f6-351">Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in reinem Schwarz-Weiß-Modus herangezogen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="9b5f6-352">Füllung</span><span class="sxs-lookup"><span data-stu-id="9b5f6-352">Fill</span></span>      | <span data-ttu-id="9b5f6-353">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-353">VgFillFormat.</span></span> <span data-ttu-id="9b5f6-354">Gibt die Füllung für diese Form an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="9b5f6-355">Weitere [](msdn-online-vml-fill-element.md) Informationen finden Sie unter Fill-Element.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="9b5f6-356">Fillcolor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-356">FillColor</span></span> | <span data-ttu-id="9b5f6-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9b5f6-358">Die Primäre Farbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="9b5f6-359">Duplikat des Color-Werts im Fill-Element.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="9b5f6-360">Der Standardwert ist Weiß.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="9b5f6-361">Element "Extrusion"</span><span class="sxs-lookup"><span data-stu-id="9b5f6-361">Extrusion element</span></span>

<span data-ttu-id="9b5f6-362">Beschreibt eine 3D-Extrusion der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="9b5f6-363">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-364">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="9b5f6-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="9b5f6-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-366">True gibt an, dass der Mittelpunkt der Drehung der Gruppe von 3D-Objekten (tatsächlich gibt es immer nur ein Objekt in der Gruppe) automatisch als Mittelpunkt der Gruppe bestimmt wird. Andernfalls wird sie durch die RotationCenter-Parameter bestimmt, die einen Bruchteil der Form darstellen, wobei 0,0,0 der Mittelpunkt ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-367">BackDepth</span><span class="sxs-lookup"><span data-stu-id="9b5f6-367">BackDepth</span></span></td>
<td><span data-ttu-id="9b5f6-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="9b5f6-369">Umfang der Rückwärtsextrusion.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-369">Amount of backward extrusion.</span></span> <span data-ttu-id="9b5f6-370">Liegt zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-371">Brightness</span><span class="sxs-lookup"><span data-stu-id="9b5f6-371">Brightness</span></span></td>
<td><span data-ttu-id="9b5f6-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9b5f6-373">Allgemeine Helligkeit der Szene.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-373">Overall brightness of the scene.</span></span> <span data-ttu-id="9b5f6-374">Der Standardwert ist &quot; 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-375">Color</span><span class="sxs-lookup"><span data-stu-id="9b5f6-375">Color</span></span></td>
<td><span data-ttu-id="9b5f6-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9b5f6-377">Die Farbe derExtrusion.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-377">The color of the extrusion.</span></span> <span data-ttu-id="9b5f6-378">Wird nur verwendet, wenn ColorMode benutzerdefiniert ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="9b5f6-379">Andernfalls legt Auto die Farbe des Effekts für dieExtrusion auf die gleiche fest wie FillColor.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-380">ColorMode</span><span class="sxs-lookup"><span data-stu-id="9b5f6-380">ColorMode</span></span></td>
<td><span data-ttu-id="9b5f6-381">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-381">Vg3DColorMode.</span></span> <span data-ttu-id="9b5f6-382">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-383">Auto (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-383">Auto (default)</span></span></li>
<li><span data-ttu-id="9b5f6-384">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-385">Diffusity</span><span class="sxs-lookup"><span data-stu-id="9b5f6-385">Diffusity</span></span></td>
<td><span data-ttu-id="9b5f6-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9b5f6-387">Das Verhältnis des Incidents zum diffus reflektierten Licht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="9b5f6-388">Werte kleiner als 1,0 sind normal, aber Werte, die höher als 1 sind, können interessante Effekte erzeugen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-389">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-389">Edge</span></span></td>
<td><span data-ttu-id="9b5f6-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9b5f6-391">Legt die Größe eines simulierten gerundeten abgedrehten Rands fest.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="9b5f6-392">Liegt in Gleitkomma pts zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="9b5f6-393">Der Standardwert ist &quot; &quot; 1pt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-394">Facet</span><span class="sxs-lookup"><span data-stu-id="9b5f6-394">Facet</span></span></td>
<td><span data-ttu-id="9b5f6-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9b5f6-396">Legt das Facet der Szene fest.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-396">Sets the facet of the scene.</span></span> <span data-ttu-id="9b5f6-397">Der Standardwert ist &quot; 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-398">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="9b5f6-398">ForeDepth</span></span></td>
<td><span data-ttu-id="9b5f6-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9b5f6-400">Umfang der Vorwärtsextrusion.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-400">Amount of forward extrusion.</span></span> <span data-ttu-id="9b5f6-401">Liegt zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-402">LightFace</span><span class="sxs-lookup"><span data-stu-id="9b5f6-402">LightFace</span></span></td>
<td><span data-ttu-id="9b5f6-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-404">Gibt an, ob die Vorderseite des Objekts auf Änderungen in der 3D-Beleuchtung reagiert, z. B. wenn sich ein Objekt dreht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-405">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="9b5f6-405">LightHarsh</span></span></td>
<td><span data-ttu-id="9b5f6-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-407">Beleuchten der Beleuchtung für die primäre Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="9b5f6-408">Der Standardwert lautet False.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="9b5f6-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-411">Beleuchten der Beleuchtung für die sekundäre Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="9b5f6-412">Der Standardwert lautet False.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-413">LightLevel</span><span class="sxs-lookup"><span data-stu-id="9b5f6-413">LightLevel</span></span></td>
<td><span data-ttu-id="9b5f6-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="9b5f6-415">Intensität der primären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-415">Intensity of the primary light source.</span></span> <span data-ttu-id="9b5f6-416">Der Standardwert ist &quot; 38000. &quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-417">LightLevel2</span></span></td>
<td><span data-ttu-id="9b5f6-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="9b5f6-419">Intensität der sekundären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="9b5f6-420">Der Standardwert ist &quot; 38000. &quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-421">LightPosition</span><span class="sxs-lookup"><span data-stu-id="9b5f6-421">LightPosition</span></span></td>
<td><span data-ttu-id="9b5f6-422">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-422">Vector3D.</span></span> <span data-ttu-id="9b5f6-423">Position der primären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-423">Position of the primary light source.</span></span> <span data-ttu-id="9b5f6-424">Der Standardwert &quot; ist 50000,0,10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-425">LightPosition2</span></span></td>
<td><span data-ttu-id="9b5f6-426">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-426">Vector3D.</span></span> <span data-ttu-id="9b5f6-427">Position der sekundären Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-427">Position of the secondary light source.</span></span> <span data-ttu-id="9b5f6-428">Der Standardwert &quot; ist -50000,0,10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-429">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="9b5f6-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="9b5f6-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-431">&quot;Lockrotationcenter bedeutet, dass die Drehung der Gruppe durch Drehwinkel[1] Grad um die y-Achse auf der Seite definiert ist, gefolgt von Drehwinkel[0] Grad um die &quot; x-Achse.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="9b5f6-432">Wenn LockRotationCenter auf False festgelegt ist, wird die Drehung als Ausrichtungswinkelgrad um den durch die Ausrichtung definierten Vektor definiert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="9b5f6-433">Beispielsweise entspricht lockrotationcenter=false orientationangle=45 orientation=(0,1,0) lockrotationcenter=true rotationangle=(0,45).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-434">Metallisch</span><span class="sxs-lookup"><span data-stu-id="9b5f6-434">Metal</span></span></td>
<td><span data-ttu-id="9b5f6-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-436">Bewirkt, dass das spiegelnde Licht die Materialfarbe und nicht die Hellquellenfarbe ist, wodurch das Objekt farbig erscheint.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-437">Ein</span><span class="sxs-lookup"><span data-stu-id="9b5f6-437">On</span></span></td>
<td><span data-ttu-id="9b5f6-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-439">Schaltet die Anzeige desExtrusionseffekts ein und aus.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-440">Orientation</span><span class="sxs-lookup"><span data-stu-id="9b5f6-440">Orientation</span></span></td>
<td><span data-ttu-id="9b5f6-441">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-441">Vector3D.</span></span> <span data-ttu-id="9b5f6-442">Ausrichtung der Kamera.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-443">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="9b5f6-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9b5f6-445">Winkel zwischen der Ausrichtung der Kamera und der XY-Ebene.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-446">Ebene</span><span class="sxs-lookup"><span data-stu-id="9b5f6-446">Plane</span></span></td>
<td><span data-ttu-id="9b5f6-447">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="9b5f6-448">Ermöglicht dieExtrusion von orthogonalen Ebenen zur Bildschirmebene.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="9b5f6-449">Erfordert, dass ForeDepth und BackDepth in Zeicheneinheiten anstelle von Emus angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="9b5f6-450">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-451">Xy</span><span class="sxs-lookup"><span data-stu-id="9b5f6-451">XY</span></span></li>
<li><span data-ttu-id="9b5f6-452">Zx</span><span class="sxs-lookup"><span data-stu-id="9b5f6-452">ZX</span></span></li>
<li><span data-ttu-id="9b5f6-453">Yz</span><span class="sxs-lookup"><span data-stu-id="9b5f6-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-454">Rendern</span><span class="sxs-lookup"><span data-stu-id="9b5f6-454">Render</span></span></td>
<td><span data-ttu-id="9b5f6-455">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-455">Vg3DRenderMode.</span></span> <span data-ttu-id="9b5f6-456">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-457">Solid (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-457">Solid (default)</span></span></li>
<li><span data-ttu-id="9b5f6-458">Drahtmodell</span><span class="sxs-lookup"><span data-stu-id="9b5f6-458">WireFrame</span></span></li>
<li><span data-ttu-id="9b5f6-459">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="9b5f6-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-460">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-460">RotationAngle</span></span></td>
<td><span data-ttu-id="9b5f6-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-462">AngleX, AngleY oder AngleZ wird durch das ShapeRotation-Attribut gesteuert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-463">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="9b5f6-463">RotationCenter</span></span></td>
<td><span data-ttu-id="9b5f6-464">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-464">Vector3D.</span></span> <span data-ttu-id="9b5f6-465">Mittelpunkt der Drehung.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-466">Schläfrigkeit</span><span class="sxs-lookup"><span data-stu-id="9b5f6-466">Shininess</span></span></td>
<td><span data-ttu-id="9b5f6-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9b5f6-468">Bestimmt, wie konzentriert oder verteilt die spiegelförmige Reflektion ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="9b5f6-469">Ein hoher Wert wäre 8 bis 10 und würde einem Spiegel ungefähren, und ein niedriger Wert wäre 2 bis 3 und würde der vereerten Bekleidung ungefähren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="9b5f6-470">Werte von 3 bis 7 werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="9b5f6-471">Hohe Werte spiegeln punktgenaue Lichtquellen wider.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-472">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-472">SkewAmt</span></span></td>
<td><span data-ttu-id="9b5f6-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="9b5f6-474">Wenn Type auf Parallel festgelegt ist, bestimmt das Attribut die Menge der Schiefe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="9b5f6-475">Liegt zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-476">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-476">SkewAngle</span></span></td>
<td><span data-ttu-id="9b5f6-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9b5f6-478">Wenn Type auf Parallel festgelegt ist, bestimmt das Attribut den Grad der Schiefe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="9b5f6-479">Der Standardwert ist &quot; -45. &quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-480">Specularity</span><span class="sxs-lookup"><span data-stu-id="9b5f6-480">Specularity</span></span></td>
<td><span data-ttu-id="9b5f6-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="9b5f6-482">Das Verhältnis zwischen Vorfall und spiegelnd reflektierten Lichten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="9b5f6-483">Werte kleiner als 1,0 sind normal, aber Werte, die höher als 1 sind, können interessante Effekte erzeugen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-484">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-484">Type</span></span></td>
<td><span data-ttu-id="9b5f6-485">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-485">VgExtrusionType.</span></span> <span data-ttu-id="9b5f6-486">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-487">Parallel (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="9b5f6-488">Perspektive</span><span class="sxs-lookup"><span data-stu-id="9b5f6-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-489">Sicht</span><span class="sxs-lookup"><span data-stu-id="9b5f6-489">Viewpoint</span></span></td>
<td><span data-ttu-id="9b5f6-490">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-490">Vector3D.</span></span> <span data-ttu-id="9b5f6-491">Der Punkt, von dem aus die Szene angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-492">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="9b5f6-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="9b5f6-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-494">Kann Werte zwischen 0,5 und -0,5 haben, um den Ursprung des Blickpunkts innerhalb des Umrandungsfelds der Form zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="9b5f6-495">Fill-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-495">Fill element</span></span>

<span data-ttu-id="9b5f6-496">Beschreibt, wie ein Pfad für Füllungen ausgefüllt werden soll, die komplexer als eine Volltonfarbe sind.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="9b5f6-497">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-498">AlignShape</span><span class="sxs-lookup"><span data-stu-id="9b5f6-498">AlignShape</span></span></td>
<td><span data-ttu-id="9b5f6-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-500">Richten Sie das Bild an der Form aus.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-500">Align the image with the shape.</span></span> <span data-ttu-id="9b5f6-501">False gibt an, dass das Bild mit dem Fenster ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-502">Angle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-502">Angle</span></span></td>
<td><span data-ttu-id="9b5f6-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="9b5f6-504">Der Winkel, entlang dem der Farbverlauf verläuft.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="9b5f6-505">0 Grad liegt entlang der horizontalen Achse von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-506">Aspekt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-506">Aspect</span></span></td>
<td><span data-ttu-id="9b5f6-507"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="9b5f6-508">Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="9b5f6-509">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-510">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-510">Value</span></span></th>
<th><span data-ttu-id="9b5f6-511">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-512">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9b5f6-512">Ignore</span></span></td>
<td><span data-ttu-id="9b5f6-513">Ignorieren von Aspektproblemen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-514">Atleast</span><span class="sxs-lookup"><span data-stu-id="9b5f6-514">AtLeast</span></span></td>
<td><span data-ttu-id="9b5f6-515">Das Bild ist mindestens so groß wie die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-516">AtMost</span><span class="sxs-lookup"><span data-stu-id="9b5f6-516">AtMost</span></span></td>
<td><span data-ttu-id="9b5f6-517">Das Bild ist nicht größer als die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-518">Color</span><span class="sxs-lookup"><span data-stu-id="9b5f6-518">Color</span></span></td>
<td><span data-ttu-id="9b5f6-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Die Hauptfüllfarbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="9b5f6-520">Identisch mit dem FillColor-Attribut in Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-521">Color2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-521">Color2</span></span></td>
<td><span data-ttu-id="9b5f6-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9b5f6-523">Die sekundäre Farbe für eine Füllung, wenn der Bildtyp Muster oder eine Farbverlaufsfüllung ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-524">Farben</span><span class="sxs-lookup"><span data-stu-id="9b5f6-524">Colors</span></span></td>
<td><span data-ttu-id="9b5f6-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="9b5f6-526">Zwischenfarben im Farbverlauf und ihre relativen Positionen entlang des Farbverlaufs, z. B. &quot; 30 % Rot, 70 % Blau, 90 % &quot; Grün.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="9b5f6-527">Primäre Farbe (Farbattribut in Form) ist 0 % und sekundäre Farbe (Color2-Attribut) 100 %.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-528">Fokus</span><span class="sxs-lookup"><span data-stu-id="9b5f6-528">Focus</span></span></td>
<td><span data-ttu-id="9b5f6-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="9b5f6-530">Fokuspunkt für lineare Farbverlaufsfüllung.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="9b5f6-531">Die Werte liegen zwischen -100 und +100.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-532">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="9b5f6-532">FocusPosition</span></span></td>
<td><span data-ttu-id="9b5f6-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-534">Position des innersten Rechtecks für radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="9b5f6-535">Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-536">FocusSize</span><span class="sxs-lookup"><span data-stu-id="9b5f6-536">FocusSize</span></span></td>
<td><span data-ttu-id="9b5f6-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Größe des innersten Rechtecks für radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="9b5f6-538">Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-539">Methode</span><span class="sxs-lookup"><span data-stu-id="9b5f6-539">Method</span></span></td>
<td><span data-ttu-id="9b5f6-540">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-540">VgSigmaType.</span></span> <span data-ttu-id="9b5f6-541">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-542">Keine</span><span class="sxs-lookup"><span data-stu-id="9b5f6-542">None</span></span></li>
<li><span data-ttu-id="9b5f6-543">Linear</span><span class="sxs-lookup"><span data-stu-id="9b5f6-543">Linear</span></span></li>
<li><span data-ttu-id="9b5f6-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="9b5f6-544">Sigma</span></span></li>
<li><span data-ttu-id="9b5f6-545">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9b5f6-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="9b5f6-546">Der Standardwert ist Sigma.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-547">Ein</span><span class="sxs-lookup"><span data-stu-id="9b5f6-547">On</span></span></td>
<td><span data-ttu-id="9b5f6-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-549">Aktiviert die Füllanzeige.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-549">Turns fill display on.</span></span> <span data-ttu-id="9b5f6-550">Identisch mit dem Fill-Attribut in Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-551">Opacity</span><span class="sxs-lookup"><span data-stu-id="9b5f6-551">Opacity</span></span></td>
<td><span data-ttu-id="9b5f6-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9b5f6-553">Deckkraft der Füllung.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-554">Opacity2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-554">Opacity2</span></span></td>
<td><span data-ttu-id="9b5f6-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9b5f6-556">Die sekundäre Deckkraft für Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-557">Origin</span><span class="sxs-lookup"><span data-stu-id="9b5f6-557">Origin</span></span></td>
<td><span data-ttu-id="9b5f6-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-559">Zeigen Sie relativ zur oberen linken Ecke des Bilds, das als Ursprung des Bilds behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="9b5f6-560">Der Standardwert ist die Mitte des Images.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-560">Default is the center of the image.</span></span> <span data-ttu-id="9b5f6-561">Der Vektor ist ein Bruchteil (von 0,0 bis 1,0) der Breite und Höhe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-562">Position</span><span class="sxs-lookup"><span data-stu-id="9b5f6-562">Position</span></span></td>
<td><span data-ttu-id="9b5f6-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-564">Zeigen Sie auf das Verweisrechteck der Form, um den Ursprung des Bilds zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="9b5f6-565">Der Standardwert ist die Mitte des Containerrechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="9b5f6-566">Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-567">Size</span><span class="sxs-lookup"><span data-stu-id="9b5f6-567">Size</span></span></td>
<td><span data-ttu-id="9b5f6-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-569">Die Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-569">The size of the image.</span></span> <span data-ttu-id="9b5f6-570">Der Standardwert ist die Pixelgröße des Bilds.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-570">Default is pixel size of the image.</span></span> <span data-ttu-id="9b5f6-571">Kann in absoluten Koordinaten oder in Prozent angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-572">Src</span><span class="sxs-lookup"><span data-stu-id="9b5f6-572">Src</span></span></td>
<td><span data-ttu-id="9b5f6-573"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge.</a></span><span class="sxs-lookup"><span data-stu-id="9b5f6-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9b5f6-574">URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9b5f6-575">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-576">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-576">Type</span></span></td>
<td><span data-ttu-id="9b5f6-577">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-577">VgFillType.</span></span> <span data-ttu-id="9b5f6-578">Es kann sich um einen der folgenden Typen handeln:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-579">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9b5f6-579">Background</span></span></li>
<li><span data-ttu-id="9b5f6-580">Frame</span><span class="sxs-lookup"><span data-stu-id="9b5f6-580">Frame</span></span></li>
<li><span data-ttu-id="9b5f6-581">Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="9b5f6-581">Gradient</span></span></li>
<li><span data-ttu-id="9b5f6-582">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="9b5f6-582">GradientCenter</span></span></li>
<li><span data-ttu-id="9b5f6-583">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="9b5f6-583">GradientRadial</span></span></li>
<li><span data-ttu-id="9b5f6-584">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-584">GradientTitle</span></span></li>
<li><span data-ttu-id="9b5f6-585">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="9b5f6-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="9b5f6-586">Muster</span><span class="sxs-lookup"><span data-stu-id="9b5f6-586">Pattern</span></span></li>
<li><span data-ttu-id="9b5f6-587">Basis</span><span class="sxs-lookup"><span data-stu-id="9b5f6-587">Solid</span></span></li>
<li><span data-ttu-id="9b5f6-588">Tile</span><span class="sxs-lookup"><span data-stu-id="9b5f6-588">Tile</span></span></li>
</ul>
<span data-ttu-id="9b5f6-589">Für Kachel, Muster und Frame müssen die Bildattribute angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="9b5f6-590">Gradient und GradientRadial erfordern, dass die Farbverlaufsattribute bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="9b5f6-591">Group-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-591">Group element</span></span>

<span data-ttu-id="9b5f6-592">Eine Gruppe ist eine Sammlung einzelner Formen, die als Einheit positioniert und transformiert werden können.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="9b5f6-593">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-593">Attribute</span></span>        |   <span data-ttu-id="9b5f6-594">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-595">Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-595">Item</span></span>   | <span data-ttu-id="9b5f6-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-597">Angegebenes Element im Array von Formen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="9b5f6-598">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-598">Length</span></span> | <span data-ttu-id="9b5f6-599">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-600">Anzahl der Formen in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="9b5f6-601">Imagedata-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-601">Imagedata element</span></span>

<span data-ttu-id="9b5f6-602">Beschreibt ein Bild, das über einer Form gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="9b5f6-603">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-603">Attribute</span></span>        |   <span data-ttu-id="9b5f6-604">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-605">BiLevel</span><span class="sxs-lookup"><span data-stu-id="9b5f6-605">BiLevel</span></span>     | <span data-ttu-id="9b5f6-606">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-607">Bild nur in zwei Farben anzeigen (in der Regel Schwarz und Weiß).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="9b5f6-608">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="9b5f6-608">BlackLevel</span></span>  | <span data-ttu-id="9b5f6-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9b5f6-610">Ermöglicht die Anpassung, die Ebene so festzulegen, dass Schwarz als echtes Schwarz angezeigt wird und alle anderen Farben als Schattierungen oberhalb von Schwarz sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9b5f6-611">Key (Schlüssel)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-611">Chromakey</span></span>   | <span data-ttu-id="9b5f6-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9b5f6-613">Transparente Bildfarbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9b5f6-614">CropBottom</span><span class="sxs-lookup"><span data-stu-id="9b5f6-614">CropBottom</span></span>  | <span data-ttu-id="9b5f6-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-616">Zuschneiden des Abstands vom unteren Rand des Bilds als Prozentsatz der Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="9b5f6-617">CropLeft</span><span class="sxs-lookup"><span data-stu-id="9b5f6-617">CropLeft</span></span>    | <span data-ttu-id="9b5f6-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-619">Zuschneiden des Abstands vom linken Bildrand als Bruchteil der Bildgröße (von 0,0 bis 1,0).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="9b5f6-620">"Out-Cropping" wird jedoch unterstützt, und daher werden Werte von kleiner als 0 und größer als 1 unterstützt. Beispielsweise würde -5, 20 die Begrenzungen um das 25-fache der Bildgröße mit 4/5 auf einer Seite des Bilds ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="9b5f6-621">CropRight</span><span class="sxs-lookup"><span data-stu-id="9b5f6-621">CropRight</span></span>   | <span data-ttu-id="9b5f6-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-623">Zuschneiden des Abstands von der rechten Seite des Bilds als Prozentsatz der Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="9b5f6-624">CropTop</span><span class="sxs-lookup"><span data-stu-id="9b5f6-624">CropTop</span></span>     | <span data-ttu-id="9b5f6-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-626">Zuschneiden des Abstands vom oberen Rand des Bilds als Prozentsatz der Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="9b5f6-627">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-627">EmbossColor</span></span> | <span data-ttu-id="9b5f6-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="9b5f6-629">Dies wird auf einen Prozentsatz der Schattenfarbe festgelegt, um einen einprägten Bildeffekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="9b5f6-630">Gewinnen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-630">Gain</span></span>        | <span data-ttu-id="9b5f6-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-632">Passt die Intensität aller Farben an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="9b5f6-633">Legt im Wesentlichen fest, wie hell weiß sein wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="9b5f6-634">Liegt zwischen 0 und 32767.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="9b5f6-635">Gamma</span><span class="sxs-lookup"><span data-stu-id="9b5f6-635">Gamma</span></span>       | <span data-ttu-id="9b5f6-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9b5f6-637">Gammakorrektur.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-637">Gamma correction.</span></span> <span data-ttu-id="9b5f6-638">Durch erhöhen des Bilds wird der Kontrast erhöht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b5f6-639">GrayScale</span><span class="sxs-lookup"><span data-stu-id="9b5f6-639">GrayScale</span></span>   | <span data-ttu-id="9b5f6-640">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-641">Bild in Graustufenfarben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9b5f6-642">Src</span><span class="sxs-lookup"><span data-stu-id="9b5f6-642">Src</span></span>         | <span data-ttu-id="9b5f6-643">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-644">URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9b5f6-645">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten verweisen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="9b5f6-646">Path-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-646">Path element</span></span>

<span data-ttu-id="9b5f6-647">Definiert den Pfad, aus dem die Form besteht, mithilfe einer Zeichenfolge, die einen umfangreichen Satz von "Stiftbewegungsbefehlen" enthält.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-648">Limo</span><span class="sxs-lookup"><span data-stu-id="9b5f6-648">Limo</span></span></td>
<td><span data-ttu-id="9b5f6-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="9b5f6-650">Definiert den Punkt, an dem die Form gestreckt wird. Beispielsweise würde sich bei einer Form vom 16. Bis zum 16.000.000.000-Mal der Mittelpunkt auf dem Strich befindet. Wenn also die Größe der Form geändert wird, streckt sich der Strich, und der Rest der Form erhält seine Abmessungen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-651">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="9b5f6-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="9b5f6-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="9b5f6-653">Array, das die Rechtecke enthält, die definieren, wohin Text gehen soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-654">V</span><span class="sxs-lookup"><span data-stu-id="9b5f6-654">V</span></span></td>
<td><span data-ttu-id="9b5f6-655"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9b5f6-656">Entspricht dem v-Attribut im Path-Tag.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="9b5f6-657">Beachten Sie, dass der Pfad dem Path-Attribut oder -Element entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-658">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-658">Value</span></span></td>
<td><span data-ttu-id="9b5f6-659"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9b5f6-660">Eine Textdarstellung der Befehle, die den Pfad definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="9b5f6-661">X- oder y-Koordinatenwerte können ein Verweis auf eine Formel in der Form &quot; @# &quot; sein, wobei # die Ordnungszahl der Formel ist, z. &quot; @2 &quot; B. .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="9b5f6-662">Diese Attributzeichenfolge besteht aus einem umfangreichen Satz von Befehlen, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-663">Befehl</span><span class="sxs-lookup"><span data-stu-id="9b5f6-663">Command</span></span></th>
<th><span data-ttu-id="9b5f6-664">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-665">ae (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="9b5f6-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span><span class="sxs-lookup"><span data-stu-id="9b5f6-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="9b5f6-667">Zeichnen eines Segments einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="9b5f6-668">Eine gerade Linie wird vom aktuellen Punkt bis zum Anfangspunkt des Segments gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-669">al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="9b5f6-670">Identisch mit ae, außer dass ein implizites m bis zum Anfangspunkt des Segments vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-671">ar (arc)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-671">ar (arc)</span></span></td>
<td><span data-ttu-id="9b5f6-672">Identisch mit at.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-672">Same as at.</span></span> <span data-ttu-id="9b5f6-673">Ein neuer Unterpfad wird jedoch durch ein impliziertes m bis zum Anfangspunkt des Bogens gestartet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-674">at (arcto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-674">at (arcto)</span></span></td>
<td><span data-ttu-id="9b5f6-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9b5f6-676">Die ersten vier Werte definieren den Begrenzungsfeld einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="9b5f6-677">Die letzten vier definieren zwei radiale Vektoren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-677">The last four define two radial vectors.</span></span> <span data-ttu-id="9b5f6-678">Es wird ein Segment der Ellipse gezeichnet, das am durch den Startradiusvektor definierten Winkel beginnt und am durch den Endvektor definierten Winkel endet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="9b5f6-679">Eine gerade Linie wird vom aktuellen Punkt bis zum Anfang des Bogens gezeichnet. Der Bogen wird immer gegen den Uhrzeigersinn gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-680">c (curveto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-680">c (curveto)</span></span></td>
<td><span data-ttu-id="9b5f6-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>bis</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="9b5f6-682">Zeichnen Sie eine kubische Bézierkurve vom aktuellen Punkt bis zur Koordinate, die von den letzten beiden Parametern angegeben wird, den Kontrollpunkten, die von den ersten vier Parametern angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="9b5f6-683">Der aktuelle Punkt wird zum Endpunkt des Bézierers.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-684">e (ende)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-684">e (end)</span></span></td>
<td><span data-ttu-id="9b5f6-685">Beenden Sie den aktuellen Satz von Unterpfaden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-685">End the current set of subpaths.</span></span> <span data-ttu-id="9b5f6-686">Eine bestimmte Gruppe von Unterpfaden (durch Ende getrennt) wird mit eofill aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="9b5f6-687">Nachfolgende Gruppen von Unterpfaden werden unabhängig aufgefüllt und vorhandenen überlagert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-688">l (lineto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-688">l (lineto)</span></span></td>
<td><span data-ttu-id="9b5f6-689">x,y</span><span class="sxs-lookup"><span data-stu-id="9b5f6-689">x,y</span></span><br/> <span data-ttu-id="9b5f6-690">Zeichnen Sie eine Linie vom aktuellen Punkt zur angegebenen x,y-Koordinate, die zum neuen aktuellen Punkt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="9b5f6-691">Es können zusätzliche Koordinatenpaare angegeben werden, um eine Polylinie zu bilden, z.B. &quot; l 10,13,45,27,89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-692">m (moveto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-692">m (moveto)</span></span></td>
<td><span data-ttu-id="9b5f6-693">x,y</span><span class="sxs-lookup"><span data-stu-id="9b5f6-693">x,y</span></span><br/> <span data-ttu-id="9b5f6-694">Starten Sie einen neuen Unterpfad an der angegebenen x,y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-695">nf (nofill)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="9b5f6-696">Der aktuelle Satz von Unterpfaden (durch Ende getrennt) wird nicht ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-697">ns (nostroke)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="9b5f6-698">Der aktuelle Satz von Unterpfaden (durch Ende getrennt) wird nicht strichen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-699">qb (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="9b5f6-700">(<strong>Kontrollpunkt</strong>(x, y))\*,<strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9b5f6-701">Definiert eine oder mehrere quadratische Bézierkurven mit Kontrollpunkten und einem Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="9b5f6-702">Zwischenpunkte (on-curve) werden durch Interpolation zwischen aufeinander folgenden Kontrollpunkten ermittelt, ähnlich wie TrueType-Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="9b5f6-703">Der Unterpfad muss kein Start sein. In diesem Fall wird der Unterpfad geschlossen, und der letzte Punkt definiert den Startpunkt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-704">qx (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="9b5f6-705"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9b5f6-706">Eine Quartalsellipse wird vom aktuellen Punkt zum angegebenen Endpunkt gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="9b5f6-707">Das elliptische Segment ist anfänglich tangential zu einer Linie parallel zur X-Achse. Das segment beginnt also horizontal.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-708">qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="9b5f6-709"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="9b5f6-710">Identisch mit qx, außer dass das elliptische Segment anfänglich tangential zu einer Linie parallel zur y-Achse ist; Das segment beginnt also vertikal.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-711">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="9b5f6-712">x,y</span><span class="sxs-lookup"><span data-stu-id="9b5f6-712">x,y</span></span> <br/> <span data-ttu-id="9b5f6-713">Zeichnen Sie eine Linie vom aktuellen Punkt zur relativen Koordinate (cpx + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="9b5f6-714">Wenn zusätzliche Koordinatenpaare angegeben werden, wird jeder neue Punkt relativ zum letzten berechnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-715">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="9b5f6-716">x,y</span><span class="sxs-lookup"><span data-stu-id="9b5f6-716">x,y</span></span><br/> <span data-ttu-id="9b5f6-717">Starten Sie einen neuen Unterpfad an den relativen Koordinaten ( cpx + x, cpy + y), wobei cpx, cpy die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-718">v (curveto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-718">v (curveto)</span></span></td>
<td><span data-ttu-id="9b5f6-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>bis</strong> (x,y)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="9b5f6-720">Kubische Bézierkurve unter Verwendung der angegebenen Koordinaten relativ zum aktuellen Punkt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="9b5f6-721">Alle Punkte werden relativ zum gleichen Ausgangspunkt berechnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-722">wa (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="9b5f6-723">Identisch mit at, aber der Bogen wird im Uhrzeigersinn gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-724">wr (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="9b5f6-725">Identisch mit ar, wird aber im Uhrzeigersinn gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-726">x (schließen)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-726">x (close)</span></span></td>
<td><span data-ttu-id="9b5f6-727">Schließen Sie den aktuellen Unterpfad, indem Sie eine gerade Linie vom aktuellen Punkt zum ursprünglichen Moveto-Punkt zeichnen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="9b5f6-728">Shadow-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-728">Shadow element</span></span>

<span data-ttu-id="9b5f6-729">Beschreibt einen Schatteneffekt auf einer Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-730">Color</span><span class="sxs-lookup"><span data-stu-id="9b5f6-730">Color</span></span></td>
<td><span data-ttu-id="9b5f6-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9b5f6-732">Farbe des primären Schattens.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-732">Color of the primary shadow.</span></span> <span data-ttu-id="9b5f6-733">Der Standardwert ist RGB(128,128,128).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-734">Color2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-734">Color2</span></span></td>
<td><span data-ttu-id="9b5f6-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9b5f6-736">Farbe des zweiten Schattens oder Hervorhebung in einem eingebettten oder gestaunten Schatten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="9b5f6-737">Der Standardwert ist RGB(203,203,203).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-738">Matrix</span><span class="sxs-lookup"><span data-stu-id="9b5f6-738">Matrix</span></span></td>
<td><span data-ttu-id="9b5f6-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="9b5f6-740">Eine Perspektivtransformationsmatrix im Format &quot; sxx,sxy,syx,syy,px,py &quot; [s=scale, p=perspective].</span><span class="sxs-lookup"><span data-stu-id="9b5f6-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="9b5f6-741">Die -Elemente geben an, wie der Schatten in Bezug auf die Form skaliert werden soll, und die p-Elemente geben an, wie der Schatten in Bezug auf die Form verzerrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="9b5f6-742">Mit der folgenden Matrix wird die Größe der Form z. B. um den Faktor 2 geändert und in alle Richtungen um den Faktor 4 verzerrt:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="9b5f6-743">&quot;2,2,2,2,4,4&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="9b5f6-744">Diese Matrix wird nur verwendet, wenn der Typ des Schattens auf Perspektive festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-745">Verdeckt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-745">Obscured</span></span></td>
<td><span data-ttu-id="9b5f6-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-747">Der Schatten kann durch gesehen werden, wenn es keine Füllung auf der Form gibt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="9b5f6-748">Der Standardwert lautet False.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-749">Offset</span><span class="sxs-lookup"><span data-stu-id="9b5f6-749">Offset</span></span></td>
<td><span data-ttu-id="9b5f6-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="9b5f6-751">Die Menge des x,y-Offsets von der Position der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="9b5f6-752">Der Standardwert ist &quot; 2pt,2pt. &quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-753">Offset2</span></span></td>
<td><span data-ttu-id="9b5f6-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-755">Betrag des x,y-Sekundenoffsets von der Position der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="9b5f6-756">Werte sind entweder eine absolute Messung oder ein Bruchwert der Form (-0,5 bis +0,5).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-757">Ein</span><span class="sxs-lookup"><span data-stu-id="9b5f6-757">On</span></span></td>
<td><span data-ttu-id="9b5f6-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-759">Schaltet die Anzeige des Schattens ein und aus.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-760">Opacity</span><span class="sxs-lookup"><span data-stu-id="9b5f6-760">Opacity</span></span></td>
<td><span data-ttu-id="9b5f6-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9b5f6-762">Deckkraft des Schatteneffekts.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-763">Origin</span><span class="sxs-lookup"><span data-stu-id="9b5f6-763">Origin</span></span></td>
<td><span data-ttu-id="9b5f6-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Ein Paar von Bruchwerten der Form von -0,5 bis +0,5.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-765">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-765">Type</span></span></td>
<td><span data-ttu-id="9b5f6-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="9b5f6-767">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-768">Single (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-768">Single (default)</span></span></li>
<li><span data-ttu-id="9b5f6-769">Double</span><span class="sxs-lookup"><span data-stu-id="9b5f6-769">Double</span></span></li>
<li><span data-ttu-id="9b5f6-770">Perspektive</span><span class="sxs-lookup"><span data-stu-id="9b5f6-770">Perspective</span></span></li>
<li><span data-ttu-id="9b5f6-771">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="9b5f6-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="9b5f6-772">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="9b5f6-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="9b5f6-773">Emboss</span><span class="sxs-lookup"><span data-stu-id="9b5f6-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="9b5f6-774">Skew-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-774">Skew element</span></span>

<span data-ttu-id="9b5f6-775">Beschreibt einen Perspektivische Schiefe-Effekt auf eine Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="9b5f6-776">Die Schiefe wird auf Vektorgrafikdaten angewendet, nicht auf Bilddaten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="9b5f6-777">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-777">Attribute</span></span>        |   <span data-ttu-id="9b5f6-778">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-779">Matrix</span><span class="sxs-lookup"><span data-stu-id="9b5f6-779">Matrix</span></span> | <span data-ttu-id="9b5f6-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-781">Eine Perspektivtransformationsmatrix im Format "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective \] .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="9b5f6-782">Wenn offset in absoluten Einheiten liegt, befinden sich px,py in emu ^ -1 Einheiten; andernfalls sind sie ein umgekehrter Bruchteil der Formgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="9b5f6-783">Offset</span><span class="sxs-lookup"><span data-stu-id="9b5f6-783">Offset</span></span> | <span data-ttu-id="9b5f6-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-785">Die Menge des x,y-Offsets von der Position der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="9b5f6-786">Der Standardwert ist "2pt,2pt".</span><span class="sxs-lookup"><span data-stu-id="9b5f6-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="9b5f6-787">Ein</span><span class="sxs-lookup"><span data-stu-id="9b5f6-787">On</span></span>     | <span data-ttu-id="9b5f6-788">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-789">Schaltet die Anzeige der Schiefe ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="9b5f6-790">Origin</span><span class="sxs-lookup"><span data-stu-id="9b5f6-790">Origin</span></span> | <span data-ttu-id="9b5f6-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-792">Ein Paar von Bruchwerten der Form von -0,5 bis +0,5.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="9b5f6-793">Stroke-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-793">Stroke element</span></span>

<span data-ttu-id="9b5f6-794">Beschreibt, wie der Pfad ge zeichnen wird, wenn etwas über eine durchfarbige Linie hinaus mit einer Volltonfarbe gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-795">Color</span><span class="sxs-lookup"><span data-stu-id="9b5f6-795">Color</span></span></td>
<td><span data-ttu-id="9b5f6-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-797">Die Farbe der Linie.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-797">The color of the line.</span></span> <span data-ttu-id="9b5f6-798">Identisch mit dem StrokeColor-Attribut in Shape, überschreibt es jedoch.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-799">Color2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-799">Color2</span></span></td>
<td><span data-ttu-id="9b5f6-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="9b5f6-801">Sekundäre Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-801">Secondary color.</span></span> <span data-ttu-id="9b5f6-802">Wird verwendet, wenn FillType auf Pattern festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-803">Dashstyle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-803">DashStyle</span></span></td>
<td><span data-ttu-id="9b5f6-804"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="9b5f6-805">Dash-Format.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-805">Dash style format.</span></span> <span data-ttu-id="9b5f6-806">Kann ein bestimmter Wert oder eine Sequenz von Zahlen mit einem benutzerdefinierten Bindestrichmuster sein.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="9b5f6-807">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-808">Solid (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-808">Solid (default)</span></span></li>
<li><span data-ttu-id="9b5f6-809">ShortDash</span><span class="sxs-lookup"><span data-stu-id="9b5f6-809">ShortDash</span></span></li>
<li><span data-ttu-id="9b5f6-810">ShortDot</span><span class="sxs-lookup"><span data-stu-id="9b5f6-810">ShortDot</span></span></li>
<li><span data-ttu-id="9b5f6-811">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="9b5f6-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="9b5f6-812">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="9b5f6-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="9b5f6-813">Punkt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-813">Dot</span></span></li>
<li><span data-ttu-id="9b5f6-814">Strich</span><span class="sxs-lookup"><span data-stu-id="9b5f6-814">Dash</span></span></li>
<li><span data-ttu-id="9b5f6-815">DashDot</span><span class="sxs-lookup"><span data-stu-id="9b5f6-815">DashDot</span></span></li>
<li><span data-ttu-id="9b5f6-816">LongDash</span><span class="sxs-lookup"><span data-stu-id="9b5f6-816">LongDash</span></span></li>
<li><span data-ttu-id="9b5f6-817">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="9b5f6-817">LongDashDot</span></span></li>
<li><span data-ttu-id="9b5f6-818">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="9b5f6-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-819">EndArrow</span><span class="sxs-lookup"><span data-stu-id="9b5f6-819">EndArrow</span></span></td>
<td><span data-ttu-id="9b5f6-820"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="9b5f6-821">Pfeilspitze für das Ende der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="9b5f6-822">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-823">Keine (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-823">None (default)</span></span></li>
<li><span data-ttu-id="9b5f6-824">Blockieren</span><span class="sxs-lookup"><span data-stu-id="9b5f6-824">Block</span></span></li>
<li><span data-ttu-id="9b5f6-825">Klassisch</span><span class="sxs-lookup"><span data-stu-id="9b5f6-825">Classic</span></span></li>
<li><span data-ttu-id="9b5f6-826">Diamond</span><span class="sxs-lookup"><span data-stu-id="9b5f6-826">Diamond</span></span></li>
<li><span data-ttu-id="9b5f6-827">Oval</span><span class="sxs-lookup"><span data-stu-id="9b5f6-827">Oval</span></span></li>
<li><span data-ttu-id="9b5f6-828">Öffnen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-828">Open</span></span></li>
<li><span data-ttu-id="9b5f6-829">Chevron</span><span class="sxs-lookup"><span data-stu-id="9b5f6-829">Chevron</span></span></li>
<li><span data-ttu-id="9b5f6-830">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="9b5f6-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-831">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="9b5f6-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="9b5f6-832"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="9b5f6-833">Pfeilspitzenlänge für das Ende der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="9b5f6-834">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-835">Short</span><span class="sxs-lookup"><span data-stu-id="9b5f6-835">Short</span></span></li>
<li><span data-ttu-id="9b5f6-836">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-836">Medium (default)</span></span></li>
<li><span data-ttu-id="9b5f6-837">Long</span><span class="sxs-lookup"><span data-stu-id="9b5f6-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-838">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="9b5f6-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="9b5f6-839"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="9b5f6-840">Die Pfeilspitzenbreite für das Ende der Linie.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="9b5f6-841">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-842">Schmalen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-842">Narrow</span></span></li>
<li><span data-ttu-id="9b5f6-843">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-843">Medium (default)</span></span></li>
<li><span data-ttu-id="9b5f6-844">Breite</span><span class="sxs-lookup"><span data-stu-id="9b5f6-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-845">Endcap</span><span class="sxs-lookup"><span data-stu-id="9b5f6-845">EndCap</span></span></td>
<td><span data-ttu-id="9b5f6-846"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="9b5f6-847">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-848">Flach</span><span class="sxs-lookup"><span data-stu-id="9b5f6-848">Flat</span></span></li>
<li><span data-ttu-id="9b5f6-849">Square</span><span class="sxs-lookup"><span data-stu-id="9b5f6-849">Square</span></span></li>
<li><span data-ttu-id="9b5f6-850">Round</span><span class="sxs-lookup"><span data-stu-id="9b5f6-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-851">FillType</span><span class="sxs-lookup"><span data-stu-id="9b5f6-851">FillType</span></span></td>
<td><span data-ttu-id="9b5f6-852"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="9b5f6-853">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-854">Solid (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-854">Solid (default)</span></span></li>
<li><span data-ttu-id="9b5f6-855">Tile</span><span class="sxs-lookup"><span data-stu-id="9b5f6-855">Tile</span></span></li>
<li><span data-ttu-id="9b5f6-856">Muster</span><span class="sxs-lookup"><span data-stu-id="9b5f6-856">Pattern</span></span></li>
<li><span data-ttu-id="9b5f6-857">Frame</span><span class="sxs-lookup"><span data-stu-id="9b5f6-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-858">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="9b5f6-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="9b5f6-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-860">Richten Sie das Bild an der Form aus.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-860">Align the image with the shape.</span></span> <span data-ttu-id="9b5f6-861">False gibt an, dass das Bild mit dem Fenster ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-862">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="9b5f6-862">ImageAspect</span></span></td>
<td><span data-ttu-id="9b5f6-863"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="9b5f6-864">Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="9b5f6-865">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-866">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-866">Value</span></span></th>
<th><span data-ttu-id="9b5f6-867">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-868">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9b5f6-868">Ignore</span></span></td>
<td><span data-ttu-id="9b5f6-869">Ignorieren von Aspektproblemen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-870">Atleast</span><span class="sxs-lookup"><span data-stu-id="9b5f6-870">AtLeast</span></span></td>
<td><span data-ttu-id="9b5f6-871">Das Bild ist mindestens so groß wie die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-872">AtMost</span><span class="sxs-lookup"><span data-stu-id="9b5f6-872">AtMost</span></span></td>
<td><span data-ttu-id="9b5f6-873">Das Bild ist nicht größer als die Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-874">Imagesize</span><span class="sxs-lookup"><span data-stu-id="9b5f6-874">ImageSize</span></span></td>
<td><span data-ttu-id="9b5f6-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="9b5f6-876">Größe des Bilds, mit dem der Pinsel bildet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="9b5f6-877">Der Standardwert ist die Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-878">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-878">JoinStyle</span></span></td>
<td><span data-ttu-id="9b5f6-879"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="9b5f6-880">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-881">Rundes (abgerundetes Gemeinsames)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="9b5f6-882">Abschrägen (abschrägtes Fugen)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="9b5f6-883">Miter (Miter-Fugen)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-884">Linestyle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-884">LineStyle</span></span></td>
<td><span data-ttu-id="9b5f6-885"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="9b5f6-886">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-887">Single</span><span class="sxs-lookup"><span data-stu-id="9b5f6-887">Single</span></span></li>
<li><span data-ttu-id="9b5f6-888">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="9b5f6-889">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="9b5f6-890">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="9b5f6-891">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-892">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="9b5f6-892">MiterLimit</span></span></td>
<td><span data-ttu-id="9b5f6-893"><a href="msdn-online-vml-vglength.md">Länge.</a></span><span class="sxs-lookup"><span data-stu-id="9b5f6-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="9b5f6-894">Der maximale Abstand zwischen dem inneren und äußeren Punkt eines Fugens.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="9b5f6-895">Diese Zahl ist ein Vielfaches der Linienstärke.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="9b5f6-896">Liegt zwischen 0 und 32.767.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-897">Ein</span><span class="sxs-lookup"><span data-stu-id="9b5f6-897">On</span></span></td>
<td><span data-ttu-id="9b5f6-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="9b5f6-899">Schaltet die Anzeige der Zeile ein und aus.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="9b5f6-900">Identisch mit dem Stroke-Attribut in Shape, überschreibt es jedoch.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-901">Opacity</span><span class="sxs-lookup"><span data-stu-id="9b5f6-901">Opacity</span></span></td>
<td><span data-ttu-id="9b5f6-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="9b5f6-903">Deckkraft des Strichs.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-904">Src</span><span class="sxs-lookup"><span data-stu-id="9b5f6-904">Src</span></span></td>
<td><span data-ttu-id="9b5f6-905">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-905">String.</span></span> <span data-ttu-id="9b5f6-906">URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="9b5f6-907">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten verweisen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-908">StartArrow</span><span class="sxs-lookup"><span data-stu-id="9b5f6-908">StartArrow</span></span></td>
<td><span data-ttu-id="9b5f6-909"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="9b5f6-910">Pfeilspitze für den Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="9b5f6-911">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-912">Keine (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-912">None (default)</span></span></li>
<li><span data-ttu-id="9b5f6-913">Blockieren</span><span class="sxs-lookup"><span data-stu-id="9b5f6-913">Block</span></span></li>
<li><span data-ttu-id="9b5f6-914">Klassisch</span><span class="sxs-lookup"><span data-stu-id="9b5f6-914">Classic</span></span></li>
<li><span data-ttu-id="9b5f6-915">Diamond</span><span class="sxs-lookup"><span data-stu-id="9b5f6-915">Diamond</span></span></li>
<li><span data-ttu-id="9b5f6-916">Oval</span><span class="sxs-lookup"><span data-stu-id="9b5f6-916">Oval</span></span></li>
<li><span data-ttu-id="9b5f6-917">Öffnen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-917">Open</span></span></li>
<li><span data-ttu-id="9b5f6-918">Chevron</span><span class="sxs-lookup"><span data-stu-id="9b5f6-918">Chevron</span></span></li>
<li><span data-ttu-id="9b5f6-919">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="9b5f6-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-920">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="9b5f6-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="9b5f6-921">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-921">VgArrowHeadLength.</span></span> <span data-ttu-id="9b5f6-922">Pfeilkopflänge für den Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="9b5f6-923">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-924">Short</span><span class="sxs-lookup"><span data-stu-id="9b5f6-924">Short</span></span></li>
<li><span data-ttu-id="9b5f6-925">Mittel (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-925">Medium (default)</span></span></li>
<li><span data-ttu-id="9b5f6-926">Long</span><span class="sxs-lookup"><span data-stu-id="9b5f6-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-927">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="9b5f6-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="9b5f6-928">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-928">VgArrowheadWidth.</span></span> <span data-ttu-id="9b5f6-929">Pfeilkopfbreite für den Anfang der Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="9b5f6-930">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-931">Narrow Medium (Standard) Wide</span><span class="sxs-lookup"><span data-stu-id="9b5f6-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-932">Weight</span><span class="sxs-lookup"><span data-stu-id="9b5f6-932">Weight</span></span></td>
<td><span data-ttu-id="9b5f6-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="9b5f6-934">Breite der Linie.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-934">Width of line.</span></span> <span data-ttu-id="9b5f6-935">Liegt zwischen 0 und 1584.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="9b5f6-936">Mit dem DashStyle-Attribut kann der Benutzer ein benutzerdefiniertes Bindestrichmuster angeben.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="9b5f6-937">Dies erfolgt mithilfe einer Reihe von Zahlen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-937">This is done using a series of numbers.</span></span> <span data-ttu-id="9b5f6-938">Bindestrichstile werden in Bezug auf die Länge des Bindestrichs (den gezeichneten Teil des Strichs) und die Länge des Abstands zwischen den Bindestrichen definiert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="9b5f6-939">Die Längen sind relativ zur Linienbreite. eine Länge von &quot; 1 &quot; entspricht der Linienbreite.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="9b5f6-940">Der EndCap-Stil wird auf jeden Bindestrich angewendet, Pfeilstile nicht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="9b5f6-941">Die Zeichenfolge definiert zuerst die Länge des Bindestrichs und dann die Länge des Leerzeichens.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="9b5f6-942">Dies kann wiederholt werden, um komplexe Bindestriche zu bilden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="9b5f6-943">Die Zeichenfolge sollte immer ein Zahlenpaar enthalten. Wenn sie eine ungerade Anzahl von Zahlen enthält, kann die letzte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="9b5f6-944">In der folgenden Tabelle sind einige typische Werte und eine Beschreibung des beabsichtigten Effekts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="9b5f6-945">&quot;0 impliziert einen Punkt, der &quot; vierfach symmetrisch sein sollte (mit runden Endcaps sollte es ein Kreis sein).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="9b5f6-946">Wenn das Zeilenendecap flach ist, sollte ein Viewer nach Möglichkeit einen integrierten Betriebssystemdstrich auswählen (d. h. etwas, das schnell gezeichnet werden kann).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="9b5f6-947">Im Folgenden sind einige Beispiele aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-949">kurze Bindestriche (jeder Bindestrich und der Abstand dazwischen ist doppelt so breit wie die Linie)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-951">punkt (jeder Bindestrich ist die Breite der Linie, während jedes Leerzeichen doppelt so breit wie die Linie ist)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-953">Bindestrich (jeder Bindestrich ist viermal so breit wie die Linie, während jedes Leerzeichen doppelt so breit wie die Linie ist)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-955">Long-Bindestrich</span><span class="sxs-lookup"><span data-stu-id="9b5f6-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-957">Bindestrich</span><span class="sxs-lookup"><span data-stu-id="9b5f6-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-959">Long-Bindestrich-Punkt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="9b5f6-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="9b5f6-961">Punktpunkt mit langem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="9b5f6-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="9b5f6-962">TextPath-Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-962">TextPath element</span></span>

<span data-ttu-id="9b5f6-963">Beschreibt einen Vektorpfad, der auf den bereitgestellten Textdaten, Schriftarten und Formatvorlagen basiert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="9b5f6-964">Der Textpfad wird so verwarnt, dass er einem **Path-Element** entspricht, sofern angegeben.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="9b5f6-965">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-965">Attribute</span></span>        |   <span data-ttu-id="9b5f6-966">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-967">FitPath</span><span class="sxs-lookup"><span data-stu-id="9b5f6-967">FitPath</span></span>  | <span data-ttu-id="9b5f6-968">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-969">Größe des Texts zum Ausfüllen des Pfads, auf dem er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="9b5f6-970">FitShape</span><span class="sxs-lookup"><span data-stu-id="9b5f6-970">FitShape</span></span> | <span data-ttu-id="9b5f6-971">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-972">Streckt den Textpfad an die Ränder des Formfelds.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="9b5f6-973">Ein</span><span class="sxs-lookup"><span data-stu-id="9b5f6-973">On</span></span>       | <span data-ttu-id="9b5f6-974">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-975">Bestimmt, ob die Zeichenpfade angezeigt werden oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="9b5f6-976">String</span><span class="sxs-lookup"><span data-stu-id="9b5f6-976">String</span></span>   | <span data-ttu-id="9b5f6-977">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-977">String.</span></span> <span data-ttu-id="9b5f6-978">Der Text, der als Textpfad gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="9b5f6-979">Glätten</span><span class="sxs-lookup"><span data-stu-id="9b5f6-979">Trim</span></span>     | <span data-ttu-id="9b5f6-980">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-981">Entfernt zusätzlichen Speicherplatz, der für Aufsteige und Nachfolger reserviert ist, wenn er nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="9b5f6-982">Xscale</span><span class="sxs-lookup"><span data-stu-id="9b5f6-982">XScale</span></span>   | <span data-ttu-id="9b5f6-983">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-984">Verwenden Sie eine gerade x-Messung, anstatt entlang des Pfads zu messen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="9b5f6-985">Im VML-Objektmodell verwendete Datentypen</span><span class="sxs-lookup"><span data-stu-id="9b5f6-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="9b5f6-986">Die folgenden Datentypen werden vom VML-Objektmodell verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="9b5f6-987">Double</span><span class="sxs-lookup"><span data-stu-id="9b5f6-987">Double</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-988">Fest</span><span class="sxs-lookup"><span data-stu-id="9b5f6-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-989">Integer</span><span class="sxs-lookup"><span data-stu-id="9b5f6-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-990">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="9b5f6-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-991">IVgColor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-992">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="9b5f6-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-993">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-994">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="9b5f6-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-995">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="9b5f6-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-996">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="9b5f6-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-997">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="9b5f6-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-998">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="9b5f6-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-999">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="9b5f6-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1000">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1003">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1003">Length</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1004">Measure</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1004">Measure</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1005">String</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1005">String</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1006">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1007">VgFraction</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="9b5f6-1008">VgTriState</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="9b5f6-1009">**Double-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1009">**Double data type**</span></span>

<span data-ttu-id="9b5f6-1010">Eine ganze Zahl mit doppelter Genauigkeit mit einem Bereich von -infinity bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="9b5f6-1011">**Fester Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1011">**Fixed data type**</span></span>

<span data-ttu-id="9b5f6-1012">Gleitkommazahl mit einem Bereich von -32.766,0 bis 32.766.0.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="9b5f6-1013">**Ganzzahliger Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1013">**Integer data type**</span></span>

<span data-ttu-id="9b5f6-1014">Eine ganze Zahl mit einem Bereich von -infinity bis infinity.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="9b5f6-1015">**IVgAdjustments-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="9b5f6-1016">Auflistung von Anpassungen an einer Form, die zum Ändern der Abmessungen einer Form verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="9b5f6-1017">Anpassungen können als temporäre Platzhalter oder aus einem beliebigen Grund verwendet werden, aus dem Sie Variablen verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="9b5f6-1018">Die Sammlung umfasst nur acht Anpassungen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="9b5f6-1019">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1019">Attribute</span></span> | <span data-ttu-id="9b5f6-1020">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1021">Exists</span></span>     | <span data-ttu-id="9b5f6-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="9b5f6-1023">Bestimmt, ob eine angegebene Anpassung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="9b5f6-1024">Beachten Sie, dass ein Index verwendet werden muss. das heißt, exists( item ) muss verwendet werden, um das Vorhandensein eines Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="9b5f6-1025">Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1025">Item</span></span>       | <span data-ttu-id="9b5f6-1026">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1027">Array von Anpassungen, die von 0 bis 7 indiziert sind.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="9b5f6-1028">Beachten Sie, dass Anpassungen möglicherweise nur spärlich angegeben werden. Das heißt, zwischengeschaltete Arraywerte werden möglicherweise nicht immer aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="9b5f6-1029">Beispielsweise könnten Element 1, 3 und 5 Werte für eine Länge von 3 enthalten, bei der item(0), item(2) und item(4) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="9b5f6-1030">Verwenden Sie das Exists-Attribut, um zu sehen, ob ein Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="9b5f6-1031">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1031">Length</span></span>     | <span data-ttu-id="9b5f6-1032">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1033">Anzahl der Anpassungen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1033">Number of adjustments.</span></span> <span data-ttu-id="9b5f6-1034">Darf nicht größer als 8 sein.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9b5f6-1035">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1035">Value</span></span>      | <span data-ttu-id="9b5f6-1036">[Zeichenfolge.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1037">Textdarstellung numerischer Werte mit Kommas zwischen den einzelnen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="9b5f6-1038">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1038">**IVgColor**</span></span>

<span data-ttu-id="9b5f6-1039">Gibt eine Farbe an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-1040">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1040">Attributes</span></span></th>
<th><span data-ttu-id="9b5f6-1041">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1042">RGB</span></span></td>
<td><span data-ttu-id="9b5f6-1043"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="9b5f6-1044">RGB-Wert (Long) der Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="9b5f6-1045">Nur gültig, wenn Type den Wert RGB hat.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1046">R</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1046">R</span></span></td>
<td><span data-ttu-id="9b5f6-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9b5f6-1048">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1048">Red component of the color.</span></span> <span data-ttu-id="9b5f6-1049">Kann zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1050">G</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1050">G</span></span></td>
<td><span data-ttu-id="9b5f6-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9b5f6-1052">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1052">Green component of the color.</span></span> <span data-ttu-id="9b5f6-1053">Kann zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1054">B</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1054">B</span></span></td>
<td><span data-ttu-id="9b5f6-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="9b5f6-1056">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1056">Blue component of the color.</span></span> <span data-ttu-id="9b5f6-1057">Kann zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1058">String</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1058">String</span></span></td>
<td><span data-ttu-id="9b5f6-1059"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge.</a></span><span class="sxs-lookup"><span data-stu-id="9b5f6-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9b5f6-1060">Textdarstellung der Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1060">Text representation of the color.</span></span> <span data-ttu-id="9b5f6-1061">Die folgenden benannten Farbtypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-1062">Schwarz (#000000)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="9b5f6-1063">Silber (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="9b5f6-1064">Grau (#808080)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="9b5f6-1065">Weiß (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="9b5f6-1066">Maroon (#800000)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="9b5f6-1067">Rot (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="9b5f6-1068">Violett (#800080)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="9b5f6-1069">Ia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="9b5f6-1070">Grün (#008000)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="9b5f6-1071">Lime (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="9b5f6-1072">Oliv (#808000)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="9b5f6-1073">Gelb (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="9b5f6-1074">Gegen (#000080)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="9b5f6-1075">Blau (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="9b5f6-1076">Teal (#008080)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="9b5f6-1077">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1078">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1078">Type</span></span></td>
<td><span data-ttu-id="9b5f6-1079"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="9b5f6-1080">Typ der Farbe.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1080">Type of color.</span></span> <span data-ttu-id="9b5f6-1081">Einer der folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-1082">Mixed</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1082">Mixed</span></span></li>
<li><span data-ttu-id="9b5f6-1083">benannt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1083">Named</span></span></li>
<li><span data-ttu-id="9b5f6-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1084">RGB</span></span></li>
<li><span data-ttu-id="9b5f6-1085">Schema</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b5f6-1086">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1086">**IVgEquation**</span></span>

<span data-ttu-id="9b5f6-1087">Für Formeln verwendete Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1088">Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1088">Operation</span></span></td>
<td><span data-ttu-id="9b5f6-1089"><strong>VgEquationOperationType</strong> Name des Vorgangs, der für die Parameter durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="9b5f6-1090">Die folgenden Vorgänge können in einer Gleichung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-1091">Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1091">Operation</span></span></th>
<th><span data-ttu-id="9b5f6-1092">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1093">Abs</span></span></td>
<td><span data-ttu-id="9b5f6-1094">Absoluter Wert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1094">Absolute value.</span></span> <br/> <span data-ttu-id="9b5f6-1095"><strong>abs</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1096">Atan2</span></span></td>
<td><span data-ttu-id="9b5f6-1097">Polararithmetische Ergebnisse in fd-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="9b5f6-1098"><strong>atan2</strong>(p1,v)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1099">Cos</span></span></td>
<td><span data-ttu-id="9b5f6-1100">Kosinus, Argument in FD-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="9b5f6-1101">v \* <strong>cos</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="9b5f6-1103">Behält die vollständige Genauigkeit bei der Zwischenberechnung bei.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="9b5f6-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="9b5f6-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1105">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1105">Ellipse</span></span></td>
<td><span data-ttu-id="9b5f6-1106">Ellipse</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1107">Wenn</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1107">If</span></span></td>
<td><span data-ttu-id="9b5f6-1108">Wenn Bedingungstest.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1108">If Condition test.</span></span> <span data-ttu-id="9b5f6-1109">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="9b5f6-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="9b5f6-1110">p1 : p2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1111">Max</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1111">Max</span></span></td>
<td><span data-ttu-id="9b5f6-1112">Der größere von zwei Werten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="9b5f6-1113"><strong>max</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1114">Mid</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1114">Mid</span></span></td>
<td><span data-ttu-id="9b5f6-1115">Durchschnitt ( v + p1)/2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1116">Min</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1116">Min</span></span></td>
<td><span data-ttu-id="9b5f6-1117">Der kleinere von zwei Werten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1117">The lesser of two values.</span></span> <span data-ttu-id="9b5f6-1118"><strong>min</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1119">Mod</span></span></td>
<td><span data-ttu-id="9b5f6-1120">Modulo</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1121">Produkt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1121">Product</span></span></td>
<td><span data-ttu-id="9b5f6-1122">Wird für Multiplikation und Division verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1122">Used for multiplication and division.</span></span> <span data-ttu-id="9b5f6-1123">v \* p1 /p2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1124">Sin</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1124">Sin</span></span></td>
<td><span data-ttu-id="9b5f6-1125">Sinus, Argument in fd-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="9b5f6-1126">v \* <strong>sin</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="9b5f6-1128">Behält die vollständige Genauigkeit bei der Zwischenberechnung bei.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="9b5f6-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1130">Sqrt</span></span></td>
<td><span data-ttu-id="9b5f6-1131">Das Ergebnis ist positiv und rundet ab.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="9b5f6-1132"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1133">Sum</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1133">Sum</span></span></td>
<td><span data-ttu-id="9b5f6-1134">Wird für Addition und Subtraktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="9b5f6-1135">v + p1 p2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1136">Sumangle</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1136">Sumangle</span></span></td>
<td><span data-ttu-id="9b5f6-1137">Vorhandener Winkel (skaliert um 65536), wobei p1 und p2 in Grad liegen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="9b5f6-1138">v + p1 \* 65536 + p2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1139">Tan</span></span></td>
<td><span data-ttu-id="9b5f6-1140">Tangens, Argument ist in fd-Einheiten (Grad multipliziert mit 65536).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="9b5f6-1141">v \* tan( p1 )</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1142">Val</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1142">Val</span></span></td>
<td><span data-ttu-id="9b5f6-1143">Definiert einen Leitfadenwert aus einem anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1144">Param1</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1144">Param1</span></span></td>
<td><span data-ttu-id="9b5f6-1145"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="9b5f6-1146">Der erste Parameter.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="9b5f6-1148"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="9b5f6-1149">Der Typ des ersten Parameters.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1149">The type of the first parameter.</span></span> <span data-ttu-id="9b5f6-1150">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-1151">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1151">Type</span></span></th>
<th><span data-ttu-id="9b5f6-1152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1153">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1153">Value</span></span></td>
<td><span data-ttu-id="9b5f6-1154">Parameter ist ein einfacher Wert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1155">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="9b5f6-1156">Parameter ist ein Verweis auf eine Anpassung.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="9b5f6-1157">Wenn der erste Parameter beispielsweise 1 ist, wird der Wert der ersten Anpassung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1158">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="9b5f6-1159">Parameter ist das Ergebnis eines Verweises auf das Ergebnis einer vorherigen Formel.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="9b5f6-1160">Wenn der erste Parameter beispielsweise 2 ist, wird das Ergebnis der Formel 2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1161">Param2</span></span></td>
<td><span data-ttu-id="9b5f6-1162"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="9b5f6-1163">Der zweite Parameter.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="9b5f6-1165"><strong>VgFormulaParamType</strong> Der Typ des Parameters 2.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1166">Val</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1166">Val</span></span></td>
<td><span data-ttu-id="9b5f6-1167"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="9b5f6-1168">Das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1169">Valtype2</span></span></td>
<td><span data-ttu-id="9b5f6-1170"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="9b5f6-1171">Der Typ des Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b5f6-1172">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="9b5f6-1173">Gibt ein festes Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="9b5f6-1174">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1174">Attribute</span></span> | <span data-ttu-id="9b5f6-1175">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1176">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1176">Value</span></span>      | <span data-ttu-id="9b5f6-1177">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1178">Textwert, der den Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="9b5f6-1179">Left</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1179">Left</span></span>       | <span data-ttu-id="9b5f6-1180">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1181">Die äußerste linke Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="9b5f6-1182">Oben</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1182">Top</span></span>        | <span data-ttu-id="9b5f6-1183">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1184">Oberste Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="9b5f6-1185">Right</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1185">Right</span></span>      | <span data-ttu-id="9b5f6-1186">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1187">Die äußerste rechte Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="9b5f6-1188">Unten</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1188">Bottom</span></span>     | <span data-ttu-id="9b5f6-1189">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1190">Die unterste Koordinate des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="9b5f6-1191">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="9b5f6-1192">Array fester Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="9b5f6-1193">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1193">Attribute</span></span> | <span data-ttu-id="9b5f6-1194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1195">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1195">Value</span></span>      | <span data-ttu-id="9b5f6-1196">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1197">Textdarstellung des Arrays.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="9b5f6-1198">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1198">Length</span></span>     | <span data-ttu-id="9b5f6-1199">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1200">Anzahl der Rechtecke in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="9b5f6-1201">Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1201">Item</span></span>       | <span data-ttu-id="9b5f6-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1203">Das Rechteckobjekt am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="9b5f6-1204">**IVgFormula-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="9b5f6-1205">Definitionen für Formeln, die den Pfad einer Form variieren oder für andere Berechnungszwecke verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="9b5f6-1206">Formeln können auf dem **Adj-Attribut** einer Form basieren, das sich ändern kann.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="9b5f6-1207">Formeln können auch auf andere Formeln verweisen.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="9b5f6-1208">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1208">Attribute</span></span>| <span data-ttu-id="9b5f6-1209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1210">Eqn</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1210">Eqn</span></span>        | <span data-ttu-id="9b5f6-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1212">Jede Formel definiert einen einzelnen Wert als Ergebnis der Auswertung des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="9b5f6-1213">Der Ausdruck wird von diesem Attribut definiert und weist die allgemeine Form eines Vorgangs auf, gefolgt von bis zu drei Argumenten, bei denen es sich um Anpassungswerte (z.B. \# 2), die Ergebnisse früherer Formeln (z. B. @2 ), feste Zahlen oder vordefinierte Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="9b5f6-1214">**IVgFormulas-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="9b5f6-1215">Eine Auflistung von Formelobjekten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="9b5f6-1216">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1216">Attribute</span></span> | <span data-ttu-id="9b5f6-1217">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1218">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1218">Length</span></span>     | <span data-ttu-id="9b5f6-1219">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1220">Anzahl der Formelobjekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="9b5f6-1221">Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1221">Item</span></span>       | <span data-ttu-id="9b5f6-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1223">Eine bestimmte Formel.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1223">A specific formula.</span></span> <span data-ttu-id="9b5f6-1224">Beachten Sie, dass das Formelarray möglicherweise für den Formtyp geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="9b5f6-1225">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="9b5f6-1226">Ein Array von Farben, die einen Farbverlauf definieren (gemischter Farbbereich).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="9b5f6-1227">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1227">Attribute</span></span> | <span data-ttu-id="9b5f6-1228">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1229">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1229">Value</span></span>      | <span data-ttu-id="9b5f6-1230">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1231">Gibt das Array von Farben an. Beispiel: "red .2; grüne 4; black .7"</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="9b5f6-1232">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1232">Length</span></span>     | <span data-ttu-id="9b5f6-1233">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1234">Anzahl der Farben im Array.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="9b5f6-1235">Methode</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1235">Method</span></span>     | <span data-ttu-id="9b5f6-1236">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1237">AddColor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1237">AddColor</span></span>    | <span data-ttu-id="9b5f6-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9b5f6-1239">Fügt eine neue Farbe am Endpunkt hinzu, der durch fraction angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="9b5f6-1240">Die neue Farbe ist standardmäßig weiß und der Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="9b5f6-1241">Die Farbe kann dann als Verweis geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="9b5f6-1242">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1242">RemoveColor</span></span> | <span data-ttu-id="9b5f6-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="9b5f6-1244">Entfernt eine Farbe am Endpunkt, der durch fraction angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="9b5f6-1245">Hinweis: Wenn 0.0 oder 1.0 nicht vorhanden ist, wird dies impliziert, und die Farbe Weiß wird zu diesem Zeitpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="9b5f6-1246">**IVgPoints-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="9b5f6-1247">Array von Punkten, die eine Form definieren.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="9b5f6-1248">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1248">Attribute</span></span> | <span data-ttu-id="9b5f6-1249">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5f6-1250">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1250">Value</span></span>      | <span data-ttu-id="9b5f6-1251">[Zeichenfolge](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1252">Textdarstellung des Arrays.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="9b5f6-1253">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1253">Length</span></span>     | <span data-ttu-id="9b5f6-1254">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="9b5f6-1255">Anzahl der Punkte in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="9b5f6-1256">Element</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1256">Item</span></span>       | <span data-ttu-id="9b5f6-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="9b5f6-1258">Der Punkt am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="9b5f6-1259">**IVgSkewMatrix-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="9b5f6-1260">Eine Matrix, die zum Strichen von Formen verwendet wird, eine perspektivische Transformationsmatrix im Format "*sxx,sxy,syx,syy,px,py* " \[ *s* =scale, *p* =perspective \] .</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="9b5f6-1261">Wenn offset in absoluten Einheiten ist, befinden sich *px,py* in emul ^-1 Einheiten; andernfalls sind sie ein umgekehrter Bruchteil der Formgröße.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="9b5f6-1262">attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1262">Attribute</span></span>   | <span data-ttu-id="9b5f6-1263">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="9b5f6-1264">XtoX</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1264">XtoX</span></span>         | <span data-ttu-id="9b5f6-1265">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9b5f6-1266">YtoX</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1266">YtoX</span></span>         | <span data-ttu-id="9b5f6-1267">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9b5f6-1268">XtoY</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1268">XtoY</span></span>         | <span data-ttu-id="9b5f6-1269">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9b5f6-1270">YtoY</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1270">YtoY</span></span>         | <span data-ttu-id="9b5f6-1271">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9b5f6-1272">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1272">PerspectiveX</span></span> | <span data-ttu-id="9b5f6-1273">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="9b5f6-1274">Perspektive</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1274">PerspectiveY</span></span> | <span data-ttu-id="9b5f6-1275">[Doppelt](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="9b5f6-1276">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="9b5f6-1277">Gibt den Offset der Schiefe an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-1278">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1278">Attributes</span></span></th>
<th><span data-ttu-id="9b5f6-1279">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1280">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1280">Value</span></span></td>
<td><span data-ttu-id="9b5f6-1281"><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="9b5f6-1282">Textdarstellung des Offsets.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1283">X</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1283">X</span></span></td>
<td><span data-ttu-id="9b5f6-1284"><a href="#data-types-used-in-the-vml-object-model">Doppelt</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1285">X-Komponente.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1285">X component.</span></span> <span data-ttu-id="9b5f6-1286">Prozentsatz oder Measure.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1286">Percentage or measure.</span></span> <span data-ttu-id="9b5f6-1287">Wenn keine Einheiten vorhanden sind, wird der ShapeRelative-Typ impliziert. andernfalls wird absoluter Typ impliziert.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1288">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1288">Y</span></span></td>
<td><span data-ttu-id="9b5f6-1289"><a href="#data-types-used-in-the-vml-object-model">Doppelt</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1290">Y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1291">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1291">Type</span></span></td>
<td><span data-ttu-id="9b5f6-1292"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="9b5f6-1293">Gibt den Typ der Transformation an.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="9b5f6-1294">Gültige Werte sind ganzzahlige Punkte im Bereich zwischen -infinity und infinity.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-1295">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1295">Type</span></span></th>
<th><span data-ttu-id="9b5f6-1296">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1297">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="9b5f6-1298">Die Werte des Offsets sind Prozentsätze (Verhältnis) der Größe der ursprünglichen Form. Ein Wert von 0,5 bedeutet z. B. einen Offset der Hälfte der Größe der Form.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1299">Absolut</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1299">Absolute</span></span></td>
<td><span data-ttu-id="9b5f6-1300">Die Werte sind absolute Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b5f6-1301">**IVgVector2D-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="9b5f6-1302">Gibt einen zweidimensionalen Vektor an, der aus zwei **Double-Zahlen** besteht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b5f6-1303">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1303">Attributes</span></span></th>
<th><span data-ttu-id="9b5f6-1304">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1305">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1305">Value</span></span></td>
<td><span data-ttu-id="9b5f6-1306"><strong>Zeichenfolge.</strong></span><span class="sxs-lookup"><span data-stu-id="9b5f6-1306"><strong>String</strong>.</span></span> <span data-ttu-id="9b5f6-1307">Textdarstellung beider Vektorzahlen, die durch ein Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1308">X</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1308">X</span></span></td>
<td><span data-ttu-id="9b5f6-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1310">X-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1311">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1311">Y</span></span></td>
<td><span data-ttu-id="9b5f6-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1313">Y-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1314">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1314">Type</span></span></td>
<td><span data-ttu-id="9b5f6-1315"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="9b5f6-1316">Erwartete Einheiten für diesen Vektor.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1316">Expected units for this vector.</span></span> <span data-ttu-id="9b5f6-1317">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-1318">Measure</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1318">Measure</span></span></li>
<li><span data-ttu-id="9b5f6-1319">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1319">Length</span></span></li>
<li><span data-ttu-id="9b5f6-1320">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="9b5f6-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1321">Fraction</span></span></li>
<li><span data-ttu-id="9b5f6-1322">Ganze Zahl in Prozent</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b5f6-1323">**IVgVector3D-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="9b5f6-1324">Gibt einen dreidimensionalen Vektor an, der aus drei **Double-Zahlen** besteht.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1325">Wert</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1325">Value</span></span></td>
<td><span data-ttu-id="9b5f6-1326"><strong>Zeichenfolge.</strong></span><span class="sxs-lookup"><span data-stu-id="9b5f6-1326"><strong>String</strong>.</span></span> <span data-ttu-id="9b5f6-1327">Textdarstellung von drei Vektorzahlen, die durch ein Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1328">X</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1328">X</span></span></td>
<td><span data-ttu-id="9b5f6-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1330">X-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1331">„Y“ zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1331">Y</span></span></td>
<td><span data-ttu-id="9b5f6-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1333">Y-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b5f6-1334">Z</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1334">Z</span></span></td>
<td><span data-ttu-id="9b5f6-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="9b5f6-1336">Z-Komponente dieses Vektors.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b5f6-1337">Typ</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1337">Type</span></span></td>
<td><span data-ttu-id="9b5f6-1338"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="9b5f6-1339">Erwartete Einheiten für diesen Vektor.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1339">Expected units for this vector.</span></span> <span data-ttu-id="9b5f6-1340">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="9b5f6-1341">Measure</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1341">Measure</span></span></li>
<li><span data-ttu-id="9b5f6-1342">Länge</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1342">Length</span></span></li>
<li><span data-ttu-id="9b5f6-1343">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="9b5f6-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1344">Fraction</span></span></li>
<li><span data-ttu-id="9b5f6-1345">Zahl</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1345">Number</span></span></li>
<li><span data-ttu-id="9b5f6-1346">Prozentsatz</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1346">Percentage</span></span></li>
<li><span data-ttu-id="9b5f6-1347">Integer</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9b5f6-1348">**Längendatentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1348">**Length data type**</span></span>

<span data-ttu-id="9b5f6-1349">Eine Gleitkommazahl mit einem Bereich von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="9b5f6-1350">**Measuredatentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1350">**Measure data type**</span></span>

<span data-ttu-id="9b5f6-1351">Eine Gleitkommazahl von -infinity bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="9b5f6-1352">**String-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1352">**String data type**</span></span>

<span data-ttu-id="9b5f6-1353">Zeichendaten beliebiger Länge.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1353">Character data of any length.</span></span>

<span data-ttu-id="9b5f6-1354">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="9b5f6-1355">Renderingmodus für Schwarz/Weiß.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="9b5f6-1356">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1356">Possible values are:</span></span>

-   <span data-ttu-id="9b5f6-1357">**Farbe**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1357">**Color**</span></span>
-   <span data-ttu-id="9b5f6-1358">**Automatisch**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1358">**Auto**</span></span>
-   <span data-ttu-id="9b5f6-1359">**Graustufen**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1359">**GrayScale**</span></span>
-   <span data-ttu-id="9b5f6-1360">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="9b5f6-1361">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1361">**InverseGray**</span></span>
-   <span data-ttu-id="9b5f6-1362">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="9b5f6-1363">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="9b5f6-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1364">**HighContrast**</span></span>
-   <span data-ttu-id="9b5f6-1365">**Schwarz**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1365">**Black**</span></span>
-   <span data-ttu-id="9b5f6-1366">**White**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1366">**White**</span></span>
-   <span data-ttu-id="9b5f6-1367">**Undrawn**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1367">**Undrawn**</span></span>

<span data-ttu-id="9b5f6-1368">**VgFraction-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1368">**VgFraction data type**</span></span>

<span data-ttu-id="9b5f6-1369">Gleitkommazahl mit einem Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="9b5f6-1370">Brüche können auch als Prozentsatz angegeben werden. z.B. "50%".</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="9b5f6-1371">**VgTriState-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="9b5f6-1372">Enumeration, die für Werte verwendet wird, die einen von drei Zuzuständen haben können:</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="9b5f6-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1373">**TRUE**</span></span>
-   <span data-ttu-id="9b5f6-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1374">**FALSE**</span></span>
-   <span data-ttu-id="9b5f6-1375">**GEMISCHT**</span><span class="sxs-lookup"><span data-stu-id="9b5f6-1375">**MIXED**</span></span>