---
description: Die Zeilen einer ListView werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil einer ListView, die als Steuerelement fungiert. In der ListView-Tabelle sind die Werte für alle ListViews definiert.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: ListView-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347942"
---
# <a name="listview-table"></a><span data-ttu-id="3199e-104">ListView-Tabelle</span><span class="sxs-lookup"><span data-stu-id="3199e-104">ListView Table</span></span>

<span data-ttu-id="3199e-105">Die Zeilen einer ListView werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil einer ListView, die als Steuerelement fungiert.</span><span class="sxs-lookup"><span data-stu-id="3199e-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="3199e-106">In der ListView-Tabelle sind die Werte für alle ListViews definiert.</span><span class="sxs-lookup"><span data-stu-id="3199e-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="3199e-107">Die ListView-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="3199e-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="3199e-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="3199e-108">Column</span></span>   | <span data-ttu-id="3199e-109">Typ</span><span class="sxs-lookup"><span data-stu-id="3199e-109">Type</span></span>                         | <span data-ttu-id="3199e-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3199e-110">Key</span></span> | <span data-ttu-id="3199e-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="3199e-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="3199e-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3199e-112">Property</span></span> | [<span data-ttu-id="3199e-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3199e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3199e-114">J</span><span class="sxs-lookup"><span data-stu-id="3199e-114">Y</span></span>   | <span data-ttu-id="3199e-115">N</span><span class="sxs-lookup"><span data-stu-id="3199e-115">N</span></span>        |
| <span data-ttu-id="3199e-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3199e-116">Order</span></span>    | [<span data-ttu-id="3199e-117">Integer</span><span class="sxs-lookup"><span data-stu-id="3199e-117">Integer</span></span>](integer.md)       | <span data-ttu-id="3199e-118">J</span><span class="sxs-lookup"><span data-stu-id="3199e-118">Y</span></span>   | <span data-ttu-id="3199e-119">N</span><span class="sxs-lookup"><span data-stu-id="3199e-119">N</span></span>        |
| <span data-ttu-id="3199e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3199e-120">Value</span></span>    | [<span data-ttu-id="3199e-121">Großformatige</span><span class="sxs-lookup"><span data-stu-id="3199e-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3199e-122">N</span><span class="sxs-lookup"><span data-stu-id="3199e-122">N</span></span>   | <span data-ttu-id="3199e-123">N</span><span class="sxs-lookup"><span data-stu-id="3199e-123">N</span></span>        |
| <span data-ttu-id="3199e-124">Text</span><span class="sxs-lookup"><span data-stu-id="3199e-124">Text</span></span>     | [<span data-ttu-id="3199e-125">Großformatige</span><span class="sxs-lookup"><span data-stu-id="3199e-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3199e-126">N</span><span class="sxs-lookup"><span data-stu-id="3199e-126">N</span></span>   | <span data-ttu-id="3199e-127">J</span><span class="sxs-lookup"><span data-stu-id="3199e-127">Y</span></span>        |
| <span data-ttu-id="3199e-128">Binary\_</span><span class="sxs-lookup"><span data-stu-id="3199e-128">Binary\_</span></span> | [<span data-ttu-id="3199e-129">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3199e-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="3199e-130">N</span><span class="sxs-lookup"><span data-stu-id="3199e-130">N</span></span>   | <span data-ttu-id="3199e-131">J</span><span class="sxs-lookup"><span data-stu-id="3199e-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3199e-132">Spalten</span><span class="sxs-lookup"><span data-stu-id="3199e-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3199e-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="3199e-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="3199e-134">Eine benannte Eigenschaft, die an dieses Element gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="3199e-134">A named property to be tied to this item.</span></span> <span data-ttu-id="3199e-135">Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil derselben ListView.</span><span class="sxs-lookup"><span data-stu-id="3199e-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="3199e-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="3199e-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="3199e-137">Eine positive ganze Zahl, mit der die Reihenfolge der Elemente bestimmt wird, die in einer einzelnen ListView-Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3199e-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="3199e-138">Die ganzen Zahlen müssen nicht aufeinander folgen.</span><span class="sxs-lookup"><span data-stu-id="3199e-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="3199e-139">Wenn eine ListView als geordnet definiert ist, sollten alle Elemente über einen Bestellwert verfügen.</span><span class="sxs-lookup"><span data-stu-id="3199e-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="3199e-140">Wenn ListView als nicht geordnet definiert ist, wird diese Spalte ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3199e-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3199e-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="3199e-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="3199e-142">Die diesem Element zugeordnete Wert Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3199e-142">The value string associated with this item.</span></span> <span data-ttu-id="3199e-143">Durch Auswählen der Zeile wird die zugehörige Eigenschaft auf diesen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3199e-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="3199e-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span><span class="sxs-lookup"><span data-stu-id="3199e-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="3199e-145">Der sichtbare, lokalisierbare Text, der dem Element zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3199e-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="3199e-146">Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den entsprechenden Eintrag in value eingestellt.</span><span class="sxs-lookup"><span data-stu-id="3199e-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="3199e-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Ärer\_</span><span class="sxs-lookup"><span data-stu-id="3199e-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="3199e-148">Die Bilddaten für das Symbol.</span><span class="sxs-lookup"><span data-stu-id="3199e-148">The image data for the icon.</span></span> <span data-ttu-id="3199e-149">Dabei handelt es sich um einen Fremdschlüssel für die [binäre Tabelle](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="3199e-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3199e-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3199e-150">Remarks</span></span>

<span data-ttu-id="3199e-151">Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der msiformatrecord-Funktion interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3199e-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="3199e-152">Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3199e-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="3199e-153">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="3199e-153">Validation</span></span>

<dl>

[<span data-ttu-id="3199e-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="3199e-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3199e-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="3199e-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3199e-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="3199e-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="3199e-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="3199e-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



