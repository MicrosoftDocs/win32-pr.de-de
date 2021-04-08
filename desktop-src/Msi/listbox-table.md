---
description: Die Zeilen eines Listen Felds werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil eines Listen Felds, das als Steuerelement fungiert. Die ListBox-Tabelle definiert die Werte für alle Listenfelder.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: ListBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960036"
---
# <a name="listbox-table"></a><span data-ttu-id="c3734-104">ListBox-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3734-104">ListBox Table</span></span>

<span data-ttu-id="c3734-105">Die Zeilen eines Listen Felds werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil eines Listen Felds, das als Steuerelement fungiert.</span><span class="sxs-lookup"><span data-stu-id="c3734-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="c3734-106">Die ListBox-Tabelle definiert die Werte für alle Listenfelder.</span><span class="sxs-lookup"><span data-stu-id="c3734-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="c3734-107">Die ListBox-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="c3734-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="c3734-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c3734-108">Column</span></span>   | <span data-ttu-id="c3734-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c3734-109">Type</span></span>                         | <span data-ttu-id="c3734-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c3734-110">Key</span></span> | <span data-ttu-id="c3734-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c3734-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="c3734-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c3734-112">Property</span></span> | [<span data-ttu-id="c3734-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c3734-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c3734-114">J</span><span class="sxs-lookup"><span data-stu-id="c3734-114">Y</span></span>   | <span data-ttu-id="c3734-115">N</span><span class="sxs-lookup"><span data-stu-id="c3734-115">N</span></span>        |
| <span data-ttu-id="c3734-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="c3734-116">Order</span></span>    | [<span data-ttu-id="c3734-117">Integer</span><span class="sxs-lookup"><span data-stu-id="c3734-117">Integer</span></span>](integer.md)       | <span data-ttu-id="c3734-118">J</span><span class="sxs-lookup"><span data-stu-id="c3734-118">Y</span></span>   | <span data-ttu-id="c3734-119">N</span><span class="sxs-lookup"><span data-stu-id="c3734-119">N</span></span>        |
| <span data-ttu-id="c3734-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c3734-120">Value</span></span>    | [<span data-ttu-id="c3734-121">Großformatige</span><span class="sxs-lookup"><span data-stu-id="c3734-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c3734-122">N</span><span class="sxs-lookup"><span data-stu-id="c3734-122">N</span></span>   | <span data-ttu-id="c3734-123">N</span><span class="sxs-lookup"><span data-stu-id="c3734-123">N</span></span>        |
| <span data-ttu-id="c3734-124">Text</span><span class="sxs-lookup"><span data-stu-id="c3734-124">Text</span></span>     | [<span data-ttu-id="c3734-125">Großformatige</span><span class="sxs-lookup"><span data-stu-id="c3734-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c3734-126">N</span><span class="sxs-lookup"><span data-stu-id="c3734-126">N</span></span>   | <span data-ttu-id="c3734-127">J</span><span class="sxs-lookup"><span data-stu-id="c3734-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c3734-128">Spalten</span><span class="sxs-lookup"><span data-stu-id="c3734-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c3734-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="c3734-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="c3734-130">Eine benannte Eigenschaft, die an dieses Element gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3734-130">A named property to be tied to this item.</span></span> <span data-ttu-id="c3734-131">Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil desselben Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="c3734-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="c3734-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c3734-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="c3734-133">Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einem einzelnen Listenfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c3734-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="c3734-134">Wenn das Listenfeld als sortiert definiert ist, sollten alle Elemente über einen Bestellwert verfügen.</span><span class="sxs-lookup"><span data-stu-id="c3734-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="c3734-135">Die ganzen Zahlen müssen nicht aufeinander folgen.</span><span class="sxs-lookup"><span data-stu-id="c3734-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="c3734-136">Wenn das Listenfeld als nicht geordnet definiert ist, wird diese Spalte ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c3734-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c3734-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="c3734-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="c3734-138">Die diesem Element zugeordnete Wert Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3734-138">The value string associated with this item.</span></span> <span data-ttu-id="c3734-139">Durch Auswählen der Zeile wird die zugehörige Eigenschaft auf diesen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3734-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="c3734-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span><span class="sxs-lookup"><span data-stu-id="c3734-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="c3734-141">Der lokalisierbare, sichtbare Text, der dem Element zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3734-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="c3734-142">Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den entsprechenden Eintrag in value eingestellt.</span><span class="sxs-lookup"><span data-stu-id="c3734-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3734-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3734-143">Remarks</span></span>

<span data-ttu-id="c3734-144">Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3734-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="c3734-145">Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c3734-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="c3734-146">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="c3734-146">Validation</span></span>

<dl>

[<span data-ttu-id="c3734-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="c3734-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c3734-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="c3734-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c3734-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="c3734-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="c3734-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="c3734-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="c3734-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="c3734-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



