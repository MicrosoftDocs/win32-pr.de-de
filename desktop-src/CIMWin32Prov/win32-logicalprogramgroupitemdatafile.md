---
description: Die Win32 \_ -WMI-Klasse logicalprogramgroupitemdatafile verknüpft die Programm Gruppenelemente des Start Menüs und der Dateien, in denen Sie gespeichert sind.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127717"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="f63f8-103">Win32 \_ logicalprogramgroupitemdatafile-Klasse</span><span class="sxs-lookup"><span data-stu-id="f63f8-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="f63f8-104">Die Win32- [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **\_ logicalprogramgroupitemdatafile** verknüpft die Programm Gruppenelemente des **Start** Menüs und der Dateien, in denen Sie gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f63f8-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="f63f8-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f63f8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f63f8-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f63f8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f63f8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f63f8-108">Member</span><span class="sxs-lookup"><span data-stu-id="f63f8-108">Members</span></span>

<span data-ttu-id="f63f8-109">Die **Win32 \_ logicalprogramgroupitemdatafile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f63f8-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="f63f8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f63f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f63f8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f63f8-111">Properties</span></span>

<span data-ttu-id="f63f8-112">Die **Win32 \_ logicalprogramgroupitemdatafile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f63f8-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f63f8-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="f63f8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f63f8-114">Datentyp: **Win32 \_ logicalprogramgroupitem**</span><span class="sxs-lookup"><span data-stu-id="f63f8-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="f63f8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f63f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f63f8-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ logicalprogramgroupitem")</span><span class="sxs-lookup"><span data-stu-id="f63f8-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="f63f8-117">Verweis auf die-Instanz, die die Programm Gruppierungen im **Startmenü** darstellt.</span><span class="sxs-lookup"><span data-stu-id="f63f8-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="f63f8-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="f63f8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f63f8-119">Datentyp: **CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="f63f8-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="f63f8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f63f8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f63f8-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")</span><span class="sxs-lookup"><span data-stu-id="f63f8-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="f63f8-122">Verweis auf die-Instanz, die die Klasse darstellt, die der Programmgruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f63f8-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f63f8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f63f8-123">Remarks</span></span>

<span data-ttu-id="f63f8-124">Die **Win32 \_ logicalprogramgroupitemdatafile** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f63f8-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f63f8-125">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="f63f8-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="f63f8-126">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="f63f8-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="f63f8-127">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="f63f8-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="f63f8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f63f8-128">Requirements</span></span>



| <span data-ttu-id="f63f8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f63f8-129">Requirement</span></span> | <span data-ttu-id="f63f8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f63f8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f63f8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f63f8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f63f8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f63f8-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f63f8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f63f8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f63f8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f63f8-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f63f8-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="f63f8-135">Namespace</span></span><br/>                | <span data-ttu-id="f63f8-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f63f8-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f63f8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f63f8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f63f8-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f63f8-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f63f8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f63f8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f63f8-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f63f8-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63f8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f63f8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63f8-142">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="f63f8-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="f63f8-143">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f63f8-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

