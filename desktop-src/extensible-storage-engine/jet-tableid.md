---
description: 'Weitere Informationen finden Sie hier: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355288"
---
# <a name="jet_tableid"></a><span data-ttu-id="ff5fd-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff5fd-103">JET_TABLEID</span></span>


<span data-ttu-id="ff5fd-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ff5fd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="ff5fd-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff5fd-105">JET_TABLEID</span></span>

<span data-ttu-id="ff5fd-106">Der JET_TABLEID-Datentyp enthält ein Handle für den Daten Bank Cursor, der für einen aufzurufenden Jet-API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="ff5fd-107">Ein Cursor kann nur mit der Sitzung verwendet werden, die zum Öffnen dieses Cursors verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="ff5fd-108">Datentypen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-108">Data Types</span></span>

<span data-ttu-id="ff5fd-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff5fd-109">JET_TABLEID</span></span>

<span data-ttu-id="ff5fd-110">Entweder **null** oder [JET_tableidNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Cursor Handle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="ff5fd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-111">Remarks</span></span>

<span data-ttu-id="ff5fd-112">Ein Cursor verwaltet die Verwendung einer Tabelle für die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="ff5fd-113">Ein Cursor kann die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="ff5fd-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="ff5fd-114">Datensätze überprüfen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-114">Scan records</span></span>

  - <span data-ttu-id="ff5fd-115">Suchen nach Datensätzen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-115">Search for records</span></span>

  - <span data-ttu-id="ff5fd-116">Effektive Sortierreihenfolge und Sichtbarkeit dieser Datensätze auswählen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="ff5fd-117">Erstellen, aktualisieren oder Löschen von Datensätzen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="ff5fd-118">Ändern des Schemas der Tabelle</span><span class="sxs-lookup"><span data-stu-id="ff5fd-118">Modify the schema of the table</span></span>

<span data-ttu-id="ff5fd-119">Die unterstützten Funktionen des Cursors können sich ändern, wenn sich der Status oder der Typ der zugrunde liegenden Tabelle ändert.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="ff5fd-120">Eine temporäre Tabelle kann z. b. die Suche nach Daten nicht zulassen, wenn Sie mit bestimmten Optionen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="ff5fd-121">Der Cursor ist immer vollständig mit der zugrunde liegenden Tabelle verbunden und interagiert ohne Zwischenspeichern direkt mit diesen Daten.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="ff5fd-122">Fast alle Kernfunktionen von ISAM, die von dieser Datenbank-Engine verfügbar gemacht werden, funktionieren über den Cursor.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="ff5fd-123">Ein Cursor kann mit [jetopentable](./jetopentable-function.md) oder [jetopumtemptable](./jetopentemptable-function.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="ff5fd-124">Ein Cursor kann mithilfe von [jetdupcursor](./jetdupcursor-function.md)dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="ff5fd-125">Ein Cursor kann mithilfe von [jetclosetable](./jetclosetable-function.md) explizit geschlossen oder mithilfe von [jetendsession](./jetendsession-function.md) oder [jetterm](./jetterm-function.md)implizit geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="ff5fd-126">Ein Cursor kann auch implizit von [jetrollback](./jetrollback-function.md) geschlossen werden, wenn er in der abgebrochenen Transaktion geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="ff5fd-127">Die maximale Anzahl von Cursorn, die zu einem beliebigen Zeitpunkt erstellt werden können, wird von [JET_paramMaxCursors](./resource-parameters.md)gesteuert, die mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="ff5fd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff5fd-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ff5fd-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5fd-130">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff5fd-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ff5fd-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5fd-132">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff5fd-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ff5fd-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ff5fd-134">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ff5fd-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ff5fd-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ff5fd-135">See Also</span></span>

[<span data-ttu-id="ff5fd-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="ff5fd-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="ff5fd-137">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="ff5fd-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="ff5fd-138">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="ff5fd-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="ff5fd-139">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="ff5fd-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="ff5fd-140">Jetopentable</span><span class="sxs-lookup"><span data-stu-id="ff5fd-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="ff5fd-141">Jetopumtemptable</span><span class="sxs-lookup"><span data-stu-id="ff5fd-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="ff5fd-142">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="ff5fd-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="ff5fd-143">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="ff5fd-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="ff5fd-144">Jetterm</span><span class="sxs-lookup"><span data-stu-id="ff5fd-144">JetTerm</span></span>](./jetterm-function.md)
