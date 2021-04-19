---
description: Wenn dieses Bit für ein Steuerelement festgelegt wird, ist die zugeordnete Eigenschaft, die in der Eigenschafts Spalte der Steuerelement Tabelle angegeben ist, eine ganze Zahl. Wenn dieses Bit nicht festgelegt ist, ist die Eigenschaft ein Zeichen folgen Wert.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Integer-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341179"
---
# <a name="integer-control-attribute"></a><span data-ttu-id="42ec7-104">Integer-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="42ec7-104">Integer Control Attribute</span></span>

<span data-ttu-id="42ec7-105">Wenn dieses Bit für ein Steuerelement festgelegt wird, ist die zugeordnete Eigenschaft, die in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md) angegeben ist, eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="42ec7-105">If this bit is set on a control, the associated property specified in the Property column of the [Control table](control-table.md) is an integer.</span></span> <span data-ttu-id="42ec7-106">Wenn dieses Bit nicht festgelegt ist, ist die Eigenschaft ein Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="42ec7-106">If this bit is not set, the property is a string value.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="42ec7-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="42ec7-107">Valid Controls</span></span>

[<span data-ttu-id="42ec7-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="42ec7-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="42ec7-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="42ec7-109">ComboBox</span></span>](combobox-control.md)

[<span data-ttu-id="42ec7-110">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="42ec7-110">Edit</span></span>](edit-control.md)

[<span data-ttu-id="42ec7-111">ListBox</span><span class="sxs-lookup"><span data-stu-id="42ec7-111">ListBox</span></span>](listbox-control.md)

[<span data-ttu-id="42ec7-112">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="42ec7-112">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="42ec7-113">Wert</span><span class="sxs-lookup"><span data-stu-id="42ec7-113">Value</span></span>



| <span data-ttu-id="42ec7-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="42ec7-114">Decimal</span></span> | <span data-ttu-id="42ec7-115">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="42ec7-115">Hexadecimal</span></span> | <span data-ttu-id="42ec7-116">Konstante</span><span class="sxs-lookup"><span data-stu-id="42ec7-116">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="42ec7-117">16</span><span class="sxs-lookup"><span data-stu-id="42ec7-117">16</span></span>      | <span data-ttu-id="42ec7-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ec7-118">0x00000010</span></span>  | <span data-ttu-id="42ec7-119">**msidbcontrolattributesinteger**</span><span class="sxs-lookup"><span data-stu-id="42ec7-119">**msidbControlAttributesInteger**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="42ec7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42ec7-120">Remarks</span></span>

<span data-ttu-id="42ec7-121">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das ganzzahlige Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="42ec7-121">To set this attribute on a control, include the Integer bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="42ec7-122">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="42ec7-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



