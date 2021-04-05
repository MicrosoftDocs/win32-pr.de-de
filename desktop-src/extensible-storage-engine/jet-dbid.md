---
description: 'Weitere Informationen finden Sie hier: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751376"
---
# <a name="jet_dbid"></a><span data-ttu-id="6fa2c-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6fa2c-103">JET_DBID</span></span>


<span data-ttu-id="6fa2c-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6fa2c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="6fa2c-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6fa2c-105">JET_DBID</span></span>

<span data-ttu-id="6fa2c-106">Der **JET_DBID** -Datentyp enthält das Handle für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="6fa2c-107">Ein Daten Bank Handle wird zum Verwalten des Schemas einer Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="6fa2c-108">Sie kann auch verwendet werden, um die Tabellen in der Datenbank zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="6fa2c-109">Datentypen</span><span class="sxs-lookup"><span data-stu-id="6fa2c-109">Data Types</span></span>

<span data-ttu-id="6fa2c-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6fa2c-110">JET_DBID</span></span>

<span data-ttu-id="6fa2c-111">Handle für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-111">Handle to the database.</span></span>

<span data-ttu-id="6fa2c-112">Der Wert JET_dbidNil gibt an, dass das Handle ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6fa2c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fa2c-113">Remarks</span></span>

<span data-ttu-id="6fa2c-114">Ein Daten Bank Handle wird durch einen Aufrufen von [jetkreatedatabase](./jetcreatedatabase-function.md) oder [jetopd](./jetopendatabase-function.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="6fa2c-115">Ein Daten Bank Handle kann von [jetclosedatabase](./jetclosedatabase-function.md) explizit geschlossen oder durch [jetendsession](./jetendsession-function.md) oder [jetterm](./jetterm-function.md)implizit geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="6fa2c-116">Ein Daten Bank Handle kann nur innerhalb der Sitzung verwendet werden, in der es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="6fa2c-117">Das vorhanden sein eines Daten Bank Handles entspricht dem logischen Öffnen einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="6fa2c-118">Ein logisches Open unterscheidet sich vom physischen Öffnen einer Datenbank. Dies geschieht, wenn eine Datenbank mit dem System verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="6fa2c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fa2c-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fa2c-120"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6fa2c-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa2c-121">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fa2c-122"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6fa2c-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa2c-123">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fa2c-124"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6fa2c-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6fa2c-125">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6fa2c-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6fa2c-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6fa2c-126">See Also</span></span>

[<span data-ttu-id="6fa2c-127">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="6fa2c-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="6fa2c-128">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="6fa2c-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="6fa2c-129">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="6fa2c-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="6fa2c-130">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="6fa2c-130">JetEndSession</span></span>](./jetendsession-function.md)
