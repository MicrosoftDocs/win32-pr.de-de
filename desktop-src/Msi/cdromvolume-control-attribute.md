---
description: Wenn das cdromvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation sowie alle CD-ROM-Volumes an.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Cdromvolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357519"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="31fe4-103">Cdromvolume-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="31fe4-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="31fe4-104">Wenn das cdromvolume-Steuerungs Bit festgelegt ist, zeigt das Steuerelement alle Volumes in der aktuellen Installation sowie alle CD-ROM-Volumes an.</span><span class="sxs-lookup"><span data-stu-id="31fe4-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="31fe4-105">Wenn dieses Bit nicht festgelegt ist, zeigt das-Steuerelement alle Volumes in der aktuellen-Installation an.</span><span class="sxs-lookup"><span data-stu-id="31fe4-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="31fe4-106">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="31fe4-106">Valid Controls</span></span>

[<span data-ttu-id="31fe4-107">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="31fe4-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="31fe4-108">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="31fe4-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="31fe4-109">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="31fe4-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="31fe4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="31fe4-110">Value</span></span>



| <span data-ttu-id="31fe4-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="31fe4-111">Decimal</span></span> | <span data-ttu-id="31fe4-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="31fe4-112">Hexadecimal</span></span> | <span data-ttu-id="31fe4-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="31fe4-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="31fe4-114">524288</span><span class="sxs-lookup"><span data-stu-id="31fe4-114">524288</span></span>  | <span data-ttu-id="31fe4-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="31fe4-115">0x00080000</span></span>  | <span data-ttu-id="31fe4-116">**msidbcontrolattributescdromvolume**</span><span class="sxs-lookup"><span data-stu-id="31fe4-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="31fe4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31fe4-117">Remarks</span></span>

<span data-ttu-id="31fe4-118">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das cdromvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="31fe4-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="31fe4-119">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="31fe4-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



