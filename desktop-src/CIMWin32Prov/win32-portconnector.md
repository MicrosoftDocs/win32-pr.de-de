---
description: Die \_ WMI-Klasse für den Win32 portconnector stellt physische Verbindungsports dar, wie z. b. DB-25 Pin männlich, Centronics oder PS/2.
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Win32_PortConnector-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214049"
---
# <a name="win32_portconnector-class"></a><span data-ttu-id="9a82a-103">Win32 \_ portconnector-Klasse</span><span class="sxs-lookup"><span data-stu-id="9a82a-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="9a82a-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ portconnector** stellt physische Verbindungsports dar, wie z. b. DB-25 Pin männlich, Centronics oder PS/2.</span><span class="sxs-lookup"><span data-stu-id="9a82a-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="9a82a-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9a82a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9a82a-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9a82a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a82a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a82a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="9a82a-108">Member</span><span class="sxs-lookup"><span data-stu-id="9a82a-108">Members</span></span>

<span data-ttu-id="9a82a-109">Die **Win32 \_ portconnector** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9a82a-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="9a82a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9a82a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a82a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9a82a-111">Properties</span></span>

<span data-ttu-id="9a82a-112">Die **Win32 \_ portconnector** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9a82a-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a82a-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9a82a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9a82a-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-117">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9a82a-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="9a82a-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-119">**Connectoriout**</span><span class="sxs-lookup"><span data-stu-id="9a82a-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-122">Anheften Sie die Konfiguration und Signal Verwendung eines physischen Verbindungs-Connector.</span><span class="sxs-lookup"><span data-stu-id="9a82a-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="9a82a-123">Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-124">**Connector Type**</span><span class="sxs-lookup"><span data-stu-id="9a82a-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-125">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9a82a-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-127">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Connector Type"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| -Typ 8, \| interner/externer connectertyp")</span><span class="sxs-lookup"><span data-stu-id="9a82a-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-128">Array physischer Attribute der von diesem Port verwendeten Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9a82a-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="9a82a-129">Diese Eigenschaft wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="9a82a-130">In der folgenden Liste sind die-Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a82a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9a82a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9a82a-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9a82a-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="9a82a-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Männlich** (2)</span><span class="sxs-lookup"><span data-stu-id="9a82a-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="9a82a-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Weiblich** (3)</span><span class="sxs-lookup"><span data-stu-id="9a82a-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="9a82a-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Abgeschirmt** (4)</span><span class="sxs-lookup"><span data-stu-id="9a82a-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="9a82a-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>Nicht **gezitet** (5)</span><span class="sxs-lookup"><span data-stu-id="9a82a-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="9a82a-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 Pins)** (6)</span><span class="sxs-lookup"><span data-stu-id="9a82a-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="9a82a-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 Pins)** (7)</span><span class="sxs-lookup"><span data-stu-id="9a82a-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="9a82a-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 Pins)** (8)</span><span class="sxs-lookup"><span data-stu-id="9a82a-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="9a82a-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 Pins)** (9)</span><span class="sxs-lookup"><span data-stu-id="9a82a-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="9a82a-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 Pins)** (10)</span><span class="sxs-lookup"><span data-stu-id="9a82a-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="9a82a-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI-Fibre Channel (DB-9, Kupfer)** (11)</span><span class="sxs-lookup"><span data-stu-id="9a82a-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="9a82a-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI-Fibre Channel (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="9a82a-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="9a82a-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI-Fibre Channel SCA-II (40 Pins)** (13)</span><span class="sxs-lookup"><span data-stu-id="9a82a-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="9a82a-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI-Fibre Channel SCA-II (20 Pins)** (14)</span><span class="sxs-lookup"><span data-stu-id="9a82a-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="9a82a-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI-Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="9a82a-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="9a82a-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Zoll (40 Pins)** (16)</span><span class="sxs-lookup"><span data-stu-id="9a82a-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="9a82a-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Zoll (44 Pins)** (17)</span><span class="sxs-lookup"><span data-stu-id="9a82a-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="9a82a-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="9a82a-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="9a82a-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="9a82a-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="9a82a-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="9a82a-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="9a82a-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="9a82a-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="9a82a-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="9a82a-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="9a82a-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="9a82a-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="9a82a-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="9a82a-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="9a82a-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="9a82a-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="9a82a-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="9a82a-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="9a82a-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="9a82a-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="9a82a-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="9a82a-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="9a82a-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="9a82a-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="9a82a-161"><span id="v.35"></span>**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="9a82a-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="9a82a-162"><span id="x.21"></span>**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="9a82a-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="9a82a-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="9a82a-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="9a82a-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="9a82a-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="9a82a-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Kategorie 3** (34)</span><span class="sxs-lookup"><span data-stu-id="9a82a-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="9a82a-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Kategorie 4** (35)</span><span class="sxs-lookup"><span data-stu-id="9a82a-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="9a82a-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Kategorie 5** (36)</span><span class="sxs-lookup"><span data-stu-id="9a82a-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="9a82a-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="9a82a-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="9a82a-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="9a82a-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="9a82a-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="9a82a-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="9a82a-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span><span class="sxs-lookup"><span data-stu-id="9a82a-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="9a82a-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="9a82a-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="9a82a-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple-GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="9a82a-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="9a82a-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="9a82a-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="9a82a-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="9a82a-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="9a82a-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="9a82a-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="9a82a-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="9a82a-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="9a82a-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="9a82a-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="9a82a-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA-Typ I** (48)</span><span class="sxs-lookup"><span data-stu-id="9a82a-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="9a82a-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA-Typ II** (49)</span><span class="sxs-lookup"><span data-stu-id="9a82a-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="9a82a-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA-Typ III** (50)</span><span class="sxs-lookup"><span data-stu-id="9a82a-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="9a82a-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV-Port** (51)</span><span class="sxs-lookup"><span data-stu-id="9a82a-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="9a82a-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="9a82a-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="9a82a-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="9a82a-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="9a82a-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="9a82a-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="9a82a-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="9a82a-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="9a82a-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 Pins)** (56)</span><span class="sxs-lookup"><span data-stu-id="9a82a-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="9a82a-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="9a82a-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="9a82a-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="9a82a-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="9a82a-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="9a82a-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="9a82a-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="9a82a-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="9a82a-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="9a82a-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="9a82a-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarot** (62)</span><span class="sxs-lookup"><span data-stu-id="9a82a-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="9a82a-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span><span class="sxs-lookup"><span data-stu-id="9a82a-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="9a82a-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="9a82a-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="9a82a-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="9a82a-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="9a82a-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Zentronik** (66)</span><span class="sxs-lookup"><span data-stu-id="9a82a-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="9a82a-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-centronik** (67)</span><span class="sxs-lookup"><span data-stu-id="9a82a-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="9a82a-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Minicentronics Type-14** (68)</span><span class="sxs-lookup"><span data-stu-id="9a82a-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="9a82a-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Minicentronics Type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="9a82a-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="9a82a-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Minicentronics Type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="9a82a-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="9a82a-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Busmaus** (71)</span><span class="sxs-lookup"><span data-stu-id="9a82a-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="9a82a-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="9a82a-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="9a82a-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="9a82a-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="9a82a-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME-Bus** (74)</span><span class="sxs-lookup"><span data-stu-id="9a82a-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="9a82a-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="9a82a-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="9a82a-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietär** (76)</span><span class="sxs-lookup"><span data-stu-id="9a82a-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="9a82a-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Platzhalter für proprietäre Prozessorkarte** (77)</span><span class="sxs-lookup"><span data-stu-id="9a82a-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="9a82a-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>Geschützter **Speicherkarten Slot** (78)</span><span class="sxs-lookup"><span data-stu-id="9a82a-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="9a82a-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Eigener e/a-Riser-Slot** (79)</span><span class="sxs-lookup"><span data-stu-id="9a82a-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="9a82a-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHz** (80)</span><span class="sxs-lookup"><span data-stu-id="9a82a-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="9a82a-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="9a82a-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="9a82a-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="9a82a-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="9a82a-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="9a82a-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="9a82a-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="9a82a-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-216">PC-98-hireso</span><span class="sxs-lookup"><span data-stu-id="9a82a-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="9a82a-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="9a82a-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="9a82a-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98note** (86)</span><span class="sxs-lookup"><span data-stu-id="9a82a-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="9a82a-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98full** (87)</span><span class="sxs-lookup"><span data-stu-id="9a82a-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="9a82a-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span><span class="sxs-lookup"><span data-stu-id="9a82a-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-221">SSE SCSI</span><span class="sxs-lookup"><span data-stu-id="9a82a-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="9a82a-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**Auf der boarddiskette** (89)</span><span class="sxs-lookup"><span data-stu-id="9a82a-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-223">Kreisförmig</span><span class="sxs-lookup"><span data-stu-id="9a82a-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="9a82a-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Dual Inline (Pin 10 Ausschneiden)** (90)</span><span class="sxs-lookup"><span data-stu-id="9a82a-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-225">On-board-IDE-Connector</span><span class="sxs-lookup"><span data-stu-id="9a82a-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="9a82a-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (PIN 26-Ausschneiden)** (91)</span><span class="sxs-lookup"><span data-stu-id="9a82a-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-227">Auf dem Disketten Verbinder</span><span class="sxs-lookup"><span data-stu-id="9a82a-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="9a82a-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span><span class="sxs-lookup"><span data-stu-id="9a82a-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-229">9 Dual Inline anheften</span><span class="sxs-lookup"><span data-stu-id="9a82a-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="9a82a-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span><span class="sxs-lookup"><span data-stu-id="9a82a-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-231">25 Pin Dual Inline</span><span class="sxs-lookup"><span data-stu-id="9a82a-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="9a82a-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**Audioeingabe von CD-ROM** (94)</span><span class="sxs-lookup"><span data-stu-id="9a82a-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="9a82a-233">50 Pin Dual Inline</span><span class="sxs-lookup"><span data-stu-id="9a82a-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-234">95</span><span class="sxs-lookup"><span data-stu-id="9a82a-234">95</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-235">68 Pin Dual Inline</span><span class="sxs-lookup"><span data-stu-id="9a82a-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-236">96</span><span class="sxs-lookup"><span data-stu-id="9a82a-236">96</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-237">On Board Sound Connector</span><span class="sxs-lookup"><span data-stu-id="9a82a-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-238">97</span><span class="sxs-lookup"><span data-stu-id="9a82a-238">97</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="9a82a-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-240">98</span><span class="sxs-lookup"><span data-stu-id="9a82a-240">98</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-241">PCI-X</span><span class="sxs-lookup"><span data-stu-id="9a82a-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-242">99</span><span class="sxs-lookup"><span data-stu-id="9a82a-242">99</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-243">SBus IEEE 1396-1993 32 Bit</span><span class="sxs-lookup"><span data-stu-id="9a82a-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-244">100</span><span class="sxs-lookup"><span data-stu-id="9a82a-244">100</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-245">SBus IEEE 1396-1993 64 Bit</span><span class="sxs-lookup"><span data-stu-id="9a82a-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-246">101</span><span class="sxs-lookup"><span data-stu-id="9a82a-246">101</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-247">MCA</span><span class="sxs-lookup"><span data-stu-id="9a82a-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-248">102</span><span class="sxs-lookup"><span data-stu-id="9a82a-248">102</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-249">Sant</span><span class="sxs-lookup"><span data-stu-id="9a82a-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-250">103</span><span class="sxs-lookup"><span data-stu-id="9a82a-250">103</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-251">XIO</span><span class="sxs-lookup"><span data-stu-id="9a82a-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-252">104</span><span class="sxs-lookup"><span data-stu-id="9a82a-252">104</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-253">HI</span><span class="sxs-lookup"><span data-stu-id="9a82a-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-254">105</span><span class="sxs-lookup"><span data-stu-id="9a82a-254">105</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-255">Ngio</span><span class="sxs-lookup"><span data-stu-id="9a82a-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-256">106</span><span class="sxs-lookup"><span data-stu-id="9a82a-256">106</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-257">PMC</span><span class="sxs-lookup"><span data-stu-id="9a82a-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-258">107</span><span class="sxs-lookup"><span data-stu-id="9a82a-258">107</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-259">MTRJ</span><span class="sxs-lookup"><span data-stu-id="9a82a-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-260">108</span><span class="sxs-lookup"><span data-stu-id="9a82a-260">108</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-261">VF-45</span><span class="sxs-lookup"><span data-stu-id="9a82a-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-262">109</span><span class="sxs-lookup"><span data-stu-id="9a82a-262">109</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-263">Zukünftige e/a-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="9a82a-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-264">110</span><span class="sxs-lookup"><span data-stu-id="9a82a-264">110</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-265">SC</span><span class="sxs-lookup"><span data-stu-id="9a82a-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-266">111</span><span class="sxs-lookup"><span data-stu-id="9a82a-266">111</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-267">SG</span><span class="sxs-lookup"><span data-stu-id="9a82a-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-268">112</span><span class="sxs-lookup"><span data-stu-id="9a82a-268">112</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-269">Electrical</span><span class="sxs-lookup"><span data-stu-id="9a82a-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-270">113</span><span class="sxs-lookup"><span data-stu-id="9a82a-270">113</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-271">Optical</span><span class="sxs-lookup"><span data-stu-id="9a82a-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-272">114</span><span class="sxs-lookup"><span data-stu-id="9a82a-272">114</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-273">Menüband</span><span class="sxs-lookup"><span data-stu-id="9a82a-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-274">115</span><span class="sxs-lookup"><span data-stu-id="9a82a-274">115</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-275">GLM</span><span class="sxs-lookup"><span data-stu-id="9a82a-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-276">116</span><span class="sxs-lookup"><span data-stu-id="9a82a-276">116</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-277">1x9</span><span class="sxs-lookup"><span data-stu-id="9a82a-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-278">117</span><span class="sxs-lookup"><span data-stu-id="9a82a-278">117</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-279">Mini-SG</span><span class="sxs-lookup"><span data-stu-id="9a82a-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-280">118</span><span class="sxs-lookup"><span data-stu-id="9a82a-280">118</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-281">LC</span><span class="sxs-lookup"><span data-stu-id="9a82a-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-282">119</span><span class="sxs-lookup"><span data-stu-id="9a82a-282">119</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-283">HSSC</span><span class="sxs-lookup"><span data-stu-id="9a82a-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-284">120</span><span class="sxs-lookup"><span data-stu-id="9a82a-284">120</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-285">VHDCI abgeschirmt (68 Pins)</span><span class="sxs-lookup"><span data-stu-id="9a82a-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-286">121</span><span class="sxs-lookup"><span data-stu-id="9a82a-286">121</span></span>
</dt> <dd>

