---
description: Stellt die Einstellungsdaten für Sicherheitsfunktionen dar.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Msvm_EthernetSwitchPortSecuritySettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869268"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="1630a-103">MSVM \_ ethernetzwitchportsecuritysettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1630a-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="1630a-104">Stellt die Einstellungsdaten für Sicherheitsfunktionen dar.</span><span class="sxs-lookup"><span data-stu-id="1630a-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="1630a-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1630a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1630a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1630a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="1630a-107">Member</span><span class="sxs-lookup"><span data-stu-id="1630a-107">Members</span></span>

<span data-ttu-id="1630a-108">Die **MSVM \_ ethernetzwitchportsecuritysettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1630a-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1630a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1630a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1630a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1630a-110">Properties</span></span>

<span data-ttu-id="1630a-111">Die **MSVM \_ ethernetzwitchportsecuritysettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1630a-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1630a-112">**' Zuweisung '**</span><span class="sxs-lookup"><span data-stu-id="1630a-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-115">Qualifizierer: **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-116">Gibt an, ob der Datenverkehr zum/vom Port 802.1 p-Informationen beibehält.</span><span class="sxs-lookup"><span data-stu-id="1630a-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="1630a-117">Enthält **true** , wenn der Datenverkehr zum/vom Port 802.1 p-Informationen beibehält, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1630a-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="1630a-118">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="1630a-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-119">**Allowmacspoofing**</span><span class="sxs-lookup"><span data-stu-id="1630a-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-122">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-123">Gibt an, ob der Port das Spoofing von Mac-Adressen zulässt.</span><span class="sxs-lookup"><span data-stu-id="1630a-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="1630a-124">Wenn diese Eigenschaft auf **true** gesetzt ist, ermöglicht der Port das spootieren von Mac-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1630a-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="1630a-125">Alle gültigen Unicast-MAC-Adress Werte sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="1630a-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="1630a-126">Wenn diese Eigenschaft auf **false** festgelegt ist, lässt der Port nur die Verwendung von Mac-Adressen zu, die in der Hyper-V-Verwaltung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="1630a-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="1630a-127">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="1630a-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-128">**Allowteaming**</span><span class="sxs-lookup"><span data-stu-id="1630a-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-131">Qualifizierer: **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-132">Gibt an, ob die mit dem Port verbundenen NICs Teil eines Teams sein können.</span><span class="sxs-lookup"><span data-stu-id="1630a-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="1630a-133">Dies gilt nur für NICs, die mit virtuellen Computern verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="1630a-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="1630a-134">Enthält **true** , wenn NIC-Team Vorgang zulässig ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1630a-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="1630a-135">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="1630a-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1630a-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1630a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1630a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1630a-139">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1630a-139">A short description of the object.</span></span> <span data-ttu-id="1630a-140">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Security Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1630a-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1630a-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1630a-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1630a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1630a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1630a-144">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1630a-144">A description of the object.</span></span> <span data-ttu-id="1630a-145">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Sicherheitseinstellungen für die Sicherheitsfunktion" fest.</span><span class="sxs-lookup"><span data-stu-id="1630a-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="1630a-146">**Dynamicipaddresslimit**</span><span class="sxs-lookup"><span data-stu-id="1630a-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1630a-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-149">Qualifizierer: **wmidataid** (12), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-150">Definiert das Limit für die Anzahl der gewonnenen dynamischen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1630a-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="1630a-151">Standardwert ist „none“.</span><span class="sxs-lookup"><span data-stu-id="1630a-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1630a-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1630a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1630a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1630a-155">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1630a-155">A display name for the object.</span></span> <span data-ttu-id="1630a-156">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Security Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1630a-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1630a-157">**Enabledhcpguard**</span><span class="sxs-lookup"><span data-stu-id="1630a-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-158">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-160">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-161">Gibt an, ob DHCP-Angebote vom Port blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="1630a-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="1630a-162">Enthält **true** , wenn DHCP-Angebote vom Port blockiert werden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1630a-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="1630a-163">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="1630a-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="1630a-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-165">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-167">Qualifizierer: **wmidataid** (14), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-168">Auf true festgelegt, wenn die festgelegte Geschwindigkeit 10G aktiviert ist, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="1630a-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="1630a-169">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="1630a-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="1630a-170">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1630a-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="1630a-171">**Enablerouterguard**</span><span class="sxs-lookup"><span data-stu-id="1630a-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-174">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-175">Gibt an, ob Routerankündigungen und routerumleitungen vom Port blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="1630a-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="1630a-176">Enthält **true** , wenn Routerankündigungen und routerumleitungen vom Port blockiert werden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1630a-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="1630a-177">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="1630a-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1630a-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1630a-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1630a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1630a-181">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1630a-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1630a-182">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1630a-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1630a-183">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1630a-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1630a-184">**Monitormode**</span><span class="sxs-lookup"><span data-stu-id="1630a-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-185">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1630a-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-186">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-187">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-188">Dies zeigt den Monitor Modus des Ports an.</span><span class="sxs-lookup"><span data-stu-id="1630a-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1630a-189">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="1630a-190">**Ziel** (1)</span><span class="sxs-lookup"><span data-stu-id="1630a-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="1630a-191">**Quelle** (2)</span><span class="sxs-lookup"><span data-stu-id="1630a-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1630a-192">**Monitorsession**</span><span class="sxs-lookup"><span data-stu-id="1630a-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-193">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1630a-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-194">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-195">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-196">Gibt den Bezeichner der Überwachungs Sitzung an, zu der dieser Port gehört.</span><span class="sxs-lookup"><span data-stu-id="1630a-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-197">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1630a-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-198">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-200">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), **wmidataid** (13), **interfacetten** (3), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-201">Reserviert</span><span class="sxs-lookup"><span data-stu-id="1630a-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="1630a-202">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1630a-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="1630a-203">**Stormlimit**</span><span class="sxs-lookup"><span data-stu-id="1630a-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-204">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1630a-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-206">Qualifizierer: **wmidataid** (11), **interfacetten** (2), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-207">Definiert das Limit von Paketen pro Sekunde für Broadcast-und Multicast-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="1630a-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="1630a-208">Standardwert ist „none“.</span><span class="sxs-lookup"><span data-stu-id="1630a-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-209">**Teamname**</span><span class="sxs-lookup"><span data-stu-id="1630a-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1630a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-212">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-213">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1630a-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-214">**TeamNumber**</span><span class="sxs-lookup"><span data-stu-id="1630a-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-215">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1630a-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-216">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-217">Qualifizierer: **wmidataid** (10), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1630a-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-218">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1630a-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="1630a-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="1630a-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1630a-220">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1630a-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1630a-221">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1630a-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1630a-222">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span><span class="sxs-lookup"><span data-stu-id="1630a-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="1630a-223">Gibt den Bezeichner des virtuellen Subnetzes an, in dem der Port Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="1630a-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="1630a-224">Der Standardwert ist „none“.</span><span class="sxs-lookup"><span data-stu-id="1630a-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1630a-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1630a-225">Requirements</span></span>



| <span data-ttu-id="1630a-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1630a-226">Requirement</span></span> | <span data-ttu-id="1630a-227">Wert</span><span class="sxs-lookup"><span data-stu-id="1630a-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1630a-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1630a-228">Minimum supported client</span></span><br/> | <span data-ttu-id="1630a-229">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1630a-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1630a-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1630a-230">Minimum supported server</span></span><br/> | <span data-ttu-id="1630a-231">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1630a-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1630a-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="1630a-232">Namespace</span></span><br/>                | <span data-ttu-id="1630a-233">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1630a-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1630a-234">MOF</span><span class="sxs-lookup"><span data-stu-id="1630a-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1630a-235"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1630a-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1630a-236">DLL</span><span class="sxs-lookup"><span data-stu-id="1630a-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1630a-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1630a-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

