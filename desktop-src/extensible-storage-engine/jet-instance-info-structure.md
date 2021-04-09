---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE_INFO Struktur'
title: JET_INSTANCE_INFO Struktur
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868380"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="70703-103">JET_INSTANCE_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="70703-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="70703-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="70703-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="70703-105">JET_INSTANCE_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="70703-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="70703-106">Die **JET_INSTANCE_INFO** -Struktur erhält Informationen über das Ausführen von Datenbankinstanzen, wenn Sie mit den Funktionen [jetgetinstanceinfo](./jetgetinstanceinfo-function.md) und [jedessnapshotfreeze](./jetossnapshotfreeze-function.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70703-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="70703-107">Member</span><span class="sxs-lookup"><span data-stu-id="70703-107">Members</span></span>

<span data-ttu-id="70703-108">**hinstanceid**</span><span class="sxs-lookup"><span data-stu-id="70703-108">**hInstanceId**</span></span>

<span data-ttu-id="70703-109">Der [JET_INSTANCE](./jet-instance.md) der angegebenen-Instanz.</span><span class="sxs-lookup"><span data-stu-id="70703-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="70703-110">**szinstancename**</span><span class="sxs-lookup"><span data-stu-id="70703-110">**szInstanceName**</span></span>

<span data-ttu-id="70703-111">Der Name der Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="70703-111">The name of the database instance.</span></span> <span data-ttu-id="70703-112">Dieser Wert kann **null** sein, wenn die Instanz keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="70703-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="70703-113">**cdatenbanken**</span><span class="sxs-lookup"><span data-stu-id="70703-113">**cDatabases**</span></span>

<span data-ttu-id="70703-114">Die Anzahl der Datenbanken, die an die Daten Bank Instanz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="70703-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="70703-115">**CDatabase** enthält auch die Größe der Arrays von Zeichen folgen, die in " **szdatabasefilename**", " **szdatabasedisplayname**" und " **szdatabaseslvfilename**" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70703-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="70703-116">**szdatabasedateiname**</span><span class="sxs-lookup"><span data-stu-id="70703-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="70703-117">Ein Array von Zeichen folgen, das jeweils den Dateinamen einer Datenbank enthält, die an die Daten Bank Instanz angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="70703-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="70703-118">Das Array verfügt über **cdatenbanken** -Elemente.</span><span class="sxs-lookup"><span data-stu-id="70703-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="70703-119">**szdatabasedisplayname**</span><span class="sxs-lookup"><span data-stu-id="70703-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="70703-120">Ein Array von Zeichen folgen, die jeweils den anzeigen Amen einer Datenbank enthalten.</span><span class="sxs-lookup"><span data-stu-id="70703-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="70703-121">Derzeit kann die Zeichenfolge NULL sein.</span><span class="sxs-lookup"><span data-stu-id="70703-121">Currently the string can be NULL.</span></span> <span data-ttu-id="70703-122">Das Array verfügt über **cdatenbanken** -Elemente.</span><span class="sxs-lookup"><span data-stu-id="70703-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="70703-123">**szdatabaseslvfilename**</span><span class="sxs-lookup"><span data-stu-id="70703-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="70703-124">Ein Array von Zeichen folgen, das jeweils den Dateinamen der an die Daten Bank Instanz angefügten SLV-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="70703-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="70703-125">Das Array verfügt über **cdatenbanken** -Elemente.</span><span class="sxs-lookup"><span data-stu-id="70703-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="70703-126">SLV-Dateien werden nicht unterstützt. Daher sollte dieses Feld ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="70703-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="70703-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70703-127">Remarks</span></span>

<span data-ttu-id="70703-128">Jede Daten Bank Instanz kann mehrere Datenbanken enthalten.</span><span class="sxs-lookup"><span data-stu-id="70703-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="70703-129">Für eine angegebene **JET_INSTANCE_INFO** Struktur ist das Array von Zeichen folgen, das für die Datenbanken zurückgegeben wird, in derselben Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="70703-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="70703-130">Beispielsweise verweisen "szdatabasedisplayname \[ i \] " und "szdatabasefilename \[ i \] " auf dieselbe Datenbank.</span><span class="sxs-lookup"><span data-stu-id="70703-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="70703-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70703-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70703-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="70703-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="70703-133">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="70703-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70703-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="70703-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70703-135">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="70703-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70703-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="70703-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="70703-137">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="70703-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70703-138"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="70703-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="70703-139">Wird als <strong>JET_INSTANCE_INFO_W</strong> (Unicode) und <strong>JET_INSTANCE_INFO _A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="70703-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="70703-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70703-140">See Also</span></span>

[<span data-ttu-id="70703-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="70703-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="70703-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="70703-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="70703-143">Jetgetinstanceingefo</span><span class="sxs-lookup"><span data-stu-id="70703-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="70703-144">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="70703-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)
