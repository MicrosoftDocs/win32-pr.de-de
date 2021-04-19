---
description: 'Windows Vista und höher: nls definiert mehrere Pseudo Gebiets Schemas, die zusätzlich zu den vorhandenen Windows-Gebiets Schemas verwendet werden können.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346927"
---
# <a name="pseudo-locales"></a><span data-ttu-id="78567-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="78567-103">Pseudo-Locales</span></span>

<span data-ttu-id="78567-104">**Windows Vista und höher:** NLS definiert mehrere Pseudo Gebiets Schemas, die zusätzlich zu den vorhandenen Windows-Gebiets Schemas verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="78567-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="78567-105">Verwenden Sie diese Pseudo Gebiets Schemas, um die Lokalisierung Ihrer Anwendungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="78567-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="78567-106">Implementierungsdetails finden Sie unter [Verwenden von Pseudo-Locales für Lokalisierungstests](using-pseudo-locales-for-localization-testing.md).</span><span class="sxs-lookup"><span data-stu-id="78567-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="78567-107">Unterstützte Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="78567-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="78567-108">Folgende Pseudo Gebiets Schemas werden von NLS unterstützt:</span><span class="sxs-lookup"><span data-stu-id="78567-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="78567-109">Basis Pseudo Gebiets Schema</span><span class="sxs-lookup"><span data-stu-id="78567-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="78567-110">Gespiegeltes (von rechts nach links) Pseudo Gebiets Schema</span><span class="sxs-lookup"><span data-stu-id="78567-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="78567-111">Pseudo Gebiets Schema der ostasiatischen Sprache</span><span class="sxs-lookup"><span data-stu-id="78567-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="78567-112">Wählen Sie das jeweilige zu verwendende Pseudo Gebiets Schema basierend auf den Code Page Zuweisungen und den Zeichen folgen für die Lokalisierung aus, z. b. Monatsnamen, Tagnamen.</span><span class="sxs-lookup"><span data-stu-id="78567-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="78567-113">Die Daten für die einzelnen Pseudo Gebiets Schemas umfassen nicht nur relevante Codepages und Tages-und Monats Zeichenfolgen für die Lokalisierung, sondern auch Daten für verschiedene andere Testfälle für NLS.</span><span class="sxs-lookup"><span data-stu-id="78567-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="78567-114">In den Testfällen werden die folgenden Datentypen untersucht:</span><span class="sxs-lookup"><span data-stu-id="78567-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="78567-115">9 [-Bit-](locale-identifiers.md)Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="78567-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="78567-116">Pseudo Gebiets Schemata bieten eine gute Möglichkeit, den Vorgang von 9-Bit-Gebiets Schema Bezeichners zu testen.</span><span class="sxs-lookup"><span data-stu-id="78567-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="78567-117">Zeichen folgen aus Sprachen, die kleine Schriftarten verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="78567-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="78567-118">Aufgrund von Einschränkungen in der Graphics Device Interface (GDI) ist die Schriftart der Benutzeroberfläche für einige Sprachen kleiner als optimal.</span><span class="sxs-lookup"><span data-stu-id="78567-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="78567-119">Pseudo Gebiets Schemas enthalten mehrere Zeichen folgen aus diesen Sprachen, kombiniert mit Zeichen folgen aus Sprachen mit mehr Standard Schriftart Behandlung.</span><span class="sxs-lookup"><span data-stu-id="78567-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="78567-120">Sie können diese Zeichen folgen beim Testen verwenden, um zu bestimmen, wie eine GDI-begrenzte Schriftart gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="78567-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="78567-121">Ungewöhnliche Zeichen folgen Längen.</span><span class="sxs-lookup"><span data-stu-id="78567-121">Unusual string lengths.</span></span> <span data-ttu-id="78567-122">Einige Gebiets Schema Informations Konstanten, z. b. [locale \_ slist](locale-slist.md) und [locale \_ icurrency](locale-icurrency.md), haben konventionelle Grenzwerte für die Zeichen folgen Größe.</span><span class="sxs-lookup"><span data-stu-id="78567-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="78567-123">Die Pseudo Gebiets Schemas unterstützen die Untersuchung unterschiedlicher Zeichen folgen Längen.</span><span class="sxs-lookup"><span data-stu-id="78567-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="78567-124">Alternative Sortierungen.</span><span class="sxs-lookup"><span data-stu-id="78567-124">Alternate sorts.</span></span> <span data-ttu-id="78567-125">Mithilfe von Pseudo Gebiets Schemas können alternative Sortierfunktionen getestet werden, wenn sich der Alternative [Sortier Auftrags Bezeichner](sort-order-identifiers.md) von der ID der Basis Sortierreihenfolge unterscheidet, die normalerweise dem Gebiets Schema zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78567-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="78567-126">Pseudo Gebiets Schema-Namen und-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="78567-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="78567-127">Die Pseudo Gebiets Schemas verfügen über Gebiets Schema [Namen](locale-names.md) , die aus dem privaten Verwendungsbereich ausgewählt werden, um Konflikte mit möglichen Zeichen folgen zu vermeiden, internationale Organisation für Normung die in die Standards 639 (ISO) und ISO 3166 eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="78567-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="78567-128">Jedes Pseudo Gebiets Schema hat auch seinen eigenen Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="78567-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="78567-129">In der folgenden Tabelle finden Sie die Namen und Bezeichner für die definierten Pseudo Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="78567-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="78567-130">Pseudo Gebiets Schema</span><span class="sxs-lookup"><span data-stu-id="78567-130">Pseudo-locale</span></span>       | <span data-ttu-id="78567-131">Gebiets Schema Name</span><span class="sxs-lookup"><span data-stu-id="78567-131">Locale name</span></span> | <span data-ttu-id="78567-132">Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="78567-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="78567-133">Basis</span><span class="sxs-lookup"><span data-stu-id="78567-133">Base</span></span>                | <span data-ttu-id="78567-134">QPS-ploc</span><span class="sxs-lookup"><span data-stu-id="78567-134">qps-ploc</span></span>    | <span data-ttu-id="78567-135">0501</span><span class="sxs-lookup"><span data-stu-id="78567-135">0501</span></span>              |
| <span data-ttu-id="78567-136">Gespiegelt</span><span class="sxs-lookup"><span data-stu-id="78567-136">Mirrored</span></span>            | <span data-ttu-id="78567-137">QPS-plocm</span><span class="sxs-lookup"><span data-stu-id="78567-137">qps-plocm</span></span>   | <span data-ttu-id="78567-138">09FF</span><span class="sxs-lookup"><span data-stu-id="78567-138">09ff</span></span>              |
| <span data-ttu-id="78567-139">Ostasiatische Sprache</span><span class="sxs-lookup"><span data-stu-id="78567-139">East Asian-language</span></span> | <span data-ttu-id="78567-140">QPS-Ploca</span><span class="sxs-lookup"><span data-stu-id="78567-140">qps-ploca</span></span>   | <span data-ttu-id="78567-141">05fe</span><span class="sxs-lookup"><span data-stu-id="78567-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="78567-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="78567-142">Example</span></span>

<span data-ttu-id="78567-143">Das folgende Beispiel zeigt Text, der für ein basispseudo Gebiets Schema angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="78567-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="78567-144">\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ!! \] ōf 2006</span><span class="sxs-lookup"><span data-stu-id="78567-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="78567-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78567-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78567-146">Gebiets Schemas und Sprachen</span><span class="sxs-lookup"><span data-stu-id="78567-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="78567-147">Gebiets Schema Bezeichner</span><span class="sxs-lookup"><span data-stu-id="78567-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="78567-148">Gebiets Schema Namen</span><span class="sxs-lookup"><span data-stu-id="78567-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="78567-149">Sortierreihenfolge-IDs</span><span class="sxs-lookup"><span data-stu-id="78567-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="78567-150">Verwenden von Pseudo-Locales für Lokalisierungstests</span><span class="sxs-lookup"><span data-stu-id="78567-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



