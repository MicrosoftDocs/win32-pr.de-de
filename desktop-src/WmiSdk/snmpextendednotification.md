---
description: Die snmpextendednotification-Klasse ist die Basisklasse für jede Klasse, die vom Notification-Type-Makro einer CIM-Klasse durch den SNMP-Anbieter zugeordnet ist.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Snmpextendednotification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368216"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="2c7da-103">Snmpextendednotification-Klasse</span><span class="sxs-lookup"><span data-stu-id="2c7da-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="2c7da-104">Die **snmpextendednotification** -Klasse ist die Basisklasse für jede Klasse, die vom [Notification-Type-](notification-type-macro.md) Makro einer CIM-Klasse durch den [SNMP-Anbieter](snmp-provider.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2c7da-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="2c7da-105">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2c7da-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="2c7da-106">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c7da-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2c7da-107">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="2c7da-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7da-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c7da-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="2c7da-109">Member</span><span class="sxs-lookup"><span data-stu-id="2c7da-109">Members</span></span>

<span data-ttu-id="2c7da-110">Die **snmpextendednotification** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c7da-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="2c7da-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7da-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c7da-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7da-112">Properties</span></span>

<span data-ttu-id="2c7da-113">Die **snmpextendednotification** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c7da-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c7da-114">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="2c7da-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-117">Die Netzwerkadresse der Entität, die die Benachrichtigung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2c7da-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="2c7da-118">Dies ist die tatsächliche Adresse des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2c7da-118">This is the actual address of the device.</span></span> <span data-ttu-id="2c7da-119">Wenn die Verwaltungs Entität SNMP über UDP verwendet, bezieht sich die Transport Adresse auf eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2c7da-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="2c7da-120">Wenn die Verwaltungs Entität SNMP über IPX verwendet, wird die Transport Adresse auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2c7da-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="2c7da-121">Diese Eigenschaft ist nur für SNMPv1 gültig.</span><span class="sxs-lookup"><span data-stu-id="2c7da-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-122">**Agenttransport**</span><span class="sxs-lookup"><span data-stu-id="2c7da-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-125">Von der sendenden Entität verwendetes Transport Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2c7da-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="2c7da-126">Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2c7da-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-127">**Agenttransportaddress**</span><span class="sxs-lookup"><span data-stu-id="2c7da-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-130">Die Netzwerkadresse der Entität, die die Benachrichtigung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="2c7da-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="2c7da-131">Dies ist die Adresse der letzten Entität, die die Benachrichtigung weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="2c7da-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="2c7da-132">Wenn die Verwaltungs Entität SNMP über UDP verwendet, bezieht sich die Transport Adresse auf eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2c7da-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="2c7da-133">Wenn die Verwaltungs Entität SNMP über IPX verwendet, bezieht sich die Transport Adresse auf eine IPX-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2c7da-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="2c7da-134">Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2c7da-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-135">**Agenttransportprotocol**</span><span class="sxs-lookup"><span data-stu-id="2c7da-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-138">Das Transportprotokoll, das von der sendenden Entität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c7da-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-139">**Community**</span><span class="sxs-lookup"><span data-stu-id="2c7da-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-142">Der Communityname, der einer Instanz des PDU zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2c7da-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="2c7da-143">Der Communityname authentifiziert den Absender des PDU.</span><span class="sxs-lookup"><span data-stu-id="2c7da-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="2c7da-144">Diese Eigenschaft ist sowohl für SNMPv1 als auch für SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2c7da-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-145">**Identifikation**</span><span class="sxs-lookup"><span data-stu-id="2c7da-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-148">Qualifizierer: **Text \_ Konvention** ("objectidentifier"), **Codierung** ("objectidentifier"), **Objekt \_ Syntax** ("objectidentifier"), **Objekt \_ Bezeichner** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="2c7da-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-149">Autorisierende Identifizierung dieser Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2c7da-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="2c7da-150">Wird direkt dem MIB-Eintrag snmptrapoid-Variablen Bindung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2c7da-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="2c7da-151">Diese Eigenschaft ist nur für SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2c7da-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-152">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c7da-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-153">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="2c7da-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-155">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="2c7da-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2c7da-156">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c7da-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="2c7da-157">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2c7da-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-158">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="2c7da-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-159">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c7da-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-161">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2c7da-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2c7da-162">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c7da-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2c7da-163">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="2c7da-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="2c7da-164">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c7da-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="2c7da-165">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2c7da-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2c7da-166">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="2c7da-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7da-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c7da-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c7da-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7da-169">Qualifizierer: **Text \_ Konvention** ("TimeTicks"), **Codierung** ("TimeTicks"), **Objekt \_ Syntax** ("TimeTicks"), **Objekt \_ Bezeichner** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="2c7da-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="2c7da-170">Zeit in Hundertstel Sekunden, seit der Netzwerk Verwaltungsteil des Agents zuletzt erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2c7da-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="2c7da-171">Dies wird der MIB-Variablen "sysUpTime. 0" zugeordnet, die den Typ " **INTEGER32**" hat.</span><span class="sxs-lookup"><span data-stu-id="2c7da-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="2c7da-172">Diese Eigenschaft wird der Eigenschaft **timestamp** der CIM-Klasse zugeordnet, die vom Typ **UInt32** ist.</span><span class="sxs-lookup"><span data-stu-id="2c7da-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="2c7da-173">Diese Eigenschaft ist nur für SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2c7da-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c7da-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c7da-174">Remarks</span></span>

<span data-ttu-id="2c7da-175">Ein [Benachrichtigungstyp](notification-type-macro.md) Makro, das Verweise auf ein [Objekttyp](object-type-macro.md) Makro mit dem Namen **timestamp** oder **Identification** enthält, verursacht einen Mapping-Konflikt.</span><span class="sxs-lookup"><span data-stu-id="2c7da-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="2c7da-176">Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="2c7da-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="2c7da-177">Ein [-Benachrichtigungstyp](notification-type-macro.md) Makro, das Verweise auf ein [Objekttyp-](object-type-macro.md) Makro namens **Community** enthält, verursacht einen zuordnungskonflikt.</span><span class="sxs-lookup"><span data-stu-id="2c7da-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="2c7da-178">Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="2c7da-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7da-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7da-179">Requirements</span></span>



| <span data-ttu-id="2c7da-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c7da-180">Requirement</span></span> | <span data-ttu-id="2c7da-181">Wert</span><span class="sxs-lookup"><span data-stu-id="2c7da-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7da-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c7da-182">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7da-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c7da-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c7da-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c7da-184">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7da-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c7da-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c7da-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c7da-186">Namespace</span></span><br/>                | <span data-ttu-id="2c7da-187">Root \\ SNMP- \\ SMIR</span><span class="sxs-lookup"><span data-stu-id="2c7da-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="2c7da-188">MOF</span><span class="sxs-lookup"><span data-stu-id="2c7da-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c7da-189"><dt>Snmpsmir. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2c7da-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c7da-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7da-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7da-191">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="2c7da-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="2c7da-192">Notification-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="2c7da-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

