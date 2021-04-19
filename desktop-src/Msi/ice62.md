---
description: ICE62 führt umfassende Prüfungen der isolatedcomponent-Tabelle für Daten aus, die zu unerwartetem Verhalten führen können.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368871"
---
# <a name="ice62"></a><span data-ttu-id="2c08c-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="2c08c-103">ICE62</span></span>

<span data-ttu-id="2c08c-104">ICE62 führt umfassende Prüfungen der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) für Daten aus, die zu unerwartetem Verhalten führen können.</span><span class="sxs-lookup"><span data-stu-id="2c08c-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="2c08c-105">Wenn ein von ICE62 gemeldeter Fehler nicht behoben werden kann, kann dies zu einem Ausfall des isolierten Komponenten Systems auf unterschiedlichste Weise führen.</span><span class="sxs-lookup"><span data-stu-id="2c08c-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="2c08c-106">Wenn z. b. das shareddllrefcount-Bit nicht für eine freigegebene Komponente festgelegt ist, kann die Registrierung für die Komponente entfernt werden, wenn eine andere Anwendung diese ComponentID verwendet und deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="2c08c-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="2c08c-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="2c08c-107">Result</span></span>

<span data-ttu-id="2c08c-108">ICE62 gibt eine Warnung oder einen Fehler aus, wenn Daten in der isolatedcomponent-Tabelle gefunden werden, die möglicherweise zu unerwartetem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="2c08c-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="2c08c-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c08c-109">Example</span></span>

<span data-ttu-id="2c08c-110">ICE62 meldet die folgenden Fehler und Warnungen für die gezeigten Beispiele.</span><span class="sxs-lookup"><span data-stu-id="2c08c-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="2c08c-111">Component2 wird als Anwendungs Komponente zur Isolation von Component1 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c08c-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="2c08c-112">Allerdings verfügt Component2 über einen Registrierungsschlüssel Pfad und stellt keinen gültigen ausführbaren Pfad zur Verfügung, der zum Isolieren der Komponente verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c08c-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="2c08c-113">Um diesen Fehler zu beheben, verwenden Sie eine andere Komponente als Anwendung für die isolierte Komponente Component1.</span><span class="sxs-lookup"><span data-stu-id="2c08c-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="2c08c-114">Component1 wird als isolierte freigegebene Komponente aufgelistet, aber das shareddllrefcount-Bit ist nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2c08c-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="2c08c-115">Dies könnte dazu führen, dass die Lebensdauer der Komponente falsch ist.</span><span class="sxs-lookup"><span data-stu-id="2c08c-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="2c08c-116">Wenn eine andere Anwendung diese Komponente verwendet (isoliert oder nicht) und deinstalliert wird, wird die Registrierung für die Komponente entfernt, aber die isolierte Kopie dieser Anwendung bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c08c-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="2c08c-117">Dies verursacht Probleme beim Reparieren und deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="2c08c-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="2c08c-118">Um diesen Fehler zu beheben, legen Sie das shareddllrefcount-Bit für die Komponente fest.</span><span class="sxs-lookup"><span data-stu-id="2c08c-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="2c08c-119">Component1 und Component2 werden von unterschiedlichen Funktionen installiert.</span><span class="sxs-lookup"><span data-stu-id="2c08c-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="2c08c-120">Component1 wird von Feature1 installiert, und Component2 wird von Feature2 installiert.</span><span class="sxs-lookup"><span data-stu-id="2c08c-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="2c08c-121">Feature1 ist kein übergeordnetes Element von Feature2. Daher ist es möglich, dass die Anwendung installiert wird, jedoch nicht die isolierte Komponente, wodurch die Isolation unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="2c08c-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="2c08c-122">Um diesen Fehler zu beheben, fügen Sie der FeatureComponents-Tabelle einen Eintrag hinzu, der Component1 mit derselben Funktion wie (oder einem übergeordneten Feature von) der Funktion, die Component2 installiert, verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2c08c-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="2c08c-123">Component1 weist eine Bedingung in der Komponenten Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="2c08c-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="2c08c-124">Wenn sich diese Bedingung während der Lebensdauer einer Installation auf einem Computer von true in false ändert, ist die isolierte Komponente möglicherweise ohne Registrierungsinformationen verwaist.</span><span class="sxs-lookup"><span data-stu-id="2c08c-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="2c08c-125">Um diese Warnung zu beheben, entfernen Sie die Bedingung, oder erstellen Sie die Bedingung so, dass Sie nie von true in false geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c08c-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="2c08c-126">Component1 ist für Component2 und Component3 isoliert, und die beiden Komponenten werden ebenfalls im gleichen Verzeichnis installiert.</span><span class="sxs-lookup"><span data-stu-id="2c08c-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="2c08c-127">Die Anwendungen haben eine isolierte Komponente gemeinsam, aber wenn eine Anwendung entfernt wird, wird die freigegebene Komponente ebenfalls entfernt, sodass die anderen Anwendungen die isolierte Komponente verlieren.</span><span class="sxs-lookup"><span data-stu-id="2c08c-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="2c08c-128">Um diese Warnung zu beheben, installieren Sie die Anwendungen in verschiedenen Verzeichnissen, oder überprüfen Sie, ob für einige der Anwendungen tatsächlich eine isolierte Komponente erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2c08c-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="2c08c-129">Isolatedcomponent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="2c08c-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="2c08c-130">Frei \_ gegebene Komponente</span><span class="sxs-lookup"><span data-stu-id="2c08c-130">Component\_Shared</span></span> | <span data-ttu-id="2c08c-131">Komponenten \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="2c08c-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="2c08c-132">Component1</span><span class="sxs-lookup"><span data-stu-id="2c08c-132">Component1</span></span>        | <span data-ttu-id="2c08c-133">Component2</span><span class="sxs-lookup"><span data-stu-id="2c08c-133">Component2</span></span>             |
| <span data-ttu-id="2c08c-134">Component1</span><span class="sxs-lookup"><span data-stu-id="2c08c-134">Component1</span></span>        | <span data-ttu-id="2c08c-135">Component3</span><span class="sxs-lookup"><span data-stu-id="2c08c-135">Component3</span></span>             |



 

