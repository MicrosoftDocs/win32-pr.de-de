---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Wechsel Datenträger an. Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Removablevolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751128"
---
# <a name="removablevolume-control-attribute"></a><span data-ttu-id="30c9a-104">Removablevolume-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="30c9a-104">RemovableVolume Control Attribute</span></span>

<span data-ttu-id="30c9a-105">Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Wechsel Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="30c9a-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the removable volumes.</span></span> <span data-ttu-id="30c9a-106">Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.</span><span class="sxs-lookup"><span data-stu-id="30c9a-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="30c9a-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="30c9a-107">Valid Controls</span></span>

[<span data-ttu-id="30c9a-108">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="30c9a-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="30c9a-109">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="30c9a-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="30c9a-110">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="30c9a-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="30c9a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="30c9a-111">Value</span></span>



| <span data-ttu-id="30c9a-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="30c9a-112">Decimal</span></span> | <span data-ttu-id="30c9a-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="30c9a-113">Hexadecimal</span></span> | <span data-ttu-id="30c9a-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="30c9a-114">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="30c9a-115">65536</span><span class="sxs-lookup"><span data-stu-id="30c9a-115">65536</span></span>   | <span data-ttu-id="30c9a-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="30c9a-116">0x00010000</span></span>  | <span data-ttu-id="30c9a-117">**msidbcontrolattributesremovablevolume**</span><span class="sxs-lookup"><span data-stu-id="30c9a-117">**msidbControlAttributesRemovableVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="30c9a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30c9a-118">Remarks</span></span>

<span data-ttu-id="30c9a-119">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das removablevolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="30c9a-119">To set this attribute on a control, include the RemovableVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="30c9a-120">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="30c9a-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



