---
description: ICE61 überprüft die upgradetabelle einer Windows Installer Datenbank.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357897"
---
# <a name="ice61"></a><span data-ttu-id="f48cb-103">ICE61</span><span class="sxs-lookup"><span data-stu-id="f48cb-103">ICE61</span></span>

<span data-ttu-id="f48cb-104">ICE61 prüft die upgradetabelle, um sicherzustellen, dass die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="f48cb-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="f48cb-105">Alle Eigenschaften von "aktionproperty" sind in der Eigenschaften Tabelle nicht vorgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="f48cb-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="f48cb-106">Alle Eigenschaften von "aktionproperty" sind öffentliche Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f48cb-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="f48cb-107">Alle Eigenschaften von "aktionproperty" sind in der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="f48cb-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="f48cb-108">Alle Eigenschaften von "aktionproperty" sind für jeden Datensatz in der upgradetabelle eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f48cb-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="f48cb-109">Alle versionmax-Werte sind nicht kleiner als die entsprechenden versionmin-Werte.</span><span class="sxs-lookup"><span data-stu-id="f48cb-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="f48cb-110">Versionmin-und versionmax-Werte sind gültige Produktversionen.</span><span class="sxs-lookup"><span data-stu-id="f48cb-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="f48cb-111">Das gültige Format der Produktversion finden Sie unter der [**ProductVersion**](productversion.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f48cb-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="f48cb-112">Es wird nicht versucht, eine neuere oder gleiche Version des aktuellen Produkts zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f48cb-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="f48cb-113">Wenn eine Warnung oder ein Fehler, der von ICE61 gemeldet wird, nicht behoben wird, führt dies im Allgemeinen zu Problemen beim Upgrade Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="f48cb-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="f48cb-114">Je nach dem genauen Fehler kann es daran liegen, Dateien von der älteren Version zu schließen, Dateien aus der älteren Version zu löschen, auch wenn Sie von der neuen Anwendung benötigt werden, oder das Upgrade abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f48cb-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="f48cb-115">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f48cb-115">Result</span></span>

<span data-ttu-id="f48cb-116">ICE61 gibt eine Warnung oder einen Fehler aus, wenn eine der oben genannten Bedingungen nicht erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="f48cb-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="f48cb-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f48cb-117">Example</span></span>

