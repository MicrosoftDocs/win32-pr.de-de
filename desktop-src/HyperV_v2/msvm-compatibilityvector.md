---
description: Verweist auf die Kompatibilitätsinformationen für einen virtuellen Computer (VM) (bei Ausführen auf einem VM-Computersystem) oder einen Host (bei der auf einem Host Computersystem ausgeführt).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866412"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="b2df6-103">MSVM \_ compatibilityvector-Klasse</span><span class="sxs-lookup"><span data-stu-id="b2df6-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="b2df6-104">Verweist auf die Kompatibilitätsinformationen für einen virtuellen Computer (VM) (bei Ausführen auf einem VM-Computersystem) oder einen Host (bei der auf einem Host Computersystem ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="b2df6-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="b2df6-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2df6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2df6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="b2df6-107">Member</span><span class="sxs-lookup"><span data-stu-id="b2df6-107">Members</span></span>

<span data-ttu-id="b2df6-108">Die **MSVM \_ compatibilityvector** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b2df6-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="b2df6-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2df6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2df6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2df6-110">Properties</span></span>

<span data-ttu-id="b2df6-111">Die **MSVM \_ compatibilityvector** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2df6-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2df6-112">**Compareoperation**</span><span class="sxs-lookup"><span data-stu-id="b2df6-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2df6-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2df6-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2df6-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2df6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2df6-115">Bezeichnet die Vergleichsoperation, bei der nur dann true zurückgegeben wird, wenn zwei Vektoren kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="b2df6-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="b2df6-116">Die Daten des virtuellen Computers befinden sich auf der linken Seite des Vergleichs, und die Daten des Hosts befinden sich auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="b2df6-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="b2df6-117">**Gleich** (0)</span><span class="sxs-lookup"><span data-stu-id="b2df6-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="b2df6-118">**Superset** (1)</span><span class="sxs-lookup"><span data-stu-id="b2df6-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="b2df6-119">**Teilmenge** (2)</span><span class="sxs-lookup"><span data-stu-id="b2df6-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="b2df6-120">**Disjoint** (3)</span><span class="sxs-lookup"><span data-stu-id="b2df6-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="b2df6-121">**GreaterThan** (4)</span><span class="sxs-lookup"><span data-stu-id="b2df6-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="b2df6-122">**GreaterThanOrEqual** (5)</span><span class="sxs-lookup"><span data-stu-id="b2df6-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="b2df6-123">**LessThan** (6)</span><span class="sxs-lookup"><span data-stu-id="b2df6-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="b2df6-124">**LessThanOrEqual** (7)</span><span class="sxs-lookup"><span data-stu-id="b2df6-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="b2df6-125">**Mehrfach** (8)</span><span class="sxs-lookup"><span data-stu-id="b2df6-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="b2df6-126">**Divisible** (9)</span><span class="sxs-lookup"><span data-stu-id="b2df6-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2df6-127">**Compatibilityinfo**</span><span class="sxs-lookup"><span data-stu-id="b2df6-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2df6-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2df6-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2df6-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2df6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2df6-130">Die tatsächlichen Kompatibilitäts Attributdaten, die für den Vergleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2df6-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="b2df6-131">**Vectorid**</span><span class="sxs-lookup"><span data-stu-id="b2df6-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2df6-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2df6-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2df6-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2df6-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2df6-134">Identifiziert einen Kompatibilitäts Vektor, der ein bestimmtes Attribut darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2df6-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="b2df6-135">Diese Eigenschaft wird verwendet, um die entsprechenden Vektoren zwischen einem Host und einem virtuellen Computer abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="b2df6-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2df6-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2df6-136">Remarks</span></span>

<span data-ttu-id="b2df6-137">Die [**getsystemcompatibilityvectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse gibt ein Array von **MSVM- \_ compatibilityvector** -Instanzen für den Host (wenn Sie auf dem Host ausgeführt werden) oder einen virtuellen Computer (wenn auf dem virtuellen Computer ausgeführt wird) zurück.</span><span class="sxs-lookup"><span data-stu-id="b2df6-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="b2df6-138">Jeder **MSVM \_ compatibilityvector** -Eintrag in der Liste beschreibt einen Kompatibilitäts Attribut Vektor.</span><span class="sxs-lookup"><span data-stu-id="b2df6-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="b2df6-139">Damit ein virtueller Computer mit einem Host kompatibel ist, müssen alle zugehörigen Kompatibilitäts Attribute mit den Attributen des Hosts kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="b2df6-140">Jeder **MSVM \_ compatibilityvector** -Eintrag verfügt über folgende Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b2df6-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="b2df6-141">**Vectorid**</span><span class="sxs-lookup"><span data-stu-id="b2df6-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="b2df6-142">Identifiziert den Kompatibilitäts Vektor eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b2df6-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="b2df6-143">Diese wird verwendet, um die Vektoren für den Vergleich zwischen einem Host und einem virtuellen Computer abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="b2df6-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="b2df6-144">**Compareoperation**</span><span class="sxs-lookup"><span data-stu-id="b2df6-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="b2df6-145">Identifiziert den Vergleichs Vorgang, der bestimmt, ob die Vektoren kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="b2df6-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="b2df6-146">**Compatibilityinfo**</span><span class="sxs-lookup"><span data-stu-id="b2df6-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="b2df6-147">Enthält das tatsächliche Kompatibilitäts Attribut. Dabei handelt es sich um die Attribut Nutzlast (z. b. Prozessor Funktions Maske, Größe von Cache Zeilen Leerung usw.).</span><span class="sxs-lookup"><span data-stu-id="b2df6-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="b2df6-148">Der Satz von Vorgängen, der für **compareoperation** definiert ist, umfasst nur grundlegende ganzzahlige Vergleiche und bitweise Logik.</span><span class="sxs-lookup"><span data-stu-id="b2df6-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="b2df6-149">Dies ermöglicht, dass der tatsächliche Inhalt von **compatibilityinfo** nicht transparent bleibt.</span><span class="sxs-lookup"><span data-stu-id="b2df6-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="b2df6-150">Der Satz von Vorgängen umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b2df6-150">The set of operations include:</span></span>



| <span data-ttu-id="b2df6-151">Compareoperation</span><span class="sxs-lookup"><span data-stu-id="b2df6-151">CompareOperation</span></span> | <span data-ttu-id="b2df6-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2df6-152">Description</span></span>                                      | <span data-ttu-id="b2df6-153">Pseudo Code Vergleich</span><span class="sxs-lookup"><span data-stu-id="b2df6-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="b2df6-154">Vmccequal</span><span class="sxs-lookup"><span data-stu-id="b2df6-154">VmCcEqual</span></span>        | <span data-ttu-id="b2df6-155">Vmattr muss auf "" gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="b2df6-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="b2df6-156">If (vmattr = = gehostet)</span><span class="sxs-lookup"><span data-stu-id="b2df6-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="b2df6-157">Vmccsuperset</span><span class="sxs-lookup"><span data-stu-id="b2df6-157">VmCcSuperSet</span></span>     | <span data-ttu-id="b2df6-158">Vmattr muss eine übergeordnete Gruppe von "sestattr" sein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="b2df6-159">If ((vmattr & "blau) = =" "</span><span class="sxs-lookup"><span data-stu-id="b2df6-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="b2df6-160">Vmccsubset</span><span class="sxs-lookup"><span data-stu-id="b2df6-160">VmCcSubSet</span></span>       | <span data-ttu-id="b2df6-161">Vmattr muss eine Teilmenge von "sestattr" sein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="b2df6-162">If ((vmattr-&-Eigenschaft) = = vmattr)</span><span class="sxs-lookup"><span data-stu-id="b2df6-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="b2df6-163">Vmccdisjointset</span><span class="sxs-lookup"><span data-stu-id="b2df6-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="b2df6-164">Bei vmattr muss es sich um eine zusammenhängende Gruppe von "hustattr" handeln</span><span class="sxs-lookup"><span data-stu-id="b2df6-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="b2df6-165">If ((vmattr-&-Eigenschaft) = = 0)</span><span class="sxs-lookup"><span data-stu-id="b2df6-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="b2df6-166">Vmccgreater</span><span class="sxs-lookup"><span data-stu-id="b2df6-166">VmCcGreater</span></span>      | <span data-ttu-id="b2df6-167">Vmattr muss höher sein als "".</span><span class="sxs-lookup"><span data-stu-id="b2df6-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="b2df6-168">If (vmattr >-Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b2df6-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="b2df6-169">Vmccgreaterequal</span><span class="sxs-lookup"><span data-stu-id="b2df6-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="b2df6-170">Vmattr muss größer als oder gleich "hustattr" sein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="b2df6-171">If (vmattr >= gehostet)</span><span class="sxs-lookup"><span data-stu-id="b2df6-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="b2df6-172">Vmccless</span><span class="sxs-lookup"><span data-stu-id="b2df6-172">VmCcLess</span></span>         | <span data-ttu-id="b2df6-173">Vmattr muss kleiner sein als "".</span><span class="sxs-lookup"><span data-stu-id="b2df6-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="b2df6-174">If (vmattr <-Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b2df6-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="b2df6-175">Vmcclessequal</span><span class="sxs-lookup"><span data-stu-id="b2df6-175">VmCcLessEqual</span></span>    | <span data-ttu-id="b2df6-176">"Vmattr" muss kleiner oder gleich "hustattr" sein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="b2df6-177">If (vmattr <= gehostet)</span><span class="sxs-lookup"><span data-stu-id="b2df6-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="b2df6-178">Vmccmultiple</span><span class="sxs-lookup"><span data-stu-id="b2df6-178">VmCcMultiple</span></span>     | <span data-ttu-id="b2df6-179">Vmattr muss ein Vielfaches von "".</span><span class="sxs-lookup"><span data-stu-id="b2df6-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="b2df6-180">If ((vmattr% hustattr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="b2df6-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="b2df6-181">Vmccdivisor</span><span class="sxs-lookup"><span data-stu-id="b2df6-181">VmCcDivisor</span></span>      | <span data-ttu-id="b2df6-182">Vmattr muss ein Divisor von "Host-r" sein.</span><span class="sxs-lookup"><span data-stu-id="b2df6-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="b2df6-183">If (("", "% vmattr") = = 0)</span><span class="sxs-lookup"><span data-stu-id="b2df6-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="b2df6-184">SCVMM muss diese Schritte ausführen, um zu bestimmen, ob ein virtueller Computer mit einem Host kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="b2df6-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="b2df6-185">**So bestimmen Sie, ob ein virtueller Computer mit einem Host kompatibel ist**</span><span class="sxs-lookup"><span data-stu-id="b2df6-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="b2df6-186">Iterieren Sie alle **MSVM \_ compatibilityvector** -Elemente für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b2df6-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="b2df6-187">Verwenden Sie für jedes **MSVM \_ compatibilityvector** -Element den in **compareoperation** angegebenen Kompatibilitäts Vorgang, um den Hardware Kompatibilitäts Vektor des virtuellen Computers mit dem entsprechenden Kompatibilitäts Vektor für den Host zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="b2df6-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="b2df6-188">Wenn alle **MSVM \_ compatibilityvector** -Elemente aus dem virtuellen Computer als kompatibel eingestuft werden, ist der virtuelle Computer mit dem Host kompatibel (aus Sicht des Prozessor Features).</span><span class="sxs-lookup"><span data-stu-id="b2df6-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2df6-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2df6-189">Requirements</span></span>



| <span data-ttu-id="b2df6-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2df6-190">Requirement</span></span> | <span data-ttu-id="b2df6-191">Wert</span><span class="sxs-lookup"><span data-stu-id="b2df6-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2df6-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2df6-192">Minimum supported client</span></span><br/> | <span data-ttu-id="b2df6-193">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b2df6-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b2df6-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2df6-194">Minimum supported server</span></span><br/> | <span data-ttu-id="b2df6-195">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2df6-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b2df6-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2df6-196">Namespace</span></span><br/>                | <span data-ttu-id="b2df6-197">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2df6-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2df6-198">MOF</span><span class="sxs-lookup"><span data-stu-id="b2df6-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2df6-199"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b2df6-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2df6-200">DLL</span><span class="sxs-lookup"><span data-stu-id="b2df6-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2df6-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2df6-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2df6-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2df6-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2df6-203">**Getsystemcompatibilityvectors**</span><span class="sxs-lookup"><span data-stu-id="b2df6-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="b2df6-204">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="b2df6-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




