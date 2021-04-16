---
description: Die SnmpNotification-Klasse wird aus dem Notification-Type-Makro einer gekapselten CIM-Klasse zugeordnet.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: SnmpNotification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530209"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="2b400-103">SnmpNotification-Klasse</span><span class="sxs-lookup"><span data-stu-id="2b400-103">SnmpNotification class</span></span>

<span data-ttu-id="2b400-104">Die **SnmpNotification** -Klasse wird aus dem [Notification-Type-](notification-type-macro.md) Makro einer gekapselten CIM-Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2b400-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="2b400-105">Dabei handelt es sich um eine Basisklasse, die vom [SNMP-Anbieter](snmp-provider.md) für jede Klasse verwendet wird, die vom [Notification-Type-](notification-type-macro.md) Makro einer gekapselten CIM-Klasse des SNMP-Anbieters zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="2b400-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="2b400-106">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2b400-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2b400-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b400-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="2b400-108">Member</span><span class="sxs-lookup"><span data-stu-id="2b400-108">Members</span></span>

<span data-ttu-id="2b400-109">Die **SnmpNotification** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2b400-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="2b400-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b400-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b400-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b400-111">Properties</span></span>

<span data-ttu-id="2b400-112">Die **SnmpNotification** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2b400-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b400-113">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="2b400-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-116">Die Netzwerkadresse der Entität, die die Benachrichtigung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2b400-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="2b400-117">Dies ist die tatsächliche Adresse des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2b400-117">This is the actual address of the device.</span></span> <span data-ttu-id="2b400-118">Wenn die Verwaltungs Entität SNMP über UDP verwendet, bezieht sich die Transport Adresse auf eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2b400-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="2b400-119">Wenn die Verwaltungs Entität SNMP über IPX verwendet, wird die Transport Adresse auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b400-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="2b400-120">Diese Eigenschaft ist nur für SNMPv1 gültig.</span><span class="sxs-lookup"><span data-stu-id="2b400-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="2b400-121">**Agenttransport**</span><span class="sxs-lookup"><span data-stu-id="2b400-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-124">Von der sendenden Entität verwendetes Transport Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2b400-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="2b400-125">Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2b400-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="2b400-126">**Agenttransportaddress**</span><span class="sxs-lookup"><span data-stu-id="2b400-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-129">Die Netzwerkadresse der Entität, die die Benachrichtigung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="2b400-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="2b400-130">Dies ist die Adresse der letzten Entität, die die Benachrichtigung weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="2b400-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="2b400-131">Wenn die Verwaltungs Entität SNMP über UDP verwendet, bezieht sich die Transport Adresse auf eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2b400-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="2b400-132">Wenn die Verwaltungs Entität SNMP über IPX verwendet, bezieht sich die Transport Adresse auf eine IPX-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2b400-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="2b400-133">Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2b400-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="2b400-134">**Agenttransportprotocol**</span><span class="sxs-lookup"><span data-stu-id="2b400-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-137">Das Transportprotokoll, das von der sendenden Entität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b400-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="2b400-138">**Community**</span><span class="sxs-lookup"><span data-stu-id="2b400-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-141">Der Communityname, der einer Instanz des PDU zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2b400-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="2b400-142">Der Communityname authentifiziert den Absender des PDU.</span><span class="sxs-lookup"><span data-stu-id="2b400-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="2b400-143">Diese Eigenschaft ist sowohl für SNMPv1 als auch für SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2b400-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="2b400-144">**Identifikation**</span><span class="sxs-lookup"><span data-stu-id="2b400-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b400-147">Qualifizierer: **Text \_ Konvention** ("objectidentifier"), **Codierung** ("objectidentifier"), **Objekt \_ Syntax** ("objectidentifier"), **Objekt \_ Bezeichner** ("1.3.6.1.6.3.1.1.4.1")</span><span class="sxs-lookup"><span data-stu-id="2b400-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="2b400-148">Autorisierende Identifizierung dieser Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2b400-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="2b400-149">Wird direkt der snmptrapoid-Variablen Bindung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2b400-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="2b400-150">Diese Eigenschaft ist nur für SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2b400-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="2b400-151">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b400-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-152">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="2b400-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2b400-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-154">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="2b400-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2b400-155">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2b400-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="2b400-156">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2b400-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b400-157">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="2b400-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-158">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b400-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b400-160">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b400-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2b400-161">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b400-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2b400-162">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="2b400-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="2b400-163">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2b400-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="2b400-164">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2b400-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2b400-165">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="2b400-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b400-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b400-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b400-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b400-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b400-168">Qualifizierer: **Text \_ Konvention** ("TimeTicks"), **Codierung** ("TimeTicks"), **Objekt \_ Syntax** ("TimeTicks"), **Objekt \_ Bezeichner** ("1.3.6.1.2.1.1.3")</span><span class="sxs-lookup"><span data-stu-id="2b400-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="2b400-169">Zeit in Hundertstel Sekunden, seit der Netzwerk Verwaltungsteil des Agents zuletzt erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b400-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="2b400-170">MIB-Variable "sysUpTime. 0", die vom Typ " **INTEGER32**" ist.</span><span class="sxs-lookup"><span data-stu-id="2b400-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="2b400-171">Diese Eigenschaft wird der Eigenschaft **timestamp** der CIM-Klasse zugeordnet, die vom Typ **UInt32** ist.</span><span class="sxs-lookup"><span data-stu-id="2b400-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="2b400-172">Diese Eigenschaft ist nur für SNMPv2C gültig.</span><span class="sxs-lookup"><span data-stu-id="2b400-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b400-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b400-173">Remarks</span></span>

<span data-ttu-id="2b400-174">Ein [Benachrichtigungstyp](notification-type-macro.md) Makro, das Verweise auf ein [Objekttyp](object-type-macro.md) Makro mit dem Namen **timestamp** oder **Identification** enthält, verursacht einen Mapping-Konflikt.</span><span class="sxs-lookup"><span data-stu-id="2b400-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="2b400-175">Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="2b400-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="2b400-176">Ein [-Benachrichtigungstyp](notification-type-macro.md) Makro, das Verweise auf ein [Objekttyp-](object-type-macro.md) Makro namens **Community** enthält, verursacht einen zuordnungskonflikt.</span><span class="sxs-lookup"><span data-stu-id="2b400-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="2b400-177">Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="2b400-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b400-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b400-178">Requirements</span></span>



| <span data-ttu-id="2b400-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b400-179">Requirement</span></span> | <span data-ttu-id="2b400-180">Wert</span><span class="sxs-lookup"><span data-stu-id="2b400-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="2b400-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b400-181">Minimum supported client</span></span><br/> | <span data-ttu-id="2b400-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b400-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="2b400-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b400-183">Minimum supported server</span></span><br/> | <span data-ttu-id="2b400-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b400-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="2b400-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b400-185">Namespace</span></span><br/>                | <span data-ttu-id="2b400-186">Root \\ SNMP- \\ localhost</span><span class="sxs-lookup"><span data-stu-id="2b400-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b400-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b400-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b400-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="2b400-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="2b400-189">Notification-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="2b400-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

