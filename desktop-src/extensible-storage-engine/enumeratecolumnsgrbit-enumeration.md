---
description: 'Weitere Informationen finden Sie hier: enumeratecolumnsgrbit-Enumeration'
title: Enumeratecolumnsgrbit-Enumeration
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352353"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="8270c-103">Enumeratecolumnsgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8270c-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="8270c-104">Optionen für jetenreeratecolumschlag.</span><span class="sxs-lookup"><span data-stu-id="8270c-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="8270c-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="8270c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8270c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8270c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8270c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8270c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8270c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8270c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a><span data-ttu-id="8270c-109">Member</span><span class="sxs-lookup"><span data-stu-id="8270c-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8270c-110">Membername</span><span class="sxs-lookup"><span data-stu-id="8270c-110">Member name</span></span></th>
<th><span data-ttu-id="8270c-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8270c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8270c-112">Keine</span><span class="sxs-lookup"><span data-stu-id="8270c-112">None</span></span></td>
<td><span data-ttu-id="8270c-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="8270c-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8270c-114">Enumeratecompressoutput</span><span class="sxs-lookup"><span data-stu-id="8270c-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="8270c-115">Beim Aufzählen von Spaltenwerten können alle Spalten, für die wir alle Werte abrufen und nur einen nicht-NULL-Spaltenwert aufweisen, in einem komprimierten Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8270c-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="8270c-116">Der Status dieser Spalten wird auf <a href="hh557250(v=exchg.10).md">columnsinglevalue</a> festgelegt, und die Größe des Spaltenwerts und der Arbeitsspeicher, der den Spaltenwert enthält, werden direkt in der <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8270c-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="8270c-117">Es ist nicht sichergestellt, dass alle berechtigten Spalten auf diese Weise komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="8270c-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="8270c-118">Weitere Informationen finden Sie unter <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="8270c-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8270c-119">Enumeratecopy</span><span class="sxs-lookup"><span data-stu-id="8270c-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="8270c-120">Diese Option gibt an, dass die geänderten Spaltenwerte des Datensatzes anstelle der ursprünglichen Spaltenwerte aufgezählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8270c-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="8270c-121">Wenn ein Spaltenwert nicht geändert wurde, wird der ursprüngliche Spaltenwert aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8270c-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="8270c-122">Auf diese Weise kann ein Spaltenwert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="8270c-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="8270c-123">Diese Option ist mit " <a href="hh578120(v=exchg.10).md">retrievecopy</a>" identisch.</span><span class="sxs-lookup"><span data-stu-id="8270c-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8270c-124">Enumerateignoredefault</span><span class="sxs-lookup"><span data-stu-id="8270c-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="8270c-125">Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist, wird kein Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8270c-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="8270c-126">Normalerweise würde der Standardwert für die Spalte, sofern vorhanden, in diesem Fall zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8270c-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="8270c-127">Wenn die Spalte auf einen anderen Wert als den Standardwert festgelegt ist, wird ein anderer Wert zurückgegeben (d. h., wenn eine Spalte mit einem Standardwert explizit auf NULL festgelegt ist, wird ein NULL-Wert als Wert für diese Spalte zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="8270c-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="8270c-128">Auch wenn diese Option angefordert wird, ist es weiterhin möglich, einen Spaltenwert anzuzeigen, der dem Standardwert entspricht.</span><span class="sxs-lookup"><span data-stu-id="8270c-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="8270c-129">Es wird nicht versucht, Spaltenwerte zu entfernen, die ihren Standardwerten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8270c-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="8270c-130">Beachten Sie, dass sich diese Option auf die Ausgabe von <a href="dn292148(v=exchg.10).md">jetenumeratecolumns (JET_SESID JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)</a> auswirkt, wenn Sie mit enumeratepresenceonly oder enumeratetaggedonly verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8270c-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8270c-131">Enumeratepresenceonly</span><span class="sxs-lookup"><span data-stu-id="8270c-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="8270c-132">Wenn ein nicht-NULL-Wert für den angeforderten Spalten-oder Spaltenwert vorhanden ist, werden die zugehörigen Daten nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8270c-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="8270c-133">Stattdessen wird der zugehörige Status für diesen Spalten-oder Spaltenwert auf <a href="hh557250(v=exchg.10).md">columnpresent</a>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8270c-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="8270c-134">Wenn der Spalten-oder Spaltenwert NULL ist, wird <a href="hh557250(v=exchg.10).md">columnnull</a> wie gewohnt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8270c-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8270c-135">Enumeratetaggedonly</span><span class="sxs-lookup"><span data-stu-id="8270c-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="8270c-136">Wenn alle Spaltenwerte im Datensatz aufgelistet werden (z. b. wenn numcolumnids NULL ist), werden nur markierte Spaltenwerte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8270c-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="8270c-137">Diese Option ist beim Auflisten eines bestimmten Arrays von Spalten-IDs nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="8270c-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8270c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8270c-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8270c-139">Referenz</span><span class="sxs-lookup"><span data-stu-id="8270c-139">Reference</span></span>

[<span data-ttu-id="8270c-140">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8270c-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="8270c-141">Enumerateignoreuserdefineddefault</span><span class="sxs-lookup"><span data-stu-id="8270c-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="8270c-142">Enumerateingerecordonly</span><span class="sxs-lookup"><span data-stu-id="8270c-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