<span data-ttu-id="9a82a-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="9a82a-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a82a-288">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9a82a-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-291">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="9a82a-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-292">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a82a-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9a82a-293">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9a82a-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="9a82a-294">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-295">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9a82a-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-298">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9a82a-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-299">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a82a-299">Description of the object.</span></span>

<span data-ttu-id="9a82a-300">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-301">**ExternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="9a82a-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-304">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 8, \| externer Verweis Zeichner")</span><span class="sxs-lookup"><span data-stu-id="9a82a-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-305">Externer Verweis Kenn Zeichner des Ports.</span><span class="sxs-lookup"><span data-stu-id="9a82a-305">External reference designator of the port.</span></span> <span data-ttu-id="9a82a-306">Externe Verweis Kenn Zeichner sind Bezeichner, die den Typ und die Verwendung des Ports bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9a82a-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="9a82a-307">Beispiel: "COM1"</span><span class="sxs-lookup"><span data-stu-id="9a82a-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9a82a-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-309">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9a82a-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-311">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9a82a-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-312">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a82a-312">Date and time the object is installed.</span></span> <span data-ttu-id="9a82a-313">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9a82a-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9a82a-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-315">**Internalreferencedesignator**</span><span class="sxs-lookup"><span data-stu-id="9a82a-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-318">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 8, \| interner Verweis Zeichner")</span><span class="sxs-lookup"><span data-stu-id="9a82a-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-319">Interner Verweis Kenn Zeichner des Ports.</span><span class="sxs-lookup"><span data-stu-id="9a82a-319">Internal reference designator of the port.</span></span> <span data-ttu-id="9a82a-320">Interne Verweis Kenn Zeichner sind für den Hersteller spezifisch und identifizieren den Standort oder die Verwendung des Ports.</span><span class="sxs-lookup"><span data-stu-id="9a82a-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="9a82a-321">Beispiel: "J101"</span><span class="sxs-lookup"><span data-stu-id="9a82a-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-322">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="9a82a-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-325">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="9a82a-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-326">Der Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="9a82a-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="9a82a-327">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-328">**Modell**</span><span class="sxs-lookup"><span data-stu-id="9a82a-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-331">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="9a82a-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-332">Der Name für das physische Element.</span><span class="sxs-lookup"><span data-stu-id="9a82a-332">Name for the physical element.</span></span>

