---
description: Die CIM \_ processexecutable-Klasse stellt einen Link zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: CIM_ProcessExecutable-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041524"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="ccc49-103">CIM \_ processexecutable-Klasse</span><span class="sxs-lookup"><span data-stu-id="ccc49-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="ccc49-104">Die **CIM \_ processexecutable** -Klasse stellt einen Link zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="ccc49-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccc49-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ccc49-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ccc49-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ccc49-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ccc49-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ccc49-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ccc49-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ccc49-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc49-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccc49-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="ccc49-110">Member</span><span class="sxs-lookup"><span data-stu-id="ccc49-110">Members</span></span>

<span data-ttu-id="ccc49-111">Die **CIM \_ processexecutable** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ccc49-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="ccc49-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ccc49-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccc49-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ccc49-113">Properties</span></span>

<span data-ttu-id="ccc49-114">Die **CIM \_ processexecutable** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ccc49-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccc49-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="ccc49-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc49-116">Datentyp: **CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="ccc49-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccc49-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (Vorgänger), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ccc49-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ccc49-119">Eine [**CIM \_**](cim-datafile.md) -Datendatei, die die Datendatei beschreibt, die an der Ausführung des Prozesses beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="ccc49-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="ccc49-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="ccc49-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc49-121">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ccc49-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccc49-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-123">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ccc49-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ccc49-124">Die Basisadresse des Moduls im Adressraum des zugeordneten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="ccc49-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="ccc49-125">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ccc49-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ccc49-126">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="ccc49-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc49-127">Datentyp: **CIM- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="ccc49-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccc49-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-129">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (abhängig), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ccc49-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ccc49-130">Ein [**CIM- \_ Prozess**](cim-process.md) , der den Prozess beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ccc49-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="ccc49-131">**Globalprocesscount**</span><span class="sxs-lookup"><span data-stu-id="ccc49-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc49-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ccc49-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccc49-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-134">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ccc49-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ccc49-135">Aktuelle Anzahl der Prozesse, bei denen die Datei in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="ccc49-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ccc49-136">**ModuleInstance**</span><span class="sxs-lookup"><span data-stu-id="ccc49-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc49-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ccc49-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccc49-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-139">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ccc49-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ccc49-140">Win32-Instanzhandle.</span><span class="sxs-lookup"><span data-stu-id="ccc49-140">Win32 instance handle.</span></span> <span data-ttu-id="ccc49-141">Diese Eigenschaft ist veraltet, und es gibt keinen Ersatzwert.</span><span class="sxs-lookup"><span data-stu-id="ccc49-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="ccc49-142">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="ccc49-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc49-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ccc49-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ccc49-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc49-145">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ccc49-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ccc49-146">Verweis Zähler der Datei im zugeordneten Prozess.</span><span class="sxs-lookup"><span data-stu-id="ccc49-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccc49-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccc49-147">Remarks</span></span>

<span data-ttu-id="ccc49-148">Die **CIM \_ processexecutable** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ccc49-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ccc49-149">WMI implementiert die **CIM \_ processexecutable** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ccc49-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="ccc49-150">Die **CIM \_ processexecutable** -Klasse ist eine dynamische Klasse.</span><span class="sxs-lookup"><span data-stu-id="ccc49-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="ccc49-151">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ccc49-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ccc49-152">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ccc49-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc49-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccc49-153">Requirements</span></span>



| <span data-ttu-id="ccc49-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccc49-154">Requirement</span></span> | <span data-ttu-id="ccc49-155">Wert</span><span class="sxs-lookup"><span data-stu-id="ccc49-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc49-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccc49-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc49-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccc49-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccc49-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccc49-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc49-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccc49-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccc49-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccc49-160">Namespace</span></span><br/>                | <span data-ttu-id="ccc49-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ccc49-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ccc49-162">MOF</span><span class="sxs-lookup"><span data-stu-id="ccc49-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccc49-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ccc49-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccc49-164">DLL</span><span class="sxs-lookup"><span data-stu-id="ccc49-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc49-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccc49-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc49-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccc49-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc49-167">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="ccc49-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

