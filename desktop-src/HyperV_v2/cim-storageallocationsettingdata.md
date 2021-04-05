---
description: Stellt Einstellungen für die Zuordnung des virtuellen Speichers dar.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: CIM_StorageAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756619"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="4023b-103">CIM- \_ Klasse "storagezugegenssettingdata"</span><span class="sxs-lookup"><span data-stu-id="4023b-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="4023b-104">Stellt Einstellungen für die Zuordnung des virtuellen Speichers dar.</span><span class="sxs-lookup"><span data-stu-id="4023b-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="4023b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4023b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="4023b-106">Member</span><span class="sxs-lookup"><span data-stu-id="4023b-106">Members</span></span>

<span data-ttu-id="4023b-107">Die **CIM \_ storagezugecationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4023b-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4023b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4023b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4023b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4023b-109">Properties</span></span>

<span data-ttu-id="4023b-110">Die **CIM \_ storagezugecationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4023b-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4023b-111">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="4023b-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4023b-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-114">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**Access**")</span><span class="sxs-lookup"><span data-stu-id="4023b-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-115">Die Lese-/Schreibunterstützung der Speicher Belegung.</span><span class="sxs-lookup"><span data-stu-id="4023b-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4023b-116">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4023b-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="4023b-117">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="4023b-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="4023b-118">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="4023b-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="4023b-119">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="4023b-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4023b-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4023b-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4023b-121">**Hostextentname**</span><span class="sxs-lookup"><span data-stu-id="4023b-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4023b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-124">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentnameformat**","**CIM \_ storagezuweisung-dateinsettingdata**.**Hostextentnamenamespace**","[**CIM \_ storageblock**](cim-storageextent.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="4023b-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-125">Ein eindeutiger Bezeichner des Host Speicher Umfangs.</span><span class="sxs-lookup"><span data-stu-id="4023b-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="4023b-126">**Hostextentnameformat**</span><span class="sxs-lookup"><span data-stu-id="4023b-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4023b-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-129">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentname**","**CIM \_ storagezugecationsettingdata**.**Otherhostextentnameformat**","[**CIM \_ storageblock**](cim-storageextent.md).**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="4023b-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-130">Das Format des **hostextentname** -Eigenschafts Werts.</span><span class="sxs-lookup"><span data-stu-id="4023b-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4023b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4023b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4023b-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4023b-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="4023b-133"><span id="SNVM"></span><span id="snvm"></span>**Snvm** (7)</span><span class="sxs-lookup"><span data-stu-id="4023b-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4023b-134">Snvm (Serial Number/Vendor/Model) ist 3 Zeichen folgen, die den Herstellernamen, den Produktnamen innerhalb des Namespaces des Anbieters und die Seriennummer im Modell Namespace darstellen.</span><span class="sxs-lookup"><span data-stu-id="4023b-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="4023b-135">Als Trennzeichen für Zeichen folgen wird "+" verwendet.</span><span class="sxs-lookup"><span data-stu-id="4023b-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="4023b-136">Leerzeichen können eingeschlossen werden und sind von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="4023b-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="4023b-137">Die Seriennummer ist die Textdarstellung der Seriennummer in hexadezimalen Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="4023b-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="4023b-138">Dies stellt den Hersteller und die Modell-ID aus den SCSI-Abfrage Daten dar. das Feld "Vendor" muss 8 Zeichen breit sein, und das Feld "Product" muss 16 Zeichen breit sein.</span><span class="sxs-lookup"><span data-stu-id="4023b-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="4023b-139">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4023b-139">For example,</span></span>

<span data-ttu-id="4023b-140">"Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458" ( \_ ist ein Leerzeichen)</span><span class="sxs-lookup"><span data-stu-id="4023b-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="4023b-141"><span id="NAA"></span><span id="naa"></span>**Naa** (9)</span><span class="sxs-lookup"><span data-stu-id="4023b-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4023b-142">9 = Naa als generisches Format.</span><span class="sxs-lookup"><span data-stu-id="4023b-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="4023b-143">Siehe</span><span class="sxs-lookup"><span data-stu-id="4023b-143">See</span></span>

<span data-ttu-id="4023b-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="4023b-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="4023b-145">Formatiert als 16 oder 32 nicht getrennte hexadezimal Zeichen (2 pro binäres Byte).</span><span class="sxs-lookup"><span data-stu-id="4023b-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="4023b-146">Beispiel: "21000020372d3c73"</span><span class="sxs-lookup"><span data-stu-id="4023b-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="4023b-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="4023b-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="4023b-148">EUI als generisches Format (EUI64) finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="4023b-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="4023b-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="4023b-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="4023b-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="4023b-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="4023b-151">T10-Hersteller Bezeichnerformat, wie von der SCSI-Abfrage VPD-Seite 83, Bezeichnertyp 1 zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="4023b-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="4023b-152">Weitere Informationen finden Sie unter T10 SPC-3-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="4023b-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="4023b-153">Dies ist die 8-Byte-ASCII-Anbieter-ID aus der T10-Registrierung, gefolgt von einem herstellerspezifischen ASCII-Bezeichner. Leerzeichen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="4023b-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="4023b-154">Bei nicht-SCSI-Volumes ist "snvm" möglicherweise die geeignetste Wahl.</span><span class="sxs-lookup"><span data-stu-id="4023b-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="4023b-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Betriebssystem-Geräte Name** (12)</span><span class="sxs-lookup"><span data-stu-id="4023b-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="4023b-156">Betriebssystem-Geräte Name (für logicaldisks).</span><span class="sxs-lookup"><span data-stu-id="4023b-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="4023b-157">Ausführliche Informationen finden Sie unter LogicalDisk Name Description.</span><span class="sxs-lookup"><span data-stu-id="4023b-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4023b-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4023b-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4023b-159">**Hostextentnamenamespace**</span><span class="sxs-lookup"><span data-stu-id="4023b-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-160">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4023b-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-162">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentname**","**CIM \_ storagezugecationsettingdata**.**Otherhostextentnamenamespace**","**CIM \_ storagezugecationsettingdata**.**Hostextentnameformat**","[**CIM \_ storageblock**](cim-storageextent.md).**Namespace**")</span><span class="sxs-lookup"><span data-stu-id="4023b-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-163">Das Benennungs Format für die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4023b-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4023b-164">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4023b-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4023b-165">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4023b-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="4023b-166">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="4023b-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="4023b-167">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="4023b-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="4023b-168">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="4023b-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="4023b-169">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="4023b-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="4023b-170">**NoDebug** (6)</span><span class="sxs-lookup"><span data-stu-id="4023b-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="4023b-171">**Snvm** (7)</span><span class="sxs-lookup"><span data-stu-id="4023b-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="4023b-172">**Betriebssystem-Geräte Namespace** (8)</span><span class="sxs-lookup"><span data-stu-id="4023b-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4023b-173">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4023b-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4023b-174">**Hostextentstartingaddress**</span><span class="sxs-lookup"><span data-stu-id="4023b-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-175">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4023b-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-177">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**"Hastresourceblocksize**", "[**CIM \_ BasedOn**](cim-basedon.md)".**StartingAddress**")</span><span class="sxs-lookup"><span data-stu-id="4023b-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-178">Die Startadresse des Host Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="4023b-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="4023b-179">Ein NULL-Val; ue gibt an, dass es keine direkte Zuordnung zwischen dem virtuellen Speicherblock und dem Host Speicherblock gibt.</span><span class="sxs-lookup"><span data-stu-id="4023b-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="4023b-180">**"Hastresourceblocksize"**</span><span class="sxs-lookup"><span data-stu-id="4023b-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-181">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4023b-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-183">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**BlockSize**"), **Punit** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="4023b-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-184">Die Größe (in Bytes) der Blöcke, die auf dem Host für die Speicher Belegung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="4023b-185">Wenn die Blockgröße variabel ist, muss die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="4023b-186">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht zutrifft, sollte der Wert "1" (unbekannt) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="4023b-187">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="4023b-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-188">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4023b-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-190">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Limit"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezucationsettingdata**".**"Hastresourceblocksize**")</span><span class="sxs-lookup"><span data-stu-id="4023b-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-191">Die maximale Block Menge, die für die Speicherressourcen Zuordnung auf dem Host erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="4023b-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="4023b-192">Die Blockgröße wird durch die Eigenschaft " **hustresourceblocksize** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="4023b-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="4023b-193">**Otherhostextentnameformat**</span><span class="sxs-lookup"><span data-stu-id="4023b-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4023b-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-196">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentnameformat**")</span><span class="sxs-lookup"><span data-stu-id="4023b-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-197">Das Format der **hostextentname** -Eigenschaft, wenn die-Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4023b-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="4023b-198">**Otherhostextentnamenamespace**</span><span class="sxs-lookup"><span data-stu-id="4023b-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4023b-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-201">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentnamenamespace**")</span><span class="sxs-lookup"><span data-stu-id="4023b-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-202">Eine Zeichenfolge, die den Namespace der **hostextentname** -Eigenschaft beschreibt, wenn der Wert der **hostextentnamenamespace** -Eigenschaft "1" (sonstige) ist.</span><span class="sxs-lookup"><span data-stu-id="4023b-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="4023b-203">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="4023b-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-204">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4023b-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-206">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Reservierung"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**"Hastresourceblocksize**")</span><span class="sxs-lookup"><span data-stu-id="4023b-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-207">Die Anzahl der Blöcke, die garantiert für die Speicherressourcen Zuordnung auf dem Host verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4023b-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="4023b-208">Die Blockgröße wird durch die Eigenschaft " **hustresourceblocksize** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="4023b-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="4023b-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="4023b-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-210">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4023b-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-212">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("virtualmenge"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**"Anzahlungsblöcke**", "**CIM \_ storagezugecationsettingdata**".**Virtualquantityunits**")</span><span class="sxs-lookup"><span data-stu-id="4023b-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-213">Die Anzahl der Blöcke, die die Speicher Belegung für den Consumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="4023b-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="4023b-214">Die **virtualmenge** -Eigenschaft kann eine Blockgröße von "1" angeben, auch wenn " **virtualresourceblocksize** " unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4023b-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="4023b-215">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="4023b-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4023b-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-218">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("virtualquantityunits"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugegenationsettingdata**".**Virtualmenge**"), **ispunit**</span><span class="sxs-lookup"><span data-stu-id="4023b-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="4023b-219">Die Einheiten, die von der **virtualmenge** -Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="4023b-220">Dieser Wert muss auf "count (Block mit fester Größe)" oder "Byte" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="4023b-221">Der Standardwert "count (Block mit fester Größe)" sollte für eine Blockgröße mit fester Größe verwendet werden, und "Byte" sollte für eine unbekannte oder Variable Blockgröße verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="4023b-222">**Virtualresourceblocksize**</span><span class="sxs-lookup"><span data-stu-id="4023b-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4023b-223">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4023b-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4023b-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4023b-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4023b-225">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**BlockSize**"), **Punit** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="4023b-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="4023b-226">Die Größe (in Bytes) der Blöcke, die die Speicher Belegungs Anforderung bilden.</span><span class="sxs-lookup"><span data-stu-id="4023b-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="4023b-227">Wenn die Blockgröße variabel ist, muss die maximale Blockgröße angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4023b-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="4023b-228">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht zutrifft, sollte die Blockgröße "1" (unbekannt) lauten.</span><span class="sxs-lookup"><span data-stu-id="4023b-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4023b-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4023b-229">Requirements</span></span>



| <span data-ttu-id="4023b-230">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4023b-230">Requirement</span></span> | <span data-ttu-id="4023b-231">Wert</span><span class="sxs-lookup"><span data-stu-id="4023b-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4023b-232">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4023b-232">Minimum supported client</span></span><br/> | <span data-ttu-id="4023b-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4023b-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4023b-234">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4023b-234">Minimum supported server</span></span><br/> | <span data-ttu-id="4023b-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4023b-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4023b-236">Namespace</span><span class="sxs-lookup"><span data-stu-id="4023b-236">Namespace</span></span><br/>                | <span data-ttu-id="4023b-237">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4023b-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4023b-238">MOF</span><span class="sxs-lookup"><span data-stu-id="4023b-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4023b-239"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4023b-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4023b-240">DLL</span><span class="sxs-lookup"><span data-stu-id="4023b-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4023b-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4023b-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4023b-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4023b-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4023b-243">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="4023b-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

