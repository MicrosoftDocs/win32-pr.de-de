---
description: 'Weitere Informationen finden Sie hier: JetOpenTempTable3-Funktion'
title: JetOpenTempTable3-Funktion
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346482"
---
# <a name="jetopentemptable3-function"></a><span data-ttu-id="a75e9-103">JetOpenTempTable3-Funktion</span><span class="sxs-lookup"><span data-stu-id="a75e9-103">JetOpenTempTable3 Function</span></span>


<span data-ttu-id="a75e9-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a75e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable3-function"></a><span data-ttu-id="a75e9-105">JetOpenTempTable3-Funktion</span><span class="sxs-lookup"><span data-stu-id="a75e9-105">JetOpenTempTable3 Function</span></span>

<span data-ttu-id="a75e9-106">Die **JetOpenTempTable3** -Funktion erstellt eine temporäre Tabelle mit einem einzelnen Index, der zum Speichern und Abrufen von Datensätzen verwendet werden kann, wie eine gewöhnliche Tabelle, die mit [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a75e9-106">The **JetOpenTempTable3** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="a75e9-107">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-107">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a75e9-108">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a75e9-108">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="a75e9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a75e9-109">Parameters</span></span>

<span data-ttu-id="a75e9-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="a75e9-110">*sesid*</span></span>

<span data-ttu-id="a75e9-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a75e9-111">The session to use for this call.</span></span>

<span data-ttu-id="a75e9-112">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="a75e9-112">*prgcolumndef*</span></span>

<span data-ttu-id="a75e9-113">Identifiziert die Spaltendefinitionen der Spalten, die in der temporären Tabelle erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-113">Identifies the column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="a75e9-114">Wichtige Einschränkungen gelten für die Spalten Definitions Optionen, die bei einer temporären Tabelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a75e9-114">Important limitations exist to the column definition options that may be used with a temporary table.</span></span> <span data-ttu-id="a75e9-115">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="a75e9-115">See the Remarks section for more information.</span></span>

<span data-ttu-id="a75e9-116">Zusätzlich zu den üblichen Spalten Definitions Optionen können auch NULL oder mehr der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.</span><span class="sxs-lookup"><span data-stu-id="a75e9-116">In addition to the usual column definition options, zero or more of the following options may also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a75e9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a75e9-117">Value</span></span></p></th>
<th><p><span data-ttu-id="a75e9-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a75e9-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-119">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="a75e9-119">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="a75e9-120">Diese Option gibt an, dass die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle absteigend und nicht aufsteigend sein soll.</span><span class="sxs-lookup"><span data-stu-id="a75e9-120">This option indicates that the sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="a75e9-121">Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-121">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-122">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="a75e9-122">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="a75e9-123">Diese Option gibt an, dass es sich bei der Spalte um eine Schlüssel Spalte für die temporäre Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-123">This option indicates that the column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="a75e9-124">Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a75e9-124">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="a75e9-125">Die erste Spaltendefinition im Array, bei der dieser Options Satz verwendet wird, ist die wichtigste Schlüssel Spalte usw.</span><span class="sxs-lookup"><span data-stu-id="a75e9-125">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="a75e9-126">Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-126">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a75e9-127">*CColumn*</span><span class="sxs-lookup"><span data-stu-id="a75e9-127">*ccolumn*</span></span>

<span data-ttu-id="a75e9-128">Siehe *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="a75e9-128">See *prgcolumndef*.</span></span>

<span data-ttu-id="a75e9-129">*pidxunicode*</span><span class="sxs-lookup"><span data-stu-id="a75e9-129">*pidxunicode*</span></span>

<span data-ttu-id="a75e9-130">Die Gebiets Schema-ID und die normalisierungs Flags, die verwendet werden, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-130">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="a75e9-131">Wenn dieser Parameter nicht vorhanden ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-131">When this parameter is not present then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="a75e9-132">Die Standard-LCID ist das US-englische Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="a75e9-132">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="a75e9-133">Wenn dieser Parameter nicht vorhanden ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-133">When this parameter is not present then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="a75e9-134">Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="a75e9-134">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="a75e9-135">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a75e9-135">*grbit*</span></span>

<span data-ttu-id="a75e9-136">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="a75e9-136">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a75e9-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a75e9-137">Value</span></span></p></th>
<th><p><span data-ttu-id="a75e9-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a75e9-138">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-139">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="a75e9-139">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="a75e9-140">Mit dieser Option wird angefordert, dass jeder Versuch, einen Datensatz mit demselben Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, sofort mit JET_errKeyDuplicate fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-140">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="a75e9-141">Wenn diese Option nicht angefordert wird, wird möglicherweise sofort ein Duplikat erkannt, oder es kann zu einem späteren Zeitpunkt in Abhängigkeit von der Strategie, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde, ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="a75e9-141">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="a75e9-142">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a75e9-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="a75e9-143">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-144">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="a75e9-144">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="a75e9-145">Diese Option zwingt den temporären Tabellen-Manager dazu, einen Versuch zu verwerfen, eine clever-Strategie zum Verwalten der temporären Tabelle zu wählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-145">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-146">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="a75e9-146">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="a75e9-147">Mit dieser Option wird angefordert, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für zwischen Abfrageergebnisse optimierte-Implementierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="a75e9-147">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="a75e9-148">Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</span><span class="sxs-lookup"><span data-stu-id="a75e9-148">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="a75e9-149">Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="a75e9-149">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="a75e9-150">Weitere Informationen finden Sie unter JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="a75e9-150">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="a75e9-151">Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a75e9-151">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-152">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="a75e9-152">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="a75e9-153">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> für die Suche nach Datensätzen nach Index Schlüssel zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-153">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="a75e9-154">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a75e9-154">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="a75e9-155">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-155">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-156">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="a75e9-156">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="a75e9-157">Mit dieser Option wird angefordert, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-157">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="a75e9-158">Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-158">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="a75e9-159">Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die JET_bitTTForwardOnly-Option ebenfalls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a75e9-159">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="a75e9-160">Es ist nicht möglich zu wissen, welches Duplikat gewinnt und welche Duplikate im allgemeinen verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-160">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="a75e9-161">Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion Option angefordert wird, gewinnt der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll, immer.</span><span class="sxs-lookup"><span data-stu-id="a75e9-161">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-162">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="a75e9-162">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="a75e9-163">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a75e9-163">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="a75e9-164">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a75e9-164">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="a75e9-165">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-165">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-166">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="a75e9-166">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="a75e9-167">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-167">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="a75e9-168">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a75e9-168">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="a75e9-169">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-169">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-170">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="a75e9-170">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="a75e9-171">Mit dieser Option wird angefordert, dass NULL-Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="a75e9-171">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-172">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="a75e9-172">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="a75e9-173">Anforderungen, um nur systeminterne Long-Werte zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-173">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="a75e9-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a75e9-175">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="a75e9-175">*ptableid*</span></span>

<span data-ttu-id="a75e9-176">Der Ausgabepuffer, der den neuen Cursor empfängt, der in der neu erstellten temporären Tabelle geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a75e9-176">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="a75e9-177">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="a75e9-177">*prgcolumnid*</span></span>

<span data-ttu-id="a75e9-178">Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-178">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="a75e9-179">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-179">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="a75e9-180">Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-180">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="a75e9-181">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a75e9-181">Return Value</span></span>

<span data-ttu-id="a75e9-182">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a75e9-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a75e9-183">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a75e9-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a75e9-184">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a75e9-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="a75e9-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a75e9-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a75e9-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a75e9-187">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-188">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="a75e9-188">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="a75e9-189"><strong>JetOpenTempTable3</strong> ist fehlgeschlagen, weil JET_bitTTForwardOnly angegeben wurde und die temporäre Tabelle wie angegeben nicht mithilfe der vorwärts Optimierung erstellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a75e9-189"><strong>JetOpenTempTable3</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="a75e9-190">Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-190">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a75e9-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a75e9-192">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-193">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="a75e9-193">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="a75e9-194">Der Index konnte nicht erstellt werden, da eine ungültige Index Definition angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a75e9-194">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="a75e9-195"><strong>JetOpenTempTable3</strong> gibt diesen Fehler zurück, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="a75e9-195"><strong>JetOpenTempTable3</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a75e9-196">Das sprachneutrale Gebiets Schema ist angegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-196">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="a75e9-197">Es wurde ein ungültiger Satz von normalisierungs Flags angegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-197">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="a75e9-198">Dieser Fehler wird nur von Windows 2000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-198">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-199">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a75e9-199">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a75e9-200">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-200">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a75e9-201">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-201">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-202">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="a75e9-202">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="a75e9-203">Der <strong>CP</strong> -Member der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-203">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="a75e9-204">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="a75e9-204">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="a75e9-205">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="a75e9-205">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-206">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="a75e9-206">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="a75e9-207">Der <strong>colttmember</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a75e9-207">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-208">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="a75e9-208">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="a75e9-209">Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Gebiets Schema-ID zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-209">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="a75e9-210">Die Gebiets Schema-ID ist möglicherweise vollständig ungültig, oder das zugehörige Sprachpaket ist möglicherweise nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-210">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-211">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="a75e9-211">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="a75e9-212">Der Index konnte nicht erstellt werden, da versucht wurde, einen ungültigen Satz von normalisierungs Flags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-212">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="a75e9-213">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-213">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="a75e9-214">Bei Windows 2000 resultieren ungültige normalisierungs Flags stattdessen JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="a75e9-214">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-215">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a75e9-215">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a75e9-216">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a75e9-216">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="a75e9-217">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-217">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a75e9-218">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="a75e9-218">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-219">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a75e9-219">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a75e9-220">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a75e9-220">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-221">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a75e9-221">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a75e9-222">Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="a75e9-222">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="a75e9-223">Cursor Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-223">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-224">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a75e9-224">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a75e9-225">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-225">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="a75e9-226"><strong>JetOpenTempTable3</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird.</span><span class="sxs-lookup"><span data-stu-id="a75e9-226"><strong>JetOpenTempTable3</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="a75e9-227">Der temporäre Tabellen-Manager weist immer einen 1-MB-Adressraum für jede temporäre Tabelle zu, die unabhängig von der zu speichernden Datenmenge erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a75e9-227">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a75e9-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a75e9-229">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a75e9-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a75e9-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a75e9-231">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a75e9-232">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-232">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a75e9-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a75e9-234">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a75e9-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-235">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="a75e9-235">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="a75e9-236">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-236">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="a75e9-237">Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a75e9-237">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-238">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="a75e9-238">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="a75e9-239">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="a75e9-239">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="a75e9-240">Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-240">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-241">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="a75e9-241">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="a75e9-242">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="a75e9-242">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="a75e9-243">Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-243">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-244">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="a75e9-244">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="a75e9-245">Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="a75e9-245">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="a75e9-246">Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-246">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a75e9-247">Bei Erfolg wird ein Cursor zurückgegeben, der für die neu erstellte temporäre Tabelle geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a75e9-247">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="a75e9-248">Der Status der temporären Datenbank wird darauf vorbereitet, die neue temporäre Tabelle zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="a75e9-248">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="a75e9-249">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-249">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="a75e9-250">Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und ein Cursor wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75e9-250">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="a75e9-251">Der Status der temporären Datenbank kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a75e9-251">The state of the temporary database may be changed.</span></span> <span data-ttu-id="a75e9-252">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-252">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a75e9-253">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a75e9-253">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-254"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a75e9-254"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a75e9-255">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a75e9-255">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-256"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a75e9-256"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a75e9-257">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a75e9-257">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-258"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a75e9-258"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a75e9-259">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a75e9-259">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a75e9-260"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a75e9-260"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a75e9-261">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a75e9-261">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a75e9-262"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a75e9-262"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a75e9-263">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a75e9-263">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a75e9-264">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a75e9-264">See Also</span></span>

[<span data-ttu-id="a75e9-265">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="a75e9-265">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="a75e9-266">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="a75e9-266">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="a75e9-267">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="a75e9-267">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="a75e9-268">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="a75e9-268">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="a75e9-269">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a75e9-269">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a75e9-270">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a75e9-270">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a75e9-271">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a75e9-271">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a75e9-272">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a75e9-272">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a75e9-273">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="a75e9-273">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="a75e9-274">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="a75e9-274">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a75e9-275">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="a75e9-275">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="a75e9-276">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="a75e9-276">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="a75e9-277">Jetmove</span><span class="sxs-lookup"><span data-stu-id="a75e9-277">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a75e9-278">Jetopumtemptable</span><span class="sxs-lookup"><span data-stu-id="a75e9-278">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="a75e9-279">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="a75e9-279">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a75e9-280">JetSeek</span><span class="sxs-lookup"><span data-stu-id="a75e9-280">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="a75e9-281">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="a75e9-281">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a75e9-282">System Parameter</span><span class="sxs-lookup"><span data-stu-id="a75e9-282">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
