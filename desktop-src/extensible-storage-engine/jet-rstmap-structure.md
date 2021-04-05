---
description: 'Weitere Informationen finden Sie hier: JET_RSTMAP Struktur'
title: JET_RSTMAP Struktur
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750553"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="04fa4-103">JET_RSTMAP Struktur</span><span class="sxs-lookup"><span data-stu-id="04fa4-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="04fa4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="04fa4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="04fa4-105">JET_RSTMAP Struktur</span><span class="sxs-lookup"><span data-stu-id="04fa4-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="04fa4-106">Die **JET_RSTMAP** -Struktur ermöglicht die Neuzuordnung von Datenbankdatei Pfaden, die während der Wiederherstellung in den Transaktions Protokollen gespeichert werden, wenn Sie von der [jetinit](./jetinit-function.md) -Funktion und der [jetexternalrestore](./jetexternalrestore-function.md) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04fa4-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="04fa4-107">Dadurch können die Datenbanken offline geschaltet oder von einer Sicherung wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="04fa4-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="04fa4-108">Member</span><span class="sxs-lookup"><span data-stu-id="04fa4-108">Members</span></span>

<span data-ttu-id="04fa4-109">**szdatabasename**</span><span class="sxs-lookup"><span data-stu-id="04fa4-109">**szDatabaseName**</span></span>

<span data-ttu-id="04fa4-110">Der aktuelle absolute Pfad einer Datenbank, die den Transaktions Protokollen zugeordnet ist, die während der Wiederherstellung wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="04fa4-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="04fa4-111">**sznewdatabasename**</span><span class="sxs-lookup"><span data-stu-id="04fa4-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="04fa4-112">Der neue absolute Pfad für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="04fa4-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="04fa4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04fa4-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04fa4-114"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="04fa4-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="04fa4-115">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="04fa4-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04fa4-116"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="04fa4-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="04fa4-117">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="04fa4-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04fa4-118"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="04fa4-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="04fa4-119">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="04fa4-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04fa4-120"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="04fa4-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="04fa4-121">Wird als <strong>JET_RSTMAP_W</strong> (Unicode) und <strong>JET_RSTMAP_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="04fa4-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="04fa4-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="04fa4-122">See Also</span></span>

[<span data-ttu-id="04fa4-123">Jetexternalrestore</span><span class="sxs-lookup"><span data-stu-id="04fa4-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="04fa4-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="04fa4-124">JetInit</span></span>](./jetinit-function.md)
