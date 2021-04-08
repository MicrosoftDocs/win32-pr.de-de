---
description: Wenn das Bitmap-Steuerelement Bit festgelegt ist, wird der Text im-Steuerelement durch ein Bitmap-Bild ersetzt. Die Text-Spalte in der Steuerelement Tabelle ist ein Fremdschlüssel in die binäre Tabelle.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Bitmap-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864436"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="b9e5f-104">Bitmap-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="b9e5f-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="b9e5f-105">Wenn das Bitmap-Steuerelement Bit festgelegt ist, wird der Text im-Steuerelement durch ein Bitmap-Bild ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b9e5f-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="b9e5f-106">Die Text-Spalte in der [Steuerelement Tabelle](control-table.md) ist ein Fremdschlüssel in die [binäre Tabelle](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5f-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="b9e5f-107">Wenn dieses Bit nicht festgelegt ist, wird der Text im-Steuerelement in der Text-Spalte der [Steuerelement Tabelle](control-table.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="b9e5f-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b9e5f-108">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b9e5f-108">Valid Controls</span></span>

[<span data-ttu-id="b9e5f-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="b9e5f-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="b9e5f-110">PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="b9e5f-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="b9e5f-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b9e5f-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="b9e5f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b9e5f-112">Value</span></span>



| <span data-ttu-id="b9e5f-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="b9e5f-113">Decimal</span></span> | <span data-ttu-id="b9e5f-114">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="b9e5f-114">Hexadecimal</span></span> | <span data-ttu-id="b9e5f-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="b9e5f-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="b9e5f-116">262144</span><span class="sxs-lookup"><span data-stu-id="b9e5f-116">262144</span></span>  | <span data-ttu-id="b9e5f-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="b9e5f-117">0x00040000</span></span>  | <span data-ttu-id="b9e5f-118">**msidbcontrolattributesbitmap**</span><span class="sxs-lookup"><span data-stu-id="b9e5f-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9e5f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9e5f-119">Remarks</span></span>

<span data-ttu-id="b9e5f-120">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das Bitmap-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="b9e5f-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="b9e5f-121">Die Text-Spalte in der Steuerelement Tabelle wird als Fremdschlüssel für die [binäre Tabelle](binary-table.md)verwendet. Daher kann das Steuerelement kein Symbolbild und keinen Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9e5f-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="b9e5f-122">Legen Sie nicht sowohl das [Symbol](icon-control-attribute.md) als auch das Bitmap-Bit fest.</span><span class="sxs-lookup"><span data-stu-id="b9e5f-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="b9e5f-123">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="b9e5f-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



