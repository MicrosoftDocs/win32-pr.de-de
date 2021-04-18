---
description: Wird in der getsummaryinformation-Methode in der MSVM \_ virtualsystemmanagementservice-Klasse verwendet, um schnell allgemeine Informationen abzurufen, die sich auf ein virtuelles System oder eine Momentaufnahme beziehen.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357423"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="7da45-103">MSVM \_ summaryinformationbase-Klasse</span><span class="sxs-lookup"><span data-stu-id="7da45-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="7da45-104">Wird in der [**getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) -Methode in der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet, um schnell allgemeine Informationen abzurufen, die sich auf ein virtuelles System oder eine Momentaufnahme beziehen.</span><span class="sxs-lookup"><span data-stu-id="7da45-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="7da45-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7da45-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da45-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da45-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="7da45-107">Member</span><span class="sxs-lookup"><span data-stu-id="7da45-107">Members</span></span>

<span data-ttu-id="7da45-108">Die **MSVM \_ summaryinformationbase** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7da45-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="7da45-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7da45-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7da45-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7da45-110">Properties</span></span>

<span data-ttu-id="7da45-111">Die **MSVM \_ summaryinformationbase** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7da45-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7da45-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="7da45-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-113">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7da45-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-115">Der Zeitpunkt, zu dem das virtuelle System oder die Momentaufnahme erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7da45-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7da45-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da45-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ managedelta Element. Elementname")</span><span class="sxs-lookup"><span data-stu-id="7da45-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="7da45-120">Der Anzeige Name für das virtuelle System oder die Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="7da45-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7da45-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7da45-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-124">Der aktuelle Zustand des virtuellen Systems oder der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="7da45-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-125">**Enhancedsessionmodestate**</span><span class="sxs-lookup"><span data-stu-id="7da45-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7da45-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-128">Gibt an, ob Verbindungen im erweiterten Modus vom Host zugelassen werden, und falls zulässig, ob Sie für den virtuellen Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7da45-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="7da45-129">**Zulässig und verfügbar** (2)</span><span class="sxs-lookup"><span data-stu-id="7da45-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="7da45-130">**Nicht zulässig** (3)</span><span class="sxs-lookup"><span data-stu-id="7da45-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="7da45-131">**Zulässig, aber nicht verfügbar** (6)</span><span class="sxs-lookup"><span data-stu-id="7da45-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7da45-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7da45-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7da45-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-135">Der aktuelle Integritäts Status des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="7da45-135">The current health state for the virtual system.</span></span> <span data-ttu-id="7da45-136">Diese Eigenschaft ist für Instanzen von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , die eine Momentaufnahme eines virtuellen Systems darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="7da45-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-137">**Hostcomputersystemname**</span><span class="sxs-lookup"><span data-stu-id="7da45-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-140">Der Name des Computers, auf dem dieser virtuelle Computer gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="7da45-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7da45-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da45-144">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ managedelta Element. InstanceId"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7da45-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7da45-145">"InstanceId" ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des instanziierten Namespace eindeutig und eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7da45-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="7da45-146">Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um Sie erforderlich zu machen, oder einen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="7da45-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="7da45-147">Diese Unterklassen können auch die bevorzugten Algorithmen zum Sicherstellen der Eindeutigkeit ändern, die unten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7da45-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="7da45-148">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="7da45-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="7da45-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="7da45-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="7da45-150">Dabei <OrgID> <LocalID> sind und durch einen Doppelpunkt (:) und wobei <OrgID> ein urheberrechtlich geschütztes, mit einem oder ein oder anderweitig eindeutiger Name enthalten muss, der der Geschäfts Entität entspricht, die die InstanceId erstellt oder definiert, oder die eine registrierte ID ist, die der Geschäfts Entität von einer anerkannten globalen Autorität zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7da45-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="7da45-151">(Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schema Klassennamen.) Außerdem <OrgID> darf keine Doppelpunkte (:) enthalten, um die Eindeutigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="7da45-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="7da45-152">Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen und angezeigt werden <OrgID> <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="7da45-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="7da45-153"><LocalID> wird von der Business-Entität gewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7da45-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="7da45-154">Wenn not NULL und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht in allen instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7da45-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="7da45-155">Wenn für von DMTF definierte Instanzen nicht auf NULL festgelegt ist, muss der "bevorzugte" Algorithmus verwendet werden, wobei <OrgID> auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7da45-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="7da45-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-159">Der eindeutige Name für das virtuelle System oder die Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="7da45-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-160">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="7da45-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-163">Die Anmerkungen, die dem virtuellen System oder der Momentaufnahme zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7da45-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="7da45-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7da45-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-167">Die Gesamtanzahl der virtuellen Prozessoren, die dem virtuellen System oder der Momentaufnahme zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7da45-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7da45-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-169">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7da45-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7da45-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da45-171">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="7da45-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7da45-172">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="7da45-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-173">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="7da45-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-176">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7da45-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="7da45-177">Diese Eigenschaft muss auf NULL festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="7da45-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-178">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="7da45-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-179">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7da45-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7da45-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da45-181">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="7da45-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7da45-182">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7da45-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-183">**Betriebszeit**</span><span class="sxs-lookup"><span data-stu-id="7da45-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-184">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7da45-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-186">Die Zeitspanne seit dem letzten Starten des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="7da45-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="7da45-187">Diese Eigenschaft ist für Instanzen von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , die eine Momentaufnahme eines virtuellen Systems darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="7da45-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-188">**Version**</span><span class="sxs-lookup"><span data-stu-id="7da45-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-191">Die Version des virtuellen Systems im Format "Major. Minor"; Beispiel: "2,0".</span><span class="sxs-lookup"><span data-stu-id="7da45-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="7da45-192">**Virtualswitchnames**</span><span class="sxs-lookup"><span data-stu-id="7da45-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-193">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7da45-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7da45-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7da45-195">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="7da45-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7da45-196">Zeichen folgen, die die anzeigen amen der virtuellen Switches auflisten, mit denen der virtuelle Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="7da45-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="7da45-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="7da45-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7da45-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7da45-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7da45-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7da45-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7da45-200">Der Untertyp des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="7da45-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="7da45-201">**Microsoft: Hyper-v: Untertyp: 1** ("Microsoft: Hyper-v: SubType: 1")</span><span class="sxs-lookup"><span data-stu-id="7da45-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="7da45-202">**Microsoft: Hyper-v: SubType: 2** ("Microsoft: Hyper-v: SubType: 2")</span><span class="sxs-lookup"><span data-stu-id="7da45-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="7da45-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7da45-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7da45-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7da45-204">Requirements</span></span>



| <span data-ttu-id="7da45-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7da45-205">Requirement</span></span> | <span data-ttu-id="7da45-206">Wert</span><span class="sxs-lookup"><span data-stu-id="7da45-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da45-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7da45-207">Minimum supported client</span></span><br/> | <span data-ttu-id="7da45-208">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7da45-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7da45-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7da45-209">Minimum supported server</span></span><br/> | <span data-ttu-id="7da45-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7da45-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7da45-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="7da45-211">Namespace</span></span><br/>                | <span data-ttu-id="7da45-212">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7da45-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7da45-213">MOF</span><span class="sxs-lookup"><span data-stu-id="7da45-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7da45-214"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7da45-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7da45-215">DLL</span><span class="sxs-lookup"><span data-stu-id="7da45-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7da45-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7da45-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7da45-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7da45-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da45-218">**CIM- \_ Ansicht**</span><span class="sxs-lookup"><span data-stu-id="7da45-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

