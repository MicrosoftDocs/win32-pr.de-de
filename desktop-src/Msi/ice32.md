---
description: ICE32 überprüft, ob die Schlüssel und Fremdschlüssel in der MSI-Datei denselben Größen-und Spalten Definitions Typen entsprechen.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362324"
---
# <a name="ice32"></a><span data-ttu-id="e0d28-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="e0d28-103">ICE32</span></span>

<span data-ttu-id="e0d28-104">ICE32 überprüft, ob die Schlüssel und Fremdschlüssel in der MSI-Datei denselben Größen-und Spalten Definitions Typen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e0d28-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="e0d28-105">Diese benutzerdefinierte Ice-Aktion führt den Vergleich mithilfe der [ \_ Validierungs Tabelle](-validation-table.md) durch und verwendet die Definitions Typen, die von " [**msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0d28-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="e0d28-106">Weitere Informationen finden Sie unter [Column Definition Format](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="e0d28-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="e0d28-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="e0d28-107">Result</span></span>

<span data-ttu-id="e0d28-108">ICE32 gibt Fehler aus, wenn die MSI-Datei Fremdschlüssel für Schlüssel mit einer anderen Spaltenlänge oder einem anderen Spaltendatentyp enthält.</span><span class="sxs-lookup"><span data-stu-id="e0d28-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="e0d28-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e0d28-109">Example</span></span>

<span data-ttu-id="e0d28-110">ICE32 gibt zwei Fehler für das folgende Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="e0d28-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="e0d28-111">Es ist ein Fremdschlüssel und ein Schlüssel definiert, die sich von der Größe unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e0d28-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="e0d28-112">Es ist ein Fremdschlüssel und ein Schlüssel definiert, die sich in Ihrem Definitionstyp unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e0d28-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="e0d28-113">[ \_ Validierungs Tabelle](-validation-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e0d28-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="e0d28-114">Tabelle</span><span class="sxs-lookup"><span data-stu-id="e0d28-114">Table</span></span> | <span data-ttu-id="e0d28-115">Spalte</span><span class="sxs-lookup"><span data-stu-id="e0d28-115">Column</span></span>  | <span data-ttu-id="e0d28-116">KeyTable</span><span class="sxs-lookup"><span data-stu-id="e0d28-116">KeyTable</span></span> | <span data-ttu-id="e0d28-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="e0d28-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="e0d28-118">File</span><span class="sxs-lookup"><span data-stu-id="e0d28-118">File</span></span>  | <span data-ttu-id="e0d28-119">Version</span><span class="sxs-lookup"><span data-stu-id="e0d28-119">Version</span></span> | <span data-ttu-id="e0d28-120">Datei</span><span class="sxs-lookup"><span data-stu-id="e0d28-120">File</span></span>     | <span data-ttu-id="e0d28-121">1</span><span class="sxs-lookup"><span data-stu-id="e0d28-121">1</span></span>         |
| <span data-ttu-id="e0d28-122">Klapp</span><span class="sxs-lookup"><span data-stu-id="e0d28-122">Flap</span></span>  | <span data-ttu-id="e0d28-123">Column8</span><span class="sxs-lookup"><span data-stu-id="e0d28-123">Column8</span></span> | <span data-ttu-id="e0d28-124">Klapp</span><span class="sxs-lookup"><span data-stu-id="e0d28-124">Flap</span></span>     | <span data-ttu-id="e0d28-125">1</span><span class="sxs-lookup"><span data-stu-id="e0d28-125">1</span></span>         |



 

