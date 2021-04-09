---
description: Qualifizierte Komponenten sind eine dereferenzierungsmethode und können verwendet werden, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Verwenden qualifizierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129357"
---
# <a name="using-qualified-components"></a><span data-ttu-id="2e21e-103">Verwenden qualifizierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="2e21e-103">Using Qualified Components</span></span>

<span data-ttu-id="2e21e-104">Qualifizierte Komponenten sind eine dereferenzierungsmethode und können verwendet werden, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="2e21e-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="2e21e-105">Um den vollständigen Pfad zurückzugeben und eine [qualifizierte Komponente](qualified-components.md)zu installieren, nennen Sie [**msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) oder [**msiprovidequalifiedcomponstex**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span><span class="sxs-lookup"><span data-stu-id="2e21e-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="2e21e-106">Um alle qualifizierten Komponenten Qualifizierer und beschreibenden Zeichen folgen aufzulisten, müssen Sie [**msienumcomponentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2e21e-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="2e21e-107">**So gruppieren Sie Komponenten in einer Kategorie qualifizierter Komponenten**</span><span class="sxs-lookup"><span data-stu-id="2e21e-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="2e21e-108">In der [Komponenten Tabelle](component-table.md) muss für jede Komponente, die in der neuen Kategorie qualifizierter Komponenten enthalten ist, ein Datensatz vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2e21e-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="2e21e-109">Erstellen Sie die Felder in der Komponenten Tabelle wie für normale Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2e21e-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="2e21e-110">Beachten Sie, dass für jede qualifizierte Komponente eine eindeutige GUID für die Komponenten-ID in der Spalte ComponentID der Komponenten Tabelle eingegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="2e21e-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="2e21e-111">Generiert eine Qualifiziererzeichenfolge für jede qualifizierte Komponente.</span><span class="sxs-lookup"><span data-stu-id="2e21e-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="2e21e-112">Der Qualifizierer muss eine eindeutige Text Zeichenfolge sein, die bei der Suche nach einer qualifizierten Komponente problemlos generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e21e-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="2e21e-113">Wenn z. b. die Komponenten in der Kategorie durch Sprache qualifiziert werden, ist der numerische Gebiets Schema Bezeichner (Locale Identifier, LCID) eine sinnvolle Qualifiziererzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2e21e-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="2e21e-114">Fügen Sie für jede qualifizierte Komponente einen Datensatz in der [Tabelle PublishComponent](publishcomponent-table.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e21e-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="2e21e-115">Geben Sie die qualifizierten Komponenten Bezeichner aus der Spalte Komponente der Komponenten Tabelle in die Spalte Komponente \_ der Tabelle PublishComponent ein.</span><span class="sxs-lookup"><span data-stu-id="2e21e-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="2e21e-116">Geben Sie die Qualifiziererzeichenfolgen für jede qualifizierte Komponente in die qualifiziererspalte</span><span class="sxs-lookup"><span data-stu-id="2e21e-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="2e21e-117">Geben Sie eine lokalisierte Zeichenfolge ein, die dem Benutzer angezeigt werden soll, und beschreiben Sie die qualifizierte Komponente in der optionalen APPDATA-Spalte.</span><span class="sxs-lookup"><span data-stu-id="2e21e-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="2e21e-118">Eine erklärende Zeichenfolge sollte in das APPDATA-Feld eingefügt werden, z. b. "Französisch Wörterbuch", anstelle der numerischen LCID.</span><span class="sxs-lookup"><span data-stu-id="2e21e-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="2e21e-119">Geben Sie den Namen der Funktion ein, von der diese Komponente in der featurespalte verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2e21e-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="2e21e-120">Der Funktions Bezeichner in diesem Feld muss auch in der featurespalte der [Featuretabelle](feature-table.md)aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2e21e-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="2e21e-121">Generieren Sie eine Kategorie-GUID für diese Kategorie qualifizierter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2e21e-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="2e21e-122">Dies muss eine gültige [GUID](guid.md)sein.</span><span class="sxs-lookup"><span data-stu-id="2e21e-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="2e21e-123">Wenn Sie ein Hilfsprogramm wie GUIDGEN zum Generieren der GUID verwenden, müssen Sie sicherstellen, dass es nur Großbuchstaben enthält.</span><span class="sxs-lookup"><span data-stu-id="2e21e-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="2e21e-124">Geben Sie für jede qualifizierte Komponente in dieser Kategorie die Kategorie-GUID in das Feld ComponentID der [Tabelle PublishComponent](publishcomponent-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="2e21e-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="2e21e-125">Im folgenden Beispiel wird veranschaulicht, wie die Kategorie "Faxvorlagen" qualifizierter Komponenten in den Tabellen "Komponente", "Feature" und "PublishComponent" verfasst wird.</span><span class="sxs-lookup"><span data-stu-id="2e21e-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="2e21e-126">PublishComponent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="2e21e-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="2e21e-127">ComponentID</span><span class="sxs-lookup"><span data-stu-id="2e21e-127">ComponentId</span></span>                  | <span data-ttu-id="2e21e-128">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="2e21e-128">Qualifier</span></span> | <span data-ttu-id="2e21e-129">AppData</span><span class="sxs-lookup"><span data-stu-id="2e21e-129">AppData</span></span>             | <span data-ttu-id="2e21e-130">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="2e21e-130">Feature\_</span></span>   | <span data-ttu-id="2e21e-131">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="2e21e-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="2e21e-132">{Faxvorlagen Kategorie GUID}</span><span class="sxs-lookup"><span data-stu-id="2e21e-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="2e21e-133">1033</span><span class="sxs-lookup"><span data-stu-id="2e21e-133">1033</span></span>      | <span data-ttu-id="2e21e-134">US-englische Vorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-134">US English template</span></span> | <span data-ttu-id="2e21e-135">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-135">FAXTemplate</span></span> | <span data-ttu-id="2e21e-136">Faxtemplatedeu</span><span class="sxs-lookup"><span data-stu-id="2e21e-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="2e21e-137">1041</span><span class="sxs-lookup"><span data-stu-id="2e21e-137">1041</span></span>      | <span data-ttu-id="2e21e-138">Japanische Vorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-138">Japanese template</span></span>   | <span data-ttu-id="2e21e-139">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-139">FAXTemplate</span></span> | <span data-ttu-id="2e21e-140">Faxtemplatejpn</span><span class="sxs-lookup"><span data-stu-id="2e21e-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="2e21e-141">1054</span><span class="sxs-lookup"><span data-stu-id="2e21e-141">1054</span></span>      | <span data-ttu-id="2e21e-142">Thailändische Vorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-142">Thai template</span></span>       | <span data-ttu-id="2e21e-143">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-143">FAXTemplate</span></span> | <span data-ttu-id="2e21e-144">Faxtemplatetha</span><span class="sxs-lookup"><span data-stu-id="2e21e-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="2e21e-145">1031</span><span class="sxs-lookup"><span data-stu-id="2e21e-145">1031</span></span>      | <span data-ttu-id="2e21e-146">Deutsche Vorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-146">German template</span></span>     | <span data-ttu-id="2e21e-147">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-147">FAXTemplate</span></span> | <span data-ttu-id="2e21e-148">Faxtemplatedeu</span><span class="sxs-lookup"><span data-stu-id="2e21e-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="2e21e-149">[Komponenten Tabelle](component-table.md) (partielle Tabelle)</span><span class="sxs-lookup"><span data-stu-id="2e21e-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="2e21e-150">Komponente</span><span class="sxs-lookup"><span data-stu-id="2e21e-150">Component</span></span>      | <span data-ttu-id="2e21e-151">ComponentID</span><span class="sxs-lookup"><span data-stu-id="2e21e-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="2e21e-152">Faxtemplatedeu</span><span class="sxs-lookup"><span data-stu-id="2e21e-152">FAXTemplateENU</span></span> | <span data-ttu-id="2e21e-153">{*Faxvorlage (US-Englisch) Komponenten-GUID*}</span><span class="sxs-lookup"><span data-stu-id="2e21e-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="2e21e-154">Faxtemplatejpn</span><span class="sxs-lookup"><span data-stu-id="2e21e-154">FAXTemplateJPN</span></span> | <span data-ttu-id="2e21e-155">{*Faxvorlage (Japanisch) Komponenten-GUID*}</span><span class="sxs-lookup"><span data-stu-id="2e21e-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="2e21e-156">Faxtemplatetha</span><span class="sxs-lookup"><span data-stu-id="2e21e-156">FAXTemplateTHA</span></span> | <span data-ttu-id="2e21e-157">{*Faxvorlage (Thai)-Komponenten-GUID*}</span><span class="sxs-lookup"><span data-stu-id="2e21e-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="2e21e-158">Faxtemplatedeu</span><span class="sxs-lookup"><span data-stu-id="2e21e-158">FAXTemplateDEU</span></span> | <span data-ttu-id="2e21e-159">{*Faxvorlage (Deutsch), Komponenten-GUID*}</span><span class="sxs-lookup"><span data-stu-id="2e21e-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="2e21e-160">[Funktions Tabelle](feature-table.md) (partielle Tabelle)</span><span class="sxs-lookup"><span data-stu-id="2e21e-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="2e21e-161">Funktion</span><span class="sxs-lookup"><span data-stu-id="2e21e-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="2e21e-162">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-162">FAXTemplate</span></span> |
| <span data-ttu-id="2e21e-163">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-163">FAXTemplate</span></span> |
| <span data-ttu-id="2e21e-164">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-164">FAXTemplate</span></span> |
| <span data-ttu-id="2e21e-165">Faxvorlage</span><span class="sxs-lookup"><span data-stu-id="2e21e-165">FAXTemplate</span></span> |



 

 

 



