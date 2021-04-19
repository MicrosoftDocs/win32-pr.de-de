---
description: Win32 \_ tcpipprinterport&\# 32; Die WMI-Klasse stellt einen TCP/IP-Dienst Zugriffspunkt dar.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Win32_TCPIPPrinterPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343199"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="93572-103">Win32 \_ tcpipprinterport-Klasse</span><span class="sxs-lookup"><span data-stu-id="93572-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="93572-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ tcpipprinterport** " stellt einen TCP/IP-Dienst Zugriffspunkt dar.</span><span class="sxs-lookup"><span data-stu-id="93572-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="93572-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93572-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="93572-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="93572-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93572-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="93572-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="93572-108">Member</span><span class="sxs-lookup"><span data-stu-id="93572-108">Members</span></span>

<span data-ttu-id="93572-109">Die **Win32 \_ tcpipprinterport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="93572-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="93572-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93572-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93572-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93572-111">Properties</span></span>

<span data-ttu-id="93572-112">Die **Win32 \_ tcpipprinterport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93572-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93572-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="93572-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-114">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93572-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93572-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-116">**True** gibt an, dass der Computer die Bytes in einem Dokument anzählt, bevor Sie an den Drucker gesendet werden, und der Drucker meldet die Anzahl der tatsächlich gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="93572-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="93572-117">Diese Funktion wird für die Diagnose verwendet, wenn fehlende Bytes in der Druckausgabe erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="93572-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="93572-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="93572-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-121">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="93572-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="93572-122">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93572-122">A short textual description of the object.</span></span>

<span data-ttu-id="93572-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-124">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="93572-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-127">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="93572-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="93572-128">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93572-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="93572-129">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="93572-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="93572-130">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93572-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-134">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="93572-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="93572-135">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93572-135">A textual description of the object.</span></span>

<span data-ttu-id="93572-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-137">**Host Kleid**</span><span class="sxs-lookup"><span data-stu-id="93572-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-140">Adresse des Geräts oder Druck Servers.</span><span class="sxs-lookup"><span data-stu-id="93572-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="93572-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93572-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-142">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="93572-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93572-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-144">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="93572-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="93572-145">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="93572-145">Indicates when the object was installed.</span></span> <span data-ttu-id="93572-146">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="93572-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="93572-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="93572-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-151">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="93572-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="93572-152">Identifiziert den Dienst Zugriffspunkt eindeutig und gibt Aufschluss über die verwaltete Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="93572-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="93572-153">Diese Funktionalität wird in der Description-Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="93572-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="93572-154">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-155">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="93572-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93572-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93572-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-158">Die Anzahl der TCP-Ports, die vom Port Monitor für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93572-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="93572-159">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="93572-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93572-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93572-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-162">Das Druck Protokoll wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="93572-162">Printing protocol used.</span></span> <span data-ttu-id="93572-163">Einige Drucker unterstützen nur LPR.</span><span class="sxs-lookup"><span data-stu-id="93572-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="93572-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="93572-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="93572-165">RAW</span><span class="sxs-lookup"><span data-stu-id="93572-165">RAW</span></span>

<span data-ttu-id="93572-166">Direktes Drucken auf einem Gerät oder Druckserver.</span><span class="sxs-lookup"><span data-stu-id="93572-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="93572-167"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="93572-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="93572-168">LPR</span><span class="sxs-lookup"><span data-stu-id="93572-168">LPR</span></span>

<span data-ttu-id="93572-169">Legacy-Protokoll, das letztendlich durch RAW ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="93572-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93572-170">**Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="93572-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-173">Der Name der Druck Warteschlange auf dem Server, wenn er mit dem LPR-Protokoll verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93572-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="93572-174">**SNMPCommunity**</span><span class="sxs-lookup"><span data-stu-id="93572-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-177">Sicherheitsstufen Wert für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="93572-177">Security level value for the device.</span></span>

