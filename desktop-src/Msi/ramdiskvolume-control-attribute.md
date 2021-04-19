---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle RAM-Datenträgervolumes an. Wenn dieses Bit nicht festgelegt ist, werden vom Steuerelement Volumes in der aktuellen Installation aufgelistet.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Ramdiskvolume-Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363450"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="58da5-104">Ramdiskvolume-Steuerungs Attribut</span><span class="sxs-lookup"><span data-stu-id="58da5-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="58da5-105">Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle RAM-Datenträgervolumes an.</span><span class="sxs-lookup"><span data-stu-id="58da5-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="58da5-106">Wenn dieses Bit nicht festgelegt ist, werden vom Steuerelement Volumes in der aktuellen Installation aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58da5-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="58da5-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="58da5-107">Valid Controls</span></span>

[<span data-ttu-id="58da5-108">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="58da5-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="58da5-109">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="58da5-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="58da5-110">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="58da5-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="58da5-111">Wert</span><span class="sxs-lookup"><span data-stu-id="58da5-111">Value</span></span>



| <span data-ttu-id="58da5-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="58da5-112">Decimal</span></span> | <span data-ttu-id="58da5-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="58da5-113">Hexadecimal</span></span> | <span data-ttu-id="58da5-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="58da5-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="58da5-115">1048567</span><span class="sxs-lookup"><span data-stu-id="58da5-115">1048567</span></span> | <span data-ttu-id="58da5-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="58da5-116">0x00100000</span></span>  | <span data-ttu-id="58da5-117">**msidbcontrolattributesramdiskvolume**</span><span class="sxs-lookup"><span data-stu-id="58da5-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="58da5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58da5-118">Remarks</span></span>

<span data-ttu-id="58da5-119">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das ramdiskvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="58da5-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="58da5-120">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="58da5-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



