---
description: 'Weitere Informationen finden Sie hier: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
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
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359497"
---
# <a name="jet_cbtyp"></a><span data-ttu-id="3f6de-103">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3f6de-103">JET_CBTYP</span></span>


<span data-ttu-id="3f6de-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3f6de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_cbtyp"></a><span data-ttu-id="3f6de-105">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3f6de-105">JET_CBTYP</span></span>

<span data-ttu-id="3f6de-106">Die **JET_CBTYP** Gruppe von Konstanten beschreibt alle möglichen Punkte in einem Vorgang, die von der Datenbank-Engine durch Aufrufen der [JET_CALLBACK](./jet-callback-callback-function.md) Callback-Funktion benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3f6de-106">The **JET_CBTYP** group of constants describes all possible points in an operation that the database engine will notify an application by calling the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span> <span data-ttu-id="3f6de-107">Die Datenbank-Engine übergibt eine dieser Konstanten im *cbyp* -Parameter der Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="3f6de-107">The database engine passes one of these constants in the *cbtyp* parameter of the callback function.</span></span> <span data-ttu-id="3f6de-108">Die Bedeutung der anderen Parameter, die von der Datenbank-Engine in diesem-Befehl weitergegeben werden, hängt von der spezifischen **JET_CBTYP** ab.</span><span class="sxs-lookup"><span data-stu-id="3f6de-108">The meaning of the other parameters passed by the database engine in this call depend on the specific **JET_CBTYP** passed.</span></span>