<span data-ttu-id="e0d28-126">Spaltendefinitionen (partiell)</span><span class="sxs-lookup"><span data-stu-id="e0d28-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="e0d28-127">Tabelle</span><span class="sxs-lookup"><span data-stu-id="e0d28-127">Table</span></span> | <span data-ttu-id="e0d28-128">Spalte</span><span class="sxs-lookup"><span data-stu-id="e0d28-128">Column</span></span>  | <span data-ttu-id="e0d28-129">type</span><span class="sxs-lookup"><span data-stu-id="e0d28-129">Type</span></span> | <span data-ttu-id="e0d28-130">Size</span><span class="sxs-lookup"><span data-stu-id="e0d28-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="e0d28-131">File</span><span class="sxs-lookup"><span data-stu-id="e0d28-131">File</span></span>  | <span data-ttu-id="e0d28-132">File</span><span class="sxs-lookup"><span data-stu-id="e0d28-132">File</span></span>    | <span data-ttu-id="e0d28-133">s</span><span class="sxs-lookup"><span data-stu-id="e0d28-133">s</span></span>    | <span data-ttu-id="e0d28-134">72</span><span class="sxs-lookup"><span data-stu-id="e0d28-134">72</span></span>   |
| <span data-ttu-id="e0d28-135">File</span><span class="sxs-lookup"><span data-stu-id="e0d28-135">File</span></span>  | <span data-ttu-id="e0d28-136">Version</span><span class="sxs-lookup"><span data-stu-id="e0d28-136">Version</span></span> | <span data-ttu-id="e0d28-137">E</span><span class="sxs-lookup"><span data-stu-id="e0d28-137">S</span></span>    | <span data-ttu-id="e0d28-138">32</span><span class="sxs-lookup"><span data-stu-id="e0d28-138">32</span></span>   |
| <span data-ttu-id="e0d28-139">Klapp</span><span class="sxs-lookup"><span data-stu-id="e0d28-139">Flap</span></span>  | <span data-ttu-id="e0d28-140">Column1</span><span class="sxs-lookup"><span data-stu-id="e0d28-140">Column1</span></span> | <span data-ttu-id="e0d28-141">i</span><span class="sxs-lookup"><span data-stu-id="e0d28-141">i</span></span>    | <span data-ttu-id="e0d28-142">2</span><span class="sxs-lookup"><span data-stu-id="e0d28-142">2</span></span>    |
| <span data-ttu-id="e0d28-143">Klapp</span><span class="sxs-lookup"><span data-stu-id="e0d28-143">Flap</span></span>  | <span data-ttu-id="e0d28-144">Column8</span><span class="sxs-lookup"><span data-stu-id="e0d28-144">Column8</span></span> | <span data-ttu-id="e0d28-145">E</span><span class="sxs-lookup"><span data-stu-id="e0d28-145">S</span></span>    | <span data-ttu-id="e0d28-146">32</span><span class="sxs-lookup"><span data-stu-id="e0d28-146">32</span></span>   |



 

<span data-ttu-id="e0d28-147">In der Spalte Version der Dateitabelle kann es sich um einen Fremdschlüssel für eine andere Datei in der Dateitabelle handeln.</span><span class="sxs-lookup"><span data-stu-id="e0d28-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="e0d28-148">Dies tritt bei Begleit Dateien auf.</span><span class="sxs-lookup"><span data-stu-id="e0d28-148">This occurs with companion files.</span></span> <span data-ttu-id="e0d28-149">In der Spalte Version ist jedoch nur eine Zeichen folgen Länge von 32 zulässig, während die Spalte Datei eine Zeichen folgen Länge von 72 zulässt.</span><span class="sxs-lookup"><span data-stu-id="e0d28-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="e0d28-150">Um diesen Fehler zu beheben, ändern Sie die Länge der Zeichenfolge entsprechend.</span><span class="sxs-lookup"><span data-stu-id="e0d28-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="e0d28-151">Es sind ein Fremdschlüssel und ein Schlüssel definiert, die sich in ihren Definitions Typen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e0d28-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="e0d28-152">Column8 der Flap-Tabelle wird als Fremdschlüssel für column1 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0d28-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="e0d28-153">Column8 ist eine Zeichen folgen Spalte und column1 eine ganzzahlige Spalte.</span><span class="sxs-lookup"><span data-stu-id="e0d28-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="e0d28-154">Die Fremdschlüssel-und Schlüsselpaare müssen so definiert sein, dass Ihre Datentypen stimmen.</span><span class="sxs-lookup"><span data-stu-id="e0d28-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0d28-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0d28-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0d28-156">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="e0d28-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



