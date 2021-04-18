---
description: Die Linien eines Kombinations Felds werden nicht als einzelne Steuerelemente behandelt. Sie sind Teil eines einzelnen Kombinations Felds, das als Steuerelement fungiert. In dieser Tabelle werden die Werte für jedes Kombinations Feld aufgelistet.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: ComboBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352431"
---
# <a name="combobox-table"></a><span data-ttu-id="925f9-104">ComboBox-Tabelle</span><span class="sxs-lookup"><span data-stu-id="925f9-104">ComboBox Table</span></span>

<span data-ttu-id="925f9-105">Die Linien eines Kombinations Felds werden nicht als einzelne Steuerelemente behandelt. Sie sind Teil eines einzelnen Kombinations Felds, das als Steuerelement fungiert.</span><span class="sxs-lookup"><span data-stu-id="925f9-105">The lines of a combo box are not treated as individual controls; they are part of a single combo box that functions as a control.</span></span> <span data-ttu-id="925f9-106">In dieser Tabelle werden die Werte für jedes Kombinations Feld aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="925f9-106">This table lists the values for each combo box.</span></span>

<span data-ttu-id="925f9-107">Die ComboBox-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="925f9-107">The ComboBox table has the following columns.</span></span>



| <span data-ttu-id="925f9-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="925f9-108">Column</span></span>   | <span data-ttu-id="925f9-109">Typ</span><span class="sxs-lookup"><span data-stu-id="925f9-109">Type</span></span>                         | <span data-ttu-id="925f9-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="925f9-110">Key</span></span> | <span data-ttu-id="925f9-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="925f9-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="925f9-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="925f9-112">Property</span></span> | [<span data-ttu-id="925f9-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="925f9-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="925f9-114">J</span><span class="sxs-lookup"><span data-stu-id="925f9-114">Y</span></span>   | <span data-ttu-id="925f9-115">N</span><span class="sxs-lookup"><span data-stu-id="925f9-115">N</span></span>        |
| <span data-ttu-id="925f9-116">Auftrag</span><span class="sxs-lookup"><span data-stu-id="925f9-116">Order</span></span>    | [<span data-ttu-id="925f9-117">Integer</span><span class="sxs-lookup"><span data-stu-id="925f9-117">Integer</span></span>](integer.md)       | <span data-ttu-id="925f9-118">J</span><span class="sxs-lookup"><span data-stu-id="925f9-118">Y</span></span>   | <span data-ttu-id="925f9-119">N</span><span class="sxs-lookup"><span data-stu-id="925f9-119">N</span></span>        |
| <span data-ttu-id="925f9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="925f9-120">Value</span></span>    | [<span data-ttu-id="925f9-121">Großformatige</span><span class="sxs-lookup"><span data-stu-id="925f9-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="925f9-122">N</span><span class="sxs-lookup"><span data-stu-id="925f9-122">N</span></span>   | <span data-ttu-id="925f9-123">N</span><span class="sxs-lookup"><span data-stu-id="925f9-123">N</span></span>        |
| <span data-ttu-id="925f9-124">Text</span><span class="sxs-lookup"><span data-stu-id="925f9-124">Text</span></span>     | [<span data-ttu-id="925f9-125">Text</span><span class="sxs-lookup"><span data-stu-id="925f9-125">Text</span></span>](text.md)             | <span data-ttu-id="925f9-126">N</span><span class="sxs-lookup"><span data-stu-id="925f9-126">N</span></span>   | <span data-ttu-id="925f9-127">J</span><span class="sxs-lookup"><span data-stu-id="925f9-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="925f9-128">Spalten</span><span class="sxs-lookup"><span data-stu-id="925f9-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="925f9-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="925f9-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="925f9-130">Eine benannte Eigenschaft, die an dieses Element gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="925f9-130">A named property to be tied to this item.</span></span> <span data-ttu-id="925f9-131">Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil desselben Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="925f9-131">All the items tied to the same property become part of the same combo box.</span></span>

</dd> <dt>

<span data-ttu-id="925f9-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="925f9-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="925f9-133">Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einer einzelnen Kombinations Feld Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="925f9-133">A positive integer used to determine the ordering of the items that appear in a single combo box list.</span></span> <span data-ttu-id="925f9-134">Die ganzen Zahlen müssen nicht aufeinander folgen.</span><span class="sxs-lookup"><span data-stu-id="925f9-134">The integers do not have to be consecutive.</span></span> <span data-ttu-id="925f9-135">Wenn ein Kombinations Feld als sortiert definiert ist, sollten alle Elemente über einen Bestellwert verfügen.</span><span class="sxs-lookup"><span data-stu-id="925f9-135">If a combo box is defined as ordered, then all the items should have an Order value.</span></span> <span data-ttu-id="925f9-136">Wenn das Kombinations Feld als nicht geordnet definiert ist, wird diese Spalte ignoriert.</span><span class="sxs-lookup"><span data-stu-id="925f9-136">If the combo box is defined as unordered, then this column is ignored.</span></span>

<span data-ttu-id="925f9-137">Nur positive Zahlen.</span><span class="sxs-lookup"><span data-stu-id="925f9-137">Positive numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="925f9-138"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="925f9-138"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="925f9-139">Die diesem Element zugeordnete Wert Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="925f9-139">The value string associated with this item.</span></span> <span data-ttu-id="925f9-140">Wenn Sie diese Zeile im Kombinations Feld auswählen, wird die zugehörige Eigenschaft (in der-Eigenschaft angegeben) auf diesen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="925f9-140">Selecting this line of the combo box sets the associated property (specified in Property) to this value.</span></span>

</dd> <dt>

<span data-ttu-id="925f9-141"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span><span class="sxs-lookup"><span data-stu-id="925f9-141"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="925f9-142">Der sichtbare, lokalisierbare Text, der dem Element zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="925f9-142">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="925f9-143">Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird für den Text standardmäßig der Wert "Value" verwendet.</span><span class="sxs-lookup"><span data-stu-id="925f9-143">If this entry or the entire column is missing, then the text defaults to the entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="925f9-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="925f9-144">Remarks</span></span>

<span data-ttu-id="925f9-145">Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="925f9-145">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="925f9-146">Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="925f9-146">The formatting occurs only when the control is created and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="925f9-147">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="925f9-147">Validation</span></span>

<dl>

[<span data-ttu-id="925f9-148">ICE03</span><span class="sxs-lookup"><span data-stu-id="925f9-148">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="925f9-149">ICE06</span><span class="sxs-lookup"><span data-stu-id="925f9-149">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="925f9-150">ICE17</span><span class="sxs-lookup"><span data-stu-id="925f9-150">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="925f9-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="925f9-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



