---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE Struktur'
title: JET_OPENTEMPORARYTABLE Struktur
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
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
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345858"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="ef733-103">JET_OPENTEMPORARYTABLE Struktur</span><span class="sxs-lookup"><span data-stu-id="ef733-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="ef733-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef733-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="ef733-105">JET_OPENTEMPORARYTABLE Struktur</span><span class="sxs-lookup"><span data-stu-id="ef733-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="ef733-106">Die **JET_OPENTEMPORARYTABLE** -Struktur enthält eine leicht erweiterbare Auflistung von Parametern für die **JET_OPENTEMPORARYTABLE** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ef733-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="ef733-107">Diese Struktur ist die temporäre Tabelle, die der [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur entspricht.</span><span class="sxs-lookup"><span data-stu-id="ef733-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="ef733-108">**Windows Vista:** Die **JET_OPENTEMPORARYTABLE** Struktur wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef733-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="ef733-109">Member</span><span class="sxs-lookup"><span data-stu-id="ef733-109">Members</span></span>

<span data-ttu-id="ef733-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ef733-110">**cbStruct**</span></span>

<span data-ttu-id="ef733-111">Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen).</span><span class="sxs-lookup"><span data-stu-id="ef733-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="ef733-112">Er muss auf sizeof (JET_TABLECREATE) in Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="ef733-113">**prgcolumndef**</span><span class="sxs-lookup"><span data-stu-id="ef733-113">**prgcolumndef**</span></span>

<span data-ttu-id="ef733-114">Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="ef733-115">**Wichtige** Einschränkungen gelten für die Spalten Definitions Optionen, die für eine temporäre Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="ef733-116">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ef733-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="ef733-117">Zusätzlich zu den üblichen Spalten Definitions Optionen können auch keine oder mehrere der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.</span><span class="sxs-lookup"><span data-stu-id="ef733-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef733-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ef733-118">Value</span></span></p></th>
<th><p><span data-ttu-id="ef733-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef733-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef733-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="ef733-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="ef733-121">Die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein.</span><span class="sxs-lookup"><span data-stu-id="ef733-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="ef733-122">Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ef733-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef733-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="ef733-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="ef733-124">Die Spalte ist eine Schlüssel Spalte für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ef733-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="ef733-125">Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ef733-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="ef733-126">Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüssel Spalte usw.</span><span class="sxs-lookup"><span data-stu-id="ef733-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="ef733-127">Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ef733-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef733-128">**CColumn**</span><span class="sxs-lookup"><span data-stu-id="ef733-128">**ccolumn**</span></span>

<span data-ttu-id="ef733-129">Siehe *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="ef733-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="ef733-130">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="ef733-130">**pidxunicode**</span></span>

<span data-ttu-id="ef733-131">Die Gebiets Schema-ID und normalisierungs Flags, die verwendet werden, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ef733-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="ef733-132">Wenn dieser Parameter nicht vorhanden ist und der *LCID* -Parameter nicht vorhanden ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ef733-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="ef733-133">Die Standard-LCID ist das US-englische Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="ef733-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="ef733-134">Wenn dieser Parameter nicht vorhanden ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ef733-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="ef733-135">Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="ef733-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="ef733-136">**grbit**</span><span class="sxs-lookup"><span data-stu-id="ef733-136">**grbit**</span></span>