<span data-ttu-id="9a82a-333">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-334">**Name**</span><span class="sxs-lookup"><span data-stu-id="9a82a-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-335">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-337">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9a82a-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-338">Die Bezeichnung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-338">Label for the object.</span></span> <span data-ttu-id="9a82a-339">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9a82a-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9a82a-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9a82a-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-344">Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9a82a-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="9a82a-345">Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="9a82a-346">Wenn nur Barcode Daten verfügbar und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** , und die Barcode Daten werden als Klassen Schlüssel in der Tag-Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a82a-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="9a82a-347">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-348">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="9a82a-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-351">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="9a82a-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-352">Teilenummer, die von der Organisation zugewiesen wurde, die für das Erstellen oder die Herstellung des physischen Elements verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="9a82a-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="9a82a-353">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-354">**PortType**</span><span class="sxs-lookup"><span data-stu-id="9a82a-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-355">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9a82a-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-357">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 8- \| Porttyp")</span><span class="sxs-lookup"><span data-stu-id="9a82a-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-358">Funktion des Ports.</span><span class="sxs-lookup"><span data-stu-id="9a82a-358">Function of the port.</span></span> <span data-ttu-id="9a82a-359">In der folgenden Liste sind die-Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9a82a-360">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="9a82a-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="9a82a-361">**Paralleler Port XT/bei kompatibel** (1)</span><span class="sxs-lookup"><span data-stu-id="9a82a-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="9a82a-362">**Paralleler Port PS/2** (2)</span><span class="sxs-lookup"><span data-stu-id="9a82a-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="9a82a-363">**Paralleler Port-ECP** (3)</span><span class="sxs-lookup"><span data-stu-id="9a82a-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="9a82a-364">**Paralleler Port-EPP** (4)</span><span class="sxs-lookup"><span data-stu-id="9a82a-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="9a82a-365">**Paralleler Port ECP/EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="9a82a-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="9a82a-366">**Serial Port XT/AT kompatibel** (6)</span><span class="sxs-lookup"><span data-stu-id="9a82a-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="9a82a-367">**Serieller Port 16450 kompatibel** (7)</span><span class="sxs-lookup"><span data-stu-id="9a82a-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="9a82a-368">**Serieller Port 16550 kompatibel** (8)</span><span class="sxs-lookup"><span data-stu-id="9a82a-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="9a82a-369">**Serieller Port 16550ein kompatibler** (9)</span><span class="sxs-lookup"><span data-stu-id="9a82a-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="9a82a-370">**SCSI-Port** (10)</span><span class="sxs-lookup"><span data-stu-id="9a82a-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="9a82a-371">**MIDI-Port** (11)</span><span class="sxs-lookup"><span data-stu-id="9a82a-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="9a82a-372">" **Joy Stick** "-Port (12)</span><span class="sxs-lookup"><span data-stu-id="9a82a-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="9a82a-373">**Tastatur Anschluss** (13)</span><span class="sxs-lookup"><span data-stu-id="9a82a-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="9a82a-374">**Mausport** (14)</span><span class="sxs-lookup"><span data-stu-id="9a82a-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="9a82a-375">SSE **SCSI** (15)</span><span class="sxs-lookup"><span data-stu-id="9a82a-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="9a82a-376">**USB** (16)</span><span class="sxs-lookup"><span data-stu-id="9a82a-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="9a82a-377">**FireWire (IEEE P1394)** (17)</span><span class="sxs-lookup"><span data-stu-id="9a82a-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="9a82a-378">**PCMCIA-Typ II** (18)</span><span class="sxs-lookup"><span data-stu-id="9a82a-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="9a82a-379">**PCMCIA-Typ II** (19)</span><span class="sxs-lookup"><span data-stu-id="9a82a-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="9a82a-380">**PCMCIA-Typ III** (20)</span><span class="sxs-lookup"><span data-stu-id="9a82a-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="9a82a-381">**CardBus** (21)</span><span class="sxs-lookup"><span data-stu-id="9a82a-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="9a82a-382">**Access Bus Port** (22)</span><span class="sxs-lookup"><span data-stu-id="9a82a-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="9a82a-383">**SCSI II** (23)</span><span class="sxs-lookup"><span data-stu-id="9a82a-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="9a82a-384">**SCSI (breit** ) (24)</span><span class="sxs-lookup"><span data-stu-id="9a82a-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="9a82a-385">**PC-98** (25)</span><span class="sxs-lookup"><span data-stu-id="9a82a-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="9a82a-386">**PC-98-hireso** (26)</span><span class="sxs-lookup"><span data-stu-id="9a82a-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="9a82a-387">**PC-H98** (27)</span><span class="sxs-lookup"><span data-stu-id="9a82a-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="9a82a-388">**Videoport** (28)</span><span class="sxs-lookup"><span data-stu-id="9a82a-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="9a82a-389">**Audioport** (29)</span><span class="sxs-lookup"><span data-stu-id="9a82a-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="9a82a-390">**Modem Anschluss** (30)</span><span class="sxs-lookup"><span data-stu-id="9a82a-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="9a82a-391">**Netzwerkport** (31)</span><span class="sxs-lookup"><span data-stu-id="9a82a-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="9a82a-392">**8251 kompatibel** (32)</span><span class="sxs-lookup"><span data-stu-id="9a82a-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="9a82a-393">**8251 FIFO-kompatibel** (33)</span><span class="sxs-lookup"><span data-stu-id="9a82a-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a82a-394">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="9a82a-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-395">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9a82a-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-397">**True** gibt an, dass das physische Element eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="9a82a-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="9a82a-398">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-399">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="9a82a-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-402">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="9a82a-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-403">Vom Hersteller zugewiesene Nummer, mit der ein physisches Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9a82a-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="9a82a-404">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-405">**SKU**</span><span class="sxs-lookup"><span data-stu-id="9a82a-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-408">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="9a82a-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-409">Die Stock Keeping Unit-Nummer für ein physisches Element.</span><span class="sxs-lookup"><span data-stu-id="9a82a-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="9a82a-410">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-411">**Status**</span><span class="sxs-lookup"><span data-stu-id="9a82a-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-414">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9a82a-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-415">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a82a-415">Current status of the object.</span></span> <span data-ttu-id="9a82a-416">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a82a-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9a82a-417">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="9a82a-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9a82a-418">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="9a82a-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9a82a-419">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a82a-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9a82a-420">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="9a82a-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9a82a-421">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9a82a-422">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="9a82a-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9a82a-423">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9a82a-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9a82a-424">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9a82a-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9a82a-425">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9a82a-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a82a-426">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9a82a-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9a82a-427">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9a82a-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9a82a-428">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9a82a-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9a82a-429">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9a82a-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9a82a-430">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9a82a-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9a82a-431">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9a82a-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9a82a-432">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9a82a-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9a82a-433">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9a82a-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9a82a-434">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9a82a-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a82a-435">**Tag**</span><span class="sxs-lookup"><span data-stu-id="9a82a-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-438">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9a82a-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-439">Eindeutiger Bezeichner einer Port Verbindung auf dem Computersystem.</span><span class="sxs-lookup"><span data-stu-id="9a82a-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="9a82a-440">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="9a82a-441">Beispiel: "Port-Connector 1"</span><span class="sxs-lookup"><span data-stu-id="9a82a-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-442">**Version**</span><span class="sxs-lookup"><span data-stu-id="9a82a-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a82a-443">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9a82a-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9a82a-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a82a-445">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="9a82a-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a82a-446">Version des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="9a82a-446">Version of the physical element.</span></span>

