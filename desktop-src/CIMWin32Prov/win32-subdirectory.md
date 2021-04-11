---
description: Die \_ WMI-Klasse der Win32-Unterverzeichnis Zuordnung bezieht sich auf ein Verzeichnis (Ordner) und eines der Unterverzeichnisse (Unterordner).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127316"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="a539f-103">Win32- \_ Unterverzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="a539f-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="a539f-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ Unterverzeichnis** Zuordnung bezieht sich auf ein Verzeichnis (Ordner) und eines der Unterverzeichnisse (Unterordner).</span><span class="sxs-lookup"><span data-stu-id="a539f-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="a539f-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a539f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a539f-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a539f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a539f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a539f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a539f-108">Member</span><span class="sxs-lookup"><span data-stu-id="a539f-108">Members</span></span>

<span data-ttu-id="a539f-109">Die **Win32- \_ Unterverzeichnis** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a539f-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="a539f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a539f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a539f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a539f-111">Properties</span></span>

<span data-ttu-id="a539f-112">Die **Win32- \_ Unterverzeichnis** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a539f-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a539f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a539f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a539f-114">Datentyp: **Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="a539f-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="a539f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a539f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a539f-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Verzeichnis")</span><span class="sxs-lookup"><span data-stu-id="a539f-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="a539f-117">Verweis auf die-Instanz, die die Eigenschaften des übergeordneten Verzeichnisses (Ordner) in dieser Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="a539f-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="a539f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a539f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a539f-119">Datentyp: **Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="a539f-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="a539f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a539f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a539f-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Verzeichnis")</span><span class="sxs-lookup"><span data-stu-id="a539f-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="a539f-122">Verweis auf die-Instanz, die das Unterverzeichnis (Unterordner) der Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="a539f-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a539f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a539f-123">Remarks</span></span>

<span data-ttu-id="a539f-124">Die **Win32- \_ Unterverzeichnis** Klasse wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a539f-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="a539f-125">Zum Zurückgeben einer Auflistung von Unterordnern für einen Ordner erstellen Sie eine Zuordnungs Abfrage, mit der das *RESULTROLE* auf *PartComponent* festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a539f-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="a539f-126">Dies gibt an, dass alle Elemente in der zurückgegebenen Auflistung die Rolle einer PartComponent oder eines unter Ordners des Ordner Objekts spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="a539f-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="a539f-127">Um den übergeordneten Ordner für einen Ordner zurückzugeben, legen Sie das *RESULTROLE* auf *GroupComponent* fest.</span><span class="sxs-lookup"><span data-stu-id="a539f-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="a539f-128">Die **Win32- \_ Unterverzeichnis** Klasse funktioniert nur auf Dateisystem Ebene direkt oberhalb oder direkt unterhalb des angegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="a539f-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="a539f-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a539f-129">Examples</span></span>

<span data-ttu-id="a539f-130">Das folgende VBScript-Beispiel gibt eine Liste aller Unterordner im Ordner C: \\ Scripts zurück.</span><span class="sxs-lookup"><span data-stu-id="a539f-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="a539f-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a539f-131">Requirements</span></span>



| <span data-ttu-id="a539f-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a539f-132">Requirement</span></span> | <span data-ttu-id="a539f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a539f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a539f-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a539f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a539f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a539f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a539f-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a539f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a539f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a539f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a539f-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="a539f-138">Namespace</span></span><br/>                | <span data-ttu-id="a539f-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a539f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a539f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a539f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a539f-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a539f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a539f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a539f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a539f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a539f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a539f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a539f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a539f-145">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="a539f-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="a539f-146">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="a539f-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
