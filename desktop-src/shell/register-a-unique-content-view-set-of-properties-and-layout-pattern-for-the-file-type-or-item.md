---
description: Sie können eine eindeutige Eigenschaften Liste für Inhalts Ansichten und ein Layoutmuster für den Dateityp oder das Element registrieren.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registriert einen Inhalts Ansichts Satz von Eigenschaften und layoutmustern für einen Dateityp oder ein Element.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104350799"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="0465c-103">Registrieren eines eindeutigen Inhalts Ansichts Satzes von Eigenschaften und eines Layoutmusters für den Dateityp oder das Element</span><span class="sxs-lookup"><span data-stu-id="0465c-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="0465c-104">Sie können eine eindeutige Eigenschaften Liste für Inhalts Ansichten und ein Layoutmuster für den Dateityp oder das Element registrieren.</span><span class="sxs-lookup"><span data-stu-id="0465c-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="0465c-105">Wenn Ihr Dateityp oder ein Element auch einer Art zugeordnet ist, überschreibt die Registrierung für die jeweilige Inhaltsansicht des Dateityps oder-Elements die Kind-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="0465c-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="0465c-106">Dies kann hilfreich sein, wenn sich die wichtigsten Eigenschaften für dieses Element von anderen Elementen derselben Art unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="0465c-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="0465c-107">Wenn Sie den Dateityp oder das Element nicht einem Elementtyp zuordnen oder die Inhaltsansicht direkt registrieren, verwendet das System die Standardinformationen der Inhaltsansicht (die in einem Registrierungsschlüssel gespeichert sind, auf den das letzte Element im Zuordnungs Array der Elemente, HKEY \_ Classes \_ root \\ \* ) folgt.</span><span class="sxs-lookup"><span data-stu-id="0465c-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="0465c-108">Bevor Sie eine benutzerdefinierte Eigenschaften Liste für Ihren Dateityp registrieren, sollten Sie sich mit dem Suchergebnis Modus und dem Suchmodus sowie den layoutmustern vertraut machen, die Ihnen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="0465c-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="0465c-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="0465c-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="0465c-110">Schritt 1: Grundlegendes zum Suchergebnis Modus und Durchsuchen-Modus</span><span class="sxs-lookup"><span data-stu-id="0465c-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="0465c-111">Die Inhaltsansicht erfordert das Definieren eines Layoutmusters und eines Satzes von Eigenschaften Listen für ein Element in einem Satz von Suchergebnissen (Suchergebnis Modus) und beim Durchsuchen eines shellorts (Durchsuchen-Modus).</span><span class="sxs-lookup"><span data-stu-id="0465c-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="0465c-112">Sie können dieselben Werte für das Suchergebnis verwenden und wie durchsuchen `Kind.Music` .</span><span class="sxs-lookup"><span data-stu-id="0465c-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="0465c-113">Alternativ dazu können Sie auch eine andere Eigenschaften Liste und/oder ein anderes Layoutmuster definieren `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="0465c-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="0465c-114">Im Fall von `Kind.Document` Suchen Benutzer häufig nach Wörtern im Text des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0465c-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="0465c-115">Daher ist das Einschließen von mehr Beispiel Text in das Suchergebnis möglicherweise die beste Wahl.</span><span class="sxs-lookup"><span data-stu-id="0465c-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="0465c-116">Im folgenden Beispiel wird die Ansicht Inhalt Durchsuchen von veranschaulicht `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="0465c-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![Durchsuchen der Inhaltsansicht von kind.docUmschlag](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="0465c-118">Da Benutzer beim Durchsuchen von Dokumenten nur selten nach einem bestimmten Text suchen, ist die Optimierung der Auswahl von Eigenschaften und des Layouts für mehr Suchergebnisse auf dem Bildschirm möglicherweise die beste Wahl.</span><span class="sxs-lookup"><span data-stu-id="0465c-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="0465c-119">Der folgende Screenshot veranschaulicht die Such Inhaltsansicht von `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="0465c-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="0465c-120">Schritt 2: Grundlegendes zu layoutmustern</span><span class="sxs-lookup"><span data-stu-id="0465c-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="0465c-121">Es gibt vier Layoutmuster: Alpha, Beta, Gamma und Delta.</span><span class="sxs-lookup"><span data-stu-id="0465c-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="0465c-122">**Alpha Layout**</span><span class="sxs-lookup"><span data-stu-id="0465c-122">**Alpha layout**</span></span>

<span data-ttu-id="0465c-123">Das Alpha-Layoutmuster ist für Dokument Suchergebnisse optimiert, die Ausschnitte enthalten.</span><span class="sxs-lookup"><span data-stu-id="0465c-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="0465c-124">Es verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="0465c-124">It has the following specifications:</span></span>

-   <span data-ttu-id="0465c-125">Zeilen: 4</span><span class="sxs-lookup"><span data-stu-id="0465c-125">Rows: 4</span></span>
-   <span data-ttu-id="0465c-126">Eigenschaften: 7</span><span class="sxs-lookup"><span data-stu-id="0465c-126">Properties: 7</span></span>
-   <span data-ttu-id="0465c-127">Alpha Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0465c-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Alpha-Layoutmuster](images/content-view/layout1.png)

-   <span data-ttu-id="0465c-129">In der folgenden Abbildung ist das Alpha-Layout dargestellt, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagramm mit einem Alpha Layoutbeispiel](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="0465c-131">In der folgenden Abbildung ist das Alpha-Layout dargestellt, wenn das Element weniger als 350 Pixel horizontalen Leerraum aufweist.</span><span class="sxs-lookup"><span data-stu-id="0465c-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Screenshot, der ein Alpha-Layoutbeispiel in Microsoft Word zeigt.](images/content-view/layout2.png)

-   <span data-ttu-id="0465c-133">In der folgenden Abbildung ist das Alpha-Layout dargestellt, wenn das Element weniger als 350 Pixel horizontalen Leerraum aufweist.</span><span class="sxs-lookup"><span data-stu-id="0465c-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Alpha Layout-Beispiel](images/content-view/alphaviewless.png)

<span data-ttu-id="0465c-135">**Beta-Layout**</span><span class="sxs-lookup"><span data-stu-id="0465c-135">**Beta Layout**</span></span>

<span data-ttu-id="0465c-136">Das Beta-Layoutmuster ist für e-Mail-Dokument Suchergebnisse optimiert, die Auszüge enthalten.</span><span class="sxs-lookup"><span data-stu-id="0465c-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="0465c-137">Es verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="0465c-137">It has the following specifications:</span></span>

-   <span data-ttu-id="0465c-138">Zeilen: 4</span><span class="sxs-lookup"><span data-stu-id="0465c-138">Rows: 4</span></span>
-   <span data-ttu-id="0465c-139">Eigenschaften: 5</span><span class="sxs-lookup"><span data-stu-id="0465c-139">Properties: 5</span></span>
-   <span data-ttu-id="0465c-140">Das Beta Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0465c-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Das Diagramm zeigt ein Beispiel für ein Beta Layout.](images/content-view/layout3.png)

-   <span data-ttu-id="0465c-142">Die folgende Abbildung zeigt das Beta Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Screenshot, der ein Beta-Layoutbeispiel für e-Mail anzeigt.](images/content-view/betaviewmore.png)

-   <span data-ttu-id="0465c-144">Die folgende Abbildung zeigt das Beta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Das Diagramm zeigt ein Beispiel für einen Beta-Layout mit weniger als 350 Pixeln horizontaler Leerraum.](images/content-view/layout4.png)

-   <span data-ttu-id="0465c-146">Die folgende Abbildung zeigt das Beta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt:</span><span class="sxs-lookup"><span data-stu-id="0465c-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![Beispiel für das Beta Layout](images/content-view/betaviewless.png)

<span data-ttu-id="0465c-148">**Gamma Layout**</span><span class="sxs-lookup"><span data-stu-id="0465c-148">**Gamma Layout**</span></span>

<span data-ttu-id="0465c-149">Das Gamma Layout-Muster ähnelt Alpha, verwendet aber ein zweizeilige Layout anstelle von vier.</span><span class="sxs-lookup"><span data-stu-id="0465c-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="0465c-150">Dieses Layout eignet sich ideal für Szenarien, in denen Sie einen Ausschnitt sehen möchten, aber mehr Elemente auf dem Bildschirm anpassen möchten, oder für Dateitypen, die weniger Speicherplatz benötigen, um die kritischsten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0465c-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="0465c-151">Das Gamma Layout verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="0465c-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="0465c-152">Zeilen: 2</span><span class="sxs-lookup"><span data-stu-id="0465c-152">Rows: 2</span></span>
-   <span data-ttu-id="0465c-153">Eigenschaften: 4</span><span class="sxs-lookup"><span data-stu-id="0465c-153">Properties: 4</span></span>
-   <span data-ttu-id="0465c-154">Die folgende Abbildung zeigt das Gamma Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagramm, das ein Beispiel für ein Gamma Layout anzeigt.](images/content-view/layout5.png)

-   <span data-ttu-id="0465c-156">Die folgende Abbildung zeigt das Gamma Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Screenshot, der ein Gamma Layout-Beispiel für ein Prüfliste-Element zeigt.](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="0465c-158">Die folgende Abbildung zeigt das Gamma Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Das Diagramm zeigt ein Beispiel für ein Gamma Layout mit weniger als 350 Pixeln horizontaler Leerraum.](images/content-view/layout6.png)

-   <span data-ttu-id="0465c-160">Beispiel für das Gamma Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Beispiel für Gamma Layout](images/content-view/gammaviewless.png)

<span data-ttu-id="0465c-162">**Delta Layout**</span><span class="sxs-lookup"><span data-stu-id="0465c-162">**Delta Layout**</span></span>

<span data-ttu-id="0465c-163">Das Delta Layoutmuster ist für die Anzeige zahlreicher kürzerer Eigenschaften wie z. b. für Musik und Bilder optimiert.</span><span class="sxs-lookup"><span data-stu-id="0465c-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="0465c-164">Es verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="0465c-164">It has the following specifications:</span></span>

-   <span data-ttu-id="0465c-165">Zeilen: 2</span><span class="sxs-lookup"><span data-stu-id="0465c-165">Rows: 2</span></span>
-   <span data-ttu-id="0465c-166">Eigenschaften: 6</span><span class="sxs-lookup"><span data-stu-id="0465c-166">Properties: 6</span></span>
-   <span data-ttu-id="0465c-167">Delta Layout, wenn das Element über 700 Pixel oder mehr horizontalen Leerraum verfügt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0465c-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagramm, das ein Delta Layoutbeispiel zeigt.](images/content-view/layout7.png)

-   <span data-ttu-id="0465c-169">Beispiel für das Delta Layout, wenn das Element über 700 Pixel oder mehr horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![Screenshot, der ein Delta Layout-Beispiel für eine Musikdatei zeigt.](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="0465c-171">Delta Layout, wenn das Element zwischen 350 und 700 Pixel horizontalen Leerraum aufweist.</span><span class="sxs-lookup"><span data-stu-id="0465c-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Diagramm, das ein Delta Layoutbeispiel anzeigt, das zwischen 350 und 700 Pixel horizontalen Leerraum enthält.](images/content-view/layout8.png)

-   <span data-ttu-id="0465c-173">Beispiel für das Delta Layout, wenn das Element zwischen 350 und 700 Pixel horizontalen Leerraum liegt.</span><span class="sxs-lookup"><span data-stu-id="0465c-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Beispiel für Delta Layout](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="0465c-175">Delta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Layoutbeispiel](images/content-view/layout9.png)

-   <span data-ttu-id="0465c-177">Beispiel für das Delta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.</span><span class="sxs-lookup"><span data-stu-id="0465c-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Screenshot, der ein Delta Layoutbeispiel für eine Musikdatei mit weniger als 350 Pixeln horizontaler Leerraum zeigt.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="0465c-179">Schritt 3: Registrieren von benutzerdefinierten Eigenschaften und Layout für Ihren Dateityp</span><span class="sxs-lookup"><span data-stu-id="0465c-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="0465c-180">Nachdem Sie den Suchergebnis Modus, den Durchsuchenmodus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaften Liste für den Dateityp registrieren.</span><span class="sxs-lookup"><span data-stu-id="0465c-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="0465c-181">**, Um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.**</span><span class="sxs-lookup"><span data-stu-id="0465c-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="0465c-182">Wählen Sie aus den vier layoutmustern: Alpha, Beta, Gamma oder Delta.</span><span class="sxs-lookup"><span data-stu-id="0465c-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="0465c-183">Berücksichtigen Sie die folgenden Formatierungs Regeln, die gleichermaßen für alle vier Layoutmuster gelten:</span><span class="sxs-lookup"><span data-stu-id="0465c-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="0465c-184">Eigenschaft 1 wird immer in einer größeren Schriftgröße angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0465c-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="0465c-185">Der Umfang der großen Schriftart, der in der Regel für den Elementnamen verwendet wird, aber auch für den Anker oder eine andere Element Eigenschaft verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0465c-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="0465c-186">Eigenschaft 4 ist für Ausschnitte in den Alpha-, Beta-und Gamma layoutmustern vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0465c-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="0465c-187">Dieser Eigenschaft wird mehr Platz in diesen Mustern zugewiesen, und Sie wird in einer grauen Schriftfarbe angezeigt, im Gegensatz zu den anderen Eigenschaften, um Sie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0465c-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="0465c-188">Die unten angegebenen Pixel Messungen liegen in relativen Pixeln vor, und die Größe enthält das Symbol/die Miniaturansicht links neben den Eigenschaften und das Leerzeichen zwischen Symbol/Miniaturansicht und Auswahl Rechteck.</span><span class="sxs-lookup"><span data-stu-id="0465c-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="0465c-189">Die meisten Eigenschaften verfügen über eine minimale Anzeige Größe.</span><span class="sxs-lookup"><span data-stu-id="0465c-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="0465c-190">Aus diesem Grund werden Sie nicht angezeigt, wenn auf einer bestimmten Ansichts Größe nicht genügend Speicherplatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0465c-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="0465c-191">Die minimale Größe ist normalerweise 100 Pixel breit.</span><span class="sxs-lookup"><span data-stu-id="0465c-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="0465c-192">Jedes Layoutmuster definiert die Anzahl der Zeilen und die Anzahl der Eigenschaften in jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="0465c-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="0465c-193">Entscheiden Sie, welche Eigenschaften im Layout angezeigt werden sollen und welche Eigenschaft Sie an jedem Speicherort anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="0465c-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="0465c-194">Berücksichtigen Sie bei der Entscheidung, welche Eigenschaft an jeder Position im Layout angezeigt werden soll, die typische Länge der Eigenschaft, ihre Wichtigkeit für den Benutzer und ob Sie gelöscht werden soll, wenn die Fenstergröße zu klein ist, um alle Eigenschaften zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="0465c-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="0465c-195">Registrieren Sie ein Layoutmuster und eine Eigenschaften Liste für Ihren Dateityp oder Elementtyp, indem Sie die folgenden Schlüssel unter dem ProgID-Registrierungsschlüssel für den Dateityp oder das Element hinzufügen (in diesem Beispiel für den Dateityp ". xyz").</span><span class="sxs-lookup"><span data-stu-id="0465c-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="0465c-196">Beachten Sie die folgenden Formatierungs Richtlinien zum Registrieren von Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0465c-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="0465c-197">Jede Registrierung beginnt mit `prop:`</span><span class="sxs-lookup"><span data-stu-id="0465c-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="0465c-198">Jede Eigenschaft erfordert den vollständigen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="0465c-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="0465c-199">Eigenschaften werden durch ein Semikolon ohne Leerzeichen voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="0465c-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="0465c-200">Eigenschaften werden in der Reihenfolge angezeigt, in der das ausgewählte Layoutmuster definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0465c-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="0465c-201">`~` Gibt an, dass die Eigenschaften Bezeichnung nicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0465c-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="0465c-202">`~System.LayoutPattern.PlaceHolder` sollte verwendet werden, wenn Sie eine im Layoutmuster angegebene Eigenschaft leer lassen möchten.</span><span class="sxs-lookup"><span data-stu-id="0465c-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="0465c-203">Der folgende Beispiel Registrierungsschlüssel veranschaulicht diese Formatierungs Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="0465c-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="0465c-204">Mögliche Werte für (contentviewmodeforbrowse) umfassen Folgendes: Prop: ~ System. itemnamedisplay; System. Author; System. layoutpattern. Platzhalter; System. Keywords; System. DateModified; ~ System. Size</span><span class="sxs-lookup"><span data-stu-id="0465c-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="0465c-205">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0465c-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0465c-206">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0465c-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0465c-207">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="0465c-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="0465c-208">Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="0465c-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="0465c-209">System. proplist. contentviewmodeforbrowse</span><span class="sxs-lookup"><span data-stu-id="0465c-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="0465c-210">System. proplist. contentviewmodeforsearch</span><span class="sxs-lookup"><span data-stu-id="0465c-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
