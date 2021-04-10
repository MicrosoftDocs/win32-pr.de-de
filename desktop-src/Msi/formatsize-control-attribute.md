---
description: Wenn dieses Bit für ein statisches Text Steuerelement festgelegt ist, versucht das-Steuerelement automatisch, den angezeigten Text als Zahl zu formatieren, die die Anzahl von Bytes darstellt.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formatsize-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215121"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="4ca19-103">Formatsize-Steuerelement Attribut</span><span class="sxs-lookup"><span data-stu-id="4ca19-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="4ca19-104">Wenn dieses Bit für ein statisches Text Steuerelement festgelegt ist, versucht das-Steuerelement automatisch, den angezeigten Text als Zahl zu formatieren, die die Anzahl von Bytes darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ca19-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="4ca19-105">Für eine ordnungsgemäße Formatierung muss der Text des Steuer Elements auf eine Zeichenfolge festgelegt werden, die eine Zahl darstellt, die in Einheiten von 512 Byte ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca19-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="4ca19-106">Der angezeigte Wert wird dann in Kilobyte (KB), Megabyte (MB) oder Gigabyte (GB) formatiert und mit der entsprechenden Zeichenfolge angezeigt, die die Einheiten darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ca19-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="4ca19-107">Weitere Informationen finden Sie unter [Text-Steuer](text-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="4ca19-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="4ca19-108">Numerischer Wert von ursprünglichem Text</span><span class="sxs-lookup"><span data-stu-id="4ca19-108">Numerical value of original text</span></span> | <span data-ttu-id="4ca19-109">Verwendete Einheiten Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ca19-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="4ca19-110">Kleiner als 20480</span><span class="sxs-lookup"><span data-stu-id="4ca19-110">Less than 20480</span></span>                  | <span data-ttu-id="4ca19-111">KB</span><span class="sxs-lookup"><span data-stu-id="4ca19-111">KB</span></span>               |
| <span data-ttu-id="4ca19-112">Kleiner als 20971520</span><span class="sxs-lookup"><span data-stu-id="4ca19-112">Less than 20971520</span></span>               | <span data-ttu-id="4ca19-113">MB</span><span class="sxs-lookup"><span data-stu-id="4ca19-113">MB</span></span>               |
| <span data-ttu-id="4ca19-114">Kleiner als 10737418240</span><span class="sxs-lookup"><span data-stu-id="4ca19-114">Less than 10737418240</span></span>            | <span data-ttu-id="4ca19-115">GB</span><span class="sxs-lookup"><span data-stu-id="4ca19-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="4ca19-116">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="4ca19-116">Valid Controls</span></span>



| <span data-ttu-id="4ca19-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="4ca19-117">Decimal</span></span> | <span data-ttu-id="4ca19-118">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="4ca19-118">Hexadecimal</span></span> | <span data-ttu-id="4ca19-119">Control</span><span class="sxs-lookup"><span data-stu-id="4ca19-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="4ca19-120">524288</span><span class="sxs-lookup"><span data-stu-id="4ca19-120">524288</span></span>  | <span data-ttu-id="4ca19-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="4ca19-121">0x00080000</span></span>  | <span data-ttu-id="4ca19-122">msidbcontrolattributesformatsize</span><span class="sxs-lookup"><span data-stu-id="4ca19-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4ca19-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ca19-123">Remarks</span></span>

<span data-ttu-id="4ca19-124">Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die formatsize-Bits in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="4ca19-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="4ca19-125">Der Text des Steuer Elements muss auf eine Zeichenfolge festgelegt werden, die eine Zahl darstellt, die in Einheiten von 512 Byte ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca19-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="4ca19-126">Der Text der Einheiten Zeichenfolgen wird in der [UIText-Tabelle](uitext-table.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="4ca19-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="4ca19-127">Die Positionierung der Einheiten Zeichenfolge wird von der [**leftunit**](leftunit.md) -Eigenschaft gesteuert.</span><span class="sxs-lookup"><span data-stu-id="4ca19-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="4ca19-128">Wenn die Eigenschaft " **leftunit** " als beliebiger Wert definiert ist, wird die Einheiten Zeichenfolge vor dem numerischen Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ca19-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="4ca19-129">Wenn im Text, der dem Steuerelement zugeordnet ist, etwas anderes als numerische Zeichen angezeigt wird, ist der angezeigte Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4ca19-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="4ca19-130">Zur Laufzeit löst das Installationsprogramm die Eigenschaft [**primaryvolumespacerequired**](primaryvolumespacerequired.md) auf die Gesamtanzahl der Bytes auf, die für die Installation in Einheiten von 512 benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca19-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="4ca19-131">Ein statisches Text Steuerelement mit formatsize Bit kann verwendet werden, um die Gesamtanzahl von Bytes, die für die Installation erforderlich sind, nach Bedarf automatisch in KB, MB oder GB zu formatieren und zu bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="4ca19-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="4ca19-132">Nehmen Sie für die Zwecke dieses Beispiels an, dass die Gesamtzahl der Bytes 18.336.768 beträgt.</span><span class="sxs-lookup"><span data-stu-id="4ca19-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="4ca19-133">Der Installer legt den Wert der Eigenschaft primaryvolumespacerequired auf 18.336.768 dividiert durch 512 oder 35.814 fest.</span><span class="sxs-lookup"><span data-stu-id="4ca19-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="4ca19-134">Die vom Text-Steuerelement mit formatsize angezeigte Zahl beträgt 17 MB.</span><span class="sxs-lookup"><span data-stu-id="4ca19-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="4ca19-135">Die numerischen Werte des ursprünglichen Texts werden in den Einheiten 512 angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ca19-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="4ca19-136">In der obigen Tabelle entspricht die Zeichenfolge 20.480 der KB-Zeichenfolge, da 20.480 mal 512 das Ergebnis 10.485.760 Bytes oder 10.240 KB ergibt.</span><span class="sxs-lookup"><span data-stu-id="4ca19-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="4ca19-137">Die in der vorherigen Tabelle aufgeführten Einheiten Zeichenfolgen beziehen sich auf Schlüssel in der [UIText-Tabelle](uitext-table.md), in der der Text der Einheits Zeichenfolge definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ca19-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="4ca19-138">Die Positionierung der Einheiten Zeichenfolge wird von der [**leftunit**](leftunit.md) -Eigenschaft gesteuert.</span><span class="sxs-lookup"><span data-stu-id="4ca19-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="4ca19-139">Wenn die Eigenschaft " **leftunit** " als beliebiger Wert definiert ist, wird die Einheiten Zeichenfolge vor dem numerischen Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ca19-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="4ca19-140">Wenn im Text, der dem Steuerelement zugeordnet ist, etwas anderes als numerische Zeichen angezeigt wird, ist der angezeigte Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4ca19-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="4ca19-141">Weitere Informationen finden Sie unter [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).</span><span class="sxs-lookup"><span data-stu-id="4ca19-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



