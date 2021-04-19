---
description: Beschreibt die lokale Installation von WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349939"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="13808-103">\_\_Cimumidentificlass</span><span class="sxs-lookup"><span data-stu-id="13808-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="13808-104">Die " **\_ \_ cimumidentifisystem** "-Klasse beschreibt die lokale Installation von WMI.</span><span class="sxs-lookup"><span data-stu-id="13808-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="13808-105">Dies ist eine Singleton-Klasse. Es gibt nur eine Instanz.</span><span class="sxs-lookup"><span data-stu-id="13808-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="13808-106">Die **\_ \_ cimumidentificlass** ist nur in den **\\ Standard** Namespaces **root** und Root verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13808-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="13808-107">Benutzer Fragen die-Instanz ab, um Informationen zur WMI-Installation zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="13808-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="13808-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="13808-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13808-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="13808-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13808-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="13808-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="13808-111">Member</span><span class="sxs-lookup"><span data-stu-id="13808-111">Members</span></span>

<span data-ttu-id="13808-112">Die **\_ \_ cimumidentifizierungsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13808-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="13808-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13808-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13808-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13808-114">Properties</span></span>

<span data-ttu-id="13808-115">Die **\_ \_ cimumidentificlass** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13808-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13808-116">**Setupdatetime**</span><span class="sxs-lookup"><span data-stu-id="13808-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13808-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13808-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13808-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13808-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13808-119">Datum und Uhrzeit der Installation.</span><span class="sxs-lookup"><span data-stu-id="13808-119">Date and time of installation.</span></span> <span data-ttu-id="13808-120">Diese Eigenschaft ist leer, nachdem das Betriebssystem zum ersten Mal installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="13808-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="13808-121">Wenn das WMI-Repository gelöscht und dann erneut erstellt wurde, enthält diese Eigenschaft das Datum und die Uhrzeit der erneuten Erstellung des Repository.</span><span class="sxs-lookup"><span data-stu-id="13808-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="13808-122">**Versioncurrentlyrunning**</span><span class="sxs-lookup"><span data-stu-id="13808-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13808-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13808-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13808-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13808-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13808-125">Gibt die Version des eigentlichen Bilds an, das den WMI-Dienst enthält, der das Common Information Model (CIM)-Repository erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="13808-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="13808-126">Da sich das Repository-Format zwischen den Versionen von WMI ändern kann, ermöglicht diese Eigenschaft zukünftigen WMI-Upgrades, zu bestimmen, ob die Datenbank aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="13808-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="13808-127">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="13808-127">The format is:</span></span>

<span data-ttu-id="13808-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="13808-128">"1.00.183.0000"</span></span>

<span data-ttu-id="13808-129">Wenn die erste Ziffer die Hauptversion ist, sind die nächsten zwei Ziffern neben Versionen, und die nächsten drei Ziffern sind die Buildnummer.</span><span class="sxs-lookup"><span data-stu-id="13808-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="13808-130">Die verbleibenden Ziffern werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13808-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="13808-131">**Versionusedtykreatedb**</span><span class="sxs-lookup"><span data-stu-id="13808-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13808-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13808-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13808-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13808-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13808-134">Gibt die Version des eigentlichen Bilds an, das den WMI-Dienst enthält, der das CIM-Repository erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="13808-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="13808-135">Da sich das Repository-Format zwischen den Versionen von WMI ändern kann, ermöglicht diese Eigenschaft zukünftigen WMI-Upgrades, zu bestimmen, ob die Datenbank aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="13808-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="13808-136">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="13808-136">The format is:</span></span>

<span data-ttu-id="13808-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="13808-137">"1.00.183.0000"</span></span>

<span data-ttu-id="13808-138">Wenn die erste Ziffer die Hauptversion ist, sind die nächsten zwei Ziffern neben Versionen, und die nächsten drei Ziffern sind die Buildnummer.</span><span class="sxs-lookup"><span data-stu-id="13808-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="13808-139">Die verbleibenden Ziffern werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13808-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="13808-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="13808-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13808-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13808-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13808-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13808-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13808-143">Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="13808-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13808-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13808-144">Remarks</span></span>

<span data-ttu-id="13808-145">Die **\_ \_ cimumidentificlass** wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="13808-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="13808-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13808-146">Examples</span></span>

<span data-ttu-id="13808-147">Im folgenden VBScript-Codebeispiel wird beschrieben, wie die Identifikationsinformationen des CIM-Objektmodells angezeigt und aus dem Beispiel Verzeichnis unter \\ \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ Scripting verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13808-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="13808-148">Im folgenden perl-Codebeispiel wird beschrieben, wie die Identifikationsinformationen des CIM-Objektmodells angezeigt und aus dem Beispiel Verzeichnis unter \\ \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ Scripting verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13808-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="13808-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13808-149">Requirements</span></span>



| <span data-ttu-id="13808-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13808-150">Requirement</span></span> | <span data-ttu-id="13808-151">Wert</span><span class="sxs-lookup"><span data-stu-id="13808-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="13808-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13808-152">Minimum supported client</span></span><br/> | <span data-ttu-id="13808-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13808-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="13808-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13808-154">Minimum supported server</span></span><br/> | <span data-ttu-id="13808-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13808-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="13808-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="13808-156">Namespace</span></span><br/>                | <span data-ttu-id="13808-157">Root</span><span class="sxs-lookup"><span data-stu-id="13808-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="13808-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13808-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13808-159">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="13808-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="13808-160">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="13808-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

