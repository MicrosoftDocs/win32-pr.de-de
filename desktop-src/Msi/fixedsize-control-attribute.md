---
description: Wenn das Steuerelement "FixedSize" festgelegt ist, wird das Bild auf das Steuerelement zugeschnitten oder zentriert, ohne seine Form oder Größe zu ändern.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: FixedSize-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751144"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="38bbd-103">FixedSize-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="38bbd-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="38bbd-104">Wenn das Steuerelement "FixedSize" festgelegt ist, wird das Bild auf das Steuerelement zugeschnitten oder zentriert, ohne seine Form oder Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="38bbd-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="38bbd-105">Wenn dieses Bit nicht festgelegt ist, wird das Bild gestreckt, um es an das Steuerelement anzupassen.</span><span class="sxs-lookup"><span data-stu-id="38bbd-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="38bbd-106">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="38bbd-106">Valid Controls</span></span>

[<span data-ttu-id="38bbd-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="38bbd-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="38bbd-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="38bbd-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="38bbd-109">Symbol:</span><span class="sxs-lookup"><span data-stu-id="38bbd-109">Icon</span></span>](icon-control.md)

[<span data-ttu-id="38bbd-110">PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="38bbd-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="38bbd-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="38bbd-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="38bbd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="38bbd-112">Value</span></span>



| <span data-ttu-id="38bbd-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="38bbd-113">Decimal</span></span> | <span data-ttu-id="38bbd-114">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="38bbd-114">Hexadecimal</span></span> | <span data-ttu-id="38bbd-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="38bbd-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="38bbd-116">1048576</span><span class="sxs-lookup"><span data-stu-id="38bbd-116">1048576</span></span> | <span data-ttu-id="38bbd-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="38bbd-117">0x00100000</span></span>  | <span data-ttu-id="38bbd-118">**msidbcontrolattributesfixedsize**</span><span class="sxs-lookup"><span data-stu-id="38bbd-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38bbd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38bbd-119">Remarks</span></span>

<span data-ttu-id="38bbd-120">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das FixedSize-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="38bbd-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="38bbd-121">Das Festlegen des FixedSize-Bits hat keine Auswirkung auf ein [CheckBox](checkbox-control.md), eine [pushtaste](pushbutton-control.md)oder eine [RadioButtonGroup](radiobuttongroup-control.md) , wenn weder die [Bitmap](bitmap-control-attribute.md) noch das [Symbol](icon-control-attribute.md) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="38bbd-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="38bbd-122">Wenn das FixedSize-Bit nicht festgelegt ist, hat dies keine Auswirkung auf ein Symbol Steuerelement oder ein einem Symbol [](iconsize-control-attribute.md) zugeordnetes PUSHBUTTON.</span><span class="sxs-lookup"><span data-stu-id="38bbd-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="38bbd-123">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="38bbd-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



