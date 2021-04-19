---
description: Stellt einen Eintrag in der Weiterleitungs Datenbank (Filter) dar, die dem transparenten Überbrückungs Dienst zugeordnet ist.
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Msvm_DynamicForwardingEntry-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368874"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="4edf9-103">MSVM \_ dynamicforwardingentry-Klasse</span><span class="sxs-lookup"><span data-stu-id="4edf9-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="4edf9-104">Stellt einen Eintrag in der Weiterleitungs Datenbank (Filter) dar, die dem transparenten Überbrückungs Dienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4edf9-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="4edf9-105">Der Eintrag ist für den Dienst schwach, wie von [**MSVM \_ transparentbridgingdynamicforwarding**](msvm-transparentbridgingdynamicforwarding.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="4edf9-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="4edf9-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4edf9-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4edf9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4edf9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="4edf9-108">Member</span><span class="sxs-lookup"><span data-stu-id="4edf9-108">Members</span></span>

<span data-ttu-id="4edf9-109">Die **MSVM \_ dynamicforwardingentry** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4edf9-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="4edf9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4edf9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4edf9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4edf9-111">Properties</span></span>

<span data-ttu-id="4edf9-112">Die **MSVM \_ dynamicforwardingentry** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4edf9-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4edf9-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4edf9-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-116">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="4edf9-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-117">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4edf9-117">A short description of the object.</span></span> <span data-ttu-id="4edf9-118">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-119">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="4edf9-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-120">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-122">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4edf9-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4edf9-123">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4edf9-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4edf9-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-125">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4edf9-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-128">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4edf9-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-129">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4edf9-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="4edf9-130">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4edf9-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="4edf9-131">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4edf9-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-135">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4edf9-135">A description of the object.</span></span> <span data-ttu-id="4edf9-136">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4edf9-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-138">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-140">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="4edf9-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4edf9-141">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4edf9-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4edf9-142">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-143">**Dynamicstatus**</span><span class="sxs-lookup"><span data-stu-id="4edf9-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-146">Der Status des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="4edf9-146">The status of the entry.</span></span> <span data-ttu-id="4edf9-147">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="4edf9-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4edf9-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Ungültig** (2)</span><span class="sxs-lookup"><span data-stu-id="4edf9-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Gelernt** (3)</span><span class="sxs-lookup"><span data-stu-id="4edf9-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Selbst** (4)</span><span class="sxs-lookup"><span data-stu-id="4edf9-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span><span class="sxs-lookup"><span data-stu-id="4edf9-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4edf9-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4edf9-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-156">Ein Anzeige Name für das Element.</span><span class="sxs-lookup"><span data-stu-id="4edf9-156">A display name for the element.</span></span> <span data-ttu-id="4edf9-157">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4edf9-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-161">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="4edf9-161">The current health of the element.</span></span> <span data-ttu-id="4edf9-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 ("OK") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4edf9-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-164">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4edf9-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-166">Wird automatisch aufgefüllt, wenn der virtuelle Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4edf9-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="4edf9-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4edf9-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-171">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="4edf9-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-172">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="4edf9-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4edf9-173">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-174">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="4edf9-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-177">Qualifizierer: **Key**, **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="4edf9-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-178">Unicast-MAC-Adresse, für die der transparente Überbrückungs Dienst Weiterleitungs-und Filter Informationen hat.</span><span class="sxs-lookup"><span data-stu-id="4edf9-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="4edf9-179">Die Mac-Adresse ist als zwölf hexadezimal Ziffern formatiert (z. b. "010203040506"), wobei jedes Paar eines der sechs Oktette der Mac-Adresse in "kanonischer" bitreihenfolge gemäß RFC 2469 darstellt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="4edf9-180">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-181">**Name**</span><span class="sxs-lookup"><span data-stu-id="4edf9-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-184">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4edf9-184">The label by which the object is known.</span></span> <span data-ttu-id="4edf9-185">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-186">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="4edf9-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-189">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4edf9-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4edf9-190">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4edf9-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4edf9-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4edf9-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-193">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4edf9-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-196">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="4edf9-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-197">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-199">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="4edf9-199">Provides high level status information.</span></span> <span data-ttu-id="4edf9-200">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4edf9-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="4edf9-201">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4edf9-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4edf9-202">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-203">**Servicecreationclassname**</span><span class="sxs-lookup"><span data-stu-id="4edf9-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-206">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4edf9-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-207">Der **Name** des-Bereichs Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4edf9-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="4edf9-208">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-209">**Service Name**</span><span class="sxs-lookup"><span data-stu-id="4edf9-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-212">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4edf9-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-213">Der Name des Bereichs Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4edf9-213">The scoping service's name.</span></span> <span data-ttu-id="4edf9-214">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-215">**Status**</span><span class="sxs-lookup"><span data-stu-id="4edf9-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-218">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4edf9-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-219">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="4edf9-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-220">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4edf9-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-222">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-223">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="4edf9-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-226">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4edf9-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-227">Der " **kreationclassname**" des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4edf9-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="4edf9-228">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-229">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="4edf9-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4edf9-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4edf9-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-232">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4edf9-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-233">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4edf9-233">The scoping system's name.</span></span> <span data-ttu-id="4edf9-234">Diese Eigenschaft wird von [**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="4edf9-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4edf9-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="4edf9-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4edf9-236">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4edf9-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4edf9-237">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4edf9-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4edf9-238">Der diesem Eintrag zugeordnete virtuelle LAN-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4edf9-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4edf9-239">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4edf9-239">Remarks</span></span>

<span data-ttu-id="4edf9-240">Der Zugriff auf die **MSVM \_ dynamicforwardingentry** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4edf9-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4edf9-241">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4edf9-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4edf9-242">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4edf9-242">Examples</span></span>

<span data-ttu-id="4edf9-243">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4edf9-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4edf9-244">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4edf9-244">Requirements</span></span>



| <span data-ttu-id="4edf9-245">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4edf9-245">Requirement</span></span> | <span data-ttu-id="4edf9-246">Wert</span><span class="sxs-lookup"><span data-stu-id="4edf9-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4edf9-247">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4edf9-247">Minimum supported client</span></span><br/> | <span data-ttu-id="4edf9-248">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4edf9-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4edf9-249">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4edf9-249">Minimum supported server</span></span><br/> | <span data-ttu-id="4edf9-250">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4edf9-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4edf9-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="4edf9-251">Namespace</span></span><br/>                | <span data-ttu-id="4edf9-252">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4edf9-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4edf9-253">MOF</span><span class="sxs-lookup"><span data-stu-id="4edf9-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4edf9-254"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4edf9-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4edf9-255">DLL</span><span class="sxs-lookup"><span data-stu-id="4edf9-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4edf9-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4edf9-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4edf9-257">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4edf9-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edf9-258">**CIM \_ dynamicforwardingentry**</span><span class="sxs-lookup"><span data-stu-id="4edf9-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="4edf9-259">[**CIM \_ dynamicforwardingentry**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4edf9-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

