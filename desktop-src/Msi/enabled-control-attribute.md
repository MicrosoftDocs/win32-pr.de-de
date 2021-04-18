---
description: Dieses Attribut gibt an, ob das angegebene Steuerelement aktiviert oder deaktiviert ist. Die meisten Steuerelemente werden bei deaktiviertem grau angezeigt.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Aktiviertes Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347878"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="3434f-104">Aktiviertes Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="3434f-104">Enabled Control Attribute</span></span>

<span data-ttu-id="3434f-105">Dieses Attribut gibt an, ob das angegebene Steuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3434f-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="3434f-106">Die meisten Steuerelemente werden bei deaktiviertem grau angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3434f-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="3434f-107">Wenn dieses Bit festgelegt ist, wird das Steuerelement als aktiviert erstellt.</span><span class="sxs-lookup"><span data-stu-id="3434f-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="3434f-108">Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement als deaktiviert erstellt.</span><span class="sxs-lookup"><span data-stu-id="3434f-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="3434f-109">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3434f-109">Valid Controls</span></span>

<span data-ttu-id="3434f-110">Alle-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3434f-110">All controls.</span></span> <span data-ttu-id="3434f-111">Die Darstellung einiger Steuerelemente, die keiner Eigenschaft zugeordnet sind, wie z. b. Bitmaps und Symbole, ist nicht durch Festlegen dieses Attributs beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="3434f-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="3434f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3434f-112">Value</span></span>



| <span data-ttu-id="3434f-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="3434f-113">Decimal</span></span> | <span data-ttu-id="3434f-114">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="3434f-114">Hexadecimal</span></span> | <span data-ttu-id="3434f-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="3434f-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="3434f-116">2</span><span class="sxs-lookup"><span data-stu-id="3434f-116">2</span></span>       | <span data-ttu-id="3434f-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3434f-117">0x00000002</span></span>  | <span data-ttu-id="3434f-118">**msidbcontrolattributesaktivierte**</span><span class="sxs-lookup"><span data-stu-id="3434f-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3434f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3434f-119">Remarks</span></span>

<span data-ttu-id="3434f-120">Sie können auch die [Tabelle "ControlCondition](controlcondition-table.md) " verwenden, um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung zu deaktivieren oder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3434f-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="3434f-121">Sie können ein Steuerelement auch aktivieren oder deaktivieren, indem Sie das Steuerelement mit einem [ControlEvent](control-events.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="3434f-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="3434f-122">Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner des Ereignisses in der Spalte Ereignis der [Tabelle EventMapping](eventmapping-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="3434f-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="3434f-123">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="3434f-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



