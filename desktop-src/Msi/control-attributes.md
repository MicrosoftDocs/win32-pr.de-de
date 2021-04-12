---
description: Informationen zu Steuerelement Attributen finden Sie unter dem Link zu einem bestimmten Steuerelement, das Sie in-Steuerelementen erstellen müssen, sowie Links zu bestimmten Steuerelement Attributen in den folgenden Listen.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Steuerelement Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347789"
---
# <a name="control-attributes"></a><span data-ttu-id="24ea3-103">Steuerelement Attribute</span><span class="sxs-lookup"><span data-stu-id="24ea3-103">Control Attributes</span></span>

<span data-ttu-id="24ea3-104">Informationen zu Steuerelement Attributen finden Sie unter dem Link zu einem bestimmten Steuerelement, das Sie in-Steuer [Elementen](controls.md) erstellen müssen, sowie Links zu bestimmten Steuerelement Attributen in den folgenden Listen.</span><span class="sxs-lookup"><span data-stu-id="24ea3-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="24ea3-105">Die folgenden Methoden werden zum Angeben der Attribute eines-Steuer Elements verwendet:</span><span class="sxs-lookup"><span data-stu-id="24ea3-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="24ea3-106">Verwenden Sie die [Tabelle "ControlCondition](controlcondition-table.md) ", um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung zu deaktivieren, zu aktivieren, auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="24ea3-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="24ea3-107">Sie können diese Tabelle auch verwenden, um das in der [Dialog Feld Tabelle](dialog-table.md)angegebene Standard Steuerelement zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="24ea3-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="24ea3-108">Abonnieren Sie das Steuerelement für ein ControlEvent in der [Tabelle EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="24ea3-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="24ea3-109">Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner ControlEvent in der Spalte Ereignis dieser Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="24ea3-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="24ea3-110">Legen Sie die Steuerelement-Attributflags für das-Steuerelement in der Attribut-Spalte der [Steuerelement Tabelle](control-table.md)fest.</span><span class="sxs-lookup"><span data-stu-id="24ea3-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="24ea3-111">Dadurch werden die Attribute bei der Erstellung des Steuer Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="24ea3-112">Einige Attribute können nicht für jedes Steuerelement festgelegt werden oder von allen oben genannten Methoden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24ea3-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="24ea3-113">Weitere Informationen finden Sie in den jeweiligen Themen zu Steuerelementen und Attributen.</span><span class="sxs-lookup"><span data-stu-id="24ea3-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="24ea3-114">Die Anfangswerte einiger Steuerelement Attribute können mit Bits in der Steuerelement [Tabelle](control-table.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="24ea3-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="24ea3-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-115">Attribute</span></span>                                          | <span data-ttu-id="24ea3-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-116">Decimal</span></span> | <span data-ttu-id="24ea3-117">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-117">Hexadecimal</span></span> | <span data-ttu-id="24ea3-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="24ea3-119">Bidi</span><span class="sxs-lookup"><span data-stu-id="24ea3-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="24ea3-120">224</span><span class="sxs-lookup"><span data-stu-id="24ea3-120">224</span></span>     | <span data-ttu-id="24ea3-121">0x000000e0</span><span class="sxs-lookup"><span data-stu-id="24ea3-121">0x000000E0</span></span>  | <span data-ttu-id="24ea3-122">**msidbcontrolattributesbidi**</span><span class="sxs-lookup"><span data-stu-id="24ea3-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="24ea3-123">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="24ea3-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="24ea3-124">2</span><span class="sxs-lookup"><span data-stu-id="24ea3-124">2</span></span>       | <span data-ttu-id="24ea3-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="24ea3-125">0x00000002</span></span>  | <span data-ttu-id="24ea3-126">**msidbcontrolattributesaktivierte**</span><span class="sxs-lookup"><span data-stu-id="24ea3-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="24ea3-127">Indirekt</span><span class="sxs-lookup"><span data-stu-id="24ea3-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="24ea3-128">8</span><span class="sxs-lookup"><span data-stu-id="24ea3-128">8</span></span>       | <span data-ttu-id="24ea3-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="24ea3-129">0x00000008</span></span>  | <span data-ttu-id="24ea3-130">**msidbcontrolattributesindirekte**</span><span class="sxs-lookup"><span data-stu-id="24ea3-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="24ea3-131">Integer-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="24ea3-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="24ea3-132">16</span><span class="sxs-lookup"><span data-stu-id="24ea3-132">16</span></span>      | <span data-ttu-id="24ea3-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="24ea3-133">0x00000010</span></span>  | <span data-ttu-id="24ea3-134">**msidbcontrolattributesinteger**</span><span class="sxs-lookup"><span data-stu-id="24ea3-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="24ea3-135">Leftscroll</span><span class="sxs-lookup"><span data-stu-id="24ea3-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="24ea3-136">128</span><span class="sxs-lookup"><span data-stu-id="24ea3-136">128</span></span>     | <span data-ttu-id="24ea3-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="24ea3-137">0x00000080</span></span>  | <span data-ttu-id="24ea3-138">**msidbcontrolattributesleftscroll**</span><span class="sxs-lookup"><span data-stu-id="24ea3-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="24ea3-139">Rechtsbündig</span><span class="sxs-lookup"><span data-stu-id="24ea3-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="24ea3-140">64</span><span class="sxs-lookup"><span data-stu-id="24ea3-140">64</span></span>      | <span data-ttu-id="24ea3-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="24ea3-141">0x00000040</span></span>  | <span data-ttu-id="24ea3-142">**msidbcontrolattributesrightausgerichteten**</span><span class="sxs-lookup"><span data-stu-id="24ea3-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="24ea3-143">Rtlro</span><span class="sxs-lookup"><span data-stu-id="24ea3-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="24ea3-144">32</span><span class="sxs-lookup"><span data-stu-id="24ea3-144">32</span></span>      | <span data-ttu-id="24ea3-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="24ea3-145">0x00000020</span></span>  | <span data-ttu-id="24ea3-146">**msidbcontrolattributesrtlro**</span><span class="sxs-lookup"><span data-stu-id="24ea3-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="24ea3-147">Sunken</span><span class="sxs-lookup"><span data-stu-id="24ea3-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="24ea3-148">4</span><span class="sxs-lookup"><span data-stu-id="24ea3-148">4</span></span>       | <span data-ttu-id="24ea3-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="24ea3-149">0x00000004</span></span>  | <span data-ttu-id="24ea3-150">**msidbcontrolattributess Unken**</span><span class="sxs-lookup"><span data-stu-id="24ea3-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="24ea3-151">Visible</span><span class="sxs-lookup"><span data-stu-id="24ea3-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="24ea3-152">1</span><span class="sxs-lookup"><span data-stu-id="24ea3-152">1</span></span>       | <span data-ttu-id="24ea3-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="24ea3-153">0x00000001</span></span>  | <span data-ttu-id="24ea3-154">**msidbcontrolattributesvisible**</span><span class="sxs-lookup"><span data-stu-id="24ea3-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="24ea3-155">Diese Attribute von Text Steuerelementen werden mit Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="24ea3-156">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-156">Attribute</span></span>                                            | <span data-ttu-id="24ea3-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-157">Decimal</span></span> | <span data-ttu-id="24ea3-158">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-158">Hexadecimal</span></span> | <span data-ttu-id="24ea3-159">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="24ea3-160">Formatsize</span><span class="sxs-lookup"><span data-stu-id="24ea3-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="24ea3-161">524288</span><span class="sxs-lookup"><span data-stu-id="24ea3-161">524288</span></span>  | <span data-ttu-id="24ea3-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="24ea3-162">0x00080000</span></span>  | <span data-ttu-id="24ea3-163">**msidbcontrolattributesformatsize**</span><span class="sxs-lookup"><span data-stu-id="24ea3-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="24ea3-164">NoPrefix</span><span class="sxs-lookup"><span data-stu-id="24ea3-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="24ea3-165">131072</span><span class="sxs-lookup"><span data-stu-id="24ea3-165">131072</span></span>  | <span data-ttu-id="24ea3-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="24ea3-166">0x00020000</span></span>  | <span data-ttu-id="24ea3-167">**msidbcontrolattributesnoprefix**</span><span class="sxs-lookup"><span data-stu-id="24ea3-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="24ea3-168">NoWrap</span><span class="sxs-lookup"><span data-stu-id="24ea3-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="24ea3-169">262144</span><span class="sxs-lookup"><span data-stu-id="24ea3-169">262144</span></span>  | <span data-ttu-id="24ea3-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="24ea3-170">0x00040000</span></span>  | <span data-ttu-id="24ea3-171">**msidbcontrolattributesnowrap**</span><span class="sxs-lookup"><span data-stu-id="24ea3-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="24ea3-172">Kennwort</span><span class="sxs-lookup"><span data-stu-id="24ea3-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="24ea3-173">2097152</span><span class="sxs-lookup"><span data-stu-id="24ea3-173">2097152</span></span> | <span data-ttu-id="24ea3-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="24ea3-174">0x00200000</span></span>  | <span data-ttu-id="24ea3-175">**msidbcontrolattributespasswordinput**</span><span class="sxs-lookup"><span data-stu-id="24ea3-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="24ea3-176">Transparent</span><span class="sxs-lookup"><span data-stu-id="24ea3-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="24ea3-177">65536</span><span class="sxs-lookup"><span data-stu-id="24ea3-177">65536</span></span>   | <span data-ttu-id="24ea3-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="24ea3-178">0x00010000</span></span>  | <span data-ttu-id="24ea3-179">**msidbcontrolattributestransparent**</span><span class="sxs-lookup"><span data-stu-id="24ea3-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="24ea3-180">Userslanguage</span><span class="sxs-lookup"><span data-stu-id="24ea3-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="24ea3-181">1048576</span><span class="sxs-lookup"><span data-stu-id="24ea3-181">1048576</span></span> | <span data-ttu-id="24ea3-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="24ea3-182">0x00100000</span></span>  | <span data-ttu-id="24ea3-183">**msidbcontrolattributesuserslanguage**</span><span class="sxs-lookup"><span data-stu-id="24ea3-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="24ea3-184">Dieses Attribut des ProgressBar-Steuer Elements wird mit einem Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="24ea3-185">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-185">Attribute</span></span>                                      | <span data-ttu-id="24ea3-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-186">Decimal</span></span> | <span data-ttu-id="24ea3-187">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-187">Hexadecimal</span></span> | <span data-ttu-id="24ea3-188">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="24ea3-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="24ea3-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="24ea3-190">65536</span><span class="sxs-lookup"><span data-stu-id="24ea3-190">65536</span></span>   | <span data-ttu-id="24ea3-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="24ea3-191">0x00010000</span></span>  | <span data-ttu-id="24ea3-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="24ea3-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="24ea3-193">Diese Attribute der Steuerelemente Volume und Verzeichnis selectcombo werden mit Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="24ea3-194">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-194">Attribute</span></span>                                                | <span data-ttu-id="24ea3-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-195">Decimal</span></span> | <span data-ttu-id="24ea3-196">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-196">Hexadecimal</span></span> | <span data-ttu-id="24ea3-197">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="24ea3-198">Cdromvolume</span><span class="sxs-lookup"><span data-stu-id="24ea3-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="24ea3-199">524288</span><span class="sxs-lookup"><span data-stu-id="24ea3-199">524288</span></span>  | <span data-ttu-id="24ea3-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="24ea3-200">0x00080000</span></span>  | <span data-ttu-id="24ea3-201">**msidbcontrolattributescdromvolume**</span><span class="sxs-lookup"><span data-stu-id="24ea3-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="24ea3-202">Fixedvolume</span><span class="sxs-lookup"><span data-stu-id="24ea3-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="24ea3-203">131072</span><span class="sxs-lookup"><span data-stu-id="24ea3-203">131072</span></span>  | <span data-ttu-id="24ea3-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="24ea3-204">0x00020000</span></span>  | <span data-ttu-id="24ea3-205">**msidbcontrolattributesfixedvolume**</span><span class="sxs-lookup"><span data-stu-id="24ea3-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="24ea3-206">Floppyvolume</span><span class="sxs-lookup"><span data-stu-id="24ea3-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="24ea3-207">2097152</span><span class="sxs-lookup"><span data-stu-id="24ea3-207">2097152</span></span> | <span data-ttu-id="24ea3-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="24ea3-208">0x00200000</span></span>  | <span data-ttu-id="24ea3-209">**msidbcontrolattributesfloppyvolume**</span><span class="sxs-lookup"><span data-stu-id="24ea3-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="24ea3-210">Ramdiskvolume</span><span class="sxs-lookup"><span data-stu-id="24ea3-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="24ea3-211">1048576</span><span class="sxs-lookup"><span data-stu-id="24ea3-211">1048576</span></span> | <span data-ttu-id="24ea3-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="24ea3-212">0x00100000</span></span>  | <span data-ttu-id="24ea3-213">**msidbcontrolattributesramdiskvolume**</span><span class="sxs-lookup"><span data-stu-id="24ea3-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="24ea3-214">Remotevolume</span><span class="sxs-lookup"><span data-stu-id="24ea3-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="24ea3-215">262144</span><span class="sxs-lookup"><span data-stu-id="24ea3-215">262144</span></span>  | <span data-ttu-id="24ea3-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="24ea3-216">0x00040000</span></span>  | <span data-ttu-id="24ea3-217">**msidbcontrolattributesremotevolume**</span><span class="sxs-lookup"><span data-stu-id="24ea3-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="24ea3-218">Removablevolume</span><span class="sxs-lookup"><span data-stu-id="24ea3-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="24ea3-219">65536</span><span class="sxs-lookup"><span data-stu-id="24ea3-219">65536</span></span>   | <span data-ttu-id="24ea3-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="24ea3-220">0x00010000</span></span>  | <span data-ttu-id="24ea3-221">**msidbcontrolattributesremovablevolume**</span><span class="sxs-lookup"><span data-stu-id="24ea3-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="24ea3-222">Diese Attribute von ListBox-und ComboBox-Steuerelementen werden mit Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="24ea3-223">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-223">Attribute</span></span>                                            | <span data-ttu-id="24ea3-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-224">Decimal</span></span> | <span data-ttu-id="24ea3-225">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-225">Hexadecimal</span></span> | <span data-ttu-id="24ea3-226">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="24ea3-227">Combolist-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="24ea3-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="24ea3-228">131072</span><span class="sxs-lookup"><span data-stu-id="24ea3-228">131072</span></span>  | <span data-ttu-id="24ea3-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="24ea3-229">0x00020000</span></span>  | <span data-ttu-id="24ea3-230">**msidbcontrolattributescombolist**</span><span class="sxs-lookup"><span data-stu-id="24ea3-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="24ea3-231">Sortiertes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="24ea3-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="24ea3-232">65536</span><span class="sxs-lookup"><span data-stu-id="24ea3-232">65536</span></span>   | <span data-ttu-id="24ea3-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="24ea3-233">0x00010000</span></span>  | <span data-ttu-id="24ea3-234">**msidbcontrolattributess orted**</span><span class="sxs-lookup"><span data-stu-id="24ea3-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="24ea3-235">Dieses Attribut des Bearbeitungs Steuer Elements wird mit einem Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="24ea3-236">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-236">Attribute</span></span>                                    | <span data-ttu-id="24ea3-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-237">Decimal</span></span> | <span data-ttu-id="24ea3-238">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-238">Hexadecimal</span></span> | <span data-ttu-id="24ea3-239">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="24ea3-240">Mehrzeiligen</span><span class="sxs-lookup"><span data-stu-id="24ea3-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="24ea3-241">65536</span><span class="sxs-lookup"><span data-stu-id="24ea3-241">65536</span></span>   | <span data-ttu-id="24ea3-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="24ea3-242">0x00010000</span></span>  | <span data-ttu-id="24ea3-243">**msidbcontrolattributesmultiline**</span><span class="sxs-lookup"><span data-stu-id="24ea3-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="24ea3-244">Diese Attribute der PictureButton-Steuerelemente werden mit Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="24ea3-245">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-245">Attribute</span></span>                                          | <span data-ttu-id="24ea3-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-246">Decimal</span></span> | <span data-ttu-id="24ea3-247">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-247">Hexadecimal</span></span> | <span data-ttu-id="24ea3-248">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="24ea3-249">Bitmap</span><span class="sxs-lookup"><span data-stu-id="24ea3-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="24ea3-250">262144</span><span class="sxs-lookup"><span data-stu-id="24ea3-250">262144</span></span>  | <span data-ttu-id="24ea3-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="24ea3-251">0x00040000</span></span>  | <span data-ttu-id="24ea3-252">**msidbcontrolattributesbitmap**</span><span class="sxs-lookup"><span data-stu-id="24ea3-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="24ea3-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="24ea3-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="24ea3-254">1048576</span><span class="sxs-lookup"><span data-stu-id="24ea3-254">1048576</span></span> | <span data-ttu-id="24ea3-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="24ea3-255">0x00100000</span></span>  | <span data-ttu-id="24ea3-256">**msidbcontrolattributesfixedsize**</span><span class="sxs-lookup"><span data-stu-id="24ea3-256">**msidbControlAttributesFixedSize**</span></span>  |
| [<span data-ttu-id="24ea3-257">Symbol:</span><span class="sxs-lookup"><span data-stu-id="24ea3-257">Icon</span></span>](icon-control-attribute.md)                 | <span data-ttu-id="24ea3-258">524288</span><span class="sxs-lookup"><span data-stu-id="24ea3-258">524288</span></span>  | <span data-ttu-id="24ea3-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="24ea3-259">0x00080000</span></span>  | <span data-ttu-id="24ea3-260">**msidbcontrolattributesicon**</span><span class="sxs-lookup"><span data-stu-id="24ea3-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="24ea3-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="24ea3-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="24ea3-262">2097152</span><span class="sxs-lookup"><span data-stu-id="24ea3-262">2097152</span></span> | <span data-ttu-id="24ea3-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="24ea3-263">0x00200000</span></span>  | <span data-ttu-id="24ea3-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="24ea3-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="24ea3-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="24ea3-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="24ea3-266">4194304</span><span class="sxs-lookup"><span data-stu-id="24ea3-266">4194304</span></span> | <span data-ttu-id="24ea3-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="24ea3-267">0x00400000</span></span>  | <span data-ttu-id="24ea3-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="24ea3-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="24ea3-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="24ea3-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="24ea3-270">6291456</span><span class="sxs-lookup"><span data-stu-id="24ea3-270">6291456</span></span> | <span data-ttu-id="24ea3-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="24ea3-271">0x00600000</span></span>  | <span data-ttu-id="24ea3-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="24ea3-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="24ea3-273">Pushlike-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="24ea3-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="24ea3-274">131072</span><span class="sxs-lookup"><span data-stu-id="24ea3-274">131072</span></span>  | <span data-ttu-id="24ea3-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="24ea3-275">0x00020000</span></span>  | <span data-ttu-id="24ea3-276">**msidbcontrolattributespushlike**</span><span class="sxs-lookup"><span data-stu-id="24ea3-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="24ea3-277">Dieses Attribut des RadioButton-Steuer Elements wird mit einem Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="24ea3-278">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-278">Attribute</span></span>                                    | <span data-ttu-id="24ea3-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-279">Decimal</span></span>  | <span data-ttu-id="24ea3-280">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-280">Hexadecimal</span></span> | <span data-ttu-id="24ea3-281">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="24ea3-282">HasBorder</span><span class="sxs-lookup"><span data-stu-id="24ea3-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="24ea3-283">16777216</span><span class="sxs-lookup"><span data-stu-id="24ea3-283">16777216</span></span> | <span data-ttu-id="24ea3-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="24ea3-284">0x01000000</span></span>  | <span data-ttu-id="24ea3-285">**msidbcontrolattributeshasborder**</span><span class="sxs-lookup"><span data-stu-id="24ea3-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="24ea3-286">Dieses Attribut des PUSHBUTTON-Steuer Elements wird mit einem Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="24ea3-287">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-287">Attribute</span></span>                                        | <span data-ttu-id="24ea3-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-288">Decimal</span></span> | <span data-ttu-id="24ea3-289">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-289">Hexadecimal</span></span> | <span data-ttu-id="24ea3-290">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="24ea3-291">Elevationshield</span><span class="sxs-lookup"><span data-stu-id="24ea3-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="24ea3-292">8388608</span><span class="sxs-lookup"><span data-stu-id="24ea3-292">8388608</span></span> | <span data-ttu-id="24ea3-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="24ea3-293">0x00800000</span></span>  | <span data-ttu-id="24ea3-294">**msidbcontrolattributeselevationshield**</span><span class="sxs-lookup"><span data-stu-id="24ea3-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="24ea3-295">Dieses Attribut des volumecostlist-Steuer Elements wird mit einem Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="24ea3-296">Attribut</span><span class="sxs-lookup"><span data-stu-id="24ea3-296">Attribute</span></span>                                                                | <span data-ttu-id="24ea3-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-297">Decimal</span></span> | <span data-ttu-id="24ea3-298">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="24ea3-298">Hexadecimal</span></span> | <span data-ttu-id="24ea3-299">Konstante</span><span class="sxs-lookup"><span data-stu-id="24ea3-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="24ea3-300">Controlshowrollbackcost</span><span class="sxs-lookup"><span data-stu-id="24ea3-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="24ea3-301">4194304</span><span class="sxs-lookup"><span data-stu-id="24ea3-301">4194304</span></span> | <span data-ttu-id="24ea3-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="24ea3-302">0x00400000</span></span>  | <span data-ttu-id="24ea3-303">**msidbcontrolshowrollbackcost**</span><span class="sxs-lookup"><span data-stu-id="24ea3-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="24ea3-304">Die folgenden Steuerelement Attribute sind nicht mit Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="24ea3-305">Diese Attribute werden in den Benutzeroberflächen Tabellen erstellt oder mithilfe von [Steuerelement Ereignissen](control-events.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24ea3-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="24ea3-306">Billboardname</span><span class="sxs-lookup"><span data-stu-id="24ea3-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="24ea3-307">Derekpropertyname</span><span class="sxs-lookup"><span data-stu-id="24ea3-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="24ea3-308">Position</span><span class="sxs-lookup"><span data-stu-id="24ea3-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="24ea3-309">Fortschrittskontrolle</span><span class="sxs-lookup"><span data-stu-id="24ea3-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="24ea3-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="24ea3-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="24ea3-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="24ea3-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="24ea3-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="24ea3-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="24ea3-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="24ea3-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="24ea3-314">Siehe [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="24ea3-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 



