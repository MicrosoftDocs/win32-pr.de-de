---
description: Weitere Informationen finden Sie in der columndefgrbit-Enumeration.
title: Columndefgrbit-Enumeration
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356551"
---
# <a name="columndefgrbit-enumeration"></a><span data-ttu-id="39f4e-103">Columndefgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="39f4e-103">ColumndefGrbit enumeration</span></span>

<span data-ttu-id="39f4e-104">Optionen für die JET_COLUMNDEF Struktur.</span><span class="sxs-lookup"><span data-stu-id="39f4e-104">Options for the JET_COLUMNDEF structure.</span></span>

<span data-ttu-id="39f4e-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="39f4e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="39f4e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39f4e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39f4e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39f4e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39f4e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39f4e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
```

## <a name="members"></a><span data-ttu-id="39f4e-109">Member</span><span class="sxs-lookup"><span data-stu-id="39f4e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="39f4e-110">Membername</span><span class="sxs-lookup"><span data-stu-id="39f4e-110">Member name</span></span></th>
<th><span data-ttu-id="39f4e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39f4e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-112">Keine</span><span class="sxs-lookup"><span data-stu-id="39f4e-112">None</span></span></td>
<td><span data-ttu-id="39f4e-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="39f4e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="39f4e-114">Columnfixed</span><span class="sxs-lookup"><span data-stu-id="39f4e-114">ColumnFixed</span></span></td>
<td><span data-ttu-id="39f4e-115">Die Spalte wird korrigiert.</span><span class="sxs-lookup"><span data-stu-id="39f4e-115">The column will be fixed.</span></span> <span data-ttu-id="39f4e-116">Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-116">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="39f4e-117">Columnfixed kann nicht mit columntagged verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-117">ColumnFixed cannot be used with ColumnTagged.</span></span> <span data-ttu-id="39f4e-118">Dieses Bit kann nicht mit langen Werten verwendet werden (d. h. JET_coltyp. LONGTEXT und JET_coltyp. LONGBINARY).</span><span class="sxs-lookup"><span data-stu-id="39f4e-118">This bit cannot be used with long values (that is JET_coltyp.LongText and JET_coltyp.LongBinary).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-119">Columntagged</span><span class="sxs-lookup"><span data-stu-id="39f4e-119">ColumnTagged</span></span></td>
<td><span data-ttu-id="39f4e-120">Die Spalte wird gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="39f4e-120">The column will be tagged.</span></span> <span data-ttu-id="39f4e-121">Markierte Spalten beanspruchen keinen Speicherplatz in der Datenbank, wenn Sie keine Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="39f4e-121">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="39f4e-122">Dieses Bit kann nicht mit columnfixed verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-122">This bit cannot be used with ColumnFixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="39f4e-123">Columnnotnull</span><span class="sxs-lookup"><span data-stu-id="39f4e-123">ColumnNotNULL</span></span></td>
<td><span data-ttu-id="39f4e-124">Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-124">The column must never be set to a NULL value.</span></span> <span data-ttu-id="39f4e-125">Unter Windows XP kann dies nur auf fixierte Spalten (Bit, Byte, Integer usw.) angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-125">On Windows XP this can only be applied to fixed columns (bit, byte, integer, etc).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-126">Columnversion</span><span class="sxs-lookup"><span data-stu-id="39f4e-126">ColumnVersion</span></span></td>
<td><span data-ttu-id="39f4e-127">Die Spalte ist eine Versions Spalte, die die Version der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="39f4e-127">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="39f4e-128">Der Wert dieser Spalte beginnt bei Null und wird für jedes Update in der Zeile automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="39f4e-128">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span> <span data-ttu-id="39f4e-129">Diese Option kann nur auf JET_coltyp angewendet werden. Lange Spalten.</span><span class="sxs-lookup"><span data-stu-id="39f4e-129">This option can only be applied to JET_coltyp.Long columns.</span></span> <span data-ttu-id="39f4e-130">Diese Option kann nicht mit ' columnautoincrement ', ' columnescrowupdate ' oder ' columntagged ' verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-130">This option cannot be used with ColumnAutoincrement, ColumnEscrowUpdate, or ColumnTagged.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="39f4e-131">Columnautoincrement</span><span class="sxs-lookup"><span data-stu-id="39f4e-131">ColumnAutoincrement</span></span></td>
<td><span data-ttu-id="39f4e-132">Die Spalte wird automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="39f4e-132">The column will automatically be incremented.</span></span> <span data-ttu-id="39f4e-133">Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="39f4e-133">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="39f4e-134">Die Zahlen sind jedoch möglicherweise nicht kontinuierlich.</span><span class="sxs-lookup"><span data-stu-id="39f4e-134">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="39f4e-135">Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, &quot; kann die AutoIncrement- &quot; Spalte die Werte {1, 2, 6, 7, 8} enthalten.</span><span class="sxs-lookup"><span data-stu-id="39f4e-135">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="39f4e-136">Dieses Bit kann nur für Spalten vom Typ JET_coltyp verwendet werden. Long oder JET_coltyp. Währungs.</span><span class="sxs-lookup"><span data-stu-id="39f4e-136">This bit can only be used on columns of type JET_coltyp.Long or JET_coltyp.Currency.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-137">Columnmultiwertig</span><span class="sxs-lookup"><span data-stu-id="39f4e-137">ColumnMultiValued</span></span></td>
<td><span data-ttu-id="39f4e-138">Die Spalte kann mehr wertig sein.</span><span class="sxs-lookup"><span data-stu-id="39f4e-138">The column can be multi-valued.</span></span> <span data-ttu-id="39f4e-139">Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-139">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="39f4e-140">Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl gekennzeichnet, die als itagsequence-Member bezeichnet wird, der zu verschiedenen Strukturen gehört, einschließlich: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN und JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="39f4e-140">The various values in a multi-valued column are identified by a number called the itagSequence member, which belongs to various structures, including: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN, and JET_ENUMCOLUMNVALUE.</span></span> <span data-ttu-id="39f4e-141">Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie können keine Spalten fester Länge oder Spalten mit variabler Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39f4e-141">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="39f4e-142">Columnescrowupdate</span><span class="sxs-lookup"><span data-stu-id="39f4e-142">ColumnEscrowUpdate</span></span></td>
<td><span data-ttu-id="39f4e-143">Gibt an, dass eine Spalte eine Spalte für die hinterlegte Aktualisierung ist.</span><span class="sxs-lookup"><span data-stu-id="39f4e-143">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="39f4e-144">Eine Spalte für das Hinterlegungs Update kann gleichzeitig von verschiedenen Sitzungen mit jetescrowupdate aktualisiert werden und behält die Transaktions Konsistenz bei.</span><span class="sxs-lookup"><span data-stu-id="39f4e-144">An escrow update column can be updated concurrently by different sessions with JetEscrowUpdate and will maintain transactional consistency.</span></span> <span data-ttu-id="39f4e-145">Eine Spalte vom Datentyp "hinterlegter" muss auch die folgenden Bedingungen erfüllen: eine Spalte für das hinterlegter-Update kann nur erstellt werden, wenn die Tabelle leer ist.</span><span class="sxs-lookup"><span data-stu-id="39f4e-145">An escrow update column must also meet the following conditions: An escrow update column can be created only when the table is empty.</span></span> <span data-ttu-id="39f4e-146">Eine Spalte vom Typ "hinterlegter" muss vom Typ "JET_coltypLong" sein.</span><span class="sxs-lookup"><span data-stu-id="39f4e-146">An escrow update column must be of type JET_coltypLong.</span></span> <span data-ttu-id="39f4e-147">Eine Spalte für das hinterlegter-Update muss einen Standardwert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39f4e-147">An escrow update column must have a default value.</span></span> <span data-ttu-id="39f4e-148">JET_bitColumnEscrowUpdate kann nicht in Verbindung mit columntagged, columnversion oder columnautoincrement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-148">JET_bitColumnEscrowUpdate cannot be used in conjunction with ColumnTagged, ColumnVersion, or ColumnAutoincrement.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-149">Columnunversioniert</span><span class="sxs-lookup"><span data-stu-id="39f4e-149">ColumnUnversioned</span></span></td>
<td><span data-ttu-id="39f4e-150">Die Spalte wird in einem ohne Versionsinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="39f4e-150">The column will be created in an without version information.</span></span> <span data-ttu-id="39f4e-151">Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="39f4e-151">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="39f4e-152">Dieses Bit ist nur bei jetaddcolumn nützlich.</span><span class="sxs-lookup"><span data-stu-id="39f4e-152">This bit is only useful with JetAddColumn.</span></span> <span data-ttu-id="39f4e-153">Sie kann nicht innerhalb einer Transaktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f4e-153">It cannot be used within a transaction.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="39f4e-154">Columnmaybenull</span><span class="sxs-lookup"><span data-stu-id="39f4e-154">ColumnMaybeNull</span></span></td>
<td><span data-ttu-id="39f4e-155">Beim äußeren Join weist der Vorgang zum Abrufen von Spalten möglicherweise keine Entsprechung aus der inneren Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="39f4e-155">In doing an outer join, the retrieve column operation might not have a match from the inner table.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-156">Columnuserdefineddefault</span><span class="sxs-lookup"><span data-stu-id="39f4e-156">ColumnUserDefinedDefault</span></span></td>
<td><span data-ttu-id="39f4e-157">Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="39f4e-157">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="39f4e-158">Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein.</span><span class="sxs-lookup"><span data-stu-id="39f4e-158">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="39f4e-159">Das Angeben von JET_bitColumnUserDefinedDefault bedeutet, dass pvdefault auf eine JET_USERDEFINEDDEFAULT Struktur verweisen muss und cbdefault auf sizeof (JET_USERDEFINEDDEFAULT) festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="39f4e-159">Specifying JET_bitColumnUserDefinedDefault means that pvDefault must point to a JET_USERDEFINEDDEFAULT structure, and cbDefault must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="39f4e-160">Ttkey</span><span class="sxs-lookup"><span data-stu-id="39f4e-160">TTKey</span></span></td>
<td><span data-ttu-id="39f4e-161">Die Spalte ist eine Schlüssel Spalte für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39f4e-161">The column will be a key column for the temporary table.</span></span> <span data-ttu-id="39f4e-162">Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39f4e-162">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="39f4e-163">Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüssel Spalte usw.</span><span class="sxs-lookup"><span data-stu-id="39f4e-163">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="39f4e-164">Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</span><span class="sxs-lookup"><span data-stu-id="39f4e-164">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="39f4e-165">Absteigend</span><span class="sxs-lookup"><span data-stu-id="39f4e-165">TTDescending</span></span></td>
<td><span data-ttu-id="39f4e-166">Die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein.</span><span class="sxs-lookup"><span data-stu-id="39f4e-166">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="39f4e-167">Wenn diese Option ohne ttkey angegeben wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="39f4e-167">If this option is specified without TTKey then this option is ignored.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="39f4e-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39f4e-168">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39f4e-169">Referenz</span><span class="sxs-lookup"><span data-stu-id="39f4e-169">Reference</span></span>

[<span data-ttu-id="39f4e-170">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="39f4e-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="39f4e-171">Columncompressed</span><span class="sxs-lookup"><span data-stu-id="39f4e-171">ColumnCompressed</span></span>](./windows7grbits.columncompressed-field.md)