<span data-ttu-id="3f6de-109">**Windows XP:**  Die **JET_CBTYP** Gruppe von Konstanten wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-109">**Windows XP:**  The **JET_CBTYP** group of constants are introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f6de-110">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="3f6de-110">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="3f6de-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f6de-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-112">JET_cbtypNull</span><span class="sxs-lookup"><span data-stu-id="3f6de-112">JET_cbtypNull</span></span><br />
<span data-ttu-id="3f6de-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f6de-113">0x00000000</span></span></p></td>
<td><p><span data-ttu-id="3f6de-114">Dieser Rückruf ist reserviert und wird immer als ungültig angesehen.</span><span class="sxs-lookup"><span data-stu-id="3f6de-114">This callback is reserved and always considered invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-115">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="3f6de-115">JET_cbtypFinalize</span></span><br />
<span data-ttu-id="3f6de-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3f6de-116">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="3f6de-117">Dieser Rückruf ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-117">This callback is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-118">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="3f6de-118">JET_cbtypBeforeInsert</span></span><br />
<span data-ttu-id="3f6de-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3f6de-119">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="3f6de-120">Dieser Rückruf tritt direkt vor dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen <a href="gg269288(v=exchg.10).md">jetupdate</a>-Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="3f6de-120">This callback will occur just before a new record is inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="3f6de-121">Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-121">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="3f6de-122">Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-122">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-123">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-123">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-124"><em>gsid</em>: die Sitzung, die den einzufügenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-124"><em>sesid</em>: The session that has the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-125"><em>DBID</em>: die Datenbank-ID der Tabelle, die den einzufügenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-125"><em>dbid</em>: The database ID of the table that contains the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-126"><em>TableID</em>: der Cursor, der den neuen Datensatz vorbereitet hat, der eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6de-126"><em>tableid</em>: The cursor that has prepared the new record to be inserted.</span></span> <span data-ttu-id="3f6de-127">Es ist wichtig zu beachten, dass der Wert einer beliebigen Version oder der AutoIncrement-Spalten zu diesem Zeitpunkt möglicherweise nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-127">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-128"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-128"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-129"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-129"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-130"><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3f6de-130"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-131"><em>ulungenutzt</em>: <strong>null</strong> wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</span><span class="sxs-lookup"><span data-stu-id="3f6de-131"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-132">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="3f6de-132">JET_cbtypAfterInsert</span></span><br />
<span data-ttu-id="3f6de-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3f6de-133">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="3f6de-134">Dieser Rückruf tritt unmittelbar nach dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">jetupdate</a> auf, aber bevor <a href="gg269288(v=exchg.10).md">jetupdate</a> an seinen Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-134">This callback will occur just after a new record has been inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but before <a href="gg269288(v=exchg.10).md">JetUpdate</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="3f6de-135">Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-135">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="3f6de-136">Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-136">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-137">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-137">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-138"><em>ssisid</em>: die Sitzung, die den soeben eingefügten Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-138"><em>sesid</em>: The session that has the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-139"><em>DBID</em>: die Datenbank-ID der Tabelle, die den soeben eingefügten Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-139"><em>dbid</em>: The database ID of the table that contains the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-140"><em>TableID</em>: ein Cursor in der Tabelle, in die der soeben eingefügte Datensatz eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-140"><em>tableid</em>: A cursor on the table into which the record that was just inserted.</span></span> <span data-ttu-id="3f6de-141">Beachten Sie, dass sich der Cursor immer noch auf demselben Index Eintrag befindet wie der vor dem Einfügen-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="3f6de-141">Note that the cursor is still positioned on the same index entry as it was in the before insert callback.</span></span> <span data-ttu-id="3f6de-142">Beachten Sie, dass dieser Index Eintrag in keiner Weise mit dem eingefügten Datensatz verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f6de-142">Further note that this index entry may not be related in any way to the record being inserted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-143"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-143"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-144"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-144"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-145"><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3f6de-145"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-146"><em>ulungenutzt</em>: <strong>null</strong> , wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-146"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-147">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="3f6de-147">JET_cbtypBeforeReplace</span></span><br />
<span data-ttu-id="3f6de-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3f6de-148">0x00000008</span></span></p></td>
<td><p><span data-ttu-id="3f6de-149">Dieser Rückruf tritt direkt vor einem vorhandenen Datensatz in einer Tabelle auf, die durch einen <a href="gg269288(v=exchg.10).md">jetupdate</a>-Rückruf geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-149">This callback will occur just prior to an existing record in a table being changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="3f6de-150">Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-150">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="3f6de-151">Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-151">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-152">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-152">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-153"><em>gsid</em>: die Sitzung, die den Datensatz enthält, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6de-153"><em>sesid</em>: The session that has the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-154"><em>DBID</em>: die Datenbank-ID der Tabelle, die den zu ändernden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-154"><em>dbid</em>: The database ID of the table that contains the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-155"><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der dem Datensatz zugeordnet ist, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6de-155"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be changed.</span></span> <span data-ttu-id="3f6de-156">Es ist wichtig zu beachten, dass der Wert einer beliebigen Version oder der AutoIncrement-Spalten zu diesem Zeitpunkt möglicherweise nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-156">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-157"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-157"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-158"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-158"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-159"><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3f6de-159"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-160"><em>ulungenutzt</em>: <strong>null</strong> wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</span><span class="sxs-lookup"><span data-stu-id="3f6de-160"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-161">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="3f6de-161">JET_cbtypAfterReplace</span></span><br />
<span data-ttu-id="3f6de-162">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f6de-162">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="3f6de-163">Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269288(v=exchg.10).md">jetupdate</a> geändert wurde, aber bevor <a href="gg269288(v=exchg.10).md">jetupdate</a> an seinen Aufrufer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-163">This callback will occur just after an existing record in a table has been changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but prior to <a href="gg269288(v=exchg.10).md">JetUpdate</a> returning to its caller.</span></span></p>
<p><span data-ttu-id="3f6de-164">Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-164">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="3f6de-165">Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-165">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-166">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-166">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-167"><em>ssisid</em>: die Sitzung mit dem Datensatz, der soeben geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-167"><em>sesid</em>: The session that has the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-168"><em>DBID</em>: die Datenbank-ID der Tabelle, die den soeben geänderten Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-168"><em>dbid</em>: The database ID of the table that contains the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-169"><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der dem Datensatz zugeordnet ist, der gerade geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-169"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-170"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-170"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-171"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-171"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-172"><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3f6de-172"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-173"><em>ulungenutzt</em>: <strong>null</strong> , wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-173"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-174">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="3f6de-174">JET_cbtypBeforeDelete</span></span><br />
<span data-ttu-id="3f6de-175">0x00000020</span><span class="sxs-lookup"><span data-stu-id="3f6de-175">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="3f6de-176">Dieser Rückruf tritt auf, kurz bevor ein vorhandener Datensatz in einer Tabelle durch einen <a href="gg269315(v=exchg.10).md">jetdelete</a>-Rückruf gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-176">This callback will occur just before an existing record in a table is deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span></span></p>
<p><span data-ttu-id="3f6de-177">Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-177">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="3f6de-178">Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-178">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-179">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-179">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-180"><em>gsid</em>: die Sitzung, die den Datensatz enthält, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6de-180"><em>sesid</em>: The session that has the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-181"><em>DBID</em>: die Datenbank-ID der Tabelle, die den zu löschenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-181"><em>dbid</em>: The database ID of the table that contains the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-182"><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der mit dem zu löschenden Datensatz verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-182"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-183"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-183"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-184"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-184"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-185"><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3f6de-185"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-186"><em>ulungenutzt</em>: <strong>null</strong> wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</span><span class="sxs-lookup"><span data-stu-id="3f6de-186"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-187">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="3f6de-187">JET_cbtypAfterDelete</span></span><br />
<span data-ttu-id="3f6de-188">0x00000040</span><span class="sxs-lookup"><span data-stu-id="3f6de-188">0x00000040</span></span></p></td>
<td><p><span data-ttu-id="3f6de-189">Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von <a href="gg269315(v=exchg.10).md">jetdelete</a> gelöscht wurde, aber bevor <a href="gg269315(v=exchg.10).md">jetdelete</a> an seinen Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-189">This callback will occur just after an existing record in a table has been deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a> but before <a href="gg269315(v=exchg.10).md">JetDelete</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="3f6de-190">Der Funktionszeiger für diesen Rückruf Grund wird entweder mithilfe von <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben oder mithilfe von <a href="gg269175(v=exchg.10).md">jetregistercallback</a>zur Laufzeit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-190">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="3f6de-191">Weitere Informationen finden Sie unter <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269175(v=exchg.10).md">jetregistercallback</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-191">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-192">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-192">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-193"><em>ssisid</em>: die Sitzung, die den soeben gelöschten Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-193"><em>sesid</em>: The session that has the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-194"><em>DBID</em>: die Datenbank-ID der Tabelle, die den soeben gelöschten Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-194"><em>dbid</em>: The database ID of the table that contains the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-195"><em>TableID</em>: ein Cursor, der auf einem Index Eintrag positioniert ist, der mit dem soeben gelöschten Datensatz verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3f6de-195"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-196"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-196"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-197"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-197"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-198"><em>pvcontext</em>: der an <a href="gg269175(v=exchg.10).md">jetregistercallback</a> oder <strong>null</strong>übergebenen Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3f6de-198"><em>pvContext</em>: the context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-199"><em>ulungenutzt</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-199"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="3f6de-200">Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-200">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-201">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="3f6de-201">JET_cbtypUserDefinedDefaultValue</span></span><br />
<span data-ttu-id="3f6de-202">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3f6de-202">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="3f6de-203">Dieser Rückruf tritt auf, wenn die Engine den benutzerdefinierten Standardwert einer Spalte aus der Anwendung abrufen muss.</span><span class="sxs-lookup"><span data-stu-id="3f6de-203">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="3f6de-204">Bei diesem Rückruf handelt es sich im Wesentlichen um eine eingeschränkte Implementierung von <a href="gg269198(v=exchg.10).md">jetretrievecolumgen</a> , die von der Anwendung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-204">This callback is essentially a limited implementation of <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> that is evaluated by the application.</span></span> <span data-ttu-id="3f6de-205">Für einen benutzerdefinierten Standardwert können maximal ein Spaltenwert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f6de-205">A maximum of one column value can be returned for a user defined default value.</span></span></p>
<p><span data-ttu-id="3f6de-206">Der Funktionszeiger für diesen Rückruf Grund wird entweder über eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur an <a href="gg294122(v=exchg.10).md">jetaddcolumn</a> übergeben oder mithilfe einer <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur in einer <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur in einer <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> Struktur an <a href="gg269343(v=exchg.10).md">jetkreatetablecolumnindex</a> übergeben.</span><span class="sxs-lookup"><span data-stu-id="3f6de-206">The function pointer for this callback reason is either passed to <a href="gg294122(v=exchg.10).md">JetAddColumn</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure or passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure in a <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure in a <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure.</span></span></p>
<p><span data-ttu-id="3f6de-207">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-207">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-208"><em>SSID</em>: die Sitzung, von der der benutzerdefinierte Standardwert berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-208"><em>sesid</em>: The session that is computing the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="3f6de-209"><em>DBID</em>: die Datenbank-ID der Tabelle, die den benutzerdefinierten Standardwert enthält.</span><span class="sxs-lookup"><span data-stu-id="3f6de-209"><em>dbid</em>: The database ID of the table that contains the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="3f6de-210"><em>TableID</em>: ein Cursor, der auf dem Datensatz positioniert ist, für den der benutzerdefinierte Standardwert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-210"><em>tableid</em>: A cursor positioned on the record for which the user defined default value is being retrieved</span></span></p></li>
<li><p><span data-ttu-id="3f6de-211"><em>pvArg1</em>: der Ausgabepuffer für den benutzerdefinierten Standardwert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-211"><em>pvArg1</em>: The output buffer for the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="3f6de-212"><em>pvArg2</em>: bei Eingabe ist dies die Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="3f6de-212"><em>pvArg2</em>: On input, this is the size of the output buffer.</span></span> <span data-ttu-id="3f6de-213">Bei der Ausgabe ist dies die tatsächliche Größe des benutzerdefinierten Standardwerts.</span><span class="sxs-lookup"><span data-stu-id="3f6de-213">On output, this is the actual size of the user defined default value.</span></span> <span data-ttu-id="3f6de-214">in beiden Fällen ist die Größe eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="3f6de-214">in either case, the size is a 32-bit unsigned integer.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-215"><em>pvcontext</em>: ein Zeiger auf einen Puffer, der die Benutzerdaten enthält, die in der <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur beim Erstellen der Spalte angegeben wurden, oder NULL, wenn kein Kontext angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-215"><em>pvContext</em>: A pointer to a buffer containing the user data specified in the <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure when the column was created or NULL if no context was provided.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-216"><em>ulungenutzt</em>: die Spalten-ID der Spalte, für die der benutzerdefinierte Standardwert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-216"><em>ulUnused</em>: The column ID of the column for which the user defined default value is being retrieved.</span></span></p></li>
</ul>
<p><span data-ttu-id="3f6de-217">Wenn vom Rückruf ein Fehler zurückgegeben wird, schlägt der Vorgang fehl, der den Rückruf verursacht.</span><span class="sxs-lookup"><span data-stu-id="3f6de-217">If an error is returned by the callback then the operation originating the callback will fail with that error.</span></span></p>
<p><span data-ttu-id="3f6de-218">Wenn JET_wrnBufferTruncated durch den Rückruf zurückgegeben wird, wird der Vorgang fortgesetzt, aber der gesamte Wert wird während des Rückrufs nicht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f6de-218">If JET_wrnBufferTruncated is returned by the callback, the operation will continue, but the entire value is not retrieved during the callback.</span></span></p>
<p><span data-ttu-id="3f6de-219">Wenn JET_wrnColumnNull durch den Rückruf zurückgegeben wird, wird der Vorgang fortgesetzt, aber der benutzerdefinierte Standardwert für die Spalte ist NULL.</span><span class="sxs-lookup"><span data-stu-id="3f6de-219">If JET_wrnColumnNull is returned by the callback, the operation will continue, but the user defined default value for the column is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-220">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="3f6de-220">JET_cbtypOnlineDefragCompleted</span></span><br />
<span data-ttu-id="3f6de-221">0x00000100</span><span class="sxs-lookup"><span data-stu-id="3f6de-221">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="3f6de-222">Dieser Rückruf tritt auf, wenn die Online Defragmentierung einer Datenbank, die von <a href="gg269317(v=exchg.10).md">jetdefragment</a> initiiert wurde, beendet wurde, weil entweder der Prozess abgeschlossen oder das Zeitlimit erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-222">This callback will occur when the online defragmentation of a database as initiated by <a href="gg269317(v=exchg.10).md">JetDefragment</a> has stopped due to either the process being completed or the time limit being reached.</span></span></p>
<p><span data-ttu-id="3f6de-223">Der Funktionszeiger für diesen Rückruf Grund wird an <a href="gg269317(v=exchg.10).md">jetdebug-Fragment</a>übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3f6de-223">The function pointer for this callback reason is passed to <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span> <span data-ttu-id="3f6de-224">Weitere Informationen finden Sie unter <a href="gg269317(v=exchg.10).md">jetdefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-224">For more information, see <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span></p>
<p><span data-ttu-id="3f6de-225">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-225">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-226"><em>gsid</em>: die Sitzung, mit der die Online Defragmentierung für die Datenbank oder JET_sesidNil für eine Streamingdatei durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-226"><em>sesid</em>: The session used to perform online defragmentation for the database or JET_sesidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-227"><em>DBID</em>: die Datenbank-ID der Datenbank, die defragmentiert oder für eine Streamingdatei JET_dbidNil.</span><span class="sxs-lookup"><span data-stu-id="3f6de-227"><em>dbid</em>: The database ID of the database being defragmented or JET_dbidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-228"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-228"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-229"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-229"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-230"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-230"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-231"><em>pvcontext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-231"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-232"><em>ulungenutzt</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-232"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="3f6de-233">Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-233">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-234">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="3f6de-234">JET_cbtypFreeCursorLS</span></span><br />
<span data-ttu-id="3f6de-235">0x00000200</span><span class="sxs-lookup"><span data-stu-id="3f6de-235">0x00000200</span></span></p></td>
<td><p><span data-ttu-id="3f6de-236">Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einem Cursor zugeordnet ist, der von der Datenbank-Engine freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-236">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="3f6de-237">Weitere Informationen finden Sie unter <a href="gg269243(v=exchg.10).md">jetsetls</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-237">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="3f6de-238">Der Funktionszeiger für diesen Rückruf Grund wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-238">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-239">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-239">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-240">- <em>sid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-240"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-241"><em>DBID</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-241"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-242"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-242"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-243"><em>pvArg1</em>: das mit <a href="gg269243(v=exchg.10).md">jetsetls</a> festgelegte Kontext Handle</span><span class="sxs-lookup"><span data-stu-id="3f6de-243"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a></span></span></p></li>
<li><p><span data-ttu-id="3f6de-244"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-244"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-245"><em>pvcontext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-245"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-246"><em>ulungenutzt</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-246"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="3f6de-247">Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-247">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-248">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="3f6de-248">JET_cbtypFreeTableLS</span></span><br />
<span data-ttu-id="3f6de-249">0x00000400</span><span class="sxs-lookup"><span data-stu-id="3f6de-249">0x00000400</span></span></p></td>
<td><p><span data-ttu-id="3f6de-250">Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einer Tabelle zugeordnet ist, die von der Datenbank-Engine freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f6de-250">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="3f6de-251">Weitere Informationen finden Sie unter <a href="gg269243(v=exchg.10).md">jetsetls</a>.</span><span class="sxs-lookup"><span data-stu-id="3f6de-251">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="3f6de-252">Der Funktionszeiger für diesen Rückruf Grund wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-252">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="3f6de-253">Die Rückruf Parameter verfügen über die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3f6de-253">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f6de-254">- <em>sid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-254"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-255"><em>DBID</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-255"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-256"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="3f6de-256"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="3f6de-257"><em>pvArg1</em>: das Kontext Handle, das mithilfe von <a href="gg269243(v=exchg.10).md">jetsetls</a>festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6de-257"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p></li>
<li><p><span data-ttu-id="3f6de-258"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-258"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-259"><em>pvcontext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-259"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="3f6de-260"><em>ulungenutzt</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-260"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="3f6de-261">Wenn vom Rückruf ein Fehler zurückgegeben wird, wird er ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-261">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="3f6de-262">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f6de-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3f6de-264">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f6de-264">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f6de-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3f6de-266">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f6de-266">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f6de-267"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3f6de-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3f6de-268">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3f6de-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3f6de-269">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f6de-269">See Also</span></span>

[<span data-ttu-id="3f6de-270">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="3f6de-270">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)
