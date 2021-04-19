---
description: 'Weitere Informationen finden Sie unter: jetdeletetable-Funktion'
title: Jetdeletetable-Funktion
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369892"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="7e2cd-103">Jetdeletetable-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e2cd-103">JetDeleteTable Function</span></span>


<span data-ttu-id="7e2cd-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7e2cd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="7e2cd-105">Jetdeletetable-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e2cd-105">JetDeleteTable Function</span></span>

<span data-ttu-id="7e2cd-106">Die **jetdeletetable** -Funktion löscht eine Tabelle in einer ESE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="7e2cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e2cd-107">Parameters</span></span>

<span data-ttu-id="7e2cd-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="7e2cd-108">*sesid*</span></span>

<span data-ttu-id="7e2cd-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="7e2cd-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="7e2cd-110">*dbid*</span></span>

<span data-ttu-id="7e2cd-111">Der für den API-Befehl zu verwendende Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="7e2cd-112">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="7e2cd-112">*szTableName*</span></span>

<span data-ttu-id="7e2cd-113">Der Name der zu löschenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="7e2cd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e2cd-114">Return Value</span></span>

<span data-ttu-id="7e2cd-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7e2cd-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7e2cd-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e2cd-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7e2cd-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="7e2cd-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e2cd-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e2cd-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7e2cd-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7e2cd-120">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2cd-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="7e2cd-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="7e2cd-122">Es wurde versucht, eine Tabelle zu löschen, während eine andere Sitzung über eine offene Tabellen-ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) mit <a href="gg294118(v=exchg.10).md">jetopentable</a> oder <a href="gg269193(v=exchg.10).md">jetdupcursor</a>verfügt.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e2cd-123">JET_errCannotDeletetemporary Tabelle</span><span class="sxs-lookup"><span data-stu-id="7e2cd-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="7e2cd-124">Es wurde versucht, eine temporäre Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="7e2cd-125">Eine temporäre Tabelle wird automatisch gelöscht, wenn Sie mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2cd-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="7e2cd-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="7e2cd-127">Es wurde versucht, eine Vorlagen Tabelle zu löschen, d. h. eine Tabelle, aus der DDL vererbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="7e2cd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e2cd-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e2cd-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7e2cd-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2cd-130">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2cd-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7e2cd-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2cd-132">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e2cd-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7e2cd-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2cd-134">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2cd-135"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7e2cd-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2cd-136">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e2cd-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7e2cd-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2cd-138">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7e2cd-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e2cd-139"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7e2cd-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7e2cd-140">Implementiert als <strong>jetdeletetablew</strong> (Unicode) und <strong>jetdeletetablea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7e2cd-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7e2cd-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7e2cd-141">See Also</span></span>

[<span data-ttu-id="7e2cd-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="7e2cd-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="7e2cd-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7e2cd-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7e2cd-144">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="7e2cd-144">JetCloseTable</span></span>](./jetclosetable-function.md)
