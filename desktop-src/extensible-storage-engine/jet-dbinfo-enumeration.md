---
description: 'Weitere Informationen finden Sie hier: JET_DbInfo-Enumeration'
title: JET_DbInfo-Enumeration
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347161"
---
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="71dbe-103">JET_DbInfo-Enumeration</span><span class="sxs-lookup"><span data-stu-id="71dbe-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="71dbe-104">Info Ebenen zum Abrufen von Datenbankinformationen.</span><span class="sxs-lookup"><span data-stu-id="71dbe-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="71dbe-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71dbe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71dbe-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71dbe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71dbe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="71dbe-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="71dbe-108">Member</span><span class="sxs-lookup"><span data-stu-id="71dbe-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="71dbe-109">Membername</span><span class="sxs-lookup"><span data-stu-id="71dbe-109">Member name</span></span></th>
<th><span data-ttu-id="71dbe-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71dbe-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71dbe-111">Dateiname</span><span class="sxs-lookup"><span data-stu-id="71dbe-111">Filename</span></span></td>
<td><span data-ttu-id="71dbe-112">Gibt den Pfad zur Datenbankdatei (Zeichenfolge) zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71dbe-113">LCID</span><span class="sxs-lookup"><span data-stu-id="71dbe-113">LCID</span></span></td>
<td><span data-ttu-id="71dbe-114">Gibt den Gebiets Schema Bezeichner (LCID) zurück, der dieser Datenbank zugeordnet ist (Int32).</span><span class="sxs-lookup"><span data-stu-id="71dbe-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71dbe-115">Optionen</span><span class="sxs-lookup"><span data-stu-id="71dbe-115">Options</span></span></td>
<td><span data-ttu-id="71dbe-116">Gibt ein <a href="hh579532(v=exchg.10).md">opendatabasegrbit</a>zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="71dbe-117">Gibt an, ob die Datenbank im exklusiven Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="71dbe-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="71dbe-118">Wenn sich die Datenbank im exklusiven Modus befindet, wird <a href="hh579532(v=exchg.10).md">exklusiv</a> zurückgegeben, andernfalls wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71dbe-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="71dbe-119">Andere Datenbank-grbit-Optionen für jetattachdatabase und jetopendatabase werden nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71dbe-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71dbe-120">Transaktionen</span><span class="sxs-lookup"><span data-stu-id="71dbe-120">Transactions</span></span></td>
<td><span data-ttu-id="71dbe-121">Gibt eine Zahl zurück, die größer ist als die maximale Ebene, auf die Transaktionen eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="71dbe-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="71dbe-122">Wenn <a href="dn292105(v=exchg.10).md">jetbegintransaction (JET_SESID)</a> so oft wie dieser Wert in der gleichen Sitzung (in derselben Sitzung, ohne Commit oder Rollback) aufgerufen wird, wird für den letzten Aufruf <a href="hh564840(v=exchg.10).md">transtoodeep</a> (Int32) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71dbe-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71dbe-123">Version</span><span class="sxs-lookup"><span data-stu-id="71dbe-123">Version</span></span></td>
<td><span data-ttu-id="71dbe-124">Gibt die Hauptversion der Datenbank-Engine (Int32) zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71dbe-125">Dateigröße</span><span class="sxs-lookup"><span data-stu-id="71dbe-125">Filesize</span></span></td>
<td><span data-ttu-id="71dbe-126">Gibt die Dateigröße der Datenbank in Seiten (Int32) zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71dbe-127">Leerraum</span><span class="sxs-lookup"><span data-stu-id="71dbe-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="71dbe-128">Gibt den eigenen Bereich der Datenbank in Seiten (Int32) zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71dbe-129">Leerraum verfügbar</span><span class="sxs-lookup"><span data-stu-id="71dbe-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="71dbe-130">Gibt den verfügbaren Speicherplatz in der Datenbank auf Seiten (Int32) zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71dbe-131">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="71dbe-131">Misc</span></span></td>
<td><span data-ttu-id="71dbe-132">Gibt ein <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71dbe-133">Dbinuse</span><span class="sxs-lookup"><span data-stu-id="71dbe-133">DBInUse</span></span></td>
<td><span data-ttu-id="71dbe-134">Gibt einen booleschen Wert zurück, der angibt, ob die Datenbank angefügt ist (boolesch).</span><span class="sxs-lookup"><span data-stu-id="71dbe-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71dbe-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="71dbe-135">PageSize</span></span></td>
<td><span data-ttu-id="71dbe-136">Gibt die Seitengröße der Datenbank zurück (Int32).</span><span class="sxs-lookup"><span data-stu-id="71dbe-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71dbe-137">FileType</span><span class="sxs-lookup"><span data-stu-id="71dbe-137">FileType</span></span></td>
<td><span data-ttu-id="71dbe-138">Gibt den Typ der Datenbank (<a href="hh566739(v=exchg.10).md">JET_filetype</a>) zurück.</span><span class="sxs-lookup"><span data-stu-id="71dbe-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="71dbe-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71dbe-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71dbe-140">Referenz</span><span class="sxs-lookup"><span data-stu-id="71dbe-140">Reference</span></span>

[<span data-ttu-id="71dbe-141">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="71dbe-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
