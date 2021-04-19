---
description: Die \_ WMI-Klasse "Win32 logicalprogramgroupdirectory Association" bezieht logische Programm Gruppen (Gruppierungen im Startmenü) und die Datei Verzeichnisse, in denen Sie gespeichert sind.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342578"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a><span data-ttu-id="09987-103">Win32 \_ logicalprogramgroupdirectory-Klasse</span><span class="sxs-lookup"><span data-stu-id="09987-103">Win32\_LogicalProgramGroupDirectory class</span></span>

<span data-ttu-id="09987-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ logicalprogramgroupdirectory** Association" bezieht logische Programm Gruppen (Gruppierungen im **Startmenü** ) und die Datei Verzeichnisse, in denen Sie gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="09987-104">The **Win32\_LogicalProgramGroupDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical program groups (groupings in the **Start** menu) and the file directories in which they are stored.</span></span>

<span data-ttu-id="09987-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="09987-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="09987-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="09987-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="09987-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09987-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="09987-108">Member</span><span class="sxs-lookup"><span data-stu-id="09987-108">Members</span></span>

<span data-ttu-id="09987-109">Die **Win32 \_ logicalprogramgroupdirectory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="09987-109">The **Win32\_LogicalProgramGroupDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="09987-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09987-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09987-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09987-111">Properties</span></span>

<span data-ttu-id="09987-112">Die **Win32 \_ logicalprogramgroupdirectory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="09987-112">The **Win32\_LogicalProgramGroupDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09987-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="09987-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09987-114">Datentyp: **Win32 \_ logicalprogramgroup**</span><span class="sxs-lookup"><span data-stu-id="09987-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="09987-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09987-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09987-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ logicalprogramgroup")</span><span class="sxs-lookup"><span data-stu-id="09987-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="09987-117">Verweis auf die Instanz, die die logische Programmgruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="09987-117">Reference to the instance representing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="09987-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="09987-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09987-119">Datentyp: **Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="09987-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="09987-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="09987-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09987-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32- \_ Verzeichnis")</span><span class="sxs-lookup"><span data-stu-id="09987-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="09987-122">Verweis auf die-Instanz, die das Datei Verzeichnis für die logische Programmgruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="09987-122">Reference to the instance representing the file directory for the logical program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09987-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09987-123">Remarks</span></span>

<span data-ttu-id="09987-124">Die **Win32 \_ logicalprogramgroupdirectory** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="09987-124">The **Win32\_LogicalProgramGroupDirectory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="09987-125">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="09987-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="09987-126">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="09987-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="09987-127">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="09987-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="09987-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09987-128">Requirements</span></span>



| <span data-ttu-id="09987-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09987-129">Requirement</span></span> | <span data-ttu-id="09987-130">Wert</span><span class="sxs-lookup"><span data-stu-id="09987-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09987-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09987-131">Minimum supported client</span></span><br/> | <span data-ttu-id="09987-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09987-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09987-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09987-133">Minimum supported server</span></span><br/> | <span data-ttu-id="09987-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09987-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09987-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="09987-135">Namespace</span></span><br/>                | <span data-ttu-id="09987-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="09987-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="09987-137">MOF</span><span class="sxs-lookup"><span data-stu-id="09987-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09987-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="09987-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="09987-139">DLL</span><span class="sxs-lookup"><span data-stu-id="09987-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09987-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09987-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09987-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09987-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09987-142">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="09987-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="09987-143">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09987-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

