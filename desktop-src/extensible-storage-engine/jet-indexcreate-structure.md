---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE Struktur'
title: JET_INDEXCREATE-Struktur
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757938"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="0e469-103">JET_INDEXCREATE-Struktur</span><span class="sxs-lookup"><span data-stu-id="0e469-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="0e469-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0e469-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="0e469-105">Die **JET_INDEXCREATE** Struktur enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank (Extensible Storage Engine) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e469-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="0e469-106">Die-Struktur wird von Funktionen wie z. b. [JetCreateIndex2](./jetcreateindex2-function.md)und in Strukturen wie [JET_TABLECREATE](./jet-tablecreate-structure.md) und [JET_TABLECREATE2](./jet-tablecreate2-structure.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e469-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="0e469-107">Member</span><span class="sxs-lookup"><span data-stu-id="0e469-107">Members</span></span>

<span data-ttu-id="0e469-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="0e469-108">**cbStruct**</span></span>

<span data-ttu-id="0e469-109">Die Größe (in Bytes) dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="0e469-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="0e469-110">Legen Sie diesen Member auf sizeof (JET_INDEXCREATE) fest.</span><span class="sxs-lookup"><span data-stu-id="0e469-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="0e469-111">**szindexname**</span><span class="sxs-lookup"><span data-stu-id="0e469-111">**szIndexName**</span></span>

<span data-ttu-id="0e469-112">Der Name des zu erstellenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="0e469-112">The name of the index to create.</span></span>

<span data-ttu-id="0e469-113">Der Name des Indexes muss die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="0e469-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="0e469-114">Sie muss kleiner als JET_cbNameMost sein, ohne dass der abschließende NULL-Wert eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="0e469-115">Sie muss aus folgenden Zeichen bestehen: 0 (null) bis 9, a bis z, a bis z und alle anderen Interpunktions Zeichen mit Ausnahme von " \! ".</span><span class="sxs-lookup"><span data-stu-id="0e469-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="0e469-116">(Ausrufezeichen), "," (Komma), " \[ " (öffnende eckige Klammer) und " \] " (schließende Klammer) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c, 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="0e469-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="0e469-117">Er darf nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="0e469-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="0e469-118">Sie muss aus mindestens einem Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="0e469-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="0e469-119">**szkey**</span><span class="sxs-lookup"><span data-stu-id="0e469-119">**szKey**</span></span>

