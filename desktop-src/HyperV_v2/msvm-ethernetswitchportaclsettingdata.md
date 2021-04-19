---
description: Stellt die Zugriffs Steuerungs Liste (ACL) für switchporteinstellungen dar.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Msvm_EthernetSwitchPortAclSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367249"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="9ebcd-103">MSVM \_ ethernetzwitchportaclsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ebcd-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="9ebcd-104">Stellt die Zugriffs Steuerungs Liste (ACL) für switchporteinstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="9ebcd-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebcd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ebcd-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="9ebcd-107">Member</span><span class="sxs-lookup"><span data-stu-id="9ebcd-107">Members</span></span>

<span data-ttu-id="9ebcd-108">Die **MSVM \_ ethernetzwitchportaclsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9ebcd-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9ebcd-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ebcd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ebcd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ebcd-110">Properties</span></span>

<span data-ttu-id="9ebcd-111">Die **MSVM \_ ethernetzwitchportaclsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ebcd-112">**Acltype**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-113">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-115">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-116">Gibt den Typ des ACL-Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ebcd-117">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="9ebcd-118">**Mac-ACL** (1)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="9ebcd-119">**IPv4-ACL** (2)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="9ebcd-120">**IPv6-ACL** (3)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ebcd-121">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-122">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-124">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-125">Dies gibt die Aktion der ACL an.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ebcd-126">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="9ebcd-127">**Zulassen** (1)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="9ebcd-128">**Verweigern** (2)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="9ebcd-129">**Meter** (3)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ebcd-130">**Anwendbarkeit**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-131">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-133">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-134">Dies gibt an, ob die ACL für den lokalen Endpunkt oder den Remote Endpunkt gilt.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ebcd-135">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="9ebcd-136">**Lokal** (1)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="9ebcd-137">**Remote** (2)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ebcd-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ebcd-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-141">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-141">A short description of the object.</span></span> <span data-ttu-id="9ebcd-142">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Switchport-ACL-Einstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ebcd-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-146">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-146">A description of the object.</span></span> <span data-ttu-id="9ebcd-147">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Basisklasse für Switch-Port-Einstellungen" fest.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-148">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-149">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-151">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-152">Dies gibt an, ob die ACL für die Eingangs-oder Ausgangs Richtung gilt.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ebcd-153">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="9ebcd-154">**Eingehende** (1)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="9ebcd-155">**Ausgehend** (2)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ebcd-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ebcd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-159">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-159">A display name for the object.</span></span> <span data-ttu-id="9ebcd-160">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Switchport-ACL-Einstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ebcd-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-164">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-165">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9ebcd-166">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-170">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-171">Die lokale Adresse der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-171">The local address of the virtual machine.</span></span> <span data-ttu-id="9ebcd-172">Dies kann eine IPv4-, IPv6-oder Mac-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-173">**Localadresssspree fixlength**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-174">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-176">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-177">Die Länge des lokalen Adress Präfixes.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-181">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-182">Der Anzeige Name der ACL.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-186">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-187">Die Remote Adresse des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="9ebcd-188">Dies kann eine IPv4-, IPv6-oder Mac-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="9ebcd-189">**Remoteadresssspfixlength**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ebcd-190">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-191">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ebcd-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9ebcd-192">Qualifizierer: **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="9ebcd-193">Die Länge des Remote Adress Präfixes.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ebcd-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ebcd-194">Requirements</span></span>



| <span data-ttu-id="9ebcd-195">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ebcd-195">Requirement</span></span> | <span data-ttu-id="9ebcd-196">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebcd-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebcd-197">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-197">Minimum supported client</span></span><br/> | <span data-ttu-id="9ebcd-198">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ebcd-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9ebcd-199">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ebcd-199">Minimum supported server</span></span><br/> | <span data-ttu-id="9ebcd-200">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ebcd-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ebcd-201">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ebcd-201">Namespace</span></span><br/>                | <span data-ttu-id="9ebcd-202">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9ebcd-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9ebcd-203">MOF</span><span class="sxs-lookup"><span data-stu-id="9ebcd-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ebcd-204"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9ebcd-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ebcd-205">DLL</span><span class="sxs-lookup"><span data-stu-id="9ebcd-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ebcd-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9ebcd-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

