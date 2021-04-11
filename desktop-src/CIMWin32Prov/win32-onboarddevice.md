---
description: Die Win32 \_ onboarddevice-WMI-Klasse stellt gängige Adapter Geräte dar, die in die Hauptplatine (System Platine) integriert sind.
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Win32_OnBoardDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214271"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="1c6b0-103">Win32 \_ onboarddevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1c6b0-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="1c6b0-104">Die **Win32 \_ onboarddevice** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt gängige Adapter Geräte dar, die in die Hauptplatine (System Platine) integriert sind.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="1c6b0-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c6b0-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c6b0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1c6b0-108">Member</span><span class="sxs-lookup"><span data-stu-id="1c6b0-108">Members</span></span>

<span data-ttu-id="1c6b0-109">Die **Win32 \_ onboarddevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1c6b0-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="1c6b0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c6b0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c6b0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c6b0-111">Properties</span></span>

<span data-ttu-id="1c6b0-112">Die **Win32 \_ onboarddevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c6b0-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-117">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-117">Short description of the object.</span></span>

<span data-ttu-id="1c6b0-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-119">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-122">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-123">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1c6b0-124">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1c6b0-125">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-129">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Description")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-130">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-130">Description of the object.</span></span>

<span data-ttu-id="1c6b0-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-135">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Device Type n")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-136">Typ des Geräts, das dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c6b0-137">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c6b0-138">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="1c6b0-139">**Video** (3)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="1c6b0-140">**SCSI-Controller** (4)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="1c6b0-141">**Ethernet** (5)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="1c6b0-142">**TokenRing** (6)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="1c6b0-143">**Sound** (7)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c6b0-144">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c6b0-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-147">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Device Status n")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-148">**True** gibt an, dass das auf-Board-Gerät verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-149">**"Anappable"**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-150">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c6b0-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-152">**True** gibt an, dass ein physisches Paket im laufenden Betrieb ausgetauscht werden kann (wenn es möglich ist, das Element durch einen physisch abweichenden, aber entsprechenden Wert zu ersetzen, während für das enthaltene Paket eine Stromversorgung angewendet wurde).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="1c6b0-153">Beispielsweise ist ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wurde, wechselseitig austauschbar.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="1c6b0-154">Alle Pakete, die sich im laufenden Betrieb austauschen lassen, sind von Natur aus austauschbar und austauschbar.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="1c6b0-155">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-157">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-159">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-160">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-160">Date and time the object was installed.</span></span> <span data-ttu-id="1c6b0-161">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1c6b0-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-163">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-166">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-167">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="1c6b0-168">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-169">**Modell**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-172">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-173">Der Name, mit dem das physische Element allgemein bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="1c6b0-174">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-175">**Name**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-178">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-179">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-179">Label by which the object is known.</span></span> <span data-ttu-id="1c6b0-180">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1c6b0-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-185">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="1c6b0-186">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="1c6b0-187">Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** , und die Barcode Daten werden als Klassen Schlüssel in der Tag-Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="1c6b0-188">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-189">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-192">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-193">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="1c6b0-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="1c6b0-194">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-195">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c6b0-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-198">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="1c6b0-199">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-200">**Ab**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-201">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c6b0-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-203">**True** gibt an, dass ein physisches Paket entfernt werden kann (wenn es so konzipiert ist, dass es in den physischen Container übernommen wird, in dem es normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="1c6b0-204">Ein Paket kann weiterhin entfernt werden, wenn die Stromversorgung "Off" sein muss, um das Entfernen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="1c6b0-205">Wenn Power "on" sein kann und das Paket entfernt werden kann, ist das Element austauschbar und kann im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="1c6b0-206">Beispielsweise ist ein zusätzlicher Akku in einem Laptop austauschbar, ebenso wie ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="1c6b0-207">Der letztere kann jedoch im laufenden Betrieb ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="1c6b0-208">Die Anzeige eines Laptops kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="1c6b0-209">Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="1c6b0-210">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-211">**Replaceable**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-212">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c6b0-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-214">**True** gibt an, dass ein physisches Paket ersetzbar ist (wenn es möglich ist, das Element mit einem physisch anderen Element zu ersetzen).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="1c6b0-215">Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="1c6b0-216">In diesem Fall wird der Prozessor als ersetzbar bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="1c6b0-217">Ein weiteres Beispiel ist ein Stromversorgung-Paket, das auf gleitenden Schienen eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="1c6b0-218">Alle Wechsel Pakete sind von Natur aus austauschbar.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="1c6b0-219">Diese Eigenschaft wird von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-223">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-224">Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="1c6b0-225">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-229">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-230">Die Stock Keeping Unit-Nummer für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="1c6b0-231">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-232">**Status**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-235">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-236">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-236">Current status of the object.</span></span> <span data-ttu-id="1c6b0-237">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1c6b0-238">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1c6b0-239">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="1c6b0-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1c6b0-240">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1c6b0-241">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1c6b0-242">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1c6b0-243">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="1c6b0-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1c6b0-244">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1c6b0-245">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c6b0-246">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c6b0-247">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1c6b0-248">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1c6b0-249">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1c6b0-250">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1c6b0-251">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1c6b0-252">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1c6b0-253">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1c6b0-254">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1c6b0-255">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c6b0-256">**Tag**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-259">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1c6b0-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-260">Eindeutiger Bezeichner des mit dem System verbundenen auf dem System verbundenen Geräts.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="1c6b0-261">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="1c6b0-262">Beispiel: "on Board Device 1"</span><span class="sxs-lookup"><span data-stu-id="1c6b0-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="1c6b0-263">**Version**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6b0-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c6b0-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6b0-266">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c6b0-267">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-267">Version of the physical element.</span></span>

<span data-ttu-id="1c6b0-268">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c6b0-269">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c6b0-269">Remarks</span></span>

<span data-ttu-id="1c6b0-270">Die **Win32-Klasse \_ onboarddevice** ist von [**CIM \_ physicalcomponent**](cim-physicalcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6b0-271">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c6b0-271">Requirements</span></span>



| <span data-ttu-id="1c6b0-272">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c6b0-272">Requirement</span></span> | <span data-ttu-id="1c6b0-273">Wert</span><span class="sxs-lookup"><span data-stu-id="1c6b0-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6b0-274">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-274">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6b0-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c6b0-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c6b0-276">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c6b0-276">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6b0-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c6b0-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c6b0-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c6b0-278">Namespace</span></span><br/>                | <span data-ttu-id="1c6b0-279">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c6b0-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c6b0-280">MOF</span><span class="sxs-lookup"><span data-stu-id="1c6b0-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c6b0-281"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b0-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c6b0-282">DLL</span><span class="sxs-lookup"><span data-stu-id="1c6b0-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c6b0-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b0-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6b0-284">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c6b0-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6b0-285">**CIM- \_ physicalcomponent**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="1c6b0-286">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="1c6b0-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