<span data-ttu-id="0e469-120">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die NULL-Werte getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="0e469-121">Jedes Token hat das Format " \<direction-specifier\> \<column-name\> ", wobei "Direction-Specification" entweder "+" oder "-" ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="0e469-122">Beispielsweise indiziert ein **szkey** -Wert von "+ ABC \\ 0-DEF \\ 0 + ghi \\ 0" die drei Spalten "ABC" (in aufsteigender Reihenfolge), "Def" (in absteigender Reihenfolge) und "ghi" (in aufsteigender Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="0e469-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="0e469-123">In der Programmiersprache C haben Zeichen folgen Literale einen impliziten **null** -Terminator. Daher wird die obige Zeichenfolge durch einen Double-NULL-Wert beendet.</span><span class="sxs-lookup"><span data-stu-id="0e469-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="0e469-124">Die Anzahl der in **szkey** angegebenen Spalten darf den Wert **JET_ccolKeyMost** nicht überschreiten (eine Versions abhängige Konstante).</span><span class="sxs-lookup"><span data-stu-id="0e469-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="0e469-125">Mindestens eine Spalte muss in **szkey** benannt werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="0e469-126">Veraltetes Verhalten: nach dem Double-NULL-Abschluss Zeichen ist es möglich, eine Sprach-ID (ein Wort, das an MAKELCID (langid, SORT_DEFAULT) übergeben wird) als Möglichkeit anzugeben, die LCID für den Index anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0e469-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="0e469-127">Es ist unzulässig, sowohl eine Sprachen-ID in **szkey** als auch eine LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) anzugeben (durch Festlegen von JET_bitIndexUnicode in *grbit*).</span><span class="sxs-lookup"><span data-stu-id="0e469-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="0e469-128">Veraltet: nach der Sprach-ID ist es möglich, **cbvarsegmac** als ushort zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e469-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="0e469-129">Das Verhalten ist nicht definiert, wenn der ushort-Wert sowohl in **szkey** als auch in der-Struktur fest **gelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="0e469-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="0e469-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="0e469-130">**cbKey**</span></span>

<span data-ttu-id="0e469-131">Die Länge von **szkey** (in Bytes), einschließlich der beiden abschließenden Nullen.</span><span class="sxs-lookup"><span data-stu-id="0e469-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="0e469-132">**grbit**</span><span class="sxs-lookup"><span data-stu-id="0e469-132">**grbit**</span></span>

<span data-ttu-id="0e469-133">Eine Gruppe von Bits, die 0 (null) oder mehr der in der folgenden Tabelle aufgeführten Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="0e469-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e469-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0e469-134">Value</span></span></p></th>
<th><p><span data-ttu-id="0e469-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0e469-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e469-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="0e469-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="0e469-137">Doppelte Indexeinträge (Schlüssel) sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0e469-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="0e469-138">Dies wird erzwungen, wenn <a href="gg269288(v=exchg.10).md">jetupdate</a> aufgerufen wird, nicht wenn <a href="gg294137(v=exchg.10).md">jetsetcolumn</a> aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="0e469-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="0e469-140">Der Index ist ein primärer Index (gruppierter Index).</span><span class="sxs-lookup"><span data-stu-id="0e469-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="0e469-141">Jede Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0e469-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="0e469-142">Wenn kein primärer Index explizit für eine Tabelle definiert wird, erstellt die Datenbank-Engine ihren eigenen primären Index.</span><span class="sxs-lookup"><span data-stu-id="0e469-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="0e469-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="0e469-144">Keine der Spalten, für die der Index erstellt wird, kann einen <strong>null</strong> -Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e469-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="0e469-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="0e469-146">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn alle indizierten Spalten <strong>null</strong>sind.</span><span class="sxs-lookup"><span data-stu-id="0e469-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="0e469-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="0e469-148">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn eine der indizierten Spalten <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="0e469-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="0e469-150">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn die erste indizierte Spalte <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="0e469-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="0e469-152">Index Vorgänge werden verzögert protokolliert.</span><span class="sxs-lookup"><span data-stu-id="0e469-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="0e469-153">JET_bitIndexLazyFlush wirkt sich nicht auf die Faulheit von Datenaktualisierungen aus.</span><span class="sxs-lookup"><span data-stu-id="0e469-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="0e469-154">Wenn der Indizierungs Vorgang durch die Beendigung des Prozesses unterbrochen wird, kann die Wiederherstellung der Datenbank dennoch in einen konsistenten Zustand versetzt werden, aber der Index ist möglicherweise nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0e469-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="0e469-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="0e469-156">Versuchen Sie nicht, den Index zu erstellen, da alle Einträge zu <strong>null</strong>ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="0e469-157">bei der Übergabe JET_bitIndexEmpty muss auch <strong>grbit</strong> JET_bitIgnoreAnyNull angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="0e469-158">Dies ist eine Leistungsverbesserung.</span><span class="sxs-lookup"><span data-stu-id="0e469-158">This is a performance enhancement.</span></span> <span data-ttu-id="0e469-159">Wenn z. b. eine neue Spalte zu einer Tabelle hinzugefügt wird, wird für diese neu hinzugefügte Spalte ein Index erstellt, und alle Datensätze in der Tabelle werden gescannt, auch wenn Sie nicht zum Index hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="0e469-160">Durch angeben JET_bitIndexEmpty wird die Überprüfung der Tabelle ausgelassen, was möglicherweise sehr lange dauern kann.</span><span class="sxs-lookup"><span data-stu-id="0e469-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="0e469-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="0e469-162">Bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="0e469-163">In der Regel kann eine Sitzung in einer Transaktion einen Index Erstellungs Vorgang nicht in einer anderen Sitzung sehen.</span><span class="sxs-lookup"><span data-stu-id="0e469-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="0e469-164">Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e469-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="0e469-165">Die zweite Indexerstellung schlägt fehl, anstatt potenziell viele unnötige Daten Bank Vorgänge zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="0e469-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="0e469-166">Die zweite Transaktion ist möglicherweise nicht in der Lage, den Index sofort zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e469-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="0e469-167">Der Index Erstellungs Vorgang muss beendet werden, bevor er verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e469-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="0e469-168">Die Sitzung darf sich zurzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e469-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="0e469-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="0e469-170">Die Angabe dieses Flags bewirkt, dass <strong>null</strong> -Werte nach den Daten für alle Spalten im Index sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="0e469-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="0e469-172">Die Angabe dieses Flags wirkt sich auf die Interpretation des LCID/pidxunicde-Union-Felds in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="0e469-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="0e469-173">Das Festlegen des Bits bedeutet, dass das Feld <strong>pidxunicode</strong> tatsächlich auf eine <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="0e469-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="0e469-174">JET_bitIndexUnicode ist nicht erforderlich, um Unicode-Daten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="0e469-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="0e469-175">Sie wird nur verwendet, um die Normalisierung von Unicode-Daten anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0e469-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="0e469-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="0e469-177">Gibt an, dass der Index ein Tupelindex ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="0e469-178">Eine Beschreibung eines tupelindexes finden Sie unter <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="0e469-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="0e469-179">JET_bitIndexTuples wurde im Betriebssystem Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="0e469-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="0e469-181">Die Angabe dieses Flags wirkt sich auf die Interpretation des Union <strong>-Felds cbvarsegmac/ptuplelimits</strong> in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="0e469-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="0e469-182">Das Festlegen dieses Bits bedeutet, dass das Feld " <strong>ptuplelimits</strong> " tatsächlich auf eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur verweist, um benutzerdefinierte tupelindexlimits zuzulassen (impliziert JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="0e469-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="0e469-183">JET_bitIndexTupleLimits wurde im Betriebssystem Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="0e469-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="0e469-185">Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="0e469-186">Andernfalls hätte der Index nur einen Eintrag für jeden mehrwertigen in der signifikantesten Schlüssel Spalte, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten multiwert aus anderen Schlüssel Spalten verwenden, bei denen es sich um mehrwertige Spalten handelt.</span><span class="sxs-lookup"><span data-stu-id="0e469-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="0e469-187">Wenn Sie z. B. dieses Flag für einen Index über Spalte a mit den Werten &quot; rot &quot; und &quot; blau &quot; und over column B mit den Werten 1 und 2 angegeben haben, &quot; &quot; &quot; &quot; werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blau &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="0e469-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="0e469-188">Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="0e469-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="0e469-189">JET_bitIndexCrossProduct wurde im Betriebssystem Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="0e469-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="0e469-191">Die Angabe dieses Flags bewirkt, dass der Index die maximale Schlüsselgröße verwendet, die im Feld <strong>cbkeymost</strong> in der-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="0e469-192">Andernfalls wird der Index JET_cbKeyMost (255) als maximale Schlüsselgröße verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e469-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="0e469-193">JET_bitIndexKeyMost wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-194">JET_bitIndexDisallowTruncation 0x00010000 bis</span><span class="sxs-lookup"><span data-stu-id="0e469-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="0e469-195">Die Angabe dieses Flags führt dazu, dass ein Update des Indexes, das zu einem abgeschnittene Schlüssel führt, mit JET_errKeyTruncated fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0e469-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="0e469-196">Andernfalls werden Schlüssel automatisch abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="0e469-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="0e469-197">Weitere Informationen zum Abschneiden von Schlüsseln finden Sie unter der <a href="gg269329(v=exchg.10).md">jetmakekey</a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0e469-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="0e469-198"><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="0e469-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="0e469-200">Die Angabe dieses Flags bewirkt, dass der Index über mehrere mehrwertige Spalten aktualisiert wird, jedoch nur mit Werten derselben <strong>itagsequence</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e469-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="0e469-201">JET_bitIndexNestedTable wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e469-202">**uldensity**</span><span class="sxs-lookup"><span data-stu-id="0e469-202">**ulDensity**</span></span>

<span data-ttu-id="0e469-203">Die prozentuale Dichte des ersten Index B +-Baums.</span><span class="sxs-lookup"><span data-stu-id="0e469-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="0e469-204">Wenn Sie eine Zahl angeben, die kleiner als 100 ist, wird zum ersten Mal mehr Speicherplatz zum Erstellen des Indexes verwendet, jedoch kann das zukünftige Wachstum des Indexes vorhanden sein, sodass die interne Fragmentierung vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="0e469-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="0e469-205">**lcid**</span></span>

<span data-ttu-id="0e469-206">Der Gebiets Schema Bezeichner (LCID), der bei der Normalisierung der Daten verwendet werden soll, wenn der JET_bitIndexUnicode Wert nicht im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="0e469-207">Die LCID wirkt sich auf die Normalisierung aus, wenn der Index über Unicode-Spalten ist.</span><span class="sxs-lookup"><span data-stu-id="0e469-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="0e469-208">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="0e469-208">**pidxunicode**</span></span>

<span data-ttu-id="0e469-209">Ein Zeiger auf eine [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) Struktur, wenn der JET_bitIndexUnicode Wert im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="0e469-210">Dies ermöglicht es dem Benutzer, benutzerdefinierte Flags anzugeben, die während der Unicode-Normalisierung an die [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="0e469-211">**cbvarsegmac**</span><span class="sxs-lookup"><span data-stu-id="0e469-211">**cbVarSegMac**</span></span>

<span data-ttu-id="0e469-212">Die maximale Länge (in Byte) der einzelnen Spalten, die im Index gespeichert werden sollen, wenn der JET_bitIndexTupleLimits Wert nicht im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="0e469-213">Die Angabe eines Werts von 0 (null) für dieses Feld entspricht:</span><span class="sxs-lookup"><span data-stu-id="0e469-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="0e469-214">Angeben von JET_cbPrimaryKeyMost für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="0e469-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="0e469-215">Angeben von JET_cbSecondaryKeyMost für einen sekundären Index.</span><span class="sxs-lookup"><span data-stu-id="0e469-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="0e469-216">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="0e469-216">**ptuplelimits**</span></span>

<span data-ttu-id="0e469-217">Ein Zeiger auf eine [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur, wenn der JET_bitIndexTupleLimits Wert im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="0e469-218">ptuplelimits wurde in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="0e469-219">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="0e469-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="0e469-220">Ein optionaler Parameter für ein Array von [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) -Strukturen, die verwendet werden, um die bedingten Spalten im Index anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0e469-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="0e469-221">**cconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="0e469-221">**cConditionalColumn**</span></span>

<span data-ttu-id="0e469-222">Die Anzahl der Strukturen im **rgconditionalcolumn** -Array.</span><span class="sxs-lookup"><span data-stu-id="0e469-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="0e469-223">**irre**</span><span class="sxs-lookup"><span data-stu-id="0e469-223">**err**</span></span>

<span data-ttu-id="0e469-224">Enthält den Rückgabecode zum Erstellen dieses Indexes.</span><span class="sxs-lookup"><span data-stu-id="0e469-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="0e469-225">**cbkeymost**</span><span class="sxs-lookup"><span data-stu-id="0e469-225">**cbKeyMost**</span></span>

<span data-ttu-id="0e469-226">Gibt die maximal zulässige Größe für Schlüssel im Index in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="0e469-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="0e469-227">Dieser Parameter wird ignoriert, wenn der JET_bitIndexKeyMost Wert nicht im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e469-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="0e469-228">Wenn dieser Parameter auf 0 (null) festgelegt ist, und JET_bitIndexKeyMost im *grbit* -Parameter angegeben wird, schlägt die Aufruf Funktion mit JET_err_InvalidDef fehl.</span><span class="sxs-lookup"><span data-stu-id="0e469-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="0e469-229">Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="0e469-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="0e469-230">Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe (JET_paramDatabasePageSize) wie folgt ab:</span><span class="sxs-lookup"><span data-stu-id="0e469-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="0e469-231">Wenn JET_paramDatabasePageSize = 2048, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="0e469-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="0e469-232">Wenn JET_paramDatabasePageSize = 4096, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="0e469-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="0e469-233">Wenn JET_paramDatabasePageSize = 8192, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="0e469-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="0e469-234">Die maximal unterstützte Schlüsselgröße für die-Instanz kann auch aus dem JET_paramKeyMost System-Parameter gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="0e469-235">**cbkeymost** wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e469-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e469-236">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e469-236">Remarks</span></span>

<span data-ttu-id="0e469-237">ESE unterstützt die Indizierung über Schlüssel Spalten, die mehrere Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e469-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="0e469-238">Um dieses Feature verwenden zu können, muss es sich bei der Spalte um einen markierten Spaltentyp (JET_bitColumnTagged) handeln, und es muss gekennzeichnet werden, damit die verschiedenen Werte mit JET_bitColumnMultiValued indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="0e469-239">In Windows-Versionen vor Windows Vista werden die Werte nur für die erste mehrwertige Schlüssel Spalte im Index im Index erweitert.</span><span class="sxs-lookup"><span data-stu-id="0e469-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="0e469-240">Für alle anderen mehrwertigen und markierten Spalten werden nur die ersten Werte im Index erweitert.</span><span class="sxs-lookup"><span data-stu-id="0e469-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="0e469-241">Angenommen, die folgenden Zeilen sind in einer Tabelle vorhanden (die Spalte Alpha ist nicht mehr wertig, während die Spalten Beta, Gamma und Delta mehr wertig sind), und ein Index wird als "+ Alpha \\ 0 + Beta \\ 0 + Gamma \\ 0 + Delta \\ 0 \\ 0" erstellt:</span><span class="sxs-lookup"><span data-stu-id="0e469-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e469-242">Alpha</span><span class="sxs-lookup"><span data-stu-id="0e469-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="0e469-243">Beta</span><span class="sxs-lookup"><span data-stu-id="0e469-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="0e469-244">Gamma</span><span class="sxs-lookup"><span data-stu-id="0e469-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="0e469-245">Delta</span><span class="sxs-lookup"><span data-stu-id="0e469-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e469-246">1</span><span class="sxs-lookup"><span data-stu-id="0e469-246">1</span></span></p></td>
<td><p><span data-ttu-id="0e469-247">ABC</span><span class="sxs-lookup"><span data-stu-id="0e469-247">ABC</span></span><br />
<span data-ttu-id="0e469-248">GHI</span><span class="sxs-lookup"><span data-stu-id="0e469-248">GHI</span></span><br />
<span data-ttu-id="0e469-249">JKL</span><span class="sxs-lookup"><span data-stu-id="0e469-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="0e469-250">MNO</span><span class="sxs-lookup"><span data-stu-id="0e469-250">MNO</span></span><br />
<span data-ttu-id="0e469-251">PQR</span><span class="sxs-lookup"><span data-stu-id="0e469-251">PQR</span></span><br />
<span data-ttu-id="0e469-252">Stu</span><span class="sxs-lookup"><span data-stu-id="0e469-252">STU</span></span></p></td>
<td><p><span data-ttu-id="0e469-253">Vwx</span><span class="sxs-lookup"><span data-stu-id="0e469-253">VWX</span></span><br />
<span data-ttu-id="0e469-254">YZ</span><span class="sxs-lookup"><span data-stu-id="0e469-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-255">2</span><span class="sxs-lookup"><span data-stu-id="0e469-255">2</span></span></p></td>
<td><p><span data-ttu-id="0e469-256">Die</span><span class="sxs-lookup"><span data-stu-id="0e469-256">THE</span></span></p></td>
<td><p><span data-ttu-id="0e469-257">REGEN</span><span class="sxs-lookup"><span data-stu-id="0e469-257">RAIN</span></span><br />
<span data-ttu-id="0e469-258">Spanien</span><span class="sxs-lookup"><span data-stu-id="0e469-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="0e469-259">IN</span><span class="sxs-lookup"><span data-stu-id="0e469-259">IN</span></span><br />
<span data-ttu-id="0e469-260">Engpässen</span><span class="sxs-lookup"><span data-stu-id="0e469-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e469-261">Der abfallende Index-Tupel werden gespeichert:</span><span class="sxs-lookup"><span data-stu-id="0e469-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="0e469-262">{1, ABC, MNO, vwx}</span><span class="sxs-lookup"><span data-stu-id="0e469-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="0e469-263">{1, ghi, MNO, vwx}</span><span class="sxs-lookup"><span data-stu-id="0e469-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="0e469-264">{1, JKL, MNO, vwx}</span><span class="sxs-lookup"><span data-stu-id="0e469-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="0e469-265">{2,, Regen, in}</span><span class="sxs-lookup"><span data-stu-id="0e469-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="0e469-266">Beachten Sie, dass {2,, Spanien, in} nicht gespeichert wird, auch wenn die Alpha Spalte in der zweiten Zeile einen einzelnen multiwert hat.</span><span class="sxs-lookup"><span data-stu-id="0e469-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="0e469-267">In Windows-Versionen ab Windows Vista können alle mehrwertigen Spalten im Index erweitert werden, indem JET_bitIndexCrossProduct angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e469-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="0e469-268">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e469-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e469-269"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0e469-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0e469-270">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0e469-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-271"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0e469-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0e469-272">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0e469-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e469-273"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0e469-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0e469-274">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0e469-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e469-275"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0e469-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0e469-276">Wird als <strong>JET_ INDEXCREATE_W</strong> (Unicode) und <strong>JET_ INDEXCREATE_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="0e469-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0e469-277">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e469-277">See also</span></span>

[<span data-ttu-id="0e469-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="0e469-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="0e469-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="0e469-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="0e469-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0e469-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0e469-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0e469-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0e469-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="0e469-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="0e469-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="0e469-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="0e469-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="0e469-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="0e469-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="0e469-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="0e469-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="0e469-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="0e469-287">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="0e469-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="0e469-288">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="0e469-288">JetUpdate</span></span>](./jetupdate-function.md)
