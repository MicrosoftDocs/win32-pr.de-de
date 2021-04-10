---
description: Eine Symbol Datei kann verschiedene Größen desselben Symbol Bilds enthalten.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Ikonsistze-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042145"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="fc80d-103">Ikonsistze-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="fc80d-103">IconSize Control Attribute</span></span>

<span data-ttu-id="fc80d-104">Eine Symbol Datei kann verschiedene Größen desselben Symbol Bilds enthalten.</span><span class="sxs-lookup"><span data-stu-id="fc80d-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="fc80d-105">Diese Bits geben an, welche Größe des Symbol Bilds geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc80d-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="fc80d-106">Wenn keines der Bits festgelegt ist, wird das erste Bild geladen.</span><span class="sxs-lookup"><span data-stu-id="fc80d-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="fc80d-107">Wenn nur **msidbControlAttributesIconSize16** festgelegt ist, wird das erste 16x16-Bild geladen.</span><span class="sxs-lookup"><span data-stu-id="fc80d-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="fc80d-108">Wenn nur **msidbControlAttributesIconSize32** festgelegt ist, wird das erste 32x32-Bild geladen.</span><span class="sxs-lookup"><span data-stu-id="fc80d-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="fc80d-109">Wenn **msidbControlAttributesIconSize48** festgelegt ist, wird das erste 48-Bild geladen.</span><span class="sxs-lookup"><span data-stu-id="fc80d-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fc80d-110">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="fc80d-110">Valid Controls</span></span>

[<span data-ttu-id="fc80d-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="fc80d-111">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="fc80d-112">Symbol:</span><span class="sxs-lookup"><span data-stu-id="fc80d-112">Icon</span></span>](icon-control.md)

[<span data-ttu-id="fc80d-113">PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="fc80d-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="fc80d-114">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="fc80d-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="fc80d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fc80d-115">Value</span></span>



| <span data-ttu-id="fc80d-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="fc80d-116">Decimal</span></span> | <span data-ttu-id="fc80d-117">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="fc80d-117">Hexadecimal</span></span> | <span data-ttu-id="fc80d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc80d-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="fc80d-119">2097152</span><span class="sxs-lookup"><span data-stu-id="fc80d-119">2097152</span></span> | <span data-ttu-id="fc80d-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="fc80d-120">0x00200000</span></span>  | <span data-ttu-id="fc80d-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="fc80d-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="fc80d-122">4194304</span><span class="sxs-lookup"><span data-stu-id="fc80d-122">4194304</span></span> | <span data-ttu-id="fc80d-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="fc80d-123">0x00400000</span></span>  | <span data-ttu-id="fc80d-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="fc80d-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="fc80d-125">6291456</span><span class="sxs-lookup"><span data-stu-id="fc80d-125">6291456</span></span> | <span data-ttu-id="fc80d-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="fc80d-126">0x00600000</span></span>  | <span data-ttu-id="fc80d-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="fc80d-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fc80d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc80d-128">Remarks</span></span>

<span data-ttu-id="fc80d-129">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die ikonsistze-Bits in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="fc80d-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="fc80d-130">Wenn das [FixedSize](fixedsize-control-attribute.md) -Bit nicht festgelegt ist, wird das geladene Bild verkleinert oder gestreckt, um es an das Symbol Steuerelement anzupassen.</span><span class="sxs-lookup"><span data-stu-id="fc80d-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="fc80d-131">Wenn das [FixedSize](fixedsize-control-attribute.md) -Bit festgelegt ist und das geladene Bild kleiner als das Symbol Steuerelement ist, wird das Bild im-Steuerelement zentriert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc80d-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="fc80d-132">Wenn das [FixedSize](fixedsize-control-attribute.md) -Bit festgelegt ist und das geladene Bild größer als das Symbol Steuerelement ist, wird das Bild so reduziert, dass es dem Steuerelement entspricht.</span><span class="sxs-lookup"><span data-stu-id="fc80d-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="fc80d-133">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc80d-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