[<span data-ttu-id="2c08c-136">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="2c08c-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="2c08c-137">Komponente</span><span class="sxs-lookup"><span data-stu-id="2c08c-137">Component</span></span>  | <span data-ttu-id="2c08c-138">ComponentID</span><span class="sxs-lookup"><span data-stu-id="2c08c-138">ComponentId</span></span> | <span data-ttu-id="2c08c-139">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="2c08c-139">Directory\_</span></span> | <span data-ttu-id="2c08c-140">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c08c-140">Attributes</span></span> | <span data-ttu-id="2c08c-141">Bedingung</span><span class="sxs-lookup"><span data-stu-id="2c08c-141">Condition</span></span>   | <span data-ttu-id="2c08c-142">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="2c08c-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="2c08c-143">Component1</span><span class="sxs-lookup"><span data-stu-id="2c08c-143">Component1</span></span> |             | <span data-ttu-id="2c08c-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="2c08c-144">Dir1</span></span>        | <span data-ttu-id="2c08c-145">0</span><span class="sxs-lookup"><span data-stu-id="2c08c-145">0</span></span>          | <span data-ttu-id="2c08c-146">MyCondition</span><span class="sxs-lookup"><span data-stu-id="2c08c-146">MYCONDITION</span></span> | <span data-ttu-id="2c08c-147">Datei1</span><span class="sxs-lookup"><span data-stu-id="2c08c-147">File1</span></span>     |
| <span data-ttu-id="2c08c-148">Component2</span><span class="sxs-lookup"><span data-stu-id="2c08c-148">Component2</span></span> |             | <span data-ttu-id="2c08c-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="2c08c-149">TARGETDIR</span></span>   | <span data-ttu-id="2c08c-150">4</span><span class="sxs-lookup"><span data-stu-id="2c08c-150">4</span></span>          |             | <span data-ttu-id="2c08c-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="2c08c-151">Registry2</span></span> |
| <span data-ttu-id="2c08c-152">Component3</span><span class="sxs-lookup"><span data-stu-id="2c08c-152">Component3</span></span> |             | <span data-ttu-id="2c08c-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="2c08c-153">TARGETDIR</span></span>   | <span data-ttu-id="2c08c-154">0</span><span class="sxs-lookup"><span data-stu-id="2c08c-154">0</span></span>          |             | <span data-ttu-id="2c08c-155">Datei3</span><span class="sxs-lookup"><span data-stu-id="2c08c-155">File3</span></span>     |



 

[<span data-ttu-id="2c08c-156">Featurecomponentstable</span><span class="sxs-lookup"><span data-stu-id="2c08c-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="2c08c-157">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="2c08c-157">Feature\_</span></span> | <span data-ttu-id="2c08c-158">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="2c08c-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="2c08c-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="2c08c-159">Feature1</span></span>  | <span data-ttu-id="2c08c-160">Component1</span><span class="sxs-lookup"><span data-stu-id="2c08c-160">Component1</span></span>  |
| <span data-ttu-id="2c08c-161">Feature2</span><span class="sxs-lookup"><span data-stu-id="2c08c-161">Feature2</span></span>  | <span data-ttu-id="2c08c-162">Component2</span><span class="sxs-lookup"><span data-stu-id="2c08c-162">Component2</span></span>  |
| <span data-ttu-id="2c08c-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="2c08c-163">Feature1</span></span>  | <span data-ttu-id="2c08c-164">Component3</span><span class="sxs-lookup"><span data-stu-id="2c08c-164">Component3</span></span>  |



 

<span data-ttu-id="2c08c-165">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="2c08c-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="2c08c-166">Funktion</span><span class="sxs-lookup"><span data-stu-id="2c08c-166">Feature</span></span>  | <span data-ttu-id="2c08c-167">Über \_ geordnetes Element</span><span class="sxs-lookup"><span data-stu-id="2c08c-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="2c08c-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="2c08c-168">Feature1</span></span> |                 |
| <span data-ttu-id="2c08c-169">Feature2</span><span class="sxs-lookup"><span data-stu-id="2c08c-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="2c08c-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c08c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c08c-171">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="2c08c-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



