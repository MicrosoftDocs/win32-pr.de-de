---
description: Dies ist eine Kombination aus der von rechts nach links gelesenen Lesefolge rtlro, den Attributen rightausgerichtete und leftscroll.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Bidi-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357523"
---
# <a name="bidi-control-attribute"></a><span data-ttu-id="a6d8d-103">Bidi-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="a6d8d-103">BiDi Control Attribute</span></span>

<span data-ttu-id="a6d8d-104">Dies ist eine Kombination aus der von rechts nach links gelesenen Lesefolge [rtlro](rtlro-control-attribute.md), den Attributen [rightausgerichtete](rightaligned-control-attribute.md)und [leftscroll](leftscroll-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d8d-104">This is a combination of the right-to-left reading order [RTLRO](rtlro-control-attribute.md), the [RightAligned](rightaligned-control-attribute.md), and [LeftScroll](leftscroll-control-attribute.md) attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="a6d8d-105">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a6d8d-105">Valid Controls</span></span>

[<span data-ttu-id="a6d8d-106">Scrollabletext</span><span class="sxs-lookup"><span data-stu-id="a6d8d-106">ScrollableText</span></span>](scrollabletext-control.md)

 

[<span data-ttu-id="a6d8d-107">Volumecostlist</span><span class="sxs-lookup"><span data-stu-id="a6d8d-107">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="a6d8d-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="a6d8d-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="a6d8d-109">Directoren auflisten</span><span class="sxs-lookup"><span data-stu-id="a6d8d-109">DirectoryList</span></span>](directorylist-control.md)

 

[<span data-ttu-id="a6d8d-110">Directoriycombo</span><span class="sxs-lookup"><span data-stu-id="a6d8d-110">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="a6d8d-111">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="a6d8d-111">Edit</span></span>](edit-control.md)

 

[<span data-ttu-id="a6d8d-112">ListBox</span><span class="sxs-lookup"><span data-stu-id="a6d8d-112">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="a6d8d-113">ListView</span><span class="sxs-lookup"><span data-stu-id="a6d8d-113">ListView</span></span>](listview-control.md)

 

[<span data-ttu-id="a6d8d-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="a6d8d-114">SelectionTree</span></span>](selectiontree-control.md)

 

[<span data-ttu-id="a6d8d-115">Volumeselectcombo</span><span class="sxs-lookup"><span data-stu-id="a6d8d-115">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="a6d8d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a6d8d-116">Value</span></span>



| <span data-ttu-id="a6d8d-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="a6d8d-117">Decimal</span></span> | <span data-ttu-id="a6d8d-118">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="a6d8d-118">Hexadecimal</span></span> | <span data-ttu-id="a6d8d-119">Konstante</span><span class="sxs-lookup"><span data-stu-id="a6d8d-119">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="a6d8d-120">224</span><span class="sxs-lookup"><span data-stu-id="a6d8d-120">224</span></span>     | <span data-ttu-id="a6d8d-121">0x000000e0</span><span class="sxs-lookup"><span data-stu-id="a6d8d-121">0x000000E0</span></span>  | <span data-ttu-id="a6d8d-122">**msidbcontrolattributesbidi**</span><span class="sxs-lookup"><span data-stu-id="a6d8d-122">**msidbControlAttributesBiDi**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a6d8d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6d8d-123">Remarks</span></span>

<span data-ttu-id="a6d8d-124">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das Bidi-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-124">To set this attribute on a control, include the BiDi bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="a6d8d-125">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="a6d8d-125">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