<span data-ttu-id="f48cb-118">ICE61 meldet die folgenden Fehler und Warnungen für die gezeigten Beispiele.</span><span class="sxs-lookup"><span data-stu-id="f48cb-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="f48cb-119">In diesem Fall würde die erste Zeile versuchen, ein Produkt derselben Version zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f48cb-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="f48cb-120">(Die versionmax-Spalte ist gleich der Produktversion in der Eigenschaften Tabelle).</span><span class="sxs-lookup"><span data-stu-id="f48cb-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="f48cb-121">Um diesen Fehler zu beheben, verwenden Sie eine Version in der versionmax-Spalte, die niedriger als die in der Eigenschaften Tabelle angegebene aktuelle Version ist.</span><span class="sxs-lookup"><span data-stu-id="f48cb-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="f48cb-122">Entfernen Sie das Bit **msidbupgradeattributesversionmaxinclusive** aus der Spalte Attribute, wenn versionmax gleich der aktuellen Version ist.</span><span class="sxs-lookup"><span data-stu-id="f48cb-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="f48cb-123">Wenn die Absicht lediglich ist, das Produkt zu erkennen und nicht zu entfernen, wird dieser Fehler auch durch Hinzufügen des **msidbupgraentattributesonlydetect** -Bits zur Spalte Attribute behoben.</span><span class="sxs-lookup"><span data-stu-id="f48cb-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="f48cb-124">Wenn die Eigenschaft nicht in der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft aufgeführt ist, wird die-Eigenschaft nicht an die Serverseite der Installation übergeben, wenn die-Eigenschaft gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f48cb-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="f48cb-125">Um diesen Fehler zu beheben, fügen Sie [**securecustomproperties**](securecustomproperties.md)die Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="f48cb-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="f48cb-126">Upgradeeigenschaften müssen öffentliche Eigenschaften sein, damit das Ergebnis an die Serverseite der Installation übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f48cb-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="f48cb-127">Um diesen Fehler zu beheben, verwenden Sie alle Großbuchstaben im Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="f48cb-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="f48cb-128">Eine Eigenschaft kann nur in einer Zeile der upgradetabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f48cb-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="f48cb-129">Um diesen Fehler zu beheben, verwenden Sie eine andere Eigenschaft für die zweite Zeile.</span><span class="sxs-lookup"><span data-stu-id="f48cb-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="f48cb-130">Die Mindestversion muss kleiner als die maximale Version sein.</span><span class="sxs-lookup"><span data-stu-id="f48cb-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="f48cb-131">Um diesen Fehler zu beheben, überprüfen Sie die Versionsnummern für Typos.</span><span class="sxs-lookup"><span data-stu-id="f48cb-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="f48cb-132">Wenn Sie richtig sind und Sie den Bereich zwischen den beiden Versionen verwenden möchten, können Sie Sie so ändern, dass versionmin kleiner als versionmax ist.</span><span class="sxs-lookup"><span data-stu-id="f48cb-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="f48cb-133">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="f48cb-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="f48cb-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f48cb-134">Property</span></span>                                                 | <span data-ttu-id="f48cb-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f48cb-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="f48cb-136">**UpgradeCode auch**</span><span class="sxs-lookup"><span data-stu-id="f48cb-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="f48cb-137">{61aa4c55-e17f-11d2-93bb-0060089a76db}</span><span class="sxs-lookup"><span data-stu-id="f48cb-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="f48cb-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="f48cb-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="f48cb-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="f48cb-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="f48cb-140">**Securecustomproperties**</span><span class="sxs-lookup"><span data-stu-id="f48cb-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="f48cb-141">Oldappfound</span><span class="sxs-lookup"><span data-stu-id="f48cb-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="f48cb-142">Upgradetabelle</span><span class="sxs-lookup"><span data-stu-id="f48cb-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="f48cb-143">UpgradeCode auch</span><span class="sxs-lookup"><span data-stu-id="f48cb-143">UpgradeCode</span></span>                            | <span data-ttu-id="f48cb-144">Versionmin</span><span class="sxs-lookup"><span data-stu-id="f48cb-144">VersionMin</span></span> | <span data-ttu-id="f48cb-145">Versionmax</span><span class="sxs-lookup"><span data-stu-id="f48cb-145">VersionMax</span></span> | <span data-ttu-id="f48cb-146">Sprache</span><span class="sxs-lookup"><span data-stu-id="f48cb-146">Language</span></span> | <span data-ttu-id="f48cb-147">Attribute</span><span class="sxs-lookup"><span data-stu-id="f48cb-147">Attributes</span></span> | <span data-ttu-id="f48cb-148">Entfernen</span><span class="sxs-lookup"><span data-stu-id="f48cb-148">Remove</span></span>                | <span data-ttu-id="f48cb-149">Aktions Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f48cb-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="f48cb-150">{61aa4c55-e17f-11d2-93bb-0060089a76db}</span><span class="sxs-lookup"><span data-stu-id="f48cb-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="f48cb-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="f48cb-151">2.01.0000</span></span>  |          | <span data-ttu-id="f48cb-152">513</span><span class="sxs-lookup"><span data-stu-id="f48cb-152">513</span></span>        |                       | <span data-ttu-id="f48cb-153">Oldappfound</span><span class="sxs-lookup"><span data-stu-id="f48cb-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="f48cb-154">{61aa4c55-e17f-11d2-93bb-0060089a76db}</span><span class="sxs-lookup"><span data-stu-id="f48cb-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="f48cb-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="f48cb-155">2.01.0001</span></span>  | <span data-ttu-id="f48cb-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="f48cb-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="f48cb-157">Oldappfound</span><span class="sxs-lookup"><span data-stu-id="f48cb-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="f48cb-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="f48cb-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="f48cb-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="f48cb-159">1.00.0000</span></span>  | <span data-ttu-id="f48cb-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="f48cb-160">2.00.0000</span></span>  | <span data-ttu-id="f48cb-161">1033</span><span class="sxs-lookup"><span data-stu-id="f48cb-161">1033</span></span>     |            | <span data-ttu-id="f48cb-162">\[Appfeatureenglish\]</span><span class="sxs-lookup"><span data-stu-id="f48cb-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="f48cb-163">Englische appfound</span><span class="sxs-lookup"><span data-stu-id="f48cb-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f48cb-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f48cb-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f48cb-165">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="f48cb-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



