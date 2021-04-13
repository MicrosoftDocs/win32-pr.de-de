---
description: Die CIM- \_ Slot-Klasse stellt Connectors dar, in die Pakete eingefügt werden.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483830"
---
# <a name="cim_slot-class"></a><span data-ttu-id="5b046-103">CIM- \_ Slot-Klasse</span><span class="sxs-lookup"><span data-stu-id="5b046-103">CIM\_Slot class</span></span>

<span data-ttu-id="5b046-104">Die **CIM- \_ Slot** -Klasse stellt Connectors dar, in die Pakete eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="5b046-105">Beispielsweise kann ein physisches Paket, das ein Laufwerk ist, in einen SCA-Slot eingefügt werden, oder eine Karte (eine Unterklasse von [CIM \_ physicalpackage](cim-physicalpackage.md)) kann in einen 16-, 32-oder 64-Bit-Erweiterungs Slot auf einem hostingboard eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="5b046-106">PCI-oder PCMCIA-Typ-III-Slots sind Beispiele für letztere.</span><span class="sxs-lookup"><span data-stu-id="5b046-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b046-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b046-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b046-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5b046-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b046-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5b046-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5b046-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b046-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b046-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="5b046-112">Member</span><span class="sxs-lookup"><span data-stu-id="5b046-112">Members</span></span>

<span data-ttu-id="5b046-113">Die **CIM- \_ Slot** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5b046-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="5b046-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b046-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b046-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b046-115">Properties</span></span>

<span data-ttu-id="5b046-116">Die **CIM- \_ Slot** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b046-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b046-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5b046-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5b046-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-121">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5b046-121">Short textual description of the object.</span></span>

<span data-ttu-id="5b046-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-123">**Connectoriout**</span><span class="sxs-lookup"><span data-stu-id="5b046-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b046-126">Eine frei Form Zeichenfolge, die die PIN-Konfiguration und die Signal Verwendung eines physischen Verbindungs Zeichens beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5b046-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="5b046-127">Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-128">**Connector Type**</span><span class="sxs-lookup"><span data-stu-id="5b046-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-129">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="5b046-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5b046-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-131">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Connector Type"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,2 ")</span><span class="sxs-lookup"><span data-stu-id="5b046-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-132">Typ des physischen Verbindungs Typs.</span><span class="sxs-lookup"><span data-stu-id="5b046-132">Type of physical connector.</span></span> <span data-ttu-id="5b046-133">Ein Array wird angegeben, um die Beschreibung von Kombinationen aus Connector-Informationen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="5b046-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="5b046-134">Beispielsweise könnte ein Array Eintrag RS-232, eine andere DB-25 und ein drittes den Connector als "männlich" definieren.</span><span class="sxs-lookup"><span data-stu-id="5b046-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="5b046-135">Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="5b046-136">0</span><span class="sxs-lookup"><span data-stu-id="5b046-136">0</span></span>
</dt> <dd>

<span data-ttu-id="5b046-137">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="5b046-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="5b046-138">1</span><span class="sxs-lookup"><span data-stu-id="5b046-138">1</span></span>
</dt> <dd>

<span data-ttu-id="5b046-139">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="5b046-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="5b046-140">2</span><span class="sxs-lookup"><span data-stu-id="5b046-140">2</span></span>
</dt> <dd>

<span data-ttu-id="5b046-141">Male</span><span class="sxs-lookup"><span data-stu-id="5b046-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="5b046-142">3</span><span class="sxs-lookup"><span data-stu-id="5b046-142">3</span></span>
</dt> <dd>

<span data-ttu-id="5b046-143">Female</span><span class="sxs-lookup"><span data-stu-id="5b046-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="5b046-144">4</span><span class="sxs-lookup"><span data-stu-id="5b046-144">4</span></span>
</dt> <dd>

<span data-ttu-id="5b046-145">Geschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="5b046-146">5</span><span class="sxs-lookup"><span data-stu-id="5b046-146">5</span></span>
</dt> <dd>

<span data-ttu-id="5b046-147">Nicht geschirmten</span><span class="sxs-lookup"><span data-stu-id="5b046-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="5b046-148">6</span><span class="sxs-lookup"><span data-stu-id="5b046-148">6</span></span>
</dt> <dd>

