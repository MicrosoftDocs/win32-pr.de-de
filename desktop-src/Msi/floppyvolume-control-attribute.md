---
description: Wenn das floppyvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Disketten Volumes an.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Floppyvolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528184"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="7579f-103">Floppyvolume-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="7579f-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="7579f-104">Wenn das floppyvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle Disketten Volumes an.</span><span class="sxs-lookup"><span data-stu-id="7579f-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="7579f-105">Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement Volumes in der aktuellen Installation auf.</span><span class="sxs-lookup"><span data-stu-id="7579f-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="7579f-106">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7579f-106">Valid Controls</span></span>

[<span data-ttu-id="7579f-107">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="7579f-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="7579f-108">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="7579f-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="7579f-109">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="7579f-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="7579f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7579f-110">Value</span></span>



| <span data-ttu-id="7579f-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="7579f-111">Decimal</span></span> | <span data-ttu-id="7579f-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="7579f-112">Hexadecimal</span></span> | <span data-ttu-id="7579f-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="7579f-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="7579f-114">2097152</span><span class="sxs-lookup"><span data-stu-id="7579f-114">2097152</span></span> | <span data-ttu-id="7579f-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="7579f-115">0x00200000</span></span>  | <span data-ttu-id="7579f-116">**msidbcontrolattributesfloppyvolume**</span><span class="sxs-lookup"><span data-stu-id="7579f-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7579f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7579f-117">Remarks</span></span>

<span data-ttu-id="7579f-118">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das floppyvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="7579f-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="7579f-119">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="7579f-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



