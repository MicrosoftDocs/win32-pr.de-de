---
description: Die CIM \_ -Bereitstellungs Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127080"
---
# <a name="cim_mount-class"></a><span data-ttu-id="74618-103">CIM \_ Mount-Klasse</span><span class="sxs-lookup"><span data-stu-id="74618-103">CIM\_Mount class</span></span>

<span data-ttu-id="74618-104">Die **CIM \_** -Bereitstellungs Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="74618-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="74618-105">Die Semantik dieser Beziehung erfordert, dass das eingebundene Verzeichnis in einem Dateisystem (über die Dateispeicher Zuordnung) enthalten ist, das sich von dem Dateisystem unterscheidet, auf das als abhängige verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="74618-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="74618-106">Das Dateisystem, das das Verzeichnis enthält, kann lokal oder Remote sein.</span><span class="sxs-lookup"><span data-stu-id="74618-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="74618-107">Beispielsweise kann ein lokales Dateisystem auf einem Solaris-Computersystem ein Verzeichnis aus dem Dateisystem einbinden, auf das über das Crom-Laufwerk des Computers (d. h. ein anderes lokales Dateisystem) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="74618-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="74618-108">Auf der anderen Seite wird das Verzeichnis zunächst in einem "Remote Fall" vom Dateisystem exportiert, das auf einem anderen Computersystem gehostet wird, z. b. als Dateiserver.</span><span class="sxs-lookup"><span data-stu-id="74618-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="74618-109">Um die beiden bereit Stellungen zu unterscheiden, sollte für die Verzeichnisse, auf die Remote zugegriffen werden kann, immer eine [**CIM- \_ Export**](cim-export.md) Zuordnung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="74618-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74618-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="74618-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="74618-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="74618-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="74618-112">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="74618-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="74618-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="74618-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74618-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="74618-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="74618-115">Member</span><span class="sxs-lookup"><span data-stu-id="74618-115">Members</span></span>

<span data-ttu-id="74618-116">Die **CIM \_** -Einstellungsklasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="74618-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="74618-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74618-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74618-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74618-118">Properties</span></span>

<span data-ttu-id="74618-119">Die **CIM \_** -Einstellungsklasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74618-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74618-120">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="74618-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74618-121">Datentyp: **CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="74618-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="74618-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74618-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74618-123">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="74618-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="74618-124">Ein [**CIM- \_ Verzeichnis**](cim-directory.md) , das das eingebundene Verzeichnis beschreibt.</span><span class="sxs-lookup"><span data-stu-id="74618-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="74618-125">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="74618-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74618-126">Datentyp: **CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="74618-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="74618-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74618-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74618-128">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="74618-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="74618-129">Ein [**CIM- \_ NFS**](cim-nfs.md) , das das Dateisystem beschreibt, in dem das Verzeichnis eingebunden ist.</span><span class="sxs-lookup"><span data-stu-id="74618-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74618-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74618-130">Remarks</span></span>

<span data-ttu-id="74618-131">**CIM \_** Die Einschleusung wird von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74618-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="74618-132">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="74618-132">WMI does not implement this class.</span></span>

<span data-ttu-id="74618-133">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74618-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="74618-134">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="74618-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="74618-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74618-135">Requirements</span></span>



| <span data-ttu-id="74618-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74618-136">Requirement</span></span> | <span data-ttu-id="74618-137">Wert</span><span class="sxs-lookup"><span data-stu-id="74618-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74618-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74618-138">Minimum supported client</span></span><br/> | <span data-ttu-id="74618-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74618-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74618-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74618-140">Minimum supported server</span></span><br/> | <span data-ttu-id="74618-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74618-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74618-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="74618-142">Namespace</span></span><br/>                | <span data-ttu-id="74618-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74618-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74618-144">MOF</span><span class="sxs-lookup"><span data-stu-id="74618-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74618-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74618-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74618-146">DLL</span><span class="sxs-lookup"><span data-stu-id="74618-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74618-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74618-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74618-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74618-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74618-149">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="74618-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

