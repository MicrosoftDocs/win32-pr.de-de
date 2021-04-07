---
description: Wenn das steuerungbit fixedvolume festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle festen internen Festplatten an.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Fixedvolume-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863551"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="427a7-103">Fixedvolume-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="427a7-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="427a7-104">Wenn das steuerungbit fixedvolume festgelegt ist, zeigt das Steuerelement alle an der aktuellen Installation beteiligten Volumes sowie alle festen internen Festplatten an.</span><span class="sxs-lookup"><span data-stu-id="427a7-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="427a7-105">Wenn dieses Bit nicht festgelegt ist, listet das Steuerelement die Volumes in der aktuellen Installation auf.</span><span class="sxs-lookup"><span data-stu-id="427a7-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="427a7-106">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="427a7-106">Valid Controls</span></span>

[<span data-ttu-id="427a7-107">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="427a7-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="427a7-108">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="427a7-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="427a7-109">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="427a7-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="427a7-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="427a7-110">Decimal</span></span> | <span data-ttu-id="427a7-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="427a7-111">Hexadecimal</span></span> | <span data-ttu-id="427a7-112">Konstante</span><span class="sxs-lookup"><span data-stu-id="427a7-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="427a7-113">131072</span><span class="sxs-lookup"><span data-stu-id="427a7-113">131072</span></span>  | <span data-ttu-id="427a7-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="427a7-114">0x00020000</span></span>  | <span data-ttu-id="427a7-115">**msidbcontrolattributesfixedvolume**</span><span class="sxs-lookup"><span data-stu-id="427a7-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="427a7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="427a7-116">Remarks</span></span>

<span data-ttu-id="427a7-117">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das fixedvolume-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="427a7-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="427a7-118">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="427a7-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



