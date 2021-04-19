---
description: Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Remotevolumes an. Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Remotevolume-Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353046"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="fb80b-104">Remotevolume-Steuerungs Attribut</span><span class="sxs-lookup"><span data-stu-id="fb80b-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="fb80b-105">Wenn dieses Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Remotevolumes an.</span><span class="sxs-lookup"><span data-stu-id="fb80b-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="fb80b-106">Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.</span><span class="sxs-lookup"><span data-stu-id="fb80b-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fb80b-107">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="fb80b-107">Valid Controls</span></span>

[<span data-ttu-id="fb80b-108">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="fb80b-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="fb80b-109">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="fb80b-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="fb80b-110">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="fb80b-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="fb80b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="fb80b-111">Value</span></span>



| <span data-ttu-id="fb80b-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="fb80b-112">Decimal</span></span> | <span data-ttu-id="fb80b-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="fb80b-113">Hexadecimal</span></span> | <span data-ttu-id="fb80b-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="fb80b-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="fb80b-115">262144</span><span class="sxs-lookup"><span data-stu-id="fb80b-115">262144</span></span>  | <span data-ttu-id="fb80b-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="fb80b-116">0x00040000</span></span>  | <span data-ttu-id="fb80b-117">**msidbcontrolattributesremotevolume**</span><span class="sxs-lookup"><span data-stu-id="fb80b-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb80b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb80b-118">Remarks</span></span>

<span data-ttu-id="fb80b-119">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das Remotevolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="fb80b-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="fb80b-120">Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="fb80b-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



