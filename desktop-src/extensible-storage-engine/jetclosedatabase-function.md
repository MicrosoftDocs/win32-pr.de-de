---
description: 'Weitere Informationen zu: jetclosedatabase-Funktion'
title: Jetclosedatabase-Funktion
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524971"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="f314d-103">Jetclosedatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="f314d-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="f314d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f314d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="f314d-105">Jetclosedatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="f314d-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="f314d-106">Die **jetclosedatabase** -Funktion schließt eine Datenbankdatei, die zuvor mit [jetopendatabase](./jetopendatabase-function.md)geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f314d-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f314d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f314d-107">Parameters</span></span>

<span data-ttu-id="f314d-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="f314d-108">*sesid*</span></span>

<span data-ttu-id="f314d-109">Der Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f314d-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="f314d-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="f314d-110">*dbid*</span></span>

<span data-ttu-id="f314d-111">Die Datenbank, die geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f314d-111">The database to be closed.</span></span>

<span data-ttu-id="f314d-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f314d-112">*grbit*</span></span>

<span data-ttu-id="f314d-113">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f314d-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="f314d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f314d-114">Return Value</span></span>

<span data-ttu-id="f314d-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f314d-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f314d-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f314d-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f314d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f314d-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="f314d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f314d-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f314d-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="f314d-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="f314d-120">Die Datenbank wurde nicht zuvor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f314d-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f314d-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="f314d-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="f314d-122">Der <em>DBID</em> -Parameter war kein gültiger Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f314d-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f314d-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f314d-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f314d-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f314d-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="f314d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f314d-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f314d-126"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f314d-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f314d-127">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f314d-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f314d-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f314d-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f314d-129">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f314d-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f314d-130"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f314d-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f314d-131">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f314d-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f314d-132"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="f314d-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f314d-133">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f314d-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f314d-134"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f314d-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f314d-135">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f314d-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f314d-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f314d-136">See Also</span></span>

[<span data-ttu-id="f314d-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f314d-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f314d-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f314d-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f314d-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f314d-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f314d-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f314d-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f314d-141">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="f314d-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="f314d-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="f314d-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="f314d-143">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="f314d-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)
