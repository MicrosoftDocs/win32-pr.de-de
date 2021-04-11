---
description: Microsoft Windows Search verwendet Eigenschafts Handler, um die Werte von Eigenschaften aus Elementen zu extrahieren, und verwendet das Eigenschafts System Schema, um zu bestimmen, wie eine bestimmte Eigenschaft indiziert werden soll.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Entwickeln von Eigenschaften Handlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214465"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="8620d-103">Entwickeln von Eigenschaften Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="8620d-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="8620d-104">Microsoft Windows Search verwendet Eigenschafts Handler, um die Werte von Eigenschaften aus Elementen zu extrahieren, und verwendet das Eigenschafts System Schema, um zu bestimmen, wie eine bestimmte Eigenschaft indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8620d-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="8620d-105">Um Eigenschaftswerte zu lesen und zu indizieren, werden die Eigenschaften Handler von Windows Search außerhalb des Prozesses aufgerufen, um die Sicherheit und Stabilität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8620d-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="8620d-106">Im Gegensatz dazu werden Eigenschaften Handler in-Process von Windows-Explorer aufgerufen, um Eigenschaftswerte zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="8620d-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="8620d-107">In diesem Thema wird das Thema " [Eigenschaften System](../properties/building-property-handlers.md) " mit speziellen Informationen zu Windows Search ergänzt. es enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="8620d-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="8620d-108">Entwurfsentscheidungen für Eigenschaften Handler</span><span class="sxs-lookup"><span data-stu-id="8620d-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="8620d-109">Eigenschafts Entscheidungen</span><span class="sxs-lookup"><span data-stu-id="8620d-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="8620d-110">Volltextunterstützung</span><span class="sxs-lookup"><span data-stu-id="8620d-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="8620d-111">Überlegungen zur Betriebs System Implementierung</span><span class="sxs-lookup"><span data-stu-id="8620d-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="8620d-112">Schreiben von Eigenschafts Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="8620d-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="8620d-113">Implementieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="8620d-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="8620d-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="8620d-115">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="8620d-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="8620d-116">Ipropertystorecapabilitäten</span><span class="sxs-lookup"><span data-stu-id="8620d-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="8620d-117">Sicherstellen, dass ihre Elemente indiziert werden</span><span class="sxs-lookup"><span data-stu-id="8620d-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="8620d-118">Installieren und Registrieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="8620d-119">Testen und Problembehandlung von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="8620d-120">Installations-und Setup Tests</span><span class="sxs-lookup"><span data-stu-id="8620d-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="8620d-121">Problembehandlung bei Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="8620d-122">Verwenden von System-Supplied-Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="8620d-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8620d-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="8620d-124">Entwurfsentscheidungen für Eigenschaften Handler</span><span class="sxs-lookup"><span data-stu-id="8620d-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="8620d-125">Das Implementieren von Eigenschaften Handlern umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="8620d-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="8620d-126">Treffen Sie Entwurfsentscheidungen bezüglich der Eigenschaften, die Sie unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="8620d-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="8620d-127">Erstellen einer Eigenschafts Beschreibungsdatei (. PropDesc) für Eigenschaften, die sich nicht bereits im Eigenschaften System befinden.</span><span class="sxs-lookup"><span data-stu-id="8620d-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="8620d-128">Implementieren und Testen des Eigenschaften Handlers.</span><span class="sxs-lookup"><span data-stu-id="8620d-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="8620d-129">Installieren und Registrieren des eigenschaftenhandlers und der Eigenschaften Beschreibungsdateien.</span><span class="sxs-lookup"><span data-stu-id="8620d-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="8620d-130">Testen der Installation und Registrierung des eigenschaftenhandlers.</span><span class="sxs-lookup"><span data-stu-id="8620d-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="8620d-131">Bevor Sie beginnen, müssen Sie die folgenden Entwurfs Fragen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="8620d-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="8620d-132">Welche Eigenschaften unterstützt das Dateiformat?</span><span class="sxs-lookup"><span data-stu-id="8620d-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="8620d-133">Sind diese Eigenschaften bereits im System Schema vorhanden?</span><span class="sxs-lookup"><span data-stu-id="8620d-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="8620d-134">Kann ein vorhandener vom System bereitgestellter Eigenschaften Handler verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="8620d-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="8620d-135">Welche Eigenschaften können Endbenutzern angezeigt werden?</span><span class="sxs-lookup"><span data-stu-id="8620d-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="8620d-136">Welche Eigenschaften können Benutzer bearbeiten?</span><span class="sxs-lookup"><span data-stu-id="8620d-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="8620d-137">Sollte die Unterstützung für die Volltextsuche von einem Eigenschafts Handler oder einem Filter stammen?</span><span class="sxs-lookup"><span data-stu-id="8620d-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="8620d-138">Muss ich Legacy Anwendungen unterstützen?</span><span class="sxs-lookup"><span data-stu-id="8620d-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="8620d-139">Wenn dies der Fall ist, was implementiere ich?</span><span class="sxs-lookup"><span data-stu-id="8620d-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="8620d-140">Bevor Sie fortfahren, finden Sie weitere Informationen unter [Verwenden von System-Supplied-Eigenschaften Handlern](#using-system-supplied-property-handlers) , um zu ermitteln, ob Sie einen vom System bereitgestellten Eigenschaften Handler verwenden können</span><span class="sxs-lookup"><span data-stu-id="8620d-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="8620d-141">Nachdem Sie diese Entscheidungen getroffen haben, können Sie formale Beschreibungen Ihrer benutzerdefinierten Eigenschaften schreiben, damit die Windows-Suchmaschine mit der Indizierung Ihrer Dateien und Eigenschaften beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="8620d-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="8620d-142">Diese formalen Beschreibungen sind XML-Dateien, die im [Eigenschafts Beschreibungs Schema](/previous-versions//cc144127(v=vs.85))beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="8620d-143">Eigenschafts Entscheidungen</span><span class="sxs-lookup"><span data-stu-id="8620d-143">Property Decisions</span></span>

<span data-ttu-id="8620d-144">Wenn Sie überlegen, welche Eigenschaften unterstützt werden sollen, sollten Sie die Indizierungs-und Suchanforderungen Ihrer Benutzer identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8620d-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="8620d-145">Beispielsweise können Sie möglicherweise 100 möglicherweise nützliche Eigenschaften für Ihren Dateityp identifizieren, aber Benutzer sind möglicherweise an der Suche nach nur einer Handvoll interessiert.</span><span class="sxs-lookup"><span data-stu-id="8620d-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="8620d-146">Außerdem empfiehlt es sich, Benutzern in Windows-Explorer eine andere, größere oder kleinere Gruppe dieser Eigenschaften anzuzeigen und Benutzern zu gestatten, nur eine Teilmenge der angezeigten Eigenschaften zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8620d-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="8620d-147">Ihr Dateityp unterstützt alle benutzerdefinierten Eigenschaften, die Sie definieren, sowie eine Reihe von System definierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8620d-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="8620d-148">Bevor Sie eine benutzerdefinierte Eigenschaft erstellen, überprüfen Sie die [Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) , um festzustellen, ob die Eigenschaft, die Sie unterstützen möchten, bereits durch eine System Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="8620d-149">Stellen Sie immer sicher, dass Sie die wichtigsten System definierten Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8620d-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="8620d-150">Es wird empfohlen, eine Matrix zu verwenden, die Sie beim Entwerfen Ihrer Eigenschaften unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8620d-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="8620d-151">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="8620d-151">Property name</span></span> | <span data-ttu-id="8620d-152">Ist Indexable?</span><span class="sxs-lookup"><span data-stu-id="8620d-152">Is indexable?</span></span> | <span data-ttu-id="8620d-153">Kann angezeigt werden?</span><span class="sxs-lookup"><span data-stu-id="8620d-153">Is displayable?</span></span> | <span data-ttu-id="8620d-154">Kann bearbeitet werden?</span><span class="sxs-lookup"><span data-stu-id="8620d-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="8620d-155">property1</span><span class="sxs-lookup"><span data-stu-id="8620d-155">property1</span></span>     | <span data-ttu-id="8620d-156">J</span><span class="sxs-lookup"><span data-stu-id="8620d-156">Y</span></span>             | <span data-ttu-id="8620d-157">J</span><span class="sxs-lookup"><span data-stu-id="8620d-157">Y</span></span>               | <span data-ttu-id="8620d-158">N</span><span class="sxs-lookup"><span data-stu-id="8620d-158">N</span></span>            |
| <span data-ttu-id="8620d-159">Eigenschaft...</span><span class="sxs-lookup"><span data-stu-id="8620d-159">property...</span></span>   | <span data-ttu-id="8620d-160">J</span><span class="sxs-lookup"><span data-stu-id="8620d-160">Y</span></span>             | <span data-ttu-id="8620d-161">J</span><span class="sxs-lookup"><span data-stu-id="8620d-161">Y</span></span>               | <span data-ttu-id="8620d-162">N</span><span class="sxs-lookup"><span data-stu-id="8620d-162">N</span></span>            |
| <span data-ttu-id="8620d-163">propertyN</span><span class="sxs-lookup"><span data-stu-id="8620d-163">propertyn</span></span>     | <span data-ttu-id="8620d-164">N</span><span class="sxs-lookup"><span data-stu-id="8620d-164">N</span></span>             | <span data-ttu-id="8620d-165">N</span><span class="sxs-lookup"><span data-stu-id="8620d-165">N</span></span>               | <span data-ttu-id="8620d-166">N</span><span class="sxs-lookup"><span data-stu-id="8620d-166">N</span></span>            |



 

<span data-ttu-id="8620d-167">Sie müssen für jede dieser Eigenschaften bestimmen, welche Attribute vorhanden sein sollten, und Sie dann formal in den Eigenschafts Beschreibungs-XML-Dateien (. PropDesc) beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8620d-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="8620d-168">Zu den Attributen zählen der Datentyp der Eigenschaft, die Bezeichnung, die Hilfe Zeichenfolge und mehr.</span><span class="sxs-lookup"><span data-stu-id="8620d-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="8620d-169">Bei indizierbaren Eigenschaften sollten Sie besonders auf die folgenden Eigenschafts Attribute achten, die im XML-Element [SearchInfo](../properties/propdesc-schema-searchinfo.md)   der Eigenschafts Beschreibungsdatei gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="8620d-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8620d-170">Attribut</span><span class="sxs-lookup"><span data-stu-id="8620d-170">Attribute</span></span></th>
<th><span data-ttu-id="8620d-171">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8620d-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8620d-172">ininvertedindex</span><span class="sxs-lookup"><span data-stu-id="8620d-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="8620d-173">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8620d-173">Optional.</span></span> <span data-ttu-id="8620d-174">Gibt an, ob ein Zeichen folgen Eigenschafts Wert in Wörter und jedes im umgekehrten Index gespeicherte Wort unterteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8620d-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="8620d-175">Der invertierte Index ermöglicht das effiziente suchen nach Wörtern und Ausdrücken über den Eigenschafts Wert mit "enthält" oder "frei Text" (z. b. Select... Where enthält einen &quot; Text &quot; ).</span><span class="sxs-lookup"><span data-stu-id="8620d-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="8620d-176">Wenn diese Einstellung auf " <strong>false</strong>" festgelegt ist, erfolgt die Suche anhand der gesamten Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8620d-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="8620d-177">Für die meisten Zeichen folgen Eigenschaften sollte diese Eigenschaft auf <strong>true</strong>festgelegt sein. für nicht-Zeichen folgen Eigenschaften sollte This auf <strong>false</strong>festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="8620d-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="8620d-178">Der Standardwert ist <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="8620d-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8620d-179">iscolumn</span><span class="sxs-lookup"><span data-stu-id="8620d-179">isColumn</span></span></td>
<td><span data-ttu-id="8620d-180">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8620d-180">Optional.</span></span> <span data-ttu-id="8620d-181">Gibt an, ob die-Eigenschaft in der Windows Search-Datenbank als Spalte gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8620d-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="8620d-182">Das Speichern der Eigenschaft als Spalte ermöglicht das Abrufen, sortieren, gruppieren und Filtern (d. h. die Verwendung eines beliebigen Prädikats außer enthält oder frei Text) für den gesamten Spaltenwert.</span><span class="sxs-lookup"><span data-stu-id="8620d-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="8620d-183">Für Eigenschaften, die dem Benutzer angezeigt werden, sollte diese Eigenschaft auf " <strong>true</strong> " festgelegt sein, es sei denn, es handelt sich um eine sehr große Text Eigenschaft (z. b</span><span class="sxs-lookup"><span data-stu-id="8620d-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="8620d-184">Der Standardwert ist <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="8620d-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8620d-185">iscolumnsparse</span><span class="sxs-lookup"><span data-stu-id="8620d-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="8620d-186">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8620d-186">Optional.</span></span> <span data-ttu-id="8620d-187">Gibt an, ob eine Eigenschaft keinen Speicherplatz annimmt, wenn der Wert <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="8620d-188">Eine nicht-Sparse-Eigenschaft benötigt für jedes Element Platz, auch wenn der Wert <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="8620d-189">Wenn die Eigenschaft mehr wertig ist, ist dieses Attribut immer " <strong>true</strong>".</span><span class="sxs-lookup"><span data-stu-id="8620d-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="8620d-190">Dieses Attribut sollte nur dann <strong>false</strong> lauten, wenn für jedes Element ein Wert vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="8620d-191">Der Standardwert ist " <strong>true</strong>".</span><span class="sxs-lookup"><span data-stu-id="8620d-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8620d-192">columnindextype</span><span class="sxs-lookup"><span data-stu-id="8620d-192">columnIndexType</span></span></td>
<td><span data-ttu-id="8620d-193">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8620d-193">Optional.</span></span> <span data-ttu-id="8620d-194">Um die Abfrage zu optimieren, kann das Windows Search-Modul sekundäre Indizes für Eigenschaften erstellen, deren iscolumn =<strong>true</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="8620d-195">Dies erfordert mehr Verarbeitung und Speicherplatz während der Indizierung, verbessert jedoch die Leistung während der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8620d-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="8620d-196">Wenn die Eigenschaft tendenziell sortiert, gruppiert oder gefiltert wird (d. h., Sie verwendet =,! =, < >, wie z. b. Übereinstimmungen), sollte dieses Attribut auf ondisk festgelegt werden &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="8620d-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="8620d-197">Der Standardwert ist " &quot; notindiziert" &quot; .</span><span class="sxs-lookup"><span data-stu-id="8620d-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="8620d-198">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8620d-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="8620d-199">Notindiziert: Es wird kein sekundärer Index erstellt.</span><span class="sxs-lookup"><span data-stu-id="8620d-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="8620d-200">Ondisk: Erstellen und speichern Sie einen sekundären Index auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="8620d-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8620d-201">MaxSize</span><span class="sxs-lookup"><span data-stu-id="8620d-201">maxSize</span></span></td>
<td><span data-ttu-id="8620d-202">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8620d-202">Optional.</span></span> <span data-ttu-id="8620d-203">Gibt die maximal zulässige Größe für den Eigenschafts Wert an, der in der Windows Search-Datenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="8620d-204">Dieser Grenzwert gilt für die einzeidualen Elemente eines Vektors, nicht für den Vektor als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="8620d-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="8620d-205">Werte, die diese Größe überschreiten, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="8620d-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="8620d-206">Der Standardwert ist &quot; 128 &quot; (Bytes).</span><span class="sxs-lookup"><span data-stu-id="8620d-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="8620d-207">Derzeit verwendet Windows Search nicht den MAXSIZE-Wert, wenn die Menge der Daten berechnet wird, die Sie aus einer Datei akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8620d-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="8620d-208">Stattdessen ist der Grenzwert, den Windows Search verwendet, das Produkt der Dateigröße und der MaxGrowFactor (Dateigröße N \* MaxGrowFactor), die aus der Registrierung bei HKEY_LOCAL_MACHINE->Software >Microsoft->Windows Search->Erteilungs-Manager->MaxGrowFactor gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="8620d-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="8620d-209">Der Standardwert für MaxGrowFactor ist vier (4).</span><span class="sxs-lookup"><span data-stu-id="8620d-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="8620d-210">Wenn Ihr Dateityp tendenziell klein ist, aber größere Eigenschaften hat, akzeptiert Windows Search möglicherweise nicht alle Eigenschaften Daten, die Sie ausgeben möchten.</span><span class="sxs-lookup"><span data-stu-id="8620d-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="8620d-211">Sie können jedoch den MaxGrowFactor-Faktor entsprechend Ihren Anforderungen erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8620d-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="8620d-212">Für das columnindextype-Attribut muss der Vorteil von schnelleren Abfragen mit der größeren Indizierungs Zeit und den Speicherplatz Kosten abgewogen werden, die die sekundären Indizes verursachen können.</span><span class="sxs-lookup"><span data-stu-id="8620d-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="8620d-213">Diese Kosten werden jedoch nur für Elemente mit einem Wert ungleich **null** gezahlt, sodass dieses Attribut für die meisten Eigenschaften auf "ondisk" festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8620d-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="8620d-214">Volltextunterstützung</span><span class="sxs-lookup"><span data-stu-id="8620d-214">Full-Text Support</span></span>

<span data-ttu-id="8620d-215">Im Allgemeinen wird die Volltextsuche von Komponenten unterstützt, die als [Filter](-search-3x-wds-extidx-filters.md)bezeichnet werden. bei textbasierten Dateitypen mit unkomplizierten Dateiformaten können Eigenschafts Handler diese Funktionalität jedoch mit weniger Entwicklungsaufwand bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8620d-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="8620d-216">Lesen Sie den Abschnitt [voll Text Inhalte](../properties/building-property-handlers-property-handlers.md) , um einen Vergleich der Filter-und eigenschaftenhandlerfunktionen zu finden, mit denen Sie entscheiden können, was für den Dateityp am besten ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="8620d-217">Besonders wichtig ist die Tatsache, dass Filter mehrere Sprachcode Bezeichner (LCIDs) pro Datei verarbeiten können, während dies bei Eigenschaften Handlern nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="8620d-218">Da Eigenschafts Handler Inhalte nicht wie Filter segmentieren können, müssen große Dateien vollständig in den Arbeitsspeicher geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="8620d-219">Überlegungen zur Betriebs System Implementierung</span><span class="sxs-lookup"><span data-stu-id="8620d-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="8620d-220">Implementierungs Informationen für Windows 7</span><span class="sxs-lookup"><span data-stu-id="8620d-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="8620d-221">In Windows 7 und höher gibt es neues Verhalten beim Registrieren eines Eigenschaften Handlers, [**IFilters**](/windows/win32/api/filter/nn-filter-ifilter)oder einer neuen Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8620d-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="8620d-222">Wenn ein neuer Eigenschaften Handler und/oder **IFilter** installiert wird, werden Dateien mit den entsprechenden Erweiterungen automatisch neu indiziert.</span><span class="sxs-lookup"><span data-stu-id="8620d-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="8620d-223">In Windows 7 wird empfohlen, dass ein [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) in Verbindung mit den entsprechenden Eigenschaften Handlern installiert wird und dass der **IFilter** vor dem Eigenschaften Handler registriert wird.</span><span class="sxs-lookup"><span data-stu-id="8620d-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="8620d-224">Durch die Registrierung des Eigenschaften Handlers wird die sofortige Neuindizierung von zuvor indizierten Dateien initiiert, ohne dass zunächst ein Neustart erforderlich ist. dabei werden alle zuvor registrierten IFilter für die Inhalts Indizierung genutzt.</span><span class="sxs-lookup"><span data-stu-id="8620d-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="8620d-225">Wenn nur ein [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ohne entsprechenden Eigenschaften Handler installiert wird, erfolgt die automatische Neuindizierung entweder nach einem Neustart des Indizierungs dienstanzdienstanzdienstanbieter oder einem Neustart des Systems.</span><span class="sxs-lookup"><span data-stu-id="8620d-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="8620d-226">Informationen zu eigenschaftenbeschreibungsflags für Windows 7 finden Sie in den folgenden Referenz Themen:</span><span class="sxs-lookup"><span data-stu-id="8620d-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="8620d-227">Getpropertystoreflags</span><span class="sxs-lookup"><span data-stu-id="8620d-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="8620d-228">PropDesc- \_ ColumnIndex- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="8620d-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="8620d-229">propde- \_ SearchInfo- \_ Flags</span><span class="sxs-lookup"><span data-stu-id="8620d-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="8620d-230">Implementierungs Informationen für Windows Vista und frühere Versionen</span><span class="sxs-lookup"><span data-stu-id="8620d-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="8620d-231">Vor Windows Vista wurden von Filtern Unterstützung für das Auswerten und Auflisten von Dateiinhalten und-Eigenschaften bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8620d-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="8620d-232">Mit der Einführung des Eigenschaften Systems behandeln Eigenschaften Handler Dateieigenschaften, während Filterdatei Inhalte verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8620d-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="8620d-233">Für Windows Vista müssen Sie nur eine partielle Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)-Schnittstelle in Abstimmung mit einem Eigenschafts Handler entwickeln, wie in [bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8620d-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="8620d-234">Obwohl das-Eigenschaften System auch in der Windows Search-Installation für Windows XP enthalten ist, ist es für Drittanbieter-und Legacy Anwendungen möglicherweise erforderlich, dass Filter sowohl Inhalte als auch Eigenschaften verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8620d-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="8620d-235">Wenn Sie auf der Windows XP-Plattform entwickeln, sollten Sie daher eine vollständige Filter Implementierung und einen Eigenschafts Handler für den Dateityp oder die benutzerdefinierte Eigenschaft bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8620d-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="8620d-236">Schreiben von Eigenschafts Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="8620d-236">Writing Property Description Files</span></span>

<span data-ttu-id="8620d-237">Die Struktur der Eigenschafts Beschreibungs-XML-Dateien (. PropDesc) wird im Thema [propertydescription](../properties/propdesc-schema-propertydescription.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8620d-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="8620d-238">Besonderes Interesse für die Suche sind die Attribute des [SearchInfo](../properties/propdesc-schema-searchinfo.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="8620d-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="8620d-239">Nachdem Sie entschieden haben, welche Eigenschaften unterstützt werden sollen, müssen Sie Eigenschafts Beschreibungsdateien für die einzelnen Eigenschaften erstellen und registrieren.</span><span class="sxs-lookup"><span data-stu-id="8620d-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="8620d-240">Wenn Sie Ihre. PropDesc-Dateien registrieren, sind Sie in der Eigenschafts Beschreibungs Liste des Schemas enthalten und werden zu Spaltennamen innerhalb des Eigenschaften Stores der Suchmaschine.</span><span class="sxs-lookup"><span data-stu-id="8620d-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="8620d-241">Sie können Ihre benutzerdefinierten Eigenschaften Beschreibungen mithilfe der [psregisterpropertyschema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) -Funktion registrieren, einer Wrapper-API, die das ipropertysystem:: registerpropertyschema des Schema Subsystems aufruft.</span><span class="sxs-lookup"><span data-stu-id="8620d-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="8620d-242">Diese Funktion informiert das Schema Subsystem über das Hinzufügen von Eigenschafts Beschreibungs-Schema Dateien (. PropDesc) mithilfe von Dateipfaden zu den. PropDesc-Dateien auf dem lokalen Computer, in der Regel das Installationsverzeichnis der Anwendung unter "Programme".</span><span class="sxs-lookup"><span data-stu-id="8620d-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="8620d-243">In der Regel Ruft ein Setup oder eine Anwendung (z. b. das Installationsprogramm des Eigenschaften Handlers) diese Methode nach der Installation der. PropDesc-Datei (en) auf.</span><span class="sxs-lookup"><span data-stu-id="8620d-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="8620d-244">Implementieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-244">Implementing Property Handlers</span></span>

<span data-ttu-id="8620d-245">Die Entwicklung eines Eigenschaften Handlers umfasst die Implementierung der folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="8620d-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="8620d-246">Iinitialzewithstream: stellt die streambasierte Initialisierung des Eigenschafts Handlers bereit.</span><span class="sxs-lookup"><span data-stu-id="8620d-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="8620d-247">IPropertyStore: Listet Eigenschaftswerte auf, ruft Sie ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="8620d-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="8620d-248">Ipropertystorecapabili: optional.</span><span class="sxs-lookup"><span data-stu-id="8620d-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="8620d-249">Gibt an, ob Benutzer eine Eigenschaft von einer Benutzeroberfläche aus bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="8620d-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="8620d-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="8620d-250">IInitializeWithStream</span></span>

<span data-ttu-id="8620d-251">Wie im Thema " [Eigenschaften System](../properties/building-property-handlers.md) " beschrieben, wird dringend empfohlen, Eigenschafts Handler mit **IInitializeWithStream** zu implementieren, um die streambasierte Initialisierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8620d-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="8620d-252">Wenn Sie IInitializeWithStream nicht implementieren möchten, muss der Eigenschafts Handler die Ausführung im Isolations Prozess deaktivieren, indem das Flag disableprocessisolation für den Registrierungsschlüssel des Eigenschaften Handlers festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8620d-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="8620d-253">Die Deaktivierung der Prozess Isolation ist in der Regel nur für Legacy-Eigenschaften Handler vorgesehen und sollte durch neuen Code energisch vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="8620d-254">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="8620d-254">IPropertyStore</span></span>

<span data-ttu-id="8620d-255">Zum Erstellen eines Eigenschaften Handlers müssen Sie die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle mit den folgenden Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="8620d-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="8620d-256">Methode</span><span class="sxs-lookup"><span data-stu-id="8620d-256">Method</span></span>   | <span data-ttu-id="8620d-257">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8620d-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="8620d-258">Commit</span><span class="sxs-lookup"><span data-stu-id="8620d-258">Commit</span></span>   | <span data-ttu-id="8620d-259">Speichert eine Eigenschafts Änderung in der Datei.</span><span class="sxs-lookup"><span data-stu-id="8620d-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="8620d-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="8620d-260">GetAt</span></span>    | <span data-ttu-id="8620d-261">Ruft einen Eigenschafts Schlüssel aus dem Array von Eigenschaften eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="8620d-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="8620d-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="8620d-262">GetCount</span></span> | <span data-ttu-id="8620d-263">Ruft die Anzahl der Eigenschaften ab, die an die Datei angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="8620d-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="8620d-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="8620d-264">GetValue</span></span> | <span data-ttu-id="8620d-265">Ruft Daten für eine bestimmte Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="8620d-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="8620d-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="8620d-266">SetValue</span></span> | <span data-ttu-id="8620d-267">Legt einen neuen Eigenschafts Wert fest oder ersetzt oder entfernt einen vorhandenen Wert.</span><span class="sxs-lookup"><span data-stu-id="8620d-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="8620d-268">Wichtige Überlegungen zur Implementierung dieser Schnittstelle sind in der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Dokumentation enthalten.</span><span class="sxs-lookup"><span data-stu-id="8620d-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="8620d-269">Wenn der Eigenschafts Handler mehrere Werte für dieselbe Eigenschaft für ein bestimmtes Element ausgibt, wird nur der letzte ausgegebene Wert im Katalog gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8620d-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="8620d-270">Ipropertystorecapabilitäten</span><span class="sxs-lookup"><span data-stu-id="8620d-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="8620d-271">Eigenschaften Handler können diese Schnittstelle optional implementieren, um die Fähigkeit eines Benutzers zu deaktivieren, bestimmte Eigenschaften zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8620d-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="8620d-272">Diese Eigenschaften sind in der Regel auf der Detailseite und im Bereich bearbeitbar, Sie können jedoch nicht unter dem implementierenden Eigenschaften Handler bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="8620d-273">Die Implementierung dieser Schnittstelle bietet eine bessere Benutzeroberfläche als die Alternative – ein einfacher Laufzeitfehler in der Shell.</span><span class="sxs-lookup"><span data-stu-id="8620d-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="8620d-274">Sicherstellen, dass ihre Elemente indiziert werden</span><span class="sxs-lookup"><span data-stu-id="8620d-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="8620d-275">Nachdem Sie den Eigenschafts Handler implementiert haben, möchten Sie sicherstellen, dass die Elemente, für die der Handler registriert ist, indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="8620d-276">Sie können den [Katalog-Manager](-search-3x-wds-mngidx-catalog-manager.md) verwenden, um die erneute Indizierung zu initiieren. Außerdem können Sie mit dem [Crawl Scope-Manager](-search-3x-wds-extidx-csm.md) Standardregeln einrichten, die die URLs angeben, die der Indexer durchforsten soll.</span><span class="sxs-lookup"><span data-stu-id="8620d-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="8620d-277">Eine weitere Möglichkeit besteht darin, das Codebeispiel "REINDEX" in den [Windows Search SDK-Beispielen](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="8620d-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="8620d-278">Weitere Informationen finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="8620d-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="8620d-279">Installieren und Registrieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="8620d-280">Nachdem der Eigenschaften Handler implementiert wurde, muss er registriert und seine Dateinamenerweiterung dem Handler zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="8620d-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="8620d-281">Das folgende Beispiel zeigt die Registrierungsschlüssel und-Werte, die hierfür erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8620d-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="8620d-282">Testen und Problembehandlung von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="8620d-283">In der folgenden Liste finden Sie Ratschläge zu den Arten von Tests, die Sie durchführen sollten:</span><span class="sxs-lookup"><span data-stu-id="8620d-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="8620d-284">Testen Sie die Ausgabe von jeder einzelnen Eigenschaft, die vom Dateityp unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8620d-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="8620d-285">Verwenden Sie große Eigenschaftswerte, z. b. ein großes-Metatag in HTML-Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="8620d-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="8620d-286">Überprüfen Sie, ob der Eigenschafts Handler Datei Handles nicht löscht, indem Sie Sie bearbeiten, nachdem Sie die Ausgabe des Eigenschaften Handlers erhalten haben, oder indem Sie ein Tool wie oh.exe vor und nach dem Auflisten von Dateieigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="8620d-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="8620d-287">Testen Sie alle Dateitypen, die dem Eigenschaften Handler zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8620d-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="8620d-288">Überprüfen Sie z. b., ob der HTML-Filter mit den Dateitypen htm und HTML funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8620d-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="8620d-289">Testen Sie mit beschädigten Dateien.</span><span class="sxs-lookup"><span data-stu-id="8620d-289">Test with corrupted files.</span></span> <span data-ttu-id="8620d-290">Der Eigenschafts Handler sollte ordnungsgemäß fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="8620d-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="8620d-291">Wenn eine Anwendung die Verschlüsselung unterstützt, testen Sie, ob der Eigenschaften Handler verschlüsselten Text ausgibt.</span><span class="sxs-lookup"><span data-stu-id="8620d-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="8620d-292">Wenn der Eigenschafts Handler die Volltextsuche unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8620d-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="8620d-293">Verwenden Sie mehrere spezielle Unicode-Zeichen im Dateiinhalt, und testen Sie Ihre Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8620d-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="8620d-294">Testen Sie die Verarbeitung sehr großer Dokumente, um sicherzustellen, dass der Eigenschafts Handler erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8620d-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="8620d-295">Installations-und Setup Tests</span><span class="sxs-lookup"><span data-stu-id="8620d-295">Installation and Setup Tests</span></span>

<span data-ttu-id="8620d-296">Schließlich müssen Sie die Installations-und Deinstallations Routinen testen.</span><span class="sxs-lookup"><span data-stu-id="8620d-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="8620d-297">Die Installation muss bei fehlgeschlagenen Installationen (z. b. beim Abbrechen und anschließenden erneuten Starten des Setups) wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="8620d-298">Die Deinstallation muss alle Dateien löschen, die dem Eigenschaften Handler zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8620d-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="8620d-299">Bei der Deinstallation dürfen Dateien nicht gelöscht werden, die mit der Installation des Eigenschaften Handlers verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="8620d-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="8620d-300">Die dem Eigenschafts Handler zugeordneten Registrierungsschlüssel müssen entfernt werden, wenn Sie deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="8620d-301">Die Deinstallation muss funktionieren, auch wenn Dateien aus dem Installationsverzeichnis gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8620d-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="8620d-302">Problembehandlung bei Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="8620d-303">Im folgenden werden einige häufige Fehler beim Entwickeln von Eigenschaften Handlern aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8620d-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="8620d-304">Installieren von. PropDesc-Dateien oder-DLLs unter einem Benutzerverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8620d-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="8620d-305">Registrieren von Komponenten mithilfe relativer Pfade.</span><span class="sxs-lookup"><span data-stu-id="8620d-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="8620d-306">Die Komponenten unter HKEY \_ Current \_ User anstelle des lokalen HKEY-Computers werden registriert \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8620d-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="8620d-307">Das Festlegen von disableprocessisolations für nicht-Stream-Handler wird vergessen.</span><span class="sxs-lookup"><span data-stu-id="8620d-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="8620d-308">Die Testdatei wird an einem nicht indizierten Speicherort platziert.</span><span class="sxs-lookup"><span data-stu-id="8620d-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="8620d-309">Wenn Sie Probleme haben, den Eigenschaftenhandler mit dem Indexer zu arbeiten, finden Sie hier einige Tipps, die Ihnen bei der Problembehandlung helfen:</span><span class="sxs-lookup"><span data-stu-id="8620d-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="8620d-310">Überprüfen Sie, ob ihre Eigenschaften Beschreibungen (. PropDesc-Dateien) nach Bedarf als iscolumn = "**true**", "isviewable ="**true**"und" isquervable = "**true**" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="8620d-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="8620d-311">Überprüfen Sie, ob sich Ihre. PropDesc-Dateien an einem globalen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="8620d-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="8620d-312">Vergewissern Sie sich, dass Sie Ihre. PropDesc-Dateien mit absoluten Pfaden registriert haben.</span><span class="sxs-lookup"><span data-stu-id="8620d-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="8620d-313">Vergewissern Sie sich, dass das Ereignisprotokoll keine Fehler beim Registrieren Ihrer. PropDesc-Datei aufgezeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="8620d-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="8620d-314">Stellen Sie sicher, dass sich Ihre DLLs an einem globalen Speicherort befinden (und nicht unter Ihrem Benutzerprofil).</span><span class="sxs-lookup"><span data-stu-id="8620d-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="8620d-315">Überprüfen Sie, ob Ihre DLLs unter HKEY- \_ Software Klassen für lokale Computer registriert sind \_ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="8620d-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="8620d-316">Stellen Sie sicher, dass Ihre DLLs mit vollständigen Pfaden registriert sind (oder reg-Zeichen folgen \_ \_ , die auf absolute Pfade erweitert werden, mithilfe von Umgebungsvariablen, die vom System Konto bekannt sind).</span><span class="sxs-lookup"><span data-stu-id="8620d-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="8620d-317">Überprüfen Sie, ob der Eigenschafts Handler im Windows-Explorer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8620d-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="8620d-318">Es wird empfohlen, IInitializeWithStream zu verwenden, wenn Sie IInitializeWithFile oder IInitializeWithItem verwenden müssen, vergewissern Sie sich, dass Sie disableprocessisolations angeben.</span><span class="sxs-lookup"><span data-stu-id="8620d-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="8620d-319">Vergewissern Sie sich, dass der Dateityp in der Systemsteuerung für die Indizierungs Optionen als indizierter Dateityp</span><span class="sxs-lookup"><span data-stu-id="8620d-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="8620d-320">Überprüfen Sie, ob sich die Testdatei an einem indizierten Speicherort befindet</span><span class="sxs-lookup"><span data-stu-id="8620d-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="8620d-321">Vergewissern Sie sich, dass die Testdatei seit der Installation des Eigenschaften Handlers geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="8620d-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="8620d-322">Wenn sich die Testdatei an einem indizierten Speicherort befindet und der Indexer diese Position bereits durchlaufen hat, müssen Sie die Datei auf irgendeine Weise ändern, um eine Neuindizierung der Datei zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="8620d-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="8620d-323">Verwenden von System-Supplied-Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="8620d-324">Windows enthält eine Reihe von vom System bereitgestellten Eigenschaften Handlern, die Sie verwenden können, wenn das Format des Dateityps kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="8620d-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="8620d-325">Wenn Sie eine neue Dateierweiterung definieren, die eines dieser Formate verwendet, können Sie die vom System bereitgestellten Handler verwenden, indem Sie die Handlerklassen-ID (CLSID) für die Dateierweiterung registrieren.</span><span class="sxs-lookup"><span data-stu-id="8620d-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="8620d-326">Sie können die in der folgenden Tabelle aufgeführte CLSID verwenden, um die vom System bereitgestellten Eigenschaften Handler für den Datei Formattyp zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8620d-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="8620d-327">Format</span><span class="sxs-lookup"><span data-stu-id="8620d-327">Format</span></span>          | <span data-ttu-id="8620d-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="8620d-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="8620d-329">OLE-DOCFILE</span><span class="sxs-lookup"><span data-stu-id="8620d-329">OLE DocFile</span></span>     | <span data-ttu-id="8620d-330">{8d80504a-0826-40c5-97e1-ebc68f 953792}</span><span class="sxs-lookup"><span data-stu-id="8620d-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="8620d-331">Speichern von Spiel-XML</span><span class="sxs-lookup"><span data-stu-id="8620d-331">Save Game XML</span></span>   | <span data-ttu-id="8620d-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="8620d-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="8620d-333">XPS-/OPC-Handler</span><span class="sxs-lookup"><span data-stu-id="8620d-333">XPS/OPC handler</span></span> | <span data-ttu-id="8620d-334">{45670fa8-ed97-4f 44-bc93-305082590bfb}</span><span class="sxs-lookup"><span data-stu-id="8620d-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="8620d-335">XML</span><span class="sxs-lookup"><span data-stu-id="8620d-335">XML</span></span>             | <span data-ttu-id="8620d-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="8620d-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="8620d-337">Vor dem Erstellen einer benutzerdefinierten Eigenschaft sollten Sie sicherstellen, dass es keine System definierte Eigenschaft gibt, die Sie stattdessen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8620d-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="8620d-338">Sie können die System definierten Eigenschaften auflisten, indem Sie [**psenumeratepropertybeschreibungen**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) aufrufen oder das Befehlszeilen Tool prop.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="8620d-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="8620d-339">Das System Schema definiert, wie diese Eigenschaften mit dem Indexer interagieren, und Sie können diese Eigenschaften nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="8620d-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="8620d-340">Außerdem muss die Anwendung, mit der Sie den Dateityp erstellen, bearbeiten und speichern, auch mit einem bestimmten Verhalten übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8620d-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="8620d-341">Wenn die Anwendung z. b. Sicheres Speichern implementiert (wobei eine temporäre Datei während der Bearbeitung erstellt wird und dann ReplaceFile () verwendet wird, um die neue Version für die alte zu tauschen), muss Sie alle Eigenschaften der ursprünglichen Datei in die neue Datei übertragen.</span><span class="sxs-lookup"><span data-stu-id="8620d-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="8620d-342">Dies bedeutet, dass die Datei von Benutzern oder anderen Anwendungen hinzugefügte Eigenschaften verliert.</span><span class="sxs-lookup"><span data-stu-id="8620d-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="8620d-343">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="8620d-343">**Example**</span></span>

<span data-ttu-id="8620d-344">Im folgenden Beispiel wird die Registrierung des vom System bereitgestellten OLE DOCFILE-Handlers für einen Dateityp mit einem gezeigt. Oledocfile-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8620d-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="8620d-345">Das folgende Beispiel zeigt die Registrierung der Eigenschaften Listen Informationen, sodass Eigenschaften von. Oledocfile-Dateien werden auf der Registerkarte Details und im Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8620d-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="8620d-346">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8620d-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8620d-347">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="8620d-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8620d-348">Eigenschafts Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="8620d-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="8620d-349">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8620d-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8620d-350">Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="8620d-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="8620d-351">Der Indizierungsprozess</span><span class="sxs-lookup"><span data-stu-id="8620d-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="8620d-352">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="8620d-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="8620d-353">System definierte Eigenschaften für benutzerdefinierte Dateiformate</span><span class="sxs-lookup"><span data-stu-id="8620d-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="8620d-354">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="8620d-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8620d-355">Eigenschaften System</span><span class="sxs-lookup"><span data-stu-id="8620d-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="8620d-356">[System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="8620d-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="8620d-357">Beispiele für Windows Search SDK</span><span class="sxs-lookup"><span data-stu-id="8620d-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
