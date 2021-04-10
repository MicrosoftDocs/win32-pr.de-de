---
description: Wenn dieses Bit festgelegt ist, werden die im Steuerelement aufgeführten Elemente in einer angegebenen Reihenfolge angezeigt. Wenn das-Bit nicht festgelegt ist, werden Elemente in alphabetischer Reihenfolge angezeigt.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Sortiertes Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041612"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="d63ae-104">Sortiertes Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="d63ae-104">Sorted Control Attribute</span></span>

<span data-ttu-id="d63ae-105">Wenn dieses Bit festgelegt ist, werden die im Steuerelement aufgeführten Elemente in einer angegebenen Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d63ae-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="d63ae-106">Wenn das-Bit nicht festgelegt ist, werden Elemente in alphabetischer Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d63ae-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="d63ae-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d63ae-107">Valid Controls</span></span>

[<span data-ttu-id="d63ae-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="d63ae-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="d63ae-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="d63ae-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="d63ae-110">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d63ae-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="d63ae-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d63ae-111">Value</span></span>



| <span data-ttu-id="d63ae-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="d63ae-112">Decimal</span></span> | <span data-ttu-id="d63ae-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="d63ae-113">Hexadecimal</span></span> | <span data-ttu-id="d63ae-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="d63ae-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="d63ae-115">65536</span><span class="sxs-lookup"><span data-stu-id="d63ae-115">65536</span></span>   | <span data-ttu-id="d63ae-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d63ae-116">0x00010000</span></span>  | <span data-ttu-id="d63ae-117">**msidbcontrolattributess orted**</span><span class="sxs-lookup"><span data-stu-id="d63ae-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d63ae-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d63ae-118">Remarks</span></span>

<span data-ttu-id="d63ae-119">Um die Elemente in einem Kombinations [Feld](combobox-control.md)zu sortieren, schließen Sie das sortierte Bit in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, und geben Sie die Element Reihenfolge in der Spalte Order der [ComboBox-Tabelle](combobox-table.md)an.</span><span class="sxs-lookup"><span data-stu-id="d63ae-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="d63ae-120">Um die Elemente in einem [ListBox](listbox-control.md)-Element zu sortieren, schließen Sie das sortierte Bit in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, und geben Sie die Element Reihenfolge in der Spalte Order der [ComboBox-Tabelle](combobox-table.md)an.</span><span class="sxs-lookup"><span data-stu-id="d63ae-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="d63ae-121">Wenn Sie die Elemente in einer [ListView](listview-control.md)sortieren möchten, schließen Sie das sortierte Bit in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein, und geben Sie die Reihenfolge der Elemente in der [ComboBox-Tabelle](combobox-table.md)an.</span><span class="sxs-lookup"><span data-stu-id="d63ae-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="d63ae-122">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="d63ae-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



