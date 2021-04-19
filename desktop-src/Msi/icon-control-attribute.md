---
description: Wenn dieses Bit festgelegt ist, wird Text durch ein Symbolbild ersetzt, und die Text-Spalte in der Steuerelement Tabelle ist ein Fremdschlüssel in die binäre Tabelle.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Symbol Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356837"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="56219-103">Symbol Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="56219-103">Icon Control Attribute</span></span>

<span data-ttu-id="56219-104">Wenn dieses Bit festgelegt ist, wird Text durch ein Symbolbild ersetzt, und die Text-Spalte in der [Steuerelement Tabelle](control-table.md) ist ein Fremdschlüssel in die [binäre Tabelle](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="56219-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="56219-105">Wenn dieses Bit nicht festgelegt ist, wird der Text im-Steuerelement in der Text-Spalte der [Steuerelement Tabelle](control-table.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="56219-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="56219-106">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="56219-106">Valid Controls</span></span>

[<span data-ttu-id="56219-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="56219-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="56219-108">PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="56219-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="56219-109">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="56219-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="56219-110">Wert</span><span class="sxs-lookup"><span data-stu-id="56219-110">Value</span></span>



| <span data-ttu-id="56219-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="56219-111">Decimal</span></span> | <span data-ttu-id="56219-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="56219-112">Hexadecimal</span></span> | <span data-ttu-id="56219-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="56219-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="56219-114">5242288</span><span class="sxs-lookup"><span data-stu-id="56219-114">5242288</span></span> | <span data-ttu-id="56219-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="56219-115">0x00080000</span></span>  | <span data-ttu-id="56219-116">**msidbcontrolattributesicon**</span><span class="sxs-lookup"><span data-stu-id="56219-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="56219-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56219-117">Remarks</span></span>

<span data-ttu-id="56219-118">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die Symbol Bits in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="56219-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="56219-119">Die Text-Spalte in der Steuerelement Tabelle wird als Fremdschlüssel für die [binäre Tabelle](binary-table.md)verwendet. Daher kann das Steuerelement kein Symbolbild und keinen Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="56219-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="56219-120">Legen Sie nicht sowohl das Symbol als auch das [Bitmap](bitmap-control-attribute.md) -Bit fest.</span><span class="sxs-lookup"><span data-stu-id="56219-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="56219-121">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="56219-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



