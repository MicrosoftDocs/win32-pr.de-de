---
description: Stellt eine Instanz einer Erweiterungs Komponente dar, die auf einem Host System installiert ist.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Msvm_InstalledEthernetSwitchExtension-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346981"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="5206d-103">MSVM \_ installedethernetzwitchextension-Klasse</span><span class="sxs-lookup"><span data-stu-id="5206d-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="5206d-104">Stellt eine Instanz einer Erweiterungs Komponente dar, die auf einem Host System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="5206d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5206d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5206d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5206d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="5206d-107">Member</span><span class="sxs-lookup"><span data-stu-id="5206d-107">Members</span></span>

<span data-ttu-id="5206d-108">Die **MSVM \_ installedethernetzwitchextension** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5206d-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="5206d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5206d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5206d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5206d-110">Properties</span></span>

<span data-ttu-id="5206d-111">Die **MSVM \_ installedethernetzwitchextension** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5206d-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5206d-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5206d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5206d-115">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5206d-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5206d-116">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5206d-116">A short description of the object.</span></span> <span data-ttu-id="5206d-117">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-118">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="5206d-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5206d-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-121">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="5206d-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5206d-122">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5206d-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5206d-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-127">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5206d-127">A description of the object.</span></span> <span data-ttu-id="5206d-128">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5206d-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5206d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-132">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="5206d-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5206d-133">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5206d-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5206d-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-138">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5206d-138">A display name for the object.</span></span> <span data-ttu-id="5206d-139">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="5206d-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-141">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5206d-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-143">Gibt den Typ der Erweiterungs Komponente an.</span><span class="sxs-lookup"><span data-stu-id="5206d-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5206d-144">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5206d-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="5206d-145">**Erfassung** (1)</span><span class="sxs-lookup"><span data-stu-id="5206d-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="5206d-146">**Filter** (2)</span><span class="sxs-lookup"><span data-stu-id="5206d-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="5206d-147">**Weiterleitung** (3)</span><span class="sxs-lookup"><span data-stu-id="5206d-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="5206d-148">**Überwachung** (4)</span><span class="sxs-lookup"><span data-stu-id="5206d-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="5206d-149">**Native** (5)</span><span class="sxs-lookup"><span data-stu-id="5206d-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5206d-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5206d-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5206d-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-153">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="5206d-153">The current health of the element.</span></span> <span data-ttu-id="5206d-154">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="5206d-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5206d-155">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5206d-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5206d-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5206d-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-158">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5206d-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-160">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5206d-160">The date and time when the object was installed.</span></span> <span data-ttu-id="5206d-161">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="5206d-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5206d-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5206d-166">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="5206d-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5206d-167">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5206d-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5206d-168">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-169">**Name**</span><span class="sxs-lookup"><span data-stu-id="5206d-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5206d-172">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5206d-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5206d-173">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-173">The label by which the object is known.</span></span> <span data-ttu-id="5206d-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-175">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="5206d-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-176">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5206d-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-178">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5206d-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5206d-179">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5206d-180">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5206d-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-182">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="5206d-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5206d-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-184">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5206d-184">The current statuses of the object.</span></span> <span data-ttu-id="5206d-185">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5206d-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-186">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="5206d-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5206d-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-189">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="5206d-189">Provides high level status information.</span></span> <span data-ttu-id="5206d-190">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5206d-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="5206d-191">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="5206d-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5206d-192">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5206d-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="5206d-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-196">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5206d-196">The current status of the object.</span></span> <span data-ttu-id="5206d-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5206d-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5206d-198">Okay</span><span class="sxs-lookup"><span data-stu-id="5206d-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="5206d-199"><span id="OK"></span><span id="ok"></span>**Okay**</span><span class="sxs-lookup"><span data-stu-id="5206d-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Zeit**</span><span class="sxs-lookup"><span data-stu-id="5206d-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Zerstört**</span><span class="sxs-lookup"><span data-stu-id="5206d-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="5206d-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred-Fehler**</span><span class="sxs-lookup"><span data-stu-id="5206d-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Fahren**</span><span class="sxs-lookup"><span data-stu-id="5206d-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Hindern**</span><span class="sxs-lookup"><span data-stu-id="5206d-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Leistungs**</span><span class="sxs-lookup"><span data-stu-id="5206d-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Gestresst**</span><span class="sxs-lookup"><span data-stu-id="5206d-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Nicht wiederherstellen**</span><span class="sxs-lookup"><span data-stu-id="5206d-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt**</span><span class="sxs-lookup"><span data-stu-id="5206d-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Verlorene Kommunikations-**</span><span class="sxs-lookup"><span data-stu-id="5206d-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5206d-211">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="5206d-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-212">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="5206d-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5206d-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-214">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5206d-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5206d-215">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5206d-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="5206d-216">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="5206d-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-219">Gibt den Anbieter an, der die Erweiterung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5206d-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="5206d-220">**Version**</span><span class="sxs-lookup"><span data-stu-id="5206d-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5206d-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5206d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5206d-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5206d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5206d-223">Die Version der Erweiterung im Format "Major. Minor", z. b. "2,0".</span><span class="sxs-lookup"><span data-stu-id="5206d-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5206d-224">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5206d-224">Requirements</span></span>



| <span data-ttu-id="5206d-225">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5206d-225">Requirement</span></span> | <span data-ttu-id="5206d-226">Wert</span><span class="sxs-lookup"><span data-stu-id="5206d-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5206d-227">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5206d-227">Minimum supported client</span></span><br/> | <span data-ttu-id="5206d-228">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5206d-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5206d-229">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5206d-229">Minimum supported server</span></span><br/> | <span data-ttu-id="5206d-230">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5206d-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5206d-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="5206d-231">Namespace</span></span><br/>                | <span data-ttu-id="5206d-232">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5206d-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5206d-233">MOF</span><span class="sxs-lookup"><span data-stu-id="5206d-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5206d-234"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5206d-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5206d-235">DLL</span><span class="sxs-lookup"><span data-stu-id="5206d-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5206d-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5206d-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

