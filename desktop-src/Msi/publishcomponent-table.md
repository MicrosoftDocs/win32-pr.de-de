---
description: In der Tabelle PublishComponent werden die in der Component-Tabelle aufgeführten Komponenten mit einer qualifizierertextzeichenfolge und einer Kategorie-ID-GUID verknüpft.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: PublishComponent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349198"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="e9010-103">PublishComponent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e9010-103">PublishComponent Table</span></span>

<span data-ttu-id="e9010-104">In der Tabelle PublishComponent werden die in der [Component-Tabelle](component-table.md) aufgeführten Komponenten mit einer qualifizierertextzeichenfolge und einer Kategorie-ID-GUID verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e9010-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="e9010-105">Komponenten mit paralleler Funktionalität, die auf diese Weise gruppiert wurden, werden als qualifizierte Komponenten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9010-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="e9010-106">Siehe [qualifizierte Komponenten](qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="e9010-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="e9010-107">Dadurch erhält das Installationsprogramm eine Methode für eine Dereferenzierung auf einer einzelnen Ebene, wenn auf Komponenten verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e9010-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="e9010-108">Siehe [verwenden qualifizierter Komponenten](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="e9010-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="e9010-109">Die PublishComponent-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="e9010-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="e9010-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="e9010-110">Column</span></span>      | <span data-ttu-id="e9010-111">Typ</span><span class="sxs-lookup"><span data-stu-id="e9010-111">Type</span></span>                         | <span data-ttu-id="e9010-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e9010-112">Key</span></span> | <span data-ttu-id="e9010-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e9010-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e9010-114">ComponentID</span><span class="sxs-lookup"><span data-stu-id="e9010-114">ComponentId</span></span> | [<span data-ttu-id="e9010-115">GUID</span><span class="sxs-lookup"><span data-stu-id="e9010-115">GUID</span></span>](guid.md)             | <span data-ttu-id="e9010-116">J</span><span class="sxs-lookup"><span data-stu-id="e9010-116">Y</span></span>   | <span data-ttu-id="e9010-117">N</span><span class="sxs-lookup"><span data-stu-id="e9010-117">N</span></span>        |
| <span data-ttu-id="e9010-118">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="e9010-118">Qualifier</span></span>   | [<span data-ttu-id="e9010-119">Text</span><span class="sxs-lookup"><span data-stu-id="e9010-119">Text</span></span>](text.md)             | <span data-ttu-id="e9010-120">J</span><span class="sxs-lookup"><span data-stu-id="e9010-120">Y</span></span>   | <span data-ttu-id="e9010-121">N</span><span class="sxs-lookup"><span data-stu-id="e9010-121">N</span></span>        |
| <span data-ttu-id="e9010-122">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="e9010-122">Component\_</span></span> | [<span data-ttu-id="e9010-123">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e9010-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="e9010-124">J</span><span class="sxs-lookup"><span data-stu-id="e9010-124">Y</span></span>   | <span data-ttu-id="e9010-125">N</span><span class="sxs-lookup"><span data-stu-id="e9010-125">N</span></span>        |
| <span data-ttu-id="e9010-126">AppData</span><span class="sxs-lookup"><span data-stu-id="e9010-126">AppData</span></span>     | [<span data-ttu-id="e9010-127">Text</span><span class="sxs-lookup"><span data-stu-id="e9010-127">Text</span></span>](text.md)             | <span data-ttu-id="e9010-128">N</span><span class="sxs-lookup"><span data-stu-id="e9010-128">N</span></span>   | <span data-ttu-id="e9010-129">J</span><span class="sxs-lookup"><span data-stu-id="e9010-129">Y</span></span>        |
| <span data-ttu-id="e9010-130">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="e9010-130">Feature\_</span></span>   | [<span data-ttu-id="e9010-131">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e9010-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="e9010-132">N</span><span class="sxs-lookup"><span data-stu-id="e9010-132">N</span></span>   | <span data-ttu-id="e9010-133">N</span><span class="sxs-lookup"><span data-stu-id="e9010-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e9010-134">Spalten</span><span class="sxs-lookup"><span data-stu-id="e9010-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e9010-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentID</span><span class="sxs-lookup"><span data-stu-id="e9010-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="e9010-136">Eine Zeichen folgen- [GUID](guid.md) , die die Kategorie der Komponenten darstellt, die gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9010-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="e9010-137">Beachten Sie, dass der Titel dieser Spalte irreführend ist.</span><span class="sxs-lookup"><span data-stu-id="e9010-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="e9010-138">Dies ist die GUID für die Kategorie qualifizierter Komponenten und ist nicht dieselbe GUID, die in der ComponentID-Spalte der [Component-Tabelle](component-table.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e9010-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="e9010-139">Hier bezieht es sich auf einen Server, der die Funktionalität einer Komponente für externe Clients anstelle der Komponente selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e9010-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="e9010-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Turnier</span><span class="sxs-lookup"><span data-stu-id="e9010-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="e9010-141">Eine Text Zeichenfolge, die den Wert in der ComponentID-Spalte qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="e9010-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="e9010-142">Ein Qualifizierer wird verwendet, um mehrere Formen derselben Komponente, z. b. eine Komponente, die in mehreren Sprachen implementiert ist, zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e9010-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="e9010-143">Dabei handelt es sich um die von [**msienbicomponentqualifier**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)zurückgegebenen qualifizierertextzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e9010-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="e9010-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="e9010-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e9010-145">Externer Schlüssel in Spalte 1 der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9010-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="e9010-146">Dieser Bezeichner verweist auf den Daten Satz der qualifizierten Komponente in der Component-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e9010-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="e9010-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>APPDATA</span><span class="sxs-lookup"><span data-stu-id="e9010-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="e9010-148">Ein optionaler Lokalisier barer Text, der die qualifizierte Komponente dieses Datensatzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e9010-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="e9010-149">Die Zeichenfolge wird häufig von der Anwendung analysiert und kann dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e9010-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="e9010-150">Die qualifizierte Komponente sollte beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e9010-150">It should describe the qualified component.</span></span> <span data-ttu-id="e9010-151">Dies kann mit [**msienumschlag componentqualifizierern**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e9010-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="e9010-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="e9010-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="e9010-153">Externer Schlüssel in Spalte 1 der [Featuretabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9010-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="e9010-154">Dies ist das Feature, das diese qualifizierte Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9010-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9010-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9010-155">Remarks</span></span>

<span data-ttu-id="e9010-156">Auf diese Tabelle wird verwiesen, wenn die [PublishComponents-Aktion](publishcomponents-action.md) oder die [unpublishcomponents-Aktion](unpublishcomponents-action.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9010-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="e9010-157">Beachten Sie, dass der Name dieser Tabelle irreführend ist.</span><span class="sxs-lookup"><span data-stu-id="e9010-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="e9010-158">Diese Tabelle ist nicht erforderlich, um Ankündigungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9010-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="e9010-159">Informationen dazu, wie Sie den Installationsstatus von Komponenten für die Ankündigung festlegen, finden Sie in der Spalte Attribute der [Komponenten Tabelle](component-table.md) und [Funktions Tabelle](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e9010-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="e9010-160">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e9010-160">Validation</span></span>

<dl>

[<span data-ttu-id="e9010-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="e9010-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e9010-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="e9010-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e9010-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="e9010-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="e9010-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="e9010-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="e9010-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="e9010-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



