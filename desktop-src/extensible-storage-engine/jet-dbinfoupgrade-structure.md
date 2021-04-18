---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOUPGRADE Struktur'
title: JET_DBINFOUPGRADE-Struktur
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345054"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="dd4f2-103">JET_DBINFOUPGRADE-Struktur</span><span class="sxs-lookup"><span data-stu-id="dd4f2-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="dd4f2-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dd4f2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="dd4f2-105">JET_DBINFOUPGRADE-Struktur</span><span class="sxs-lookup"><span data-stu-id="dd4f2-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="dd4f2-106">Die **JET_DBINFOUPGRADE** Struktur enthält Informationen zum Upgradestatus der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="dd4f2-107">Dieser Wert wird nur abgerufen, wenn **JET_DBINFOUPGRADE** an [jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefilinput Info](./jetgetdatabasefileinfo-function.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="dd4f2-108">Diese Struktur ist für aktuelle Betriebssystemversionen der Datenbank-Engine nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="dd4f2-109">Member</span><span class="sxs-lookup"><span data-stu-id="dd4f2-109">Members</span></span>

<span data-ttu-id="dd4f2-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-110">**cbStruct**</span></span>

<span data-ttu-id="dd4f2-111">Legen Sie auf die Größe der **JET_DBINFOUPGRADE** Struktur in Bytes fest.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="dd4f2-112">**cbfilesizelow**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="dd4f2-113">Das niedrige **DWORD** , das die aktuelle Dateigröße für die Datenbank widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="dd4f2-114">**cbfilesizehigh**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="dd4f2-115">Das hohe **DWORD** , das die aktuelle Dateigröße für die Datenbank widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="dd4f2-116">**cbfreespacerequiredlow**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="dd4f2-117">Das niedrige **DWORD** des geschätzten freien Speicherplatzes, der für ein direktes Upgrade benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="dd4f2-118">**cbfreespacerequiredhigh**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="dd4f2-119">Das hohe **DWORD** des geschätzten freien Speicherplatzes, der für ein direktes Upgrade benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="dd4f2-120">**csectoupgrade**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-120">**csecToUpgrade**</span></span>

<span data-ttu-id="dd4f2-121">Die geschätzte Zeit, die für das Upgrade benötigt wird (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="dd4f2-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="dd4f2-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-122">**ulFlags**</span></span>

<span data-ttu-id="dd4f2-123">Ein Bitfeld, das aus null oder mehr der folgenden Flags besteht: **fupgradable**, **falsoryupgrade**.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="dd4f2-124">**fupgradable**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-124">**fUpgradable**</span></span>

<span data-ttu-id="dd4f2-125">Die Datenbank kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-125">The database is upgradeable.</span></span>

<span data-ttu-id="dd4f2-126">**falsch aktualisiert**</span><span class="sxs-lookup"><span data-stu-id="dd4f2-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="dd4f2-127">Die Datenbank wird auf das aktuelle Datenbankformat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="dd4f2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd4f2-128">Remarks</span></span>

<span data-ttu-id="dd4f2-129">Eine **JET_DBINFOUPGRADE** Struktur wird durch einen Aufrufen von [jetgetdatabaseinfo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefileinfo](./jetgetdatabasefileinfo-function.md)aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="dd4f2-130">Wenn die Funktion nicht erfolgreich ausgeführt werden kann, ist der Inhalt der-Struktur nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="dd4f2-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd4f2-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd4f2-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dd4f2-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dd4f2-133">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd4f2-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dd4f2-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dd4f2-135">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd4f2-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dd4f2-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dd4f2-137">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="dd4f2-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="dd4f2-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dd4f2-138">See Also</span></span>

[<span data-ttu-id="dd4f2-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dd4f2-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dd4f2-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dd4f2-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dd4f2-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dd4f2-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dd4f2-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dd4f2-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dd4f2-143">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="dd4f2-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="dd4f2-144">Jetgetobjectinfo</span><span class="sxs-lookup"><span data-stu-id="dd4f2-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="dd4f2-145">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="dd4f2-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="dd4f2-146">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="dd4f2-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
