---
description: ICE92 überprüft, ob eine Komponente ohne Komponenten-ID-GUID nicht auch als permanente Komponente angegeben wird.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866088"
---
# <a name="ice92"></a><span data-ttu-id="5bd14-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="5bd14-103">ICE92</span></span>

<span data-ttu-id="5bd14-104">ICE92 überprüft, ob eine Komponente ohne Komponenten-ID-GUID nicht auch als permanente Komponente angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bd14-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="5bd14-105">Diese benutzerdefinierte Ice-Aktion überprüft die Komponenten [Tabelle](component-table.md) auf Komponenten, die keine [GUID](guid.md) im Feld "ComponentId" aufweisen, und überprüft, ob das **msidbcomponentattributespermanent** -Flag im Feld "Attribute" nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5bd14-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="5bd14-106">ICE92 überprüft auch, ob keine Komponente sowohl das **msidbcomponentattributespermanent** -Attribut als auch das **msidbcomponentattributesuninstallonabgelöst** -Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="5bd14-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="5bd14-107">Wenn die ComponentID-Spalte NULL ist, registriert das Installationsprogramm die Komponente nicht, und die Komponente kann vom Installationsprogramm nicht entfernt oder repariert werden.</span><span class="sxs-lookup"><span data-stu-id="5bd14-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="5bd14-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="5bd14-108">Result</span></span>

<span data-ttu-id="5bd14-109">ICE92 gibt den folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="5bd14-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="5bd14-110">ICE92-Fehler</span><span class="sxs-lookup"><span data-stu-id="5bd14-110">ICE92 error</span></span>                                                          | <span data-ttu-id="5bd14-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5bd14-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd14-112">Die Komponente ' \[ 1 \] ' weist keine ComponentID auf und ist als permanent gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="5bd14-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="5bd14-113">Der Eintrag für diese Komponente in der Component-Tabelle weist in der ComponentID-Spalte den Wert NULL auf und weist **msidbcomponentattributespermanent** in der Spalte Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="5bd14-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="5bd14-114">ICE92 gibt die folgende Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="5bd14-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="5bd14-115">ICE92-Warnung</span><span class="sxs-lookup"><span data-stu-id="5bd14-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="5bd14-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5bd14-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd14-117">Die Komponente " \[ 1 \] " ist als permanent gekennzeichnet und wird bei der Deinstallation deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="5bd14-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="5bd14-118">Das Uninstall-on-Ablösung-Attribut wird ignoriert, da die Komponente permanent ist.</span><span class="sxs-lookup"><span data-stu-id="5bd14-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="5bd14-119">Der Eintrag für diese Komponente in der [Komponenten Tabelle](component-table.md) enthält sowohl das **msidbcomponentattributespermanente** -Attribut als auch das **msidbcomponentattributesuninstallonabgelöst** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="5bd14-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="5bd14-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5bd14-120">Example</span></span>

<span data-ttu-id="5bd14-121">ICE92 meldet den folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5bd14-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="5bd14-122">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="5bd14-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5bd14-123">Komponente</span><span class="sxs-lookup"><span data-stu-id="5bd14-123">Component</span></span>  | <span data-ttu-id="5bd14-124">ComponentID</span><span class="sxs-lookup"><span data-stu-id="5bd14-124">ComponentId</span></span> | <span data-ttu-id="5bd14-125">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="5bd14-125">Directory\_</span></span> | <span data-ttu-id="5bd14-126">Attribute</span><span class="sxs-lookup"><span data-stu-id="5bd14-126">Attributes</span></span> | <span data-ttu-id="5bd14-127">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="5bd14-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="5bd14-128">Component1</span><span class="sxs-lookup"><span data-stu-id="5bd14-128">Component1</span></span> |             | <span data-ttu-id="5bd14-129">Directoren</span><span class="sxs-lookup"><span data-stu-id="5bd14-129">DirectoryA</span></span>  | <span data-ttu-id="5bd14-130">16</span><span class="sxs-lookup"><span data-stu-id="5bd14-130">16</span></span>         | <span data-ttu-id="5bd14-131">Mit der</span><span class="sxs-lookup"><span data-stu-id="5bd14-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="5bd14-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5bd14-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bd14-133">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="5bd14-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