<span data-ttu-id="9a82a-447">Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9a82a-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a82a-448">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a82a-448">Remarks</span></span>

<span data-ttu-id="9a82a-449">Die **Win32 \_ portconnector** -Klasse wird von [**CIM \_ physicalconnector**](cim-physicalconnector.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9a82a-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a82a-450">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a82a-450">Requirements</span></span>



| <span data-ttu-id="9a82a-451">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a82a-451">Requirement</span></span> | <span data-ttu-id="9a82a-452">Wert</span><span class="sxs-lookup"><span data-stu-id="9a82a-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a82a-453">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a82a-453">Minimum supported client</span></span><br/> | <span data-ttu-id="9a82a-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a82a-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a82a-455">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a82a-455">Minimum supported server</span></span><br/> | <span data-ttu-id="9a82a-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a82a-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a82a-457">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a82a-457">Namespace</span></span><br/>                | <span data-ttu-id="9a82a-458">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9a82a-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a82a-459">MOF</span><span class="sxs-lookup"><span data-stu-id="9a82a-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a82a-460"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9a82a-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a82a-461">DLL</span><span class="sxs-lookup"><span data-stu-id="9a82a-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a82a-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a82a-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a82a-463">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a82a-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a82a-464">**CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="9a82a-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="9a82a-465">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9a82a-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
