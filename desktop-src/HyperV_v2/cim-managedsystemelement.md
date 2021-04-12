---
description: CIM \_ ManagedSystemElement ist die Basisklasse für die System Element Hierarchie. Jede Komponente eines Systems kann durch diese Klasse oder deren Unterklassen möglicherweise dargestellt werden.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: CIM_ManagedSystemElement-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216771"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="cfec8-104">CIM_ManagedSystemElement-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="cfec8-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="cfec8-105">**CIM \_ ManagedSystemElement** ist die Basisklasse für die System Element Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="cfec8-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="cfec8-106">Jede Komponente eines Systems kann durch diese Klasse oder deren Unterklassen möglicherweise dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cfec8-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfec8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfec8-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
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
};
```

## <a name="members"></a><span data-ttu-id="cfec8-108">Member</span><span class="sxs-lookup"><span data-stu-id="cfec8-108">Members</span></span>

<span data-ttu-id="cfec8-109">Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cfec8-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="cfec8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cfec8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfec8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cfec8-111">Properties</span></span>

<span data-ttu-id="cfec8-112">Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cfec8-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfec8-113">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="cfec8-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfec8-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-116">Gibt die Fähigkeit der Instrumentierung an, mit diesem Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="cfec8-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="cfec8-117">Ein **null** -Wert gibt an, dass die Instrumentierung diese Eigenschaft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cfec8-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfec8-118">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cfec8-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="cfec8-119">**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="cfec8-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="cfec8-120">**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="cfec8-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="cfec8-121">**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="cfec8-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cfec8-122">**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="cfec8-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfec8-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cfec8-124">**Anbieter reserviert** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="cfec8-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfec8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-128">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**Primarystatus**","**CIM \_ ManagedSystemElement**.**Healthstate**")</span><span class="sxs-lookup"><span data-stu-id="cfec8-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-129">Gibt zusätzliche Status Details an, die die **primarystatus** -Eigenschaft ergänzen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="cfec8-130">Ein **null** -Wert gibt an, dass die Instrumentierung diese Eigenschaft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cfec8-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="cfec8-131">**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="cfec8-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="cfec8-132">**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="cfec8-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cfec8-133">**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="cfec8-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="cfec8-134">**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="cfec8-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="cfec8-135">**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="cfec8-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="cfec8-136">**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="cfec8-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfec8-137">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cfec8-138">**Anbieter reserviert** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="cfec8-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfec8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-142">Gibt den aktuellen Zustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="cfec8-142">Indicates the current health of the element.</span></span> <span data-ttu-id="cfec8-143">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise die Integrität seiner unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="cfec8-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfec8-144">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cfec8-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cfec8-145">**OK** (5)</span><span class="sxs-lookup"><span data-stu-id="cfec8-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="cfec8-146">Heruntergestuft **/Warnung** (10)</span><span class="sxs-lookup"><span data-stu-id="cfec8-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="cfec8-147">**Kleinerer Fehler** (15)</span><span class="sxs-lookup"><span data-stu-id="cfec8-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="cfec8-148">**Größerer Fehler** (20)</span><span class="sxs-lookup"><span data-stu-id="cfec8-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="cfec8-149">**Kritischer Fehler** (25)</span><span class="sxs-lookup"><span data-stu-id="cfec8-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="cfec8-150">**Nicht BEHEB barer Fehler** (30)</span><span class="sxs-lookup"><span data-stu-id="cfec8-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfec8-151">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cfec8-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-153">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="cfec8-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-155">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="cfec8-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-156">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cfec8-156">Indicates when the object was installed.</span></span> <span data-ttu-id="cfec8-157">Das Fehlen eines Werts weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cfec8-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="cfec8-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="cfec8-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cfec8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-161">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="cfec8-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-162">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="cfec8-162">The label by which the object is known.</span></span> <span data-ttu-id="cfec8-163">Bei einer Unterklasse kann die **Name** -Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cfec8-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="cfec8-164">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="cfec8-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfec8-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-167">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="cfec8-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-168">Gibt den aktuellen Betriebszustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="cfec8-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="cfec8-169">Diese Eigenschaft kann verwendet werden, um weitere Details zum Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="cfec8-170">Ein **null** -Wert gibt an, dass die Instrumentierung diese Eigenschaft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cfec8-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="cfec8-171">"Unknown" gibt an</span><span class="sxs-lookup"><span data-stu-id="cfec8-171">"Unknown" indicates</span></span>

<span data-ttu-id="cfec8-172">"None" gibt an, dass</span><span class="sxs-lookup"><span data-stu-id="cfec8-172">"None" indicates that</span></span>

<span data-ttu-id="cfec8-173">Deten</span><span class="sxs-lookup"><span data-stu-id="cfec8-173">"Servicing"</span></span>

<span data-ttu-id="cfec8-174">Fahren</span><span class="sxs-lookup"><span data-stu-id="cfec8-174">"Starting"</span></span>

<span data-ttu-id="cfec8-175">Hindern</span><span class="sxs-lookup"><span data-stu-id="cfec8-175">"Stopping"</span></span>

<span data-ttu-id="cfec8-176">"Beendet" und "abgebrochen" sind ähnlich, obwohl das erste</span><span class="sxs-lookup"><span data-stu-id="cfec8-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="cfec8-177">"Ruhende" gibt an, dass</span><span class="sxs-lookup"><span data-stu-id="cfec8-177">"Dormant" indicates that</span></span>

<span data-ttu-id="cfec8-178">"Abgeschlossen" zeigt an, dass t</span><span class="sxs-lookup"><span data-stu-id="cfec8-178">"Completed" indicates that t</span></span>

<span data-ttu-id="cfec8-179">Nen</span><span class="sxs-lookup"><span data-stu-id="cfec8-179">"Migrating"</span></span>

<span data-ttu-id="cfec8-180">"Immigration"</span><span class="sxs-lookup"><span data-stu-id="cfec8-180">"Immigrating"</span></span>

<span data-ttu-id="cfec8-181">"Migration"</span><span class="sxs-lookup"><span data-stu-id="cfec8-181">"Emigrating"</span></span>

<span data-ttu-id="cfec8-182">"Herunterfahren"</span><span class="sxs-lookup"><span data-stu-id="cfec8-182">"Shutting Down"</span></span>

<span data-ttu-id="cfec8-183">"In Test"</span><span class="sxs-lookup"><span data-stu-id="cfec8-183">"In Test"</span></span>

<span data-ttu-id="cfec8-184">Übergang</span><span class="sxs-lookup"><span data-stu-id="cfec8-184">"Transitioning"</span></span>

<span data-ttu-id="cfec8-185">"In Dienst"</span><span class="sxs-lookup"><span data-stu-id="cfec8-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfec8-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cfec8-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-187">Die-Implementierung ist in der Regel in der Lage, diese Eigenschaft zurückzugeben, kann dies jedoch zu diesem Zeitpunkt nicht tun.</span><span class="sxs-lookup"><span data-stu-id="cfec8-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="cfec8-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="cfec8-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-189">Die Implementierung (Provider) ist in der Lage, einen Wert für diese Eigenschaft zurückzugeben, aber nicht jemals für diese bestimmte Hardware/Software. die Eigenschaft wird nicht absichtlich verwendet, da Sie keine aussagekräftigen Informationen hinzufügt (wie im Fall einer Eigenschaft, die zum Hinzufügen zusätzlicher Informationen zu einer anderen Eigenschaft vorgesehen ist).</span><span class="sxs-lookup"><span data-stu-id="cfec8-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="cfec8-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="cfec8-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-191">Beschreibt ein Element, das konfiguriert, gewartet, bereinigt oder anderweitig verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="cfec8-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cfec8-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="cfec8-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-193">Beschreibt ein Element, das initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cfec8-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cfec8-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="cfec8-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-195">Beschreibt ein Element, das zu einem ordnungsgemäßen Ende gebracht wird.</span><span class="sxs-lookup"><span data-stu-id="cfec8-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="cfec8-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="cfec8-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-197">Ein sauberer und ordnungsgemäßes Ende ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cfec8-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="cfec8-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="cfec8-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-199">Es ist ein abruptes Beenden aufgetreten, bei dem der Status und die Konfiguration des Elements möglicherweise aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="cfec8-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="cfec8-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-201">Das Element ist inaktiv oder inaktiv.</span><span class="sxs-lookup"><span data-stu-id="cfec8-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="cfec8-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="cfec8-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-203">Das Element hat seinen Vorgang abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-203">The element has completed its operation.</span></span> <span data-ttu-id="cfec8-204">Dieser Wert sollte entweder mit "OK", "Fehler" oder "heruntergestuft" in "primarystatus" kombiniert werden, damit ein Client ermitteln kann, ob der vollständige Vorgang mit "OK (bestanden)" abgeschlossen, mit "Fehler" (Fehler) abgeschlossen oder mit "heruntergestuft" abgeschlossen wurde (der Vorgang wurde beendet, aber nicht abgeschlossen oder ein Fehler nicht gemeldet).</span><span class="sxs-lookup"><span data-stu-id="cfec8-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="cfec8-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="cfec8-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-206">Das Element wird zwischen Host Elementen verschoben.</span><span class="sxs-lookup"><span data-stu-id="cfec8-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="cfec8-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="cfec8-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-208">Das Element wird vom Host Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="cfec8-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="cfec8-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="cfec8-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-210">Das Element wird zu einem neuen Host Element verschoben.</span><span class="sxs-lookup"><span data-stu-id="cfec8-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="cfec8-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="cfec8-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="cfec8-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="cfec8-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-213">Beschreibt ein Element, das zu einem abrupten beenden geführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfec8-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cfec8-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="cfec8-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-215">Das-Element führt Testfunktionen aus.</span><span class="sxs-lookup"><span data-stu-id="cfec8-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="cfec8-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="cfec8-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-217">Beschreibt ein Element, das zwischen Zuständen besteht, d. h., es ist nicht vollständig im vorherigen Zustand oder im nächsten Zustand verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfec8-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="cfec8-218">Dieser Wert sollte verwendet werden, wenn andere Werte, die auf einen Übergang zu einem bestimmten Zustand hindeuten, nicht anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="cfec8-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="cfec8-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="cfec8-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-220">Beschreibt ein Element, das sich im Dienst und betriebsbereit befindet.</span><span class="sxs-lookup"><span data-stu-id="cfec8-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfec8-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cfec8-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="cfec8-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-224">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="cfec8-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-226">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**".**Status Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="cfec8-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-227">Enthält Indikatoren zum aktuellen Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="cfec8-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="cfec8-228">Der erste Wert der **OperationalStatus** -Eigenschaft sollte den primären Status für das Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfec8-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="cfec8-229">Die **OperationalStatus** -Eigenschaft ersetzt die veraltete **Status** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cfec8-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="cfec8-230">Aufgrund der weit verbreiteten Verwendung der Eigenschaft " **Status** " in Verwaltungs Anwendungen wird dringend empfohlen, dass Anbieter oder Instrumentation die Eigenschaften " **Status** " und " **OperationalStatus** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="cfec8-231">Bei instrumentiertem **Status** sollte auch der primäre Status des Elements bereitgestellt werden, da es sich um eine einwertige Eigenschaft handelt.</span><span class="sxs-lookup"><span data-stu-id="cfec8-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfec8-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cfec8-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cfec8-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cfec8-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cfec8-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="cfec8-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cfec8-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (3** )</span><span class="sxs-lookup"><span data-stu-id="cfec8-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cfec8-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (4)</span><span class="sxs-lookup"><span data-stu-id="cfec8-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-237">Das Element funktioniert, erfordert jedoch Aufmerksamkeit.</span><span class="sxs-lookup"><span data-stu-id="cfec8-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="cfec8-238">Beispiele für "betonte" Zustände sind Überlastung, überlastet usw.</span><span class="sxs-lookup"><span data-stu-id="cfec8-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="cfec8-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (5)</span><span class="sxs-lookup"><span data-stu-id="cfec8-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-240">Ein Element funktioniert nominisch, Vorhersage eines Fehlers in naher Zukunft.</span><span class="sxs-lookup"><span data-stu-id="cfec8-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cfec8-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="cfec8-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="cfec8-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="cfec8-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cfec8-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (8)</span><span class="sxs-lookup"><span data-stu-id="cfec8-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cfec8-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (9** )</span><span class="sxs-lookup"><span data-stu-id="cfec8-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="cfec8-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (10)</span><span class="sxs-lookup"><span data-stu-id="cfec8-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-246">Ein ordnungsgemäßes Beenden ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cfec8-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="cfec8-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (11)</span><span class="sxs-lookup"><span data-stu-id="cfec8-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-248">Ein Element, das konfiguriert, gewartet, bereinigt oder anderweitig verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="cfec8-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cfec8-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)</span><span class="sxs-lookup"><span data-stu-id="cfec8-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-250">Das Überwachungssystem kennt dieses Element, aber es war noch nie in der Lage, Kommunikation mit ihm herzustellen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="cfec8-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)</span><span class="sxs-lookup"><span data-stu-id="cfec8-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-252">Das managedsystem-Element ist bekanntermaßen vorhanden und wurde in der Vergangenheit erfolgreich kontaktiert, ist aber zurzeit nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="cfec8-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="cfec8-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (14)</span><span class="sxs-lookup"><span data-stu-id="cfec8-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-254">Eine abrupte Beendigung, bei der der Zustand und die Konfiguration des Elements möglicherweise aktualisiert werden müssen, ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cfec8-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="cfec8-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (15)</span><span class="sxs-lookup"><span data-stu-id="cfec8-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-256">Das Element ist inaktiv oder inaktiv.</span><span class="sxs-lookup"><span data-stu-id="cfec8-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="cfec8-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (16)</span><span class="sxs-lookup"><span data-stu-id="cfec8-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-258">Dieses Element ist möglicherweise "OK", aber dass ein anderes Element, von dem es abhängt, fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="cfec8-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="cfec8-259">Ein Beispiel hierfür ist ein Netzwerkdienst oder ein Endpunkt, der aufgrund von Netzwerkproblemen auf niedrigerer Ebene nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="cfec8-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="cfec8-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (17)</span><span class="sxs-lookup"><span data-stu-id="cfec8-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-261">Das Element hat seinen Vorgang abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cfec8-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="cfec8-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Energie Modus** (18)</span><span class="sxs-lookup"><span data-stu-id="cfec8-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cfec8-263">Das-Element verfügt über zusätzliche Energiemodell Informationen, die in der zugeordneten powermanagementservice-Zuordnung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cfec8-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfec8-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cfec8-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-266">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="cfec8-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfec8-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-269">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**".**Detailedstatus**","**CIM \_ ManagedSystemElement**.**Healthstate**")</span><span class="sxs-lookup"><span data-stu-id="cfec8-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-270">Gibt einen Statuswert auf hoher Ebene an.</span><span class="sxs-lookup"><span data-stu-id="cfec8-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfec8-271">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cfec8-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cfec8-272">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="cfec8-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cfec8-273">Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="cfec8-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cfec8-274">**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="cfec8-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfec8-275">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cfec8-276">**Anbieter reserviert** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="cfec8-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-277">**Status**</span><span class="sxs-lookup"><span data-stu-id="cfec8-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cfec8-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-280">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ ManagedSystemElement**".**OperationalStatus**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="cfec8-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-281">Gibt den primären Status des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="cfec8-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="cfec8-282">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cfec8-282">This property is deprecated.</span></span> <span data-ttu-id="cfec8-283">Sie wird durch die Eigenschaft **OperationalStatus** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cfec8-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="cfec8-284">Wenn Sie sich für die Verwendung der **Status** -Eigenschaft für die Abwärtskompatibilität entscheiden, sollte Sie für die **OperationalStatus** -Eigenschaft sekundär sein.</span><span class="sxs-lookup"><span data-stu-id="cfec8-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="cfec8-285">("OK")</span><span class="sxs-lookup"><span data-stu-id="cfec8-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-286">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="cfec8-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-287">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="cfec8-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-288">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="cfec8-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-289">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="cfec8-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-290">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="cfec8-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-291">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="cfec8-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-292">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="cfec8-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-293">("Gestresst")</span><span class="sxs-lookup"><span data-stu-id="cfec8-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-294">("Nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="cfec8-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-295">("Kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="cfec8-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-296">("Verlorene comm")</span><span class="sxs-lookup"><span data-stu-id="cfec8-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cfec8-297">("Beendet")</span><span class="sxs-lookup"><span data-stu-id="cfec8-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfec8-298">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="cfec8-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfec8-299">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cfec8-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cfec8-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfec8-301">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**".**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="cfec8-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="cfec8-302">Gibt Beschreibungen der entsprechenden Werte im **OperationalStatus** -Array an.</span><span class="sxs-lookup"><span data-stu-id="cfec8-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="cfec8-303">Wenn z. b. ein Element in der **OperationalStatus** -Eigenschaft den Wert **stoppt**, enthält das-Element am gleichen Array Index in dieser Eigenschaft möglicherweise eine Erläuterung, warum ein Objekt beendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfec8-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfec8-304">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfec8-304">Requirements</span></span>



| <span data-ttu-id="cfec8-305">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfec8-305">Requirement</span></span> | <span data-ttu-id="cfec8-306">Wert</span><span class="sxs-lookup"><span data-stu-id="cfec8-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfec8-307">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfec8-307">Minimum supported client</span></span><br/> | <span data-ttu-id="cfec8-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cfec8-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cfec8-309">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfec8-309">Minimum supported server</span></span><br/> | <span data-ttu-id="cfec8-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfec8-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cfec8-311">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfec8-311">Namespace</span></span><br/>                | <span data-ttu-id="cfec8-312">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cfec8-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cfec8-313">MOF</span><span class="sxs-lookup"><span data-stu-id="cfec8-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfec8-314"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cfec8-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfec8-315">DLL</span><span class="sxs-lookup"><span data-stu-id="cfec8-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfec8-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfec8-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cfec8-317">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfec8-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfec8-318">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="cfec8-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

