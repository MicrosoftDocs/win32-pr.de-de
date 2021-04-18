---
description: Wenn dieses Bit in einem Kontrollkästchen oder einer Optionsfeld Gruppe festgelegt ist, wird die Schaltfläche mit der Darstellung einer Schaltfläche "Push" gezeichnet, aber die Logik bleibt unverändert. Wenn das-Bit nicht festgelegt ist, werden die Steuerelemente in Ihrem üblichen Stil gezeichnet.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Pushlike-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351664"
---
# <a name="pushlike-control-attribute"></a><span data-ttu-id="11931-104">Pushlike-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="11931-104">PushLike Control Attribute</span></span>

<span data-ttu-id="11931-105">Wenn dieses Bit in einem Kontrollkästchen oder einer Optionsfeld Gruppe festgelegt ist, wird die Schaltfläche mit der Darstellung einer Schaltfläche "Push" gezeichnet, aber die Logik bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="11931-105">If this bit is set on a check box or a radio button group, the button is drawn with the appearance of a push button, but its logic stays the same.</span></span> <span data-ttu-id="11931-106">Wenn das-Bit nicht festgelegt ist, werden die Steuerelemente in Ihrem üblichen Stil gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="11931-106">If the bit is not set, the controls are drawn in their usual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="11931-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="11931-107">Valid Controls</span></span>

<span data-ttu-id="11931-108">[CheckBox](checkbox-control.md)-[RadioButtonGroup](radiobuttongroup-control.md)</span><span class="sxs-lookup"><span data-stu-id="11931-108">[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)</span></span>

## <a name="value"></a><span data-ttu-id="11931-109">Wert</span><span class="sxs-lookup"><span data-stu-id="11931-109">Value</span></span>



| <span data-ttu-id="11931-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="11931-110">Decimal</span></span> | <span data-ttu-id="11931-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="11931-111">Hexadecimal</span></span> | <span data-ttu-id="11931-112">Konstante</span><span class="sxs-lookup"><span data-stu-id="11931-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="11931-113">131072</span><span class="sxs-lookup"><span data-stu-id="11931-113">131072</span></span>  | <span data-ttu-id="11931-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11931-114">0x00020000</span></span>  | <span data-ttu-id="11931-115">**msidbcontrolattributespushlike**</span><span class="sxs-lookup"><span data-stu-id="11931-115">**msidbControlAttributesPushLike**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11931-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11931-116">Remarks</span></span>

<span data-ttu-id="11931-117">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das pushlike-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="11931-117">To set this attribute on a control, include the PushLike bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="11931-118">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="11931-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



