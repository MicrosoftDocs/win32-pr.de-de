---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 19 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Benutzerdefinierter Aktionstyp 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362792"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="7ae32-103">Benutzerdefinierter Aktionstyp 19</span><span class="sxs-lookup"><span data-stu-id="7ae32-103">Custom Action Type 19</span></span>

<span data-ttu-id="7ae32-104">Diese benutzerdefinierte Aktion zeigt eine angegebene Fehlermeldung an, gibt einen Fehler zurück und beendet dann die Installation.</span><span class="sxs-lookup"><span data-stu-id="7ae32-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="7ae32-105">Die angezeigte Fehlermeldung kann als Zeichenfolge oder als Index in der [Fehler Tabelle](error-table.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ae32-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="7ae32-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="7ae32-106">Source</span></span>

<span data-ttu-id="7ae32-107">Belassen Sie die Spalte "Source" der [Tabelle "CustomAction](customaction-table.md) " leer.</span><span class="sxs-lookup"><span data-stu-id="7ae32-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="7ae32-108">Typwert</span><span class="sxs-lookup"><span data-stu-id="7ae32-108">Type Value</span></span>

<span data-ttu-id="7ae32-109">Fügen Sie den folgenden Wert in die Spalte Type der Tabelle CustomAction ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7ae32-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="7ae32-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7ae32-110">Constants</span></span>                                                               | <span data-ttu-id="7ae32-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="7ae32-111">Hexadecimal</span></span> | <span data-ttu-id="7ae32-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="7ae32-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="7ae32-113">**msidbcustomaktiontypetextdata**  +  **msidbcustomaktiontypesourcefile**</span><span class="sxs-lookup"><span data-stu-id="7ae32-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="7ae32-114">0x013</span><span class="sxs-lookup"><span data-stu-id="7ae32-114">0x013</span></span>       | <span data-ttu-id="7ae32-115">19</span><span class="sxs-lookup"><span data-stu-id="7ae32-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="7ae32-116">Ziel</span><span class="sxs-lookup"><span data-stu-id="7ae32-116">Target</span></span>

<span data-ttu-id="7ae32-117">Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält eine Text Zeichenfolge, die mit der in [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (ohne numerische feldspezifizierer) angegebenen Funktionalität formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ae32-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="7ae32-118">Die zu ersetzenden Parameter sind in eckige Klammern ( \[ ...) eingeschlossen \] und können Eigenschaften, Umgebungsvariablen (% prefix), Dateipfade ( \# Präfix) oder Komponenten Verzeichnispfade ($ prefix) sein.</span><span class="sxs-lookup"><span data-stu-id="7ae32-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="7ae32-119">Wenn die Zeichenfolge nach der Formatierung in eine ganze Zahl ausgewertet wird, wird diese Ganzzahl als Index in der [Fehler Tabelle](error-table.md) verwendet, um die anzuzeigende Meldung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7ae32-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="7ae32-120">Wenn die Zeichenfolge nach der Formatierung nicht numerische Zeichen enthält, wird die Zeichenfolge selbst als Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ae32-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7ae32-121">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="7ae32-121">Return Processing Options</span></span>

<span data-ttu-id="7ae32-122">Die benutzerdefinierte Aktion verwendet keine Optionen.</span><span class="sxs-lookup"><span data-stu-id="7ae32-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7ae32-123">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="7ae32-123">Execution Scheduling Options</span></span>

<span data-ttu-id="7ae32-124">Die benutzerdefinierte Aktion verwendet keine Optionen.</span><span class="sxs-lookup"><span data-stu-id="7ae32-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7ae32-125">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="7ae32-125">In-Script Execution Options</span></span>

<span data-ttu-id="7ae32-126">Die benutzerdefinierte Aktion verwendet keine Optionen.</span><span class="sxs-lookup"><span data-stu-id="7ae32-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="7ae32-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7ae32-127">Return Values</span></span>

<span data-ttu-id="7ae32-128">Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7ae32-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae32-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ae32-129">Remarks</span></span>

<span data-ttu-id="7ae32-130">Beispielsweise geben die benutzerdefinierten Aktionen CAError1, CAError2, CAError3 und CAError4 diese Nachrichten zurück.</span><span class="sxs-lookup"><span data-stu-id="7ae32-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="7ae32-131">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="7ae32-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="7ae32-132">Aktion</span><span class="sxs-lookup"><span data-stu-id="7ae32-132">Action</span></span>   | <span data-ttu-id="7ae32-133">type</span><span class="sxs-lookup"><span data-stu-id="7ae32-133">Type</span></span> | <span data-ttu-id="7ae32-134">`Source`</span><span class="sxs-lookup"><span data-stu-id="7ae32-134">Source</span></span> | <span data-ttu-id="7ae32-135">Ziel</span><span class="sxs-lookup"><span data-stu-id="7ae32-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="7ae32-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="7ae32-136">CAError1</span></span> | <span data-ttu-id="7ae32-137">19</span><span class="sxs-lookup"><span data-stu-id="7ae32-137">19</span></span>   |        | <span data-ttu-id="7ae32-138">\[Eigenschaft PROP1\]</span><span class="sxs-lookup"><span data-stu-id="7ae32-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="7ae32-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="7ae32-139">CAError2</span></span> | <span data-ttu-id="7ae32-140">19</span><span class="sxs-lookup"><span data-stu-id="7ae32-140">19</span></span>   |        | <span data-ttu-id="7ae32-141">Installationsfehler aufgrund von error2.</span><span class="sxs-lookup"><span data-stu-id="7ae32-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="7ae32-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="7ae32-142">CAError3</span></span> | <span data-ttu-id="7ae32-143">19</span><span class="sxs-lookup"><span data-stu-id="7ae32-143">19</span></span>   |        | <span data-ttu-id="7ae32-144">25000</span><span class="sxs-lookup"><span data-stu-id="7ae32-144">25000</span></span>                               |
| <span data-ttu-id="7ae32-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="7ae32-145">CAError4</span></span> | <span data-ttu-id="7ae32-146">19</span><span class="sxs-lookup"><span data-stu-id="7ae32-146">19</span></span>   |        | <span data-ttu-id="7ae32-147">\[Prop2\]</span><span class="sxs-lookup"><span data-stu-id="7ae32-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="7ae32-148">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="7ae32-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="7ae32-149">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7ae32-149">Property</span></span> | <span data-ttu-id="7ae32-150">Wert</span><span class="sxs-lookup"><span data-stu-id="7ae32-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="7ae32-151">Eigenschaft PROP1</span><span class="sxs-lookup"><span data-stu-id="7ae32-151">Prop1</span></span>    | <span data-ttu-id="7ae32-152">"Fehler bei der Installation aufgrund von Error1".</span><span class="sxs-lookup"><span data-stu-id="7ae32-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="7ae32-153">Prop2</span><span class="sxs-lookup"><span data-stu-id="7ae32-153">Prop2</span></span>    | <span data-ttu-id="7ae32-154">"25100"</span><span class="sxs-lookup"><span data-stu-id="7ae32-154">"25100"</span></span>                               |



 

[<span data-ttu-id="7ae32-155">Fehler Tabelle</span><span class="sxs-lookup"><span data-stu-id="7ae32-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="7ae32-156">Code</span><span class="sxs-lookup"><span data-stu-id="7ae32-156">Code</span></span>  | <span data-ttu-id="7ae32-157">`Message`</span><span class="sxs-lookup"><span data-stu-id="7ae32-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="7ae32-158">25000</span><span class="sxs-lookup"><span data-stu-id="7ae32-158">25000</span></span> | <span data-ttu-id="7ae32-159">Installationsfehler aufgrund von Error3.</span><span class="sxs-lookup"><span data-stu-id="7ae32-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="7ae32-160">25100</span><span class="sxs-lookup"><span data-stu-id="7ae32-160">25100</span></span> | <span data-ttu-id="7ae32-161">Installationsfehler aufgrund von Error4.</span><span class="sxs-lookup"><span data-stu-id="7ae32-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="7ae32-162">Diese benutzerdefinierten Aktionen geben die folgenden Fehlermeldungen zurück:</span><span class="sxs-lookup"><span data-stu-id="7ae32-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="7ae32-163">Benutzerdefinierte Aktion</span><span class="sxs-lookup"><span data-stu-id="7ae32-163">Custom action</span></span> | <span data-ttu-id="7ae32-164">Zurückgegebene Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7ae32-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="7ae32-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="7ae32-165">CAError1</span></span>      | <span data-ttu-id="7ae32-166">Installationsfehler aufgrund von Error1.</span><span class="sxs-lookup"><span data-stu-id="7ae32-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="7ae32-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="7ae32-167">CAError2</span></span>      | <span data-ttu-id="7ae32-168">Installationsfehler aufgrund von error2.</span><span class="sxs-lookup"><span data-stu-id="7ae32-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="7ae32-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="7ae32-169">CAError3</span></span>      | <span data-ttu-id="7ae32-170">Installationsfehler aufgrund von Error3.</span><span class="sxs-lookup"><span data-stu-id="7ae32-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="7ae32-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="7ae32-171">CAError4</span></span>      | <span data-ttu-id="7ae32-172">Installationsfehler aufgrund von Error4.</span><span class="sxs-lookup"><span data-stu-id="7ae32-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="7ae32-173">Beachten Sie Folgendes: da die Reihenfolge der Auswertung von Startbedingungen durch das Erstellen der [LaunchCondition-Tabelle](launchcondition-table.md)nicht garantiert werden kann, sollten Sie benutzerdefinierte Aktionen vom Typ 19 benutzerdefinierte Aktionen in der Installation verwenden, um Bedingungen in einer bestimmten Reihenfolge auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="7ae32-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ae32-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ae32-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae32-175">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="7ae32-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