<span data-ttu-id="5b046-149">SCSI (A) hohe Dichte (50 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-150">7</span><span class="sxs-lookup"><span data-stu-id="5b046-150">7</span></span>
</dt> <dd>

<span data-ttu-id="5b046-151">SCSI (A) niedrige Dichte (50 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-152">8</span><span class="sxs-lookup"><span data-stu-id="5b046-152">8</span></span>
</dt> <dd>

<span data-ttu-id="5b046-153">SCSI (P) High-Density (68 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-154">9</span><span class="sxs-lookup"><span data-stu-id="5b046-154">9</span></span>
</dt> <dd>

<span data-ttu-id="5b046-155">SCSI SCA-I (80 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-156">10</span><span class="sxs-lookup"><span data-stu-id="5b046-156">10</span></span>
</dt> <dd>

<span data-ttu-id="5b046-157">SCSI SCA-II (80 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-158">11</span><span class="sxs-lookup"><span data-stu-id="5b046-158">11</span></span>
</dt> <dd>

<span data-ttu-id="5b046-159">SCSI-Fibre Channel (DB-9, Kupfer)</span><span class="sxs-lookup"><span data-stu-id="5b046-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-160">12</span><span class="sxs-lookup"><span data-stu-id="5b046-160">12</span></span>
</dt> <dd>

<span data-ttu-id="5b046-161">SCSI-Fibre Channel (Fibre)</span><span class="sxs-lookup"><span data-stu-id="5b046-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-162">13</span><span class="sxs-lookup"><span data-stu-id="5b046-162">13</span></span>
</dt> <dd>

<span data-ttu-id="5b046-163">SCSI-Fibre Channel SCA-II (40 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-164">14</span><span class="sxs-lookup"><span data-stu-id="5b046-164">14</span></span>
</dt> <dd>

<span data-ttu-id="5b046-165">SCSI-Fibre Channel SCA-II (20 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-166">15</span><span class="sxs-lookup"><span data-stu-id="5b046-166">15</span></span>
</dt> <dd>

<span data-ttu-id="5b046-167">SCSI-Fibre Channel BNC</span><span class="sxs-lookup"><span data-stu-id="5b046-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-168">16</span><span class="sxs-lookup"><span data-stu-id="5b046-168">16</span></span>
</dt> <dd>

<span data-ttu-id="5b046-169">ATA 3-1/2 Zoll (40 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-170">17</span><span class="sxs-lookup"><span data-stu-id="5b046-170">17</span></span>
</dt> <dd>

<span data-ttu-id="5b046-171">ATA 2-1/2 Zoll (44 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-172">18</span><span class="sxs-lookup"><span data-stu-id="5b046-172">18</span></span>
</dt> <dd>

<span data-ttu-id="5b046-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="5b046-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="5b046-174">19</span><span class="sxs-lookup"><span data-stu-id="5b046-174">19</span></span>
</dt> <dd>

<span data-ttu-id="5b046-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="5b046-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="5b046-176">20</span><span class="sxs-lookup"><span data-stu-id="5b046-176">20</span></span>
</dt> <dd>

<span data-ttu-id="5b046-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="5b046-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="5b046-178">21</span><span class="sxs-lookup"><span data-stu-id="5b046-178">21</span></span>
</dt> <dd>

<span data-ttu-id="5b046-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="5b046-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="5b046-180">22</span><span class="sxs-lookup"><span data-stu-id="5b046-180">22</span></span>
</dt> <dd>

<span data-ttu-id="5b046-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="5b046-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="5b046-182">23</span><span class="sxs-lookup"><span data-stu-id="5b046-182">23</span></span>
</dt> <dd>

<span data-ttu-id="5b046-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="5b046-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="5b046-184">24</span><span class="sxs-lookup"><span data-stu-id="5b046-184">24</span></span>
</dt> <dd>

<span data-ttu-id="5b046-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="5b046-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="5b046-186">25</span><span class="sxs-lookup"><span data-stu-id="5b046-186">25</span></span>
</dt> <dd>

<span data-ttu-id="5b046-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="5b046-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="5b046-188">26</span><span class="sxs-lookup"><span data-stu-id="5b046-188">26</span></span>
</dt> <dd>

<span data-ttu-id="5b046-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="5b046-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="5b046-190">27</span><span class="sxs-lookup"><span data-stu-id="5b046-190">27</span></span>
</dt> <dd>

<span data-ttu-id="5b046-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="5b046-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="5b046-192">28</span><span class="sxs-lookup"><span data-stu-id="5b046-192">28</span></span>
</dt> <dd>

<span data-ttu-id="5b046-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="5b046-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="5b046-194">29</span><span class="sxs-lookup"><span data-stu-id="5b046-194">29</span></span>
</dt> <dd>

<span data-ttu-id="5b046-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="5b046-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="5b046-196">30</span><span class="sxs-lookup"><span data-stu-id="5b046-196">30</span></span>
</dt> <dd>

<span data-ttu-id="5b046-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="5b046-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="5b046-198">31</span><span class="sxs-lookup"><span data-stu-id="5b046-198">31</span></span>
</dt> <dd>

<span data-ttu-id="5b046-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="5b046-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="5b046-200">32</span><span class="sxs-lookup"><span data-stu-id="5b046-200">32</span></span>
</dt> <dd>

<span data-ttu-id="5b046-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="5b046-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="5b046-202">33</span><span class="sxs-lookup"><span data-stu-id="5b046-202">33</span></span>
</dt> <dd>

<span data-ttu-id="5b046-203">AUI</span><span class="sxs-lookup"><span data-stu-id="5b046-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="5b046-204">34</span><span class="sxs-lookup"><span data-stu-id="5b046-204">34</span></span>
</dt> <dd>

<span data-ttu-id="5b046-205">UTP Kategorie 3</span><span class="sxs-lookup"><span data-stu-id="5b046-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="5b046-206">35</span><span class="sxs-lookup"><span data-stu-id="5b046-206">35</span></span>
</dt> <dd>

<span data-ttu-id="5b046-207">UTP Kategorie 4</span><span class="sxs-lookup"><span data-stu-id="5b046-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="5b046-208">36</span><span class="sxs-lookup"><span data-stu-id="5b046-208">36</span></span>
</dt> <dd>

<span data-ttu-id="5b046-209">UTP Kategorie 5</span><span class="sxs-lookup"><span data-stu-id="5b046-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="5b046-210">37</span><span class="sxs-lookup"><span data-stu-id="5b046-210">37</span></span>
</dt> <dd>

<span data-ttu-id="5b046-211">BNC</span><span class="sxs-lookup"><span data-stu-id="5b046-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-212">38</span><span class="sxs-lookup"><span data-stu-id="5b046-212">38</span></span>
</dt> <dd>

<span data-ttu-id="5b046-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="5b046-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="5b046-214">39</span><span class="sxs-lookup"><span data-stu-id="5b046-214">39</span></span>
</dt> <dd>

<span data-ttu-id="5b046-215">RJ45</span><span class="sxs-lookup"><span data-stu-id="5b046-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="5b046-216">40</span><span class="sxs-lookup"><span data-stu-id="5b046-216">40</span></span>
</dt> <dd>

<span data-ttu-id="5b046-217">Fiber-MIC</span><span class="sxs-lookup"><span data-stu-id="5b046-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-218">41</span><span class="sxs-lookup"><span data-stu-id="5b046-218">41</span></span>
</dt> <dd>

<span data-ttu-id="5b046-219">Apple AUI</span><span class="sxs-lookup"><span data-stu-id="5b046-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="5b046-220">42</span><span class="sxs-lookup"><span data-stu-id="5b046-220">42</span></span>
</dt> <dd>

<span data-ttu-id="5b046-221">Apple-GeoPort</span><span class="sxs-lookup"><span data-stu-id="5b046-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="5b046-222">43</span><span class="sxs-lookup"><span data-stu-id="5b046-222">43</span></span>
</dt> <dd>

<span data-ttu-id="5b046-223">PCI</span><span class="sxs-lookup"><span data-stu-id="5b046-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="5b046-224">44</span><span class="sxs-lookup"><span data-stu-id="5b046-224">44</span></span>
</dt> <dd>

<span data-ttu-id="5b046-225">ISA</span><span class="sxs-lookup"><span data-stu-id="5b046-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="5b046-226">45</span><span class="sxs-lookup"><span data-stu-id="5b046-226">45</span></span>
</dt> <dd>

<span data-ttu-id="5b046-227">EISA</span><span class="sxs-lookup"><span data-stu-id="5b046-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="5b046-228">46</span><span class="sxs-lookup"><span data-stu-id="5b046-228">46</span></span>
</dt> <dd>

<span data-ttu-id="5b046-229">VESA</span><span class="sxs-lookup"><span data-stu-id="5b046-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="5b046-230">47</span><span class="sxs-lookup"><span data-stu-id="5b046-230">47</span></span>
</dt> <dd>

<span data-ttu-id="5b046-231">PCMCIA</span><span class="sxs-lookup"><span data-stu-id="5b046-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="5b046-232">48</span><span class="sxs-lookup"><span data-stu-id="5b046-232">48</span></span>
</dt> <dd>

<span data-ttu-id="5b046-233">PCMCIA-Typ I</span><span class="sxs-lookup"><span data-stu-id="5b046-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="5b046-234">49</span><span class="sxs-lookup"><span data-stu-id="5b046-234">49</span></span>
</dt> <dd>

<span data-ttu-id="5b046-235">PCMCIA-Typ II</span><span class="sxs-lookup"><span data-stu-id="5b046-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="5b046-236">50</span><span class="sxs-lookup"><span data-stu-id="5b046-236">50</span></span>
</dt> <dd>

<span data-ttu-id="5b046-237">PCMCIA-Typ III</span><span class="sxs-lookup"><span data-stu-id="5b046-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="5b046-238">51</span><span class="sxs-lookup"><span data-stu-id="5b046-238">51</span></span>
</dt> <dd>

<span data-ttu-id="5b046-239">ZV-Port</span><span class="sxs-lookup"><span data-stu-id="5b046-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="5b046-240">52</span><span class="sxs-lookup"><span data-stu-id="5b046-240">52</span></span>
</dt> <dd>

<span data-ttu-id="5b046-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="5b046-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="5b046-242">53</span><span class="sxs-lookup"><span data-stu-id="5b046-242">53</span></span>
</dt> <dd>

<span data-ttu-id="5b046-243">USB</span><span class="sxs-lookup"><span data-stu-id="5b046-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="5b046-244">54</span><span class="sxs-lookup"><span data-stu-id="5b046-244">54</span></span>
</dt> <dd>

<span data-ttu-id="5b046-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="5b046-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="5b046-246">55</span><span class="sxs-lookup"><span data-stu-id="5b046-246">55</span></span>
</dt> <dd>

<span data-ttu-id="5b046-247">HIPPI</span><span class="sxs-lookup"><span data-stu-id="5b046-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="5b046-248">56</span><span class="sxs-lookup"><span data-stu-id="5b046-248">56</span></span>
</dt> <dd>

<span data-ttu-id="5b046-249">HSSDC (6 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-250">57</span><span class="sxs-lookup"><span data-stu-id="5b046-250">57</span></span>
</dt> <dd>

<span data-ttu-id="5b046-251">GBIC</span><span class="sxs-lookup"><span data-stu-id="5b046-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-252">58</span><span class="sxs-lookup"><span data-stu-id="5b046-252">58</span></span>
</dt> <dd>

<span data-ttu-id="5b046-253">DIN</span><span class="sxs-lookup"><span data-stu-id="5b046-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="5b046-254">59</span><span class="sxs-lookup"><span data-stu-id="5b046-254">59</span></span>
</dt> <dd>

<span data-ttu-id="5b046-255">Mini-DIN</span><span class="sxs-lookup"><span data-stu-id="5b046-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="5b046-256">60</span><span class="sxs-lookup"><span data-stu-id="5b046-256">60</span></span>
</dt> <dd>

<span data-ttu-id="5b046-257">Micro-DIN</span><span class="sxs-lookup"><span data-stu-id="5b046-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="5b046-258">61</span><span class="sxs-lookup"><span data-stu-id="5b046-258">61</span></span>
</dt> <dd>

<span data-ttu-id="5b046-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="5b046-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="5b046-260">62</span><span class="sxs-lookup"><span data-stu-id="5b046-260">62</span></span>
</dt> <dd>

<span data-ttu-id="5b046-261">Infrarot</span><span class="sxs-lookup"><span data-stu-id="5b046-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="5b046-262">63</span><span class="sxs-lookup"><span data-stu-id="5b046-262">63</span></span>
</dt> <dd>

<span data-ttu-id="5b046-263">HP-HIL</span><span class="sxs-lookup"><span data-stu-id="5b046-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="5b046-264">64</span><span class="sxs-lookup"><span data-stu-id="5b046-264">64</span></span>
</dt> <dd>

<span data-ttu-id="5b046-265">Access. Bus</span><span class="sxs-lookup"><span data-stu-id="5b046-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="5b046-266">65</span><span class="sxs-lookup"><span data-stu-id="5b046-266">65</span></span>
</dt> <dd>

<span data-ttu-id="5b046-267">NuBus</span><span class="sxs-lookup"><span data-stu-id="5b046-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="5b046-268">66</span><span class="sxs-lookup"><span data-stu-id="5b046-268">66</span></span>
</dt> <dd>

<span data-ttu-id="5b046-269">Zentronik</span><span class="sxs-lookup"><span data-stu-id="5b046-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="5b046-270">67</span><span class="sxs-lookup"><span data-stu-id="5b046-270">67</span></span>
</dt> <dd>

<span data-ttu-id="5b046-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="5b046-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="5b046-272">68</span><span class="sxs-lookup"><span data-stu-id="5b046-272">68</span></span>
</dt> <dd>

<span data-ttu-id="5b046-273">Mini-Centronics Typ-14</span><span class="sxs-lookup"><span data-stu-id="5b046-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="5b046-274">69</span><span class="sxs-lookup"><span data-stu-id="5b046-274">69</span></span>
</dt> <dd>

<span data-ttu-id="5b046-275">Mini-Centronics Typ-20</span><span class="sxs-lookup"><span data-stu-id="5b046-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="5b046-276">70</span><span class="sxs-lookup"><span data-stu-id="5b046-276">70</span></span>
</dt> <dd>

<span data-ttu-id="5b046-277">Mini-Centronics Typ-26</span><span class="sxs-lookup"><span data-stu-id="5b046-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="5b046-278">71</span><span class="sxs-lookup"><span data-stu-id="5b046-278">71</span></span>
</dt> <dd>

<span data-ttu-id="5b046-279">Busmaus</span><span class="sxs-lookup"><span data-stu-id="5b046-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="5b046-280">72</span><span class="sxs-lookup"><span data-stu-id="5b046-280">72</span></span>
</dt> <dd>

<span data-ttu-id="5b046-281">ADB</span><span class="sxs-lookup"><span data-stu-id="5b046-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="5b046-282">73</span><span class="sxs-lookup"><span data-stu-id="5b046-282">73</span></span>
</dt> <dd>

<span data-ttu-id="5b046-283">AGP</span><span class="sxs-lookup"><span data-stu-id="5b046-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="5b046-284">74</span><span class="sxs-lookup"><span data-stu-id="5b046-284">74</span></span>
</dt> <dd>

<span data-ttu-id="5b046-285">VME-Bus</span><span class="sxs-lookup"><span data-stu-id="5b046-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="5b046-286">75</span><span class="sxs-lookup"><span data-stu-id="5b046-286">75</span></span>
</dt> <dd>

<span data-ttu-id="5b046-287">VME64</span><span class="sxs-lookup"><span data-stu-id="5b046-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="5b046-288">76</span><span class="sxs-lookup"><span data-stu-id="5b046-288">76</span></span>
</dt> <dd>

<span data-ttu-id="5b046-289">Proprietär</span><span class="sxs-lookup"><span data-stu-id="5b046-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="5b046-290">77</span><span class="sxs-lookup"><span data-stu-id="5b046-290">77</span></span>
</dt> <dd>

<span data-ttu-id="5b046-291">Platzhalter für proprietäre Prozessorkarte</span><span class="sxs-lookup"><span data-stu-id="5b046-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="5b046-292">78</span><span class="sxs-lookup"><span data-stu-id="5b046-292">78</span></span>
</dt> <dd>

<span data-ttu-id="5b046-293">Eigener Speicherkarten Slot</span><span class="sxs-lookup"><span data-stu-id="5b046-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="5b046-294">79</span><span class="sxs-lookup"><span data-stu-id="5b046-294">79</span></span>
</dt> <dd>

<span data-ttu-id="5b046-295">Eigener e/a-Riser-Slot</span><span class="sxs-lookup"><span data-stu-id="5b046-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="5b046-296">80</span><span class="sxs-lookup"><span data-stu-id="5b046-296">80</span></span>
</dt> <dd>

<span data-ttu-id="5b046-297">PCI-66MHz</span><span class="sxs-lookup"><span data-stu-id="5b046-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="5b046-298">81</span><span class="sxs-lookup"><span data-stu-id="5b046-298">81</span></span>
</dt> <dd>

<span data-ttu-id="5b046-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="5b046-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="5b046-300">82</span><span class="sxs-lookup"><span data-stu-id="5b046-300">82</span></span>
</dt> <dd>

<span data-ttu-id="5b046-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="5b046-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="5b046-302">83</span><span class="sxs-lookup"><span data-stu-id="5b046-302">83</span></span>
</dt> <dd>

<span data-ttu-id="5b046-303">PC-98</span><span class="sxs-lookup"><span data-stu-id="5b046-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="5b046-304">84</span><span class="sxs-lookup"><span data-stu-id="5b046-304">84</span></span>
</dt> <dd>

<span data-ttu-id="5b046-305">PC-98-hireso</span><span class="sxs-lookup"><span data-stu-id="5b046-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="5b046-306">85</span><span class="sxs-lookup"><span data-stu-id="5b046-306">85</span></span>
</dt> <dd>

<span data-ttu-id="5b046-307">PC-H98</span><span class="sxs-lookup"><span data-stu-id="5b046-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="5b046-308">86</span><span class="sxs-lookup"><span data-stu-id="5b046-308">86</span></span>
</dt> <dd>

<span data-ttu-id="5b046-309">PC-98note</span><span class="sxs-lookup"><span data-stu-id="5b046-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="5b046-310">87</span><span class="sxs-lookup"><span data-stu-id="5b046-310">87</span></span>
</dt> <dd>

<span data-ttu-id="5b046-311">PC-98full</span><span class="sxs-lookup"><span data-stu-id="5b046-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="5b046-312">88</span><span class="sxs-lookup"><span data-stu-id="5b046-312">88</span></span>
</dt> <dd>

<span data-ttu-id="5b046-313">SSE SCSI</span><span class="sxs-lookup"><span data-stu-id="5b046-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="5b046-314">89</span><span class="sxs-lookup"><span data-stu-id="5b046-314">89</span></span>
</dt> <dd>

<span data-ttu-id="5b046-315">Kreisförmig</span><span class="sxs-lookup"><span data-stu-id="5b046-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="5b046-316">90</span><span class="sxs-lookup"><span data-stu-id="5b046-316">90</span></span>
</dt> <dd>

<span data-ttu-id="5b046-317">On-board-IDE-Connector</span><span class="sxs-lookup"><span data-stu-id="5b046-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="5b046-318">91</span><span class="sxs-lookup"><span data-stu-id="5b046-318">91</span></span>
</dt> <dd>

<span data-ttu-id="5b046-319">Auf dem Disketten Verbinder</span><span class="sxs-lookup"><span data-stu-id="5b046-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="5b046-320">92</span><span class="sxs-lookup"><span data-stu-id="5b046-320">92</span></span>
</dt> <dd>

<span data-ttu-id="5b046-321">9 Dual Inline anheften</span><span class="sxs-lookup"><span data-stu-id="5b046-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5b046-322">93</span><span class="sxs-lookup"><span data-stu-id="5b046-322">93</span></span>
</dt> <dd>

<span data-ttu-id="5b046-323">25 Pin Dual Inline</span><span class="sxs-lookup"><span data-stu-id="5b046-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5b046-324">94</span><span class="sxs-lookup"><span data-stu-id="5b046-324">94</span></span>
</dt> <dd>

<span data-ttu-id="5b046-325">50 Pin Dual Inline</span><span class="sxs-lookup"><span data-stu-id="5b046-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5b046-326">95</span><span class="sxs-lookup"><span data-stu-id="5b046-326">95</span></span>
</dt> <dd>

<span data-ttu-id="5b046-327">68 Pin Dual Inline</span><span class="sxs-lookup"><span data-stu-id="5b046-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5b046-328">96</span><span class="sxs-lookup"><span data-stu-id="5b046-328">96</span></span>
</dt> <dd>

<span data-ttu-id="5b046-329">On Board Sound Connector</span><span class="sxs-lookup"><span data-stu-id="5b046-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="5b046-330">97</span><span class="sxs-lookup"><span data-stu-id="5b046-330">97</span></span>
</dt> <dd>

<span data-ttu-id="5b046-331">Mini Jack</span><span class="sxs-lookup"><span data-stu-id="5b046-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="5b046-332">98</span><span class="sxs-lookup"><span data-stu-id="5b046-332">98</span></span>
</dt> <dd>

<span data-ttu-id="5b046-333">PCI-X</span><span class="sxs-lookup"><span data-stu-id="5b046-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="5b046-334">99</span><span class="sxs-lookup"><span data-stu-id="5b046-334">99</span></span>
</dt> <dd>

<span data-ttu-id="5b046-335">SBus IEEE 1396-1993 32 Bit</span><span class="sxs-lookup"><span data-stu-id="5b046-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="5b046-336">100</span><span class="sxs-lookup"><span data-stu-id="5b046-336">100</span></span>
</dt> <dd>

<span data-ttu-id="5b046-337">SBus IEEE 1396-1993 64 Bit</span><span class="sxs-lookup"><span data-stu-id="5b046-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="5b046-338">101</span><span class="sxs-lookup"><span data-stu-id="5b046-338">101</span></span>
</dt> <dd>

<span data-ttu-id="5b046-339">MCA</span><span class="sxs-lookup"><span data-stu-id="5b046-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="5b046-340">102</span><span class="sxs-lookup"><span data-stu-id="5b046-340">102</span></span>
</dt> <dd>

<span data-ttu-id="5b046-341">Sant</span><span class="sxs-lookup"><span data-stu-id="5b046-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="5b046-342">103</span><span class="sxs-lookup"><span data-stu-id="5b046-342">103</span></span>
</dt> <dd>

<span data-ttu-id="5b046-343">XIO</span><span class="sxs-lookup"><span data-stu-id="5b046-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="5b046-344">104</span><span class="sxs-lookup"><span data-stu-id="5b046-344">104</span></span>
</dt> <dd>

<span data-ttu-id="5b046-345">HI</span><span class="sxs-lookup"><span data-stu-id="5b046-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="5b046-346">105</span><span class="sxs-lookup"><span data-stu-id="5b046-346">105</span></span>
</dt> <dd>

<span data-ttu-id="5b046-347">Ngio</span><span class="sxs-lookup"><span data-stu-id="5b046-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="5b046-348">106</span><span class="sxs-lookup"><span data-stu-id="5b046-348">106</span></span>
</dt> <dd>

<span data-ttu-id="5b046-349">PMC</span><span class="sxs-lookup"><span data-stu-id="5b046-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-350">107</span><span class="sxs-lookup"><span data-stu-id="5b046-350">107</span></span>
</dt> <dd>

<span data-ttu-id="5b046-351">MTRJ</span><span class="sxs-lookup"><span data-stu-id="5b046-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="5b046-352">108</span><span class="sxs-lookup"><span data-stu-id="5b046-352">108</span></span>
</dt> <dd>

<span data-ttu-id="5b046-353">VF-45</span><span class="sxs-lookup"><span data-stu-id="5b046-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="5b046-354">109</span><span class="sxs-lookup"><span data-stu-id="5b046-354">109</span></span>
</dt> <dd>

<span data-ttu-id="5b046-355">Zukünftige e/a-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5b046-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="5b046-356">110</span><span class="sxs-lookup"><span data-stu-id="5b046-356">110</span></span>
</dt> <dd>

<span data-ttu-id="5b046-357">SC</span><span class="sxs-lookup"><span data-stu-id="5b046-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-358">111</span><span class="sxs-lookup"><span data-stu-id="5b046-358">111</span></span>
</dt> <dd>

<span data-ttu-id="5b046-359">SG</span><span class="sxs-lookup"><span data-stu-id="5b046-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="5b046-360">112</span><span class="sxs-lookup"><span data-stu-id="5b046-360">112</span></span>
</dt> <dd>

<span data-ttu-id="5b046-361">Electrical</span><span class="sxs-lookup"><span data-stu-id="5b046-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="5b046-362">113</span><span class="sxs-lookup"><span data-stu-id="5b046-362">113</span></span>
</dt> <dd>

<span data-ttu-id="5b046-363">Optical</span><span class="sxs-lookup"><span data-stu-id="5b046-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="5b046-364">114</span><span class="sxs-lookup"><span data-stu-id="5b046-364">114</span></span>
</dt> <dd>

<span data-ttu-id="5b046-365">Menüband</span><span class="sxs-lookup"><span data-stu-id="5b046-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="5b046-366">115</span><span class="sxs-lookup"><span data-stu-id="5b046-366">115</span></span>
</dt> <dd>

<span data-ttu-id="5b046-367">GLM</span><span class="sxs-lookup"><span data-stu-id="5b046-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="5b046-368">116</span><span class="sxs-lookup"><span data-stu-id="5b046-368">116</span></span>
</dt> <dd>

<span data-ttu-id="5b046-369">1x9</span><span class="sxs-lookup"><span data-stu-id="5b046-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="5b046-370">117</span><span class="sxs-lookup"><span data-stu-id="5b046-370">117</span></span>
</dt> <dd>

<span data-ttu-id="5b046-371">Mini-SG</span><span class="sxs-lookup"><span data-stu-id="5b046-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="5b046-372">118</span><span class="sxs-lookup"><span data-stu-id="5b046-372">118</span></span>
</dt> <dd>

<span data-ttu-id="5b046-373">LC</span><span class="sxs-lookup"><span data-stu-id="5b046-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-374">119</span><span class="sxs-lookup"><span data-stu-id="5b046-374">119</span></span>
</dt> <dd>

<span data-ttu-id="5b046-375">HSSC</span><span class="sxs-lookup"><span data-stu-id="5b046-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="5b046-376">120</span><span class="sxs-lookup"><span data-stu-id="5b046-376">120</span></span>
</dt> <dd>

<span data-ttu-id="5b046-377">VHDCI abgeschirmt (68 Pins)</span><span class="sxs-lookup"><span data-stu-id="5b046-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5b046-378">121</span><span class="sxs-lookup"><span data-stu-id="5b046-378">121</span></span>
</dt> <dd>

<span data-ttu-id="5b046-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="5b046-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b046-380">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="5b046-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-383">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b046-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-384">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b046-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5b046-385">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5b046-386">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-387">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b046-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-390">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5b046-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-391">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5b046-391">Textual description of the object.</span></span>

<span data-ttu-id="5b046-392">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-393">**Erhöht**</span><span class="sxs-lookup"><span data-stu-id="5b046-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-394">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="5b046-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-396">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="5b046-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-397">Maximale Höhe einer Adapterkarte in Zoll, die in den Slot eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b046-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5b046-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-399">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b046-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-401">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="5b046-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-402">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5b046-402">Date and time the object was installed.</span></span> <span data-ttu-id="5b046-403">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5b046-404">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-405">**Verlängert**</span><span class="sxs-lookup"><span data-stu-id="5b046-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-406">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="5b046-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-408">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")</span><span class="sxs-lookup"><span data-stu-id="5b046-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-409">Maximale Länge in Zoll einer Adapterkarte, die in den Slot eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b046-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-410">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5b046-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-411">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-413">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b046-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-414">Die Organisation, die das physische Element erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="5b046-414">Organization that produced the physical element.</span></span> <span data-ttu-id="5b046-415">Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="5b046-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="5b046-416">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-417">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="5b046-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-418">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b046-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-420">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="5b046-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-421">Maximale Busbreite von Adapterkarten in Bits, die in den Slot eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="5b046-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="5b046-422">**8** (0)</span><span class="sxs-lookup"><span data-stu-id="5b046-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="5b046-423">**16** (1)</span><span class="sxs-lookup"><span data-stu-id="5b046-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="5b046-424">**32** (2)</span><span class="sxs-lookup"><span data-stu-id="5b046-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="5b046-425">**64** (3)</span><span class="sxs-lookup"><span data-stu-id="5b046-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="5b046-426">**128** (4)</span><span class="sxs-lookup"><span data-stu-id="5b046-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b046-427">**Modell**</span><span class="sxs-lookup"><span data-stu-id="5b046-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-430">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b046-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-431">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="5b046-432">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-433">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b046-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-436">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5b046-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-437">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-437">Label by which the object is known.</span></span> <span data-ttu-id="5b046-438">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5b046-439">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-440">**Number**</span><span class="sxs-lookup"><span data-stu-id="5b046-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-441">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b046-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b046-443">Die physische Slot-Nummer, die als Index in einer System Slot-Tabelle verwendet werden kann, um zu bestimmen, ob der Slot physisch besetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5b046-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b046-447">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5b046-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5b046-448">Ein Beispiel hierfür sind Barcode Daten, die einem Element zugeordnet sind, das ebenfalls über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="5b046-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="5b046-449">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b046-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="5b046-450">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-451">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5b046-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-452">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-454">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b046-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-455">Die Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="5b046-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="5b046-456">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-457">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="5b046-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-458">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5b046-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b046-460">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="5b046-461">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-462">**Zweck Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b046-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-465">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Slot**.**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="5b046-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-466">Frei Form Zeichenfolge, die beschreibt, wie dieser Slot physisch eindeutig ist und dass er spezielle Hardwaretypen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="5b046-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="5b046-467">Diese Eigenschaft hat nur Bedeutung, wenn die entsprechende boolesche **SpecialPurpose** -Eigenschaft auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-468">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5b046-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-471">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b046-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-472">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5b046-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5b046-473">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-474">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5b046-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-477">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b046-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-478">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="5b046-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="5b046-479">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-480">**Specialzweck**</span><span class="sxs-lookup"><span data-stu-id="5b046-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-481">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5b046-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-483">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Slot**.**Zweck Beschreibung**")</span><span class="sxs-lookup"><span data-stu-id="5b046-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-484">**True** gibt an, dass der Slot physisch eindeutig ist und spezielle Hardwaretypen (z. b. einen Grafikprozessor Slot) enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="5b046-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="5b046-485">**True** gibt an, dass die Eigenschaft " **zieldescription** " angeben soll, wie der Slot eindeutig oder der Zweck des Slots ist.</span><span class="sxs-lookup"><span data-stu-id="5b046-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-486">**Status**</span><span class="sxs-lookup"><span data-stu-id="5b046-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-488">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-489">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="5b046-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-490">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5b046-490">Current status of the object.</span></span> <span data-ttu-id="5b046-491">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5b046-492">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="5b046-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5b046-493">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5b046-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5b046-494">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5b046-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5b046-495">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5b046-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b046-496">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5b046-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5b046-497">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5b046-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5b046-498">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5b046-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5b046-499">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="5b046-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5b046-500">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5b046-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5b046-501">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="5b046-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5b046-502">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="5b046-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5b046-503">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="5b046-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5b046-504">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="5b046-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b046-505">**Supportshotplug**</span><span class="sxs-lookup"><span data-stu-id="5b046-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-506">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5b046-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b046-508">**True** gibt an, dass der Slot das Hot-Plugging von Adapterkarten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b046-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-509">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5b046-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-510">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-511">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-512">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b046-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-513">Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert.</span><span class="sxs-lookup"><span data-stu-id="5b046-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="5b046-514">Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="5b046-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="5b046-515">Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware/Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5b046-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="5b046-516">Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="5b046-517">Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b046-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="5b046-518">Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5b046-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="5b046-519">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-520">**Theritäts Bewertung**</span><span class="sxs-lookup"><span data-stu-id="5b046-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-521">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b046-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-522">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-523">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="5b046-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-524">Maximale thermische Unterschiede des Slots in Milliwatt.</span><span class="sxs-lookup"><span data-stu-id="5b046-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="5b046-525">**Vccmixedvoltagesupport**</span><span class="sxs-lookup"><span data-stu-id="5b046-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-526">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="5b046-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5b046-527">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-528">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="5b046-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-529">VCC-Spannung wird vom Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b046-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b046-530">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5b046-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5b046-531">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="5b046-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="5b046-532">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="5b046-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="5b046-533">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="5b046-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b046-534">**Version**</span><span class="sxs-lookup"><span data-stu-id="5b046-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b046-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b046-536">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-537">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b046-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b046-538">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="5b046-538">Version of the physical element.</span></span>

<span data-ttu-id="5b046-539">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5b046-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b046-540">**Vppmixedvoltagesupport**</span><span class="sxs-lookup"><span data-stu-id="5b046-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b046-541">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="5b046-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5b046-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b046-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b046-543">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Slot \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="5b046-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="5b046-544">VPP-Spannung wird vom Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b046-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b046-545">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5b046-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5b046-546">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="5b046-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="5b046-547">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="5b046-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="5b046-548">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="5b046-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="5b046-549">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="5b046-549">**12V** (4)</span></span>


<span data-ttu-id="5b046-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5b046-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5b046-551">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b046-551">Remarks</span></span>

<span data-ttu-id="5b046-552">Die **CIM- \_ Slot** -Klasse wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5b046-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="5b046-553">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5b046-553">WMI does not implement this class.</span></span> <span data-ttu-id="5b046-554">Informationen zu WMI-Klassen, die vom **CIM- \_ Slot** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="5b046-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5b046-555">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5b046-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b046-556">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5b046-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b046-557">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b046-557">Requirements</span></span>



| <span data-ttu-id="5b046-558">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b046-558">Requirement</span></span> | <span data-ttu-id="5b046-559">Wert</span><span class="sxs-lookup"><span data-stu-id="5b046-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b046-560">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b046-560">Minimum supported client</span></span><br/> | <span data-ttu-id="5b046-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b046-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b046-562">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b046-562">Minimum supported server</span></span><br/> | <span data-ttu-id="5b046-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b046-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b046-564">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b046-564">Namespace</span></span><br/>                | <span data-ttu-id="5b046-565">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5b046-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b046-566">MOF</span><span class="sxs-lookup"><span data-stu-id="5b046-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b046-567"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5b046-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b046-568">DLL</span><span class="sxs-lookup"><span data-stu-id="5b046-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b046-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b046-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b046-570">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b046-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b046-571">**CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="5b046-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 

