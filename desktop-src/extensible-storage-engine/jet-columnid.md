---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861963"
---
# <a name="jet_columnid"></a><span data-ttu-id="97c6c-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="97c6c-103">JET_COLUMNID</span></span>


<span data-ttu-id="97c6c-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="97c6c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="97c6c-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="97c6c-105">JET_COLUMNID</span></span>

<span data-ttu-id="97c6c-106">Der **JET_COLUMNID** -Datentyp identifiziert eine Spalte in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="97c6c-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="97c6c-107">Datentypen</span><span class="sxs-lookup"><span data-stu-id="97c6c-107">Data Types</span></span>

<span data-ttu-id="97c6c-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="97c6c-108">JET_COLUMNID</span></span>

<span data-ttu-id="97c6c-109">Identifiziert eine Spalte in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="97c6c-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="97c6c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97c6c-110">Remarks</span></span>

<span data-ttu-id="97c6c-111">Spalten-IDs sind innerhalb einer einzelnen Tabelle eindeutig.</span><span class="sxs-lookup"><span data-stu-id="97c6c-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="97c6c-112">Wenn eine Spalte bekanntermaßen über eine bestimmte Spalten-ID verfügt, weist Sie immer diese Spalten-ID auf.</span><span class="sxs-lookup"><span data-stu-id="97c6c-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="97c6c-113">Durch die Wiederherstellung aus einer Sicherung wird der Wert einer Spalten-ID nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="97c6c-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="97c6c-114">Wenn jedoch eine oder mehrere Tabellen Spalten, vor einer bestimmten Tabellenspalte, gelöscht werden, kann eine Compact-Datenbank den Wert einer Spalten-ID ändern.</span><span class="sxs-lookup"><span data-stu-id="97c6c-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="97c6c-115">In einigen Fällen sind Spalten-IDs die einzige Möglichkeit zum Identifizieren von Spalten.</span><span class="sxs-lookup"><span data-stu-id="97c6c-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="97c6c-116">Wenn eine temporäre Tabelle erstellt wird, haben die Spalten keine Namen, aber ein Array von Spalten-IDs wird von der Create-Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97c6c-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="97c6c-117">Spalten in verschiedenen Tabellen können dieselbe Spalten-ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="97c6c-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="97c6c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97c6c-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97c6c-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="97c6c-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="97c6c-120">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="97c6c-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c6c-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="97c6c-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="97c6c-122">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="97c6c-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c6c-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="97c6c-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="97c6c-124">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="97c6c-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

