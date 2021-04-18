---
description: Hier werden die Funktionen des zugeordneten MSVM- \_ Computer Systems beschrieben.
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Msvm_VirtualSystemCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214416"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="76147-103">MSVM \_ virtualsystemfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="76147-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="76147-104">Hier werden die Funktionen des zugeordneten [**MSVM- \_ Computer Systems**](msvm-computersystem.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76147-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="76147-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76147-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76147-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="76147-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="76147-107">Member</span><span class="sxs-lookup"><span data-stu-id="76147-107">Members</span></span>

<span data-ttu-id="76147-108">Die **MSVM \_ virtualsystemfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="76147-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="76147-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76147-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76147-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76147-110">Properties</span></span>

<span data-ttu-id="76147-111">Die **MSVM \_ virtualsystemfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76147-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76147-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="76147-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76147-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76147-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76147-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="76147-115">A short description of the object.</span></span> <span data-ttu-id="76147-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76147-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76147-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76147-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76147-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76147-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="76147-120">A description of the object.</span></span> <span data-ttu-id="76147-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76147-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="76147-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76147-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76147-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76147-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="76147-125">A display name for the object.</span></span> <span data-ttu-id="76147-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76147-127">**Elementnameeditsupported**</span><span class="sxs-lookup"><span data-stu-id="76147-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="76147-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76147-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76147-130">Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="76147-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="76147-131">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="76147-132">**Elementnamemask**</span><span class="sxs-lookup"><span data-stu-id="76147-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76147-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76147-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76147-135">Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="76147-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="76147-136">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="76147-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76147-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76147-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76147-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76147-140">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="76147-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="76147-141">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="76147-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="76147-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76147-143">**Maxelementnamelen**</span><span class="sxs-lookup"><span data-stu-id="76147-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-144">Datentyp: **unit16**</span><span class="sxs-lookup"><span data-stu-id="76147-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="76147-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76147-146">Qualifizierer: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="76147-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="76147-147">Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="76147-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="76147-148">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="76147-149">**Requestedstaatunter stützt**</span><span class="sxs-lookup"><span data-stu-id="76147-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76147-150">Datentyp: **unit16** Array</span><span class="sxs-lookup"><span data-stu-id="76147-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="76147-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="76147-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76147-152">Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="76147-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="76147-153">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="76147-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="76147-154">Wert</span><span class="sxs-lookup"><span data-stu-id="76147-154">Value</span></span>                                                                         | <span data-ttu-id="76147-155">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="76147-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="76147-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="76147-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="76147-157">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="76147-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="76147-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="76147-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="76147-159">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="76147-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="76147-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="76147-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="76147-161">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="76147-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="76147-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="76147-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="76147-163">Offline</span><span class="sxs-lookup"><span data-stu-id="76147-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="76147-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="76147-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="76147-165">Test</span><span class="sxs-lookup"><span data-stu-id="76147-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="76147-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="76147-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="76147-167">Wickeln</span><span class="sxs-lookup"><span data-stu-id="76147-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="76147-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="76147-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="76147-169">Stilllegen</span><span class="sxs-lookup"><span data-stu-id="76147-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="76147-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="76147-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="76147-171">Reboot</span><span class="sxs-lookup"><span data-stu-id="76147-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="76147-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="76147-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="76147-173">Reset</span><span class="sxs-lookup"><span data-stu-id="76147-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76147-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76147-174">Requirements</span></span>



| <span data-ttu-id="76147-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76147-175">Requirement</span></span> | <span data-ttu-id="76147-176">Wert</span><span class="sxs-lookup"><span data-stu-id="76147-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76147-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76147-177">Minimum supported client</span></span><br/> | <span data-ttu-id="76147-178">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76147-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="76147-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76147-179">Minimum supported server</span></span><br/> | <span data-ttu-id="76147-180">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76147-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76147-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="76147-181">Namespace</span></span><br/>                | <span data-ttu-id="76147-182">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="76147-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="76147-183">MOF</span><span class="sxs-lookup"><span data-stu-id="76147-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76147-184"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="76147-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76147-185">DLL</span><span class="sxs-lookup"><span data-stu-id="76147-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76147-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76147-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

