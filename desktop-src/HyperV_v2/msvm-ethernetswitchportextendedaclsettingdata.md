---
description: Stellt die erweiterten Port-ACL-Einstellungen dar.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Msvm_EthernetSwitchPortExtendedAclSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348685"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="b9a18-103">MSVM \_ ethernetzwitchportextendedaclsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9a18-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="b9a18-104">Stellt die erweiterten Port-ACL-Einstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="b9a18-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="b9a18-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9a18-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a18-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9a18-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="b9a18-107">Member</span><span class="sxs-lookup"><span data-stu-id="b9a18-107">Members</span></span>

<span data-ttu-id="b9a18-108">Die **MSVM \_ ethernetzwitchportextendedaclsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b9a18-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b9a18-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9a18-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9a18-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9a18-110">Properties</span></span>

<span data-ttu-id="b9a18-111">Die **MSVM \_ ethernetzwitchportextendedaclsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9a18-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9a18-112">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="b9a18-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-113">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b9a18-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-115">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-116">Die Aktion der erweiterten ACL.</span><span class="sxs-lookup"><span data-stu-id="b9a18-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9a18-117">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="b9a18-118">**Zulassen** (1)</span><span class="sxs-lookup"><span data-stu-id="b9a18-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="b9a18-119">**Verweigern** (2)</span><span class="sxs-lookup"><span data-stu-id="b9a18-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9a18-120">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="b9a18-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-121">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b9a18-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-123">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-124">Gibt an, ob die erweiterte ACL für die eingehende oder ausgehende Richtung gilt.</span><span class="sxs-lookup"><span data-stu-id="b9a18-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9a18-125">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="b9a18-126">**Eingehende** (1)</span><span class="sxs-lookup"><span data-stu-id="b9a18-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="b9a18-127">**Ausgehend** (2)</span><span class="sxs-lookup"><span data-stu-id="b9a18-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9a18-128">**Idlesessiontimeout**</span><span class="sxs-lookup"><span data-stu-id="b9a18-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9a18-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-131">Qualifizierer: **wmidataid** (11), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-132">Timeout Wert für Leerlauf Sitzung (in Sekunden) für Zustands behaftete ACL.</span><span class="sxs-lookup"><span data-stu-id="b9a18-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-133">**Isolationid**</span><span class="sxs-lookup"><span data-stu-id="b9a18-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9a18-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-136">**Qualifizierer: interfacetten** (1), **interfacetten-Vision** (0), **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="b9a18-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-137">Die Isolations-ID, für die die erweiterte ACL angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a18-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-138">**LocalIPAddress**</span><span class="sxs-lookup"><span data-stu-id="b9a18-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9a18-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-141">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-142">Die lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b9a18-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="b9a18-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9a18-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-146">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-147">Der lokale Port Bereich.</span><span class="sxs-lookup"><span data-stu-id="b9a18-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="b9a18-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9a18-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-152">Der Anzeige Name der erweiterten ACL.</span><span class="sxs-lookup"><span data-stu-id="b9a18-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-153">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="b9a18-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9a18-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-156">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-157">Die Protokoll Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b9a18-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-158">**RemoteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="b9a18-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9a18-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-161">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-162">Die Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b9a18-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-163">**Remoteport**</span><span class="sxs-lookup"><span data-stu-id="b9a18-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9a18-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-166">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-167">Der Remote Port Bereich.</span><span class="sxs-lookup"><span data-stu-id="b9a18-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-168">**Zustandsbehaftet**</span><span class="sxs-lookup"><span data-stu-id="b9a18-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-169">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9a18-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-171">Qualifizierer: **wmidataid** (10), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-172">Gibt an, ob die erweiterte ACL Zustands behaftet oder zustandslos ist.</span><span class="sxs-lookup"><span data-stu-id="b9a18-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="b9a18-173">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b9a18-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9a18-174">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9a18-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9a18-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b9a18-176">Qualifizierer: **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b9a18-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b9a18-177">Die Gewichtung, die auf die erweiterte ACL angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9a18-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9a18-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9a18-178">Requirements</span></span>



| <span data-ttu-id="b9a18-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9a18-179">Requirement</span></span> | <span data-ttu-id="b9a18-180">Wert</span><span class="sxs-lookup"><span data-stu-id="b9a18-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a18-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9a18-181">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a18-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b9a18-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b9a18-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9a18-183">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a18-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9a18-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b9a18-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9a18-185">Namespace</span></span><br/>                | <span data-ttu-id="b9a18-186">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b9a18-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b9a18-187">MOF</span><span class="sxs-lookup"><span data-stu-id="b9a18-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9a18-188"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b9a18-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9a18-189">DLL</span><span class="sxs-lookup"><span data-stu-id="b9a18-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9a18-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9a18-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9a18-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9a18-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9a18-192">**MSVM \_ ethernetzwitchportfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="b9a18-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

