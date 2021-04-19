---
description: Stellt eine Zuordnung zwischen einem Dienst und einem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: CIM_ServiceAffectsElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349025"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="65470-103">CIM \_ serviceaffectselements-Klasse</span><span class="sxs-lookup"><span data-stu-id="65470-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="65470-104">Stellt eine Zuordnung zwischen einem Dienst und einem verwalteten Element dar, das von seiner Ausführung betroffen sein kann.</span><span class="sxs-lookup"><span data-stu-id="65470-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="65470-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65470-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="65470-106">Member</span><span class="sxs-lookup"><span data-stu-id="65470-106">Members</span></span>

<span data-ttu-id="65470-107">Die **CIM \_ serviceaffectselements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="65470-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="65470-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65470-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65470-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65470-109">Properties</span></span>

<span data-ttu-id="65470-110">Die **CIM \_ serviceaffectselements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="65470-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65470-111">**Affectedelta-Element**</span><span class="sxs-lookup"><span data-stu-id="65470-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65470-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="65470-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="65470-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65470-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65470-114">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65470-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65470-115">Das verwaltete Element, das vom Dienst betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="65470-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="65470-116">**Affectingelement**</span><span class="sxs-lookup"><span data-stu-id="65470-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65470-117">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="65470-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="65470-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65470-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65470-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65470-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65470-120">Der Dienst, der das verwaltete Element beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="65470-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="65470-121">**Elementeffects**</span><span class="sxs-lookup"><span data-stu-id="65470-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65470-122">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="65470-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="65470-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65470-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65470-124">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ serviceaffectselements**".**Otherelementeffect-Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="65470-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="65470-125">Die Auswirkung auf das verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="65470-125">The effect on the managed element.</span></span> <span data-ttu-id="65470-126">Dieses Array entspricht dem Array **otherelementeffectarbeschreibungen** .</span><span class="sxs-lookup"><span data-stu-id="65470-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="65470-127">\- Exklusive Verwendung (2): kein anderer Dienst kann diese Zuordnung zum Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="65470-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="65470-128">\- Leistungs Beeinträchtigung (3): als veraltet markiert, um "verbraucht", "steigert die Leistung" oder "Beeinträchtigung der Leistung".</span><span class="sxs-lookup"><span data-stu-id="65470-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="65470-129">Die Ausführung des-Dienstanbieter kann die Leistung des-Elements verbessern oder beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="65470-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="65470-130">Dies kann als Nebeneffekt der Ausführung oder als beabsichtigte Folge der vom Dienst bereitgestellten Methoden auftreten.</span><span class="sxs-lookup"><span data-stu-id="65470-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="65470-131">\- Element Integrität (4): als veraltet markiert, um "verbraucht", "erhöht die Integrität" oder "verschlechtert die Integrität".</span><span class="sxs-lookup"><span data-stu-id="65470-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="65470-132">Die Ausführung des Dienstanbieter kann die Integrität des Elements verbessern oder verringern.</span><span class="sxs-lookup"><span data-stu-id="65470-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="65470-133">Dies kann als Nebeneffekt der Ausführung oder als beabsichtigte Folge der vom Dienst bereitgestellten Methoden auftreten.</span><span class="sxs-lookup"><span data-stu-id="65470-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="65470-134">\- Verwaltet (5): der Dienst verwaltet das-Element.</span><span class="sxs-lookup"><span data-stu-id="65470-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="65470-135">\- Verbraucht (6): die Ausführung des Dienstanbieter nutzt ein oder alle zugeordneten Elemente, da der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65470-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="65470-136">Beispielsweise kann der Dienst CPU-Zyklen beanspruchen, die sich auf die Leistung auswirken können, oder Speicher, der sich sowohl auf die Leistung als auch auf die Integrität auswirkt.</span><span class="sxs-lookup"><span data-stu-id="65470-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="65470-137">(Beispielsweise kann der Mangel an freiem Speicher die Integrität beeinträchtigen, da dadurch die Möglichkeit verringert wird, den Zustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="65470-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="65470-138">) "Verbraucht" kann allein oder in Verbindung mit anderen Werten verwendet werden, insbesondere "Beeinträchtigung der Leistung" und "Beeinträchtigung der Integrität".</span><span class="sxs-lookup"><span data-stu-id="65470-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="65470-139">"Verwaltet" und nicht "verbraucht" sollten verwendet werden, um die von einem Dienst bereitgestellten Zuordnungs Dienste widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="65470-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="65470-140">\- Erhöht die Integrität (7): der Dienst kann die Integrität des zugeordneten Elements verbessern.</span><span class="sxs-lookup"><span data-stu-id="65470-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="65470-141">\- Beeinträchtigt Integrität (8): der Dienst beeinträchtigt möglicherweise die Integrität des zugeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="65470-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="65470-142">\- Steigert die Leistung (9): der Dienst kann die Leistung des zugeordneten Elements verbessern.</span><span class="sxs-lookup"><span data-stu-id="65470-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="65470-143">\- Beeinträchtigt die Leistung (10): der Dienst beeinträchtigt möglicherweise die Leistung des zugeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="65470-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="65470-144">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="65470-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="65470-145">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="65470-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="65470-146">**Exklusive Verwendung** (2)</span><span class="sxs-lookup"><span data-stu-id="65470-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="65470-147">**Leistungs Beeinträchtigung** (3)</span><span class="sxs-lookup"><span data-stu-id="65470-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="65470-148">**Element Integrität** (4)</span><span class="sxs-lookup"><span data-stu-id="65470-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="65470-149">**Verwaltet** (5)</span><span class="sxs-lookup"><span data-stu-id="65470-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="65470-150">**Verbraucht** (6)</span><span class="sxs-lookup"><span data-stu-id="65470-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="65470-151">**Erhöht die Integrität** (7)</span><span class="sxs-lookup"><span data-stu-id="65470-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="65470-152">Beeinträchtigung der **Integrität** (8)</span><span class="sxs-lookup"><span data-stu-id="65470-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="65470-153">Verb **Essern der Leistung** (9)</span><span class="sxs-lookup"><span data-stu-id="65470-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="65470-154">Beeinträchtigung der **Leistung** (10)</span><span class="sxs-lookup"><span data-stu-id="65470-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="65470-155">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="65470-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="65470-156">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="65470-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="65470-157">**Otherelementeffect-Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="65470-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65470-158">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="65470-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65470-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="65470-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65470-160">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ serviceaffectselements**".**Elementeffects**")</span><span class="sxs-lookup"><span data-stu-id="65470-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="65470-161">Jedes Element im Array stellt zusätzliche Informationen für das entsprechende Element im **elementeffects** -Array bereit.</span><span class="sxs-lookup"><span data-stu-id="65470-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="65470-162">Für jedes Element im Element " **elementeffects** ", das auf " **other** " ("1") festgelegt ist, ist eine Beschreibung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="65470-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65470-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65470-163">Requirements</span></span>



| <span data-ttu-id="65470-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65470-164">Requirement</span></span> | <span data-ttu-id="65470-165">Wert</span><span class="sxs-lookup"><span data-stu-id="65470-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65470-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65470-166">Minimum supported client</span></span><br/> | <span data-ttu-id="65470-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="65470-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="65470-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65470-168">Minimum supported server</span></span><br/> | <span data-ttu-id="65470-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65470-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="65470-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="65470-170">Namespace</span></span><br/>                | <span data-ttu-id="65470-171">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="65470-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="65470-172">MOF</span><span class="sxs-lookup"><span data-stu-id="65470-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65470-173"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="65470-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65470-174">DLL</span><span class="sxs-lookup"><span data-stu-id="65470-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65470-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65470-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