<span data-ttu-id="ef733-137">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="ef733-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef733-138">Wert</span><span class="sxs-lookup"><span data-stu-id="ef733-138">Value</span></span></p></th>
<th><p><span data-ttu-id="ef733-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef733-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef733-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="ef733-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="ef733-141">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> für die Suche nach Datensätzen nach Index Schlüssel zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="ef733-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="ef733-142">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ef733-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="ef733-143">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="ef733-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef733-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="ef733-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="ef733-145">Fordert an, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="ef733-146">Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ef733-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="ef733-147">Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die JET_bitTTForwardOnly-Option ebenfalls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ef733-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="ef733-148">Im Allgemeinen ist es nicht möglich, zu ermitteln, welches Duplikat erfolgreich ist und welche Duplikate verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="ef733-149">Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion-Option angefordert wird, ist der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ef733-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef733-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="ef733-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="ef733-151">Fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ef733-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="ef733-152">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ef733-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="ef733-153">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="ef733-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef733-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="ef733-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="ef733-155">Fordert an, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="ef733-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="ef733-156">Wenn diese Funktionalität nicht erforderlich ist, ist es am besten, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ef733-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="ef733-157">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="ef733-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef733-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="ef733-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="ef733-159">Fordert an, dass <strong>null</strong> -Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="ef733-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef733-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="ef733-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="ef733-161">Zwingt den temporären Tabellen-Manager, die Suche nach der optimalen Strategie zu verwerfen, um die Verwaltung der temporären Tabelle zu verbessern, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="ef733-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef733-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="ef733-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="ef733-163">Jeder Versuch, einen Datensatz mit dem gleichen Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, schlägt mit JET_errKeyDuplicate sofort fehl.</span><span class="sxs-lookup"><span data-stu-id="ef733-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="ef733-164">Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt, und es wird ein Fehler zurückgegeben. Dies hängt von der Strategie ab, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef733-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="ef733-165">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ef733-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="ef733-166">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="ef733-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef733-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="ef733-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="ef733-168">Die temporäre Tabelle wird nur erstellt, wenn der temporäre Tabellen-Manager die-Implementierung verwenden kann, die für zwischen Abfrageergebnisse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef733-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="ef733-169">Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</span><span class="sxs-lookup"><span data-stu-id="ef733-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="ef733-170">Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="ef733-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="ef733-171">Weitere Informationen finden Sie unter JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="ef733-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="ef733-172"><strong>Windows Server 2003:  </strong> Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef733-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef733-173">**prgcolumnid**</span><span class="sxs-lookup"><span data-stu-id="ef733-173">**prgcolumnid**</span></span>

<span data-ttu-id="ef733-174">Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ef733-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="ef733-175">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ef733-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="ef733-176">Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ef733-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="ef733-177">**cbkeymost**</span><span class="sxs-lookup"><span data-stu-id="ef733-177">**cbKeyMost**</span></span>

<span data-ttu-id="ef733-178">Die maximale Größe für einen Schlüssel, der eine bestimmte Zeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef733-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="ef733-179">Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="ef733-180">Das Abschneiden von Schlüsseln ist wichtig, da sich dies auf den Fall auswirkt, dass Zeilen als verschieden betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="ef733-181">Wenn dieser Parameter auf 0 oder JET_cbKeyMostMin (255) festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik identisch mit der maximalen Schlüsselgröße, die von Windows Server 2003 und früheren Versionen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ef733-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="ef733-182">Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseiten Größe für die-Instanz (JET_paramDatabasePageSize) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ef733-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="ef733-183">Weitere Informationen finden Sie unter JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="ef733-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="ef733-184">**cbvarsegmac**</span><span class="sxs-lookup"><span data-stu-id="ef733-184">**cbVarSegMac**</span></span>

<span data-ttu-id="ef733-185">Die maximale Datenmenge, die in einer Spalte mit variabler Länge verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef733-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="ef733-186">Dieser Parameter kann verwendet werden, um die Menge des von einer bestimmten Schlüssel Spalte genutzten schlüsselplatzes zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ef733-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="ef733-187">Dieser Grenzwert ist in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ef733-187">This limit is in bytes.</span></span> <span data-ttu-id="ef733-188">Wenn dieser Parameter 0 (null) ist oder mit dem *cbkeymost* -Parameter identisch ist, ist kein Limit wirksam.</span><span class="sxs-lookup"><span data-stu-id="ef733-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="ef733-189">**TableID**</span><span class="sxs-lookup"><span data-stu-id="ef733-189">**tableid**</span></span>

<span data-ttu-id="ef733-190">Das Tabellen Handle für die temporäre Tabelle, die als Ergebnis eines erfolgreichen [jetopumtemporarytable](./jetopentemporarytable-function.md)-Aufrufes erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef733-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="ef733-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef733-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef733-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ef733-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef733-193">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ef733-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef733-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef733-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef733-195">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ef733-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef733-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ef733-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef733-197">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ef733-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ef733-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef733-198">See Also</span></span>

[<span data-ttu-id="ef733-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="ef733-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="ef733-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="ef733-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="ef733-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="ef733-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="ef733-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ef733-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ef733-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="ef733-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="ef733-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ef733-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ef733-205">Jetopumtemporarytable</span><span class="sxs-lookup"><span data-stu-id="ef733-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="ef733-206">System Parameter für Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="ef733-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