<span data-ttu-id="93572-178">Beispiel: "Public"</span><span class="sxs-lookup"><span data-stu-id="93572-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="93572-179">**SNMPDevIndex**</span><span class="sxs-lookup"><span data-stu-id="93572-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-180">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93572-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93572-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-182">SNMP-Indexnummer dieses Geräts für den SNMP-Agent.</span><span class="sxs-lookup"><span data-stu-id="93572-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="93572-183">**Snmpaktivierte**</span><span class="sxs-lookup"><span data-stu-id="93572-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93572-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93572-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93572-186">**True** gibt an, dass dieser Drucker [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) unterstützt und umfassende Statusinformationen vom Gerät bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="93572-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="93572-187">**Status**</span><span class="sxs-lookup"><span data-stu-id="93572-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-190">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="93572-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="93572-191">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="93572-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="93572-192">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="93572-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="93572-193">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="93572-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="93572-194">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="93572-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="93572-195">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="93572-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="93572-196">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="93572-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="93572-197">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="93572-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="93572-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="93572-199">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="93572-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="93572-200">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="93572-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="93572-201">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="93572-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="93572-202">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="93572-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93572-203">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="93572-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="93572-204">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="93572-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="93572-205">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="93572-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="93572-206">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="93572-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="93572-207">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="93572-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="93572-208">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="93572-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="93572-209">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="93572-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="93572-210">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="93572-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="93572-211">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="93572-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93572-212">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="93572-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-215">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="93572-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="93572-216">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="93572-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="93572-217">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-218">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="93572-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93572-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93572-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-221">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="93572-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="93572-222">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="93572-222">The scoping system's name.</span></span>

<span data-ttu-id="93572-223">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="93572-224">**Type**</span><span class="sxs-lookup"><span data-stu-id="93572-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93572-225">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93572-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93572-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93572-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93572-227">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93572-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93572-228">Typ von SAP, z. b. angefügt oder umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="93572-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="93572-229">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93572-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="93572-230">**Schreiben** (1)</span><span class="sxs-lookup"><span data-stu-id="93572-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="93572-231">**Lesen** (2)</span><span class="sxs-lookup"><span data-stu-id="93572-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="93572-232">**Umgeleitet** (4)</span><span class="sxs-lookup"><span data-stu-id="93572-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="93572-233">**Net \_ Angefügt** (8)</span><span class="sxs-lookup"><span data-stu-id="93572-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93572-234">**unbekannt** (16)</span><span class="sxs-lookup"><span data-stu-id="93572-234">**unknown** (16)</span></span>


<span data-ttu-id="93572-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="93572-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="93572-236">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93572-236">Remarks</span></span>

<span data-ttu-id="93572-237">Die **Win32-Klasse \_ tcpipprinterport** wird von [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) abgeleitet, das von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="93572-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="93572-238">Zum Löschen einer Instanz dieser WMI-Klasse ist die **SeLoadDriverPrivilege** -Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93572-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="93572-239">Der folgende Skript Ausschnitt veranschaulicht, wie Sie eine Verbindung mit WMI herstellen, die diese Berechtigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="93572-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="93572-240">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93572-240">Examples</span></span>

<span data-ttu-id="93572-241">Das folgende PowerShell-Beispiel entfernt einen Drucker und den zugeordneten tcpip-Druckerport.</span><span class="sxs-lookup"><span data-stu-id="93572-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="93572-242">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93572-242">Requirements</span></span>



| <span data-ttu-id="93572-243">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93572-243">Requirement</span></span> | <span data-ttu-id="93572-244">Wert</span><span class="sxs-lookup"><span data-stu-id="93572-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93572-245">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93572-245">Minimum supported client</span></span><br/> | <span data-ttu-id="93572-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93572-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="93572-247">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93572-247">Minimum supported server</span></span><br/> | <span data-ttu-id="93572-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93572-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="93572-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="93572-249">Namespace</span></span><br/>                | <span data-ttu-id="93572-250">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93572-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="93572-251">MOF</span><span class="sxs-lookup"><span data-stu-id="93572-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93572-252"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="93572-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="93572-253">DLL</span><span class="sxs-lookup"><span data-stu-id="93572-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93572-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93572-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="93572-255">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93572-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93572-256">**CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="93572-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="93572-257">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="93572-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
