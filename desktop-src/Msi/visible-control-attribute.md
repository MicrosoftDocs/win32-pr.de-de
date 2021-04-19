---
description: Wenn das sichtbare Steuerelement Bit festgelegt ist, wird das Steuerelement im Dialogfeld angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das-Steuerelement im Dialogfeld ausgeblendet. Der sichtbare oder verborgene Zustand des sichtbaren Steuerelement Attributs kann später durch ein Steuerelement Ereignis geändert werden.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Visible-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346510"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="955ff-105">Visible-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="955ff-105">Visible Control Attribute</span></span>

<span data-ttu-id="955ff-106">Wenn das sichtbare Steuerelement Bit festgelegt ist, wird das Steuerelement im Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="955ff-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="955ff-107">Wenn dieses Bit nicht festgelegt ist, wird das-Steuerelement im Dialogfeld ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="955ff-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="955ff-108">Der sichtbare oder verborgene Zustand des sichtbaren Steuerelement Attributs kann später durch ein [Steuerelement Ereignis](control-events.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="955ff-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="955ff-109">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="955ff-109">Valid Controls</span></span>

<span data-ttu-id="955ff-110">Alle-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="955ff-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="955ff-111">Wert</span><span class="sxs-lookup"><span data-stu-id="955ff-111">Value</span></span>



| <span data-ttu-id="955ff-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="955ff-112">Decimal</span></span> | <span data-ttu-id="955ff-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="955ff-113">Hexadecimal</span></span> | <span data-ttu-id="955ff-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="955ff-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="955ff-115">1</span><span class="sxs-lookup"><span data-stu-id="955ff-115">1</span></span>       | <span data-ttu-id="955ff-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="955ff-116">0x00000001</span></span>  | <span data-ttu-id="955ff-117">**msidbcontrolattributesvisible**</span><span class="sxs-lookup"><span data-stu-id="955ff-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="955ff-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="955ff-118">Remarks</span></span>

<span data-ttu-id="955ff-119">Sie können die [Tabelle "ControlCondition](controlcondition-table.md) " verwenden, um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung anzuzeigen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="955ff-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="955ff-120">Sie können ein Steuerelement auch ein-oder ausblenden, indem Sie das Steuerelement einem [ControlEvent](control-events.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="955ff-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="955ff-121">Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner des Ereignisses in der Spalte Ereignis der [Tabelle EventMapping](eventmapping-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="955ff-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="955ff-122">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="955ff-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



