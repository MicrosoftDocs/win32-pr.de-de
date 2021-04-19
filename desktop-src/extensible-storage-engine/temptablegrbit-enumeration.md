---
description: Weitere Informationen finden Sie in der temptablegrbit-Enumeration.
title: Temptablegrbit-Enumeration
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372811"
---
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="b5448-103">Temptablegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b5448-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="b5448-104">Optionen für die Erstellung temporärer Tabellen.</span><span class="sxs-lookup"><span data-stu-id="b5448-104">Options for temporary table creation.</span></span>

<span data-ttu-id="b5448-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="b5448-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b5448-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5448-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5448-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5448-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5448-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5448-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
```

## <a name="members"></a><span data-ttu-id="b5448-109">Member</span><span class="sxs-lookup"><span data-stu-id="b5448-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b5448-110">Membername</span><span class="sxs-lookup"><span data-stu-id="b5448-110">Member name</span></span></th>
<th><span data-ttu-id="b5448-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5448-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b5448-112">Keine</span><span class="sxs-lookup"><span data-stu-id="b5448-112">None</span></span></td>
<td><span data-ttu-id="b5448-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="b5448-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b5448-114">Zierenden</span><span class="sxs-lookup"><span data-stu-id="b5448-114">Indexed</span></span></td>
<td><span data-ttu-id="b5448-115">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von JetSeek für die Suche nach Datensätzen nach Index Schlüssel zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="b5448-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="b5448-116">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="b5448-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="b5448-117">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="b5448-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b5448-118">Eindeutig</span><span class="sxs-lookup"><span data-stu-id="b5448-118">Unique</span></span></td>
<td><span data-ttu-id="b5448-119">Mit dieser Option wird angefordert, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b5448-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="b5448-120">Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="b5448-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="b5448-121">Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die Option <a href="dn351284(v=exchg.10).md">ForwardOnly</a> ebenfalls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b5448-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="b5448-122">Es ist nicht möglich zu wissen, welches Duplikat gewinnt und welche Duplikate im allgemeinen verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="b5448-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="b5448-123">Wenn jedoch die errorondupli-sertion-Option angefordert wird, gewinnt der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5448-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b5448-124">Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="b5448-124">Updatable</span></span></td>
<td><span data-ttu-id="b5448-125">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b5448-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="b5448-126">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="b5448-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="b5448-127">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="b5448-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b5448-128">Bildlauffähigkeit</span><span class="sxs-lookup"><span data-stu-id="b5448-128">Scrollable</span></span></td>
<td><span data-ttu-id="b5448-129">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="dn292217(v=exchg.10).md">jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)</a>zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5448-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="b5448-130">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="b5448-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="b5448-131">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="b5448-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b5448-132">Sortnullshigh</span><span class="sxs-lookup"><span data-stu-id="b5448-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="b5448-133">Mit dieser Option wird angefordert, dass NULL-Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="b5448-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b5448-134">Forcematerialisierung</span><span class="sxs-lookup"><span data-stu-id="b5448-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="b5448-135">Diese Option zwingt den temporären Tabellen-Manager dazu, einen Versuch zu verwerfen, eine clever-Strategie zum Verwalten der temporären Tabelle zu wählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="b5448-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b5448-136">Erroronduplialisieinsertion</span><span class="sxs-lookup"><span data-stu-id="b5448-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="b5448-137">Mit dieser Option wird angefordert, dass jeder Versuch, einen Datensatz mit demselben Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, sofort mit <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b5448-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="b5448-138">Wenn diese Option nicht angefordert wird, wird möglicherweise sofort ein Duplikat erkannt, oder es kann zu einem späteren Zeitpunkt in Abhängigkeit von der Strategie, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde, ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="b5448-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="b5448-139">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="b5448-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="b5448-140">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="b5448-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b5448-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5448-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5448-142">Referenz</span><span class="sxs-lookup"><span data-stu-id="b5448-142">Reference</span></span>

[<span data-ttu-id="b5448-143">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5448-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="b5448-144">Nur Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="b5448-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="b5448-145">Intrinsies clvsonly</span><span class="sxs-lookup"><span data-stu-id="b5448-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)
