---
description: 'Weitere Informationen finden Sie hier: JET_cbtyp-Enumeration'
title: JET_cbtyp-Enumeration
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356822"
---
# <a name="jet_cbtyp-enumeration"></a><span data-ttu-id="d41e7-103">JET_cbtyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d41e7-103">JET_cbtyp enumeration</span></span>

<span data-ttu-id="d41e7-104">Der Typ des Status, der gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-104">Type of progress being reported.</span></span>

<span data-ttu-id="d41e7-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="d41e7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d41e7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d41e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d41e7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d41e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d41e7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d41e7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
```

## <a name="members"></a><span data-ttu-id="d41e7-109">Member</span><span class="sxs-lookup"><span data-stu-id="d41e7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d41e7-110">Membername</span><span class="sxs-lookup"><span data-stu-id="d41e7-110">Member name</span></span></th>
<th><span data-ttu-id="d41e7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d41e7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d41e7-112">Null</span><span class="sxs-lookup"><span data-stu-id="d41e7-112">Null</span></span></td>
<td><span data-ttu-id="d41e7-113">Dieser Rückruf ist reserviert und wird immer als ungültig angesehen.</span><span class="sxs-lookup"><span data-stu-id="d41e7-113">This callback is reserved and always considered invalid.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d41e7-114">Abschließen</span><span class="sxs-lookup"><span data-stu-id="d41e7-114">Finalize</span></span></td>
<td><span data-ttu-id="d41e7-115">Eine finalisierbare Spalte ist auf 0 (null) übergegangen.</span><span class="sxs-lookup"><span data-stu-id="d41e7-115">A finalizable column has gone to zero.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d41e7-116">Beforeingesert</span><span class="sxs-lookup"><span data-stu-id="d41e7-116">BeforeInsert</span></span></td>
<td><span data-ttu-id="d41e7-117">Dieser Rückruf tritt direkt vor dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen jetupdate-Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="d41e7-117">This callback will occur just before a new record is inserted into a table by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d41e7-118">AfterInsert</span><span class="sxs-lookup"><span data-stu-id="d41e7-118">AfterInsert</span></span></td>
<td><span data-ttu-id="d41e7-119">Dieser Rückruf tritt unmittelbar nach dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen jetupdate-Rückruf auf, aber bevor jetupdate zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-119">This callback will occur just after a new record has been inserted into a table by a call to JetUpdate but before JetUpdate returns.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d41e7-120">Beforereplace</span><span class="sxs-lookup"><span data-stu-id="d41e7-120">BeforeReplace</span></span></td>
<td><span data-ttu-id="d41e7-121">Dieser Rückruf tritt direkt vor einem vorhandenen Datensatz in einer Tabelle auf, die durch einen jetupdate-Rückruf geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-121">This callback will occur just prior to an existing record in a table being changed by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d41e7-122">After replace</span><span class="sxs-lookup"><span data-stu-id="d41e7-122">AfterReplace</span></span></td>
<td><span data-ttu-id="d41e7-123">Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen jetupdate-Rückruf geändert wurde, jedoch bevor jetupdate zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-123">This callback will occur just after an existing record in a table has been changed by a call to JetUpdate but prior to JetUpdate returning.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d41e7-124">BeforeDelete</span><span class="sxs-lookup"><span data-stu-id="d41e7-124">BeforeDelete</span></span></td>
<td><span data-ttu-id="d41e7-125">Dieser Rückruf tritt auf, kurz bevor ein vorhandener Datensatz in einer Tabelle durch einen jetdelete-Rückruf gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-125">This callback will occur just before an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d41e7-126">AfterDelete</span><span class="sxs-lookup"><span data-stu-id="d41e7-126">AfterDelete</span></span></td>
<td><span data-ttu-id="d41e7-127">Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen-Befehl von jetdelete gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-127">This callback will occur just after an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d41e7-128">Userdefineddefaultvalue</span><span class="sxs-lookup"><span data-stu-id="d41e7-128">UserDefinedDefaultValue</span></span></td>
<td><span data-ttu-id="d41e7-129">Dieser Rückruf tritt auf, wenn die Engine den benutzerdefinierten Standardwert einer Spalte aus der Anwendung abrufen muss.</span><span class="sxs-lookup"><span data-stu-id="d41e7-129">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="d41e7-130">Bei diesem Rückruf handelt es sich im Wesentlichen um eine eingeschränkte Implementierung von jetretrievecolumgen, die von der Anwendung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-130">This callback is essentially a limited implementation of JetRetrieveColumn that is evaluated by the application.</span></span> <span data-ttu-id="d41e7-131">Für einen benutzerdefinierten Standardwert können maximal ein Spaltenwert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d41e7-131">A maximum of one column value can be returned for a user defined default value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d41e7-132">Onlinedefragabgeschlossen</span><span class="sxs-lookup"><span data-stu-id="d41e7-132">OnlineDefragCompleted</span></span></td>
<td><span data-ttu-id="d41e7-133">Dieser Rückruf tritt auf, wenn die Online Defragmentierung einer Datenbank, die von jetdefragment initiiert wurde, beendet wurde, weil entweder der Prozess abgeschlossen oder das Zeitlimit erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="d41e7-133">This callback will occur when the online defragmentation of a database as initiated by JetDefragment has stopped due to either the process being completed or the time limit being reached.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d41e7-134">Freecursorls</span><span class="sxs-lookup"><span data-stu-id="d41e7-134">FreeCursorLS</span></span></td>
<td><span data-ttu-id="d41e7-135">Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einem Cursor zugeordnet ist, der von der Datenbank-Engine freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-135">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="d41e7-136">Weitere Informationen finden Sie unter jetsetls.</span><span class="sxs-lookup"><span data-stu-id="d41e7-136">For more information, see JetSetLS.</span></span> <span data-ttu-id="d41e7-137">Der Delegat für diesen Rückruf Grund wird mithilfe von jetsetsystemparameter mit JET_paramRuntimeCallback konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d41e7-137">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d41e7-138">Freetablels</span><span class="sxs-lookup"><span data-stu-id="d41e7-138">FreeTableLS</span></span></td>
<td><span data-ttu-id="d41e7-139">Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einer Tabelle zugeordnet ist, die von der Datenbank-Engine freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d41e7-139">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="d41e7-140">Weitere Informationen finden Sie unter jetsetls.</span><span class="sxs-lookup"><span data-stu-id="d41e7-140">For more information, see JetSetLS.</span></span> <span data-ttu-id="d41e7-141">Der Delegat für diesen Rückruf Grund wird mithilfe von jetsetsystemparameter mit JET_paramRuntimeCallback konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d41e7-141">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d41e7-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d41e7-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d41e7-143">Referenz</span><span class="sxs-lookup"><span data-stu-id="d41e7-143">Reference</span></span>

[<span data-ttu-id="d41e7-144">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d41e7-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
