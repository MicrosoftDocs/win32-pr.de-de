---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE2 Struktur'
title: JET_INDEXCREATE2-Struktur
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960967"
---
# <a name="jet_indexcreate2-structure"></a><span data-ttu-id="5a044-103">JET_INDEXCREATE2-Struktur</span><span class="sxs-lookup"><span data-stu-id="5a044-103">JET_INDEXCREATE2 Structure</span></span>


<span data-ttu-id="5a044-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a044-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5a044-105">Die **JET_INDEXCREATE2** Struktur enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank (Extensible Storage Engine) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a044-105">The **JET_INDEXCREATE2** structure contains the information that is required to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="5a044-106">Die-Struktur wird von Funktionen wie z. b. [JetCreateIndex2](./jetcreateindex2-function.md)und in Strukturen wie [JET_TABLECREATE](./jet-tablecreate-structure.md) und [JET_TABLECREATE2](./jet-tablecreate2-structure.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a044-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

<span data-ttu-id="5a044-107">Die **JET_INDEXCREATE2** Struktur wurde mit dem Betriebssystem Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-107">The **JET_INDEXCREATE2** structure was introduced in the Windows 7 operating system.</span></span>

```cpp
typedef struct tagJET_INDEXCREATE2 {
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
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="5a044-108">Member</span><span class="sxs-lookup"><span data-stu-id="5a044-108">Members</span></span>

<span data-ttu-id="5a044-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5a044-109">**cbStruct**</span></span>

<span data-ttu-id="5a044-110">Die Größe (in Bytes) dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="5a044-110">The size, in bytes, of this structure.</span></span> <span data-ttu-id="5a044-111">Legen Sie diesen Member auf sizeof (JET_INDEXCREATE2) fest.</span><span class="sxs-lookup"><span data-stu-id="5a044-111">Set this member to sizeof( JET_INDEXCREATE2 ).</span></span>

<span data-ttu-id="5a044-112">**szindexname**</span><span class="sxs-lookup"><span data-stu-id="5a044-112">**szIndexName**</span></span>

<span data-ttu-id="5a044-113">Der Name des zu erstellenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="5a044-113">The name of the index to create.</span></span>

<span data-ttu-id="5a044-114">Der Name muss die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="5a044-114">The name should meet the following conditions:</span></span>

  - <span data-ttu-id="5a044-115">Er sollte kleiner als JET_cbNameMost sein, ohne dass der abschließende NULL-Wert eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-115">It should be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="5a044-116">Sie muss aus folgenden Zeichen bestehen: 0 (null) bis 9, a bis z, a bis z und alle anderen Interpunktions Zeichen mit Ausnahme von " \! ".</span><span class="sxs-lookup"><span data-stu-id="5a044-116">It must consist of the following set of characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="5a044-117">(Ausrufezeichen), "," (Komma), " \[ " (öffnende eckige Klammer) und " \] " (schließende Klammer) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="5a044-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="5a044-118">Er darf nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="5a044-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="5a044-119">Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="5a044-120">**szkey**</span><span class="sxs-lookup"><span data-stu-id="5a044-120">**szKey**</span></span>

<span data-ttu-id="5a044-121">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die NULL-Werte getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-121">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="5a044-122">Jedes Token hat das Format " \<direction-specifier\> \<column-name\> ", wobei "Direction-Specification" entweder "+" oder "-" ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-122">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="5a044-123">Beispielsweise indiziert ein **szkey** -Wert von "+ ABC \\ 0-DEF \\ 0 + ghi \\ 0" die drei Spalten "ABC" (in aufsteigender Reihenfolge), "Def" (in absteigender Reihenfolge) und "ghi" (in aufsteigender Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="5a044-123">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="5a044-124">In der Programmiersprache C haben Zeichen folgen Literale einen impliziten **null** -Terminator, sodass die obige Zeichenfolge durch einen Double-NULL-Wert beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-124">In the C language, string literals have an implied **NULL** terminator, so the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="5a044-125">Die Anzahl der in **szkey** angegebenen Spalten darf JET_ccolKeyMost (eine Versions abhängige Konstante) nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="5a044-125">The number of columns specified in **szKey** must not exceed JET_ccolKeyMost (a version-dependent constant).</span></span>

<span data-ttu-id="5a044-126">Mindestens eine Spalte muss in **szkey** benannt werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-126">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="5a044-127">Veraltetes Verhalten: nach dem Double-NULL-Abschluss Zeichen ist es möglich, eine Sprach-ID (ein Wort, das an MAKELCID (langid, SORT_DEFAULT) übergeben wird) als Möglichkeit anzugeben, die LCID für den Index anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5a044-127">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="5a044-128">Es ist unzulässig, sowohl eine Sprachen-ID in **szkey** als auch eine LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) anzugeben (durch Festlegen von JET_bitIndexUnicode in *grbit*).</span><span class="sxs-lookup"><span data-stu-id="5a044-128">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="5a044-129">Veraltet: nach der Sprach-ID ist es möglich, **cbvarsegmac** als **UShort** -Datentyp zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5a044-129">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a **USHORT** data type.</span></span> <span data-ttu-id="5a044-130">Das Verhalten ist nicht definiert, wenn der ushort-Wert sowohl in **szkey** als auch in der-Struktur fest **gelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="5a044-130">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="5a044-131">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="5a044-131">**cbKey**</span></span>

<span data-ttu-id="5a044-132">Die Länge (in Byte) von **szkey**, einschließlich der beiden abschließenden Nullen.</span><span class="sxs-lookup"><span data-stu-id="5a044-132">The length, in bytes, of **szKey**, including the two terminating nulls.</span></span>

<span data-ttu-id="5a044-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="5a044-133">**grbit**</span></span>

<span data-ttu-id="5a044-134">Eine Gruppe von Bits, die NULL oder mehr der Wert Optionen enthalten, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5a044-134">A group of bits that contain zero or more of the value options that are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a044-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5a044-135">Value</span></span></p></th>
<th><p><span data-ttu-id="5a044-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a044-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a044-137">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="5a044-137">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="5a044-138">Doppelte Indexeinträge (Schlüssel) sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5a044-138">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="5a044-139">Dies wird erzwungen, wenn <a href="gg269288(v=exchg.10).md">jetupdate</a> aufgerufen wird, nicht wenn <a href="gg294137(v=exchg.10).md">jetsetcolumn</a> aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-139">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-140">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="5a044-140">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="5a044-141">Der Index ist ein primärer Index (gruppierter Index).</span><span class="sxs-lookup"><span data-stu-id="5a044-141">The index is a primary (clustered) index.</span></span> <span data-ttu-id="5a044-142">Jede Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5a044-142">Every table must have exactly one primary index.</span></span> <span data-ttu-id="5a044-143">Wenn kein primärer Index explizit für eine Tabelle definiert wird, erstellt die Datenbank-Engine ihren eigenen primären Index.</span><span class="sxs-lookup"><span data-stu-id="5a044-143">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-144">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="5a044-144">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="5a044-145">Keine der Spalten, für die der Index erstellt wird, kann einen <strong>null</strong> -Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="5a044-145">None of the columns over which the index is created may contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-146">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="5a044-146">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="5a044-147">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn alle indizierten Spalten <strong>null</strong>sind.</span><span class="sxs-lookup"><span data-stu-id="5a044-147">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-148">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="5a044-148">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="5a044-149">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn eine der indizierten Spalten <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-149">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-150">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="5a044-150">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="5a044-151">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn die erste indizierte Spalte <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-151">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-152">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="5a044-152">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="5a044-153">Gibt an, dass die Index Vorgänge verzögert protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-153">Specifies that the index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="5a044-154">JET_bitIndexLazyFlush wirkt sich nicht auf die Faulheit von Datenaktualisierungen aus.</span><span class="sxs-lookup"><span data-stu-id="5a044-154">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="5a044-155">Wenn der Indizierungs Vorgang durch die Beendigung des Prozesses unterbrochen wird, kann die Wiederherstellung der Datenbank dennoch in einen konsistenten Zustand versetzt werden, aber der Index ist möglicherweise nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5a044-155">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-156">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="5a044-156">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="5a044-157">Versuchen Sie nicht, den Index zu erstellen, da alle Einträge zu <strong>null</strong>ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-157">Do not try to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="5a044-158"><strong>grbit</strong> Muss auch JET_bitIgnoreAnyNull angeben, wenn JET_bitIndexEmpty übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-158"><strong>grbit</strong> MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="5a044-159">Dies ist eine Leistungsverbesserung.</span><span class="sxs-lookup"><span data-stu-id="5a044-159">This is a performance enhancement.</span></span> <span data-ttu-id="5a044-160">Wenn z. b. eine neue Spalte zu einer Tabelle hinzugefügt wird und dann ein Index für diese neu hinzugefügte Spalte erstellt wird, werden alle Datensätze in der Tabelle gescannt, auch wenn Sie nicht zum Index hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-160">For example, if a new column is added to a table, and then an index is created over this newly added column, all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="5a044-161">Durch angeben JET_bitIndexEmpty wird die Überprüfung der Tabelle ausgelassen, was möglicherweise sehr lange dauern kann.</span><span class="sxs-lookup"><span data-stu-id="5a044-161">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-162">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="5a044-162">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="5a044-163">JET_bitIndexUnversioned bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-163">JET_bitIndexUnversioned causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="5a044-164">Normalerweise kann eine Sitzung in einer Transaktion einen Index Erstellungs Vorgang nicht in einer anderen Sitzung sehen.</span><span class="sxs-lookup"><span data-stu-id="5a044-164">Ordinarily, a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="5a044-165">Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a044-165">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="5a044-166">Die zweite Indexerstellung schlägt einfach fehl, anstatt potenziell viele unnötige Daten Bank Vorgänge zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="5a044-166">The second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="5a044-167">Die zweite Transaktion ist möglicherweise nicht in der Lage, den Index sofort zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a044-167">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="5a044-168">Der Index Erstellungs Vorgang muss beendet werden, bevor er verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a044-168">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="5a044-169">Die Sitzung darf sich zurzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a044-169">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-170">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="5a044-170">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="5a044-171">Die Angabe dieses Flags bewirkt, dass <strong>null</strong> -Werte nach den Daten für alle Spalten im Index sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-171">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-172">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="5a044-172">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="5a044-173">Die Angabe dieses Flags wirkt sich auf die Interpretation des LCID/pidxunicde-Union-Felds in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="5a044-173">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="5a044-174">Das Festlegen des Bits bedeutet, dass das Feld pidxunicode tatsächlich auf eine <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="5a044-174">Setting the bit means that the pidxunicode field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="5a044-175">JET_bitIndexUnicode ist nicht erforderlich, um Unicode-Daten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="5a044-175">JET_bitIndexUnicode is not required to index Unicode data.</span></span> <span data-ttu-id="5a044-176">Es ist nur erforderlich, um die Normalisierung von Unicode-Daten anzupassen.</span><span class="sxs-lookup"><span data-stu-id="5a044-176">It is only needed to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-177">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="5a044-177">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="5a044-178">Gibt an, dass der Index ein Tupelindex ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-178">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="5a044-179">Eine Beschreibung eines tupelindexes finden Sie unter <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="5a044-179">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="5a044-180">Der JET_bitIndexTuples Wert wurde im Betriebssystem Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-180">The JET_bitIndexTuples value was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-181">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="5a044-181">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="5a044-182">Die Angabe dieses Flags wirkt sich auf die Interpretation des Union <strong>-Felds cbvarsegmac/ptuplelimits</strong> in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="5a044-182">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="5a044-183">Das Festlegen dieses Bits bedeutet, dass das Feld " <strong>ptuplelimits</strong> " tatsächlich auf eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur verweist, um benutzerdefinierte tupelindexlimits zuzulassen (impliziert JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="5a044-183">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="5a044-184">Der <strong>JET_bitIndexTupleLimits</strong> Wert wurde im Betriebssystem Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-184">The <strong>JET_bitIndexTupleLimits</strong> value was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-185">JET_bitIndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="5a044-185">JET_bitIndexCrossProduct</span></span><br />
<span data-ttu-id="5a044-186">0x00004000</span><span class="sxs-lookup"><span data-stu-id="5a044-186">0x00004000</span></span></p></td>
<td><p><span data-ttu-id="5a044-187">Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-187">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="5a044-188">Andernfalls hätte der Index nur einen Eintrag für jeden mehrwertigen in der signifikantesten Schlüssel Spalte, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten multiwert aus anderen Schlüssel Spalten verwenden, die mehrwertige Spalten sind.</span><span class="sxs-lookup"><span data-stu-id="5a044-188">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multi valued columns.</span></span></p>
<p><span data-ttu-id="5a044-189">Wenn Sie z. B. dieses Flag für einen Index über Spalte a mit den Werten &quot; rot &quot; und &quot; blau &quot; und over column B mit den Werten &quot; 1 &quot; und 2 angegeben &quot; &quot; haben, werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blau &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="5a044-189">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot;, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="5a044-190">Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="5a044-190">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="5a044-191">Der <strong>JET_bitIndexCrossProduct</strong> Wert wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-191">The <strong>JET_bitIndexCrossProduct</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-192">JET_bitIndexKeyMost</span><span class="sxs-lookup"><span data-stu-id="5a044-192">JET_bitIndexKeyMost</span></span><br />
<span data-ttu-id="5a044-193">0x00008000</span><span class="sxs-lookup"><span data-stu-id="5a044-193">0x00008000</span></span></p></td>
<td><p><span data-ttu-id="5a044-194">Die Angabe dieses Flags bewirkt, dass der Index die maximale Schlüsselgröße verwendet, die im Feld <strong>cbkeymost</strong> in der-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-194">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="5a044-195">Andernfalls wird der Index JET_cbKeyMost (255) als maximale Schlüsselgröße verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a044-195">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="5a044-196">Der <strong>JET_bitIndexKeyMost</strong> Wert wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-196">The <strong>JET_bitIndexKeyMost</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-197">JET_bitIndexDisallowTruncation</span><span class="sxs-lookup"><span data-stu-id="5a044-197">JET_bitIndexDisallowTruncation</span></span><br />
<span data-ttu-id="5a044-198">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5a044-198">0x00010000</span></span></p></td>
<td><p><span data-ttu-id="5a044-199">Die Angabe dieses Flags führt dazu, dass jedes Update des Indexes, das zu einem abgeschnittene Schlüssel führt, mit dem JET_errKeyTruncated-Antwort Code fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="5a044-199">Specifying this flag will cause any update to the index that would result in a truncated key to fail with the JET_errKeyTruncated response code.</span></span> <span data-ttu-id="5a044-200">Andernfalls werden Schlüssel automatisch abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="5a044-200">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="5a044-201">Weitere Informationen zum Abschneiden von Schlüsseln finden Sie unter <a href="gg269329(v=exchg.10).md">jetmakekey</a>.</span><span class="sxs-lookup"><span data-stu-id="5a044-201">For more information about key truncation, see <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p>
<p><span data-ttu-id="5a044-202">Der <strong>JET_bitIndexDisallowTruncation</strong> Wert wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-202">The <strong>JET_bitIndexDisallowTruncation</strong> value was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a044-203">**uldensity**</span><span class="sxs-lookup"><span data-stu-id="5a044-203">**ulDensity**</span></span>

<span data-ttu-id="5a044-204">Die prozentuale Dichte des ersten Index B +-Baums.</span><span class="sxs-lookup"><span data-stu-id="5a044-204">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="5a044-205">Wenn Sie eine Zahl angeben, die kleiner als 100 ist, wird zum ersten Mal mehr Speicherplatz zum Erstellen des Indexes verwendet, jedoch kann das zukünftige Wachstum des Indexes vorhanden sein, sodass die interne Fragmentierung vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-205">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="5a044-206">**lcid**</span><span class="sxs-lookup"><span data-stu-id="5a044-206">**lcid**</span></span>

<span data-ttu-id="5a044-207">Der Gebiets Schema Bezeichner (LCID), der bei der Normalisierung der Daten verwendet werden soll, wenn der JET_bitIndexUnicode Wert nicht im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-207">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="5a044-208">Die LCID wirkt sich auf die Normalisierung aus, wenn der Index über Unicode-Spalten ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-208">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="5a044-209">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="5a044-209">**pidxunicode**</span></span>

<span data-ttu-id="5a044-210">Ein Zeiger auf eine [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) Struktur, wenn der JET_bitIndexUnicode Wert im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-210">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="5a044-211">Dies ermöglicht es dem Benutzer, benutzerdefinierte Flags anzugeben, die während der Unicode-Normalisierung an die [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-211">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="5a044-212">**cbvarsegmac**</span><span class="sxs-lookup"><span data-stu-id="5a044-212">**cbVarSegMac**</span></span>

<span data-ttu-id="5a044-213">Die maximale Länge (in Byte) der einzelnen Spalten, die im Index gespeichert werden sollen, wenn der JET_bitIndexTupleLimits Wert nicht im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-213">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="5a044-214">Die Angabe eines Werts von 0 (null) für dieses Feld entspricht Folgendem:</span><span class="sxs-lookup"><span data-stu-id="5a044-214">Specifying a value of 0 (zero) for this field is equivalent to the following:</span></span>

  - <span data-ttu-id="5a044-215">Angeben von JET_cbPrimaryKeyMost für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="5a044-215">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="5a044-216">Angeben von JET_cbSecondaryKeyMost für einen sekundären Index.</span><span class="sxs-lookup"><span data-stu-id="5a044-216">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="5a044-217">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="5a044-217">**ptuplelimits**</span></span>

<span data-ttu-id="5a044-218">Ein Zeiger auf eine [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur, wenn der JET_bitIndexTupleLimits Wert im *grbit* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5a044-218">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="5a044-219">**ptuplelimits** wurde in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-219">**ptuplelimits** was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="5a044-220">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="5a044-220">**rgconditionalcolumn**</span></span>

<span data-ttu-id="5a044-221">Ein optionaler Parameter für ein Array von [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) -Strukturen, die verwendet werden, um die bedingten Spalten im Index anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5a044-221">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="5a044-222">**cconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="5a044-222">**cConditionalColumn**</span></span>

<span data-ttu-id="5a044-223">Die Anzahl der Strukturen im **rgconditionalcolumn** -Array.</span><span class="sxs-lookup"><span data-stu-id="5a044-223">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="5a044-224">**irre**</span><span class="sxs-lookup"><span data-stu-id="5a044-224">**err**</span></span>

<span data-ttu-id="5a044-225">Enthält den Rückgabecode zum Erstellen dieses Indexes.</span><span class="sxs-lookup"><span data-stu-id="5a044-225">Contains the return code for creating this index.</span></span>

<span data-ttu-id="5a044-226">**cbkeymost**</span><span class="sxs-lookup"><span data-stu-id="5a044-226">**cbKeyMost**</span></span>

<span data-ttu-id="5a044-227">Gibt die maximal zulässige Größe für Schlüssel im Index in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="5a044-227">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="5a044-228">Dieser Parameter wird ignoriert, wenn JET_bitIndexKeyMost nicht im *grbit* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5a044-228">This parameter is ignored if JET_bitIndexKeyMost is not specified in *grbit* parameter.</span></span> <span data-ttu-id="5a044-229">Wenn dieser Parameter auf 0 (null) festgelegt ist, und JET_bitIndexKeyMost im *grbit* -Member angegeben wird, schlägt die Aufruf Funktion mit JET_err_InvalidDef fehl.</span><span class="sxs-lookup"><span data-stu-id="5a044-229">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* member, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="5a044-230">Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="5a044-230">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="5a044-231">Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe (JET_paramDatabasePageSize) wie folgt ab:</span><span class="sxs-lookup"><span data-stu-id="5a044-231">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize) as follows:</span></span>

  - <span data-ttu-id="5a044-232">Wenn JET_paramDatabasePageSize = 2048, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="5a044-232">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="5a044-233">Wenn JET_paramDatabasePageSize = 4096, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="5a044-233">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="5a044-234">Wenn JET_paramDatabasePageSize = 8192, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="5a044-234">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="5a044-235">Die maximal unterstützte maximale Schlüsselgröße für die-Instanz kann auch aus dem JET_paramKeyMost System-Parameter gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-235">The maximum supported maximum key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="5a044-236">**cbkeymost** wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-236">**cbKeyMost** was introduced in Windows Vista.</span></span>

<span data-ttu-id="5a044-237">**pspacehints**</span><span class="sxs-lookup"><span data-stu-id="5a044-237">**pSpacehints**</span></span>

<span data-ttu-id="5a044-238">Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5a044-238">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure.</span></span>

<span data-ttu-id="5a044-239">**pspacehints** wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a044-239">**pSpacehints** was introduced in Windows 7.</span></span>

### <a name="remarks"></a><span data-ttu-id="5a044-240">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a044-240">Remarks</span></span>

<span data-ttu-id="5a044-241">ESE unterstützt die Indizierung über Schlüssel Spalten, die mehrere Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="5a044-241">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="5a044-242">Um dieses Feature verwenden zu können, muss es sich bei der Spalte um einen markierten Spaltentyp (JET_bitColumnTagged) handeln, und es muss gekennzeichnet werden, damit die verschiedenen Werte mit JET_bitColumnMultiValued indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-242">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="5a044-243">In Windows-Versionen vor Windows Vista werden die Werte nur für die erste mehrwertige Schlüssel Spalte im Index im Index erweitert.</span><span class="sxs-lookup"><span data-stu-id="5a044-243">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="5a044-244">Für alle anderen mehrwertigen und markierten Spalten werden nur die ersten Werte im Index erweitert.</span><span class="sxs-lookup"><span data-stu-id="5a044-244">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="5a044-245">Angenommen, die folgenden Zeilen sind in einer Tabelle vorhanden (die Spalte Alpha ist nicht mehr wertig, während die Spalten Beta, Gamma und Delta mehr wertig sind), und ein Index wird als "+ Alpha \\ 0 + Beta \\ 0 + Gamma \\ 0 + Delta \\ 0 \\ 0" erstellt:</span><span class="sxs-lookup"><span data-stu-id="5a044-245">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a044-246">Alpha</span><span class="sxs-lookup"><span data-stu-id="5a044-246">Alpha</span></span></p></th>
<th><p><span data-ttu-id="5a044-247">Beta</span><span class="sxs-lookup"><span data-stu-id="5a044-247">Beta</span></span></p></th>
<th><p><span data-ttu-id="5a044-248">Gamma</span><span class="sxs-lookup"><span data-stu-id="5a044-248">Gamma</span></span></p></th>
<th><p><span data-ttu-id="5a044-249">Delta</span><span class="sxs-lookup"><span data-stu-id="5a044-249">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a044-250">1</span><span class="sxs-lookup"><span data-stu-id="5a044-250">1</span></span></p></td>
<td><p><span data-ttu-id="5a044-251">ABC</span><span class="sxs-lookup"><span data-stu-id="5a044-251">ABC</span></span><br />
<span data-ttu-id="5a044-252">GHI</span><span class="sxs-lookup"><span data-stu-id="5a044-252">GHI</span></span><br />
<span data-ttu-id="5a044-253">JKL</span><span class="sxs-lookup"><span data-stu-id="5a044-253">JKL</span></span></p></td>
<td><p><span data-ttu-id="5a044-254">MNO</span><span class="sxs-lookup"><span data-stu-id="5a044-254">MNO</span></span><br />
<span data-ttu-id="5a044-255">PQR</span><span class="sxs-lookup"><span data-stu-id="5a044-255">PQR</span></span><br />
<span data-ttu-id="5a044-256">Stu</span><span class="sxs-lookup"><span data-stu-id="5a044-256">STU</span></span></p></td>
<td><p><span data-ttu-id="5a044-257">Vwx</span><span class="sxs-lookup"><span data-stu-id="5a044-257">VWX</span></span><br />
<span data-ttu-id="5a044-258">YZ</span><span class="sxs-lookup"><span data-stu-id="5a044-258">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-259">2</span><span class="sxs-lookup"><span data-stu-id="5a044-259">2</span></span></p></td>
<td><p><span data-ttu-id="5a044-260">Die</span><span class="sxs-lookup"><span data-stu-id="5a044-260">THE</span></span></p></td>
<td><p><span data-ttu-id="5a044-261">REGEN</span><span class="sxs-lookup"><span data-stu-id="5a044-261">RAIN</span></span><br />
<span data-ttu-id="5a044-262">Spanien</span><span class="sxs-lookup"><span data-stu-id="5a044-262">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="5a044-263">IN</span><span class="sxs-lookup"><span data-stu-id="5a044-263">IN</span></span><br />
<span data-ttu-id="5a044-264">Engpässen</span><span class="sxs-lookup"><span data-stu-id="5a044-264">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a044-265">Die folgenden indextupel werden gespeichert:</span><span class="sxs-lookup"><span data-stu-id="5a044-265">The following index-tuples will be stored:</span></span>

<span data-ttu-id="5a044-266">{1, ABC, MNO, vwx}</span><span class="sxs-lookup"><span data-stu-id="5a044-266">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="5a044-267">{1, ghi, MNO, vwx}</span><span class="sxs-lookup"><span data-stu-id="5a044-267">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="5a044-268">{1, JKL, MNO, vwx}</span><span class="sxs-lookup"><span data-stu-id="5a044-268">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="5a044-269">{2,, Regen, in}</span><span class="sxs-lookup"><span data-stu-id="5a044-269">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="5a044-270">Beachten Sie, dass {2,, Spanien, in} nicht gespeichert wird, auch wenn die Alpha Spalte in der zweiten Zeile einen einzelnen multiwert hat.</span><span class="sxs-lookup"><span data-stu-id="5a044-270">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="5a044-271">In Windows-Versionen ab Windows Vista können alle mehrwertigen Spalten im Index erweitert werden, indem JET_bitIndexCrossProduct angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a044-271">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="5a044-272">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a044-272">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a044-273"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5a044-273"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a044-274">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5a044-274">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-275"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5a044-275"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a044-276">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5a044-276">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a044-277"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5a044-277"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a044-278">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5a044-278">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a044-279"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5a044-279"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5a044-280">Wird als <strong>JET_ INDEXCREATE2_W</strong> (Unicode) und <strong>JET_ INDEXCREATE2_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a044-280">Implemented as <strong>JET_ INDEXCREATE2_W</strong> (Unicode) and <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5a044-281">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a044-281">See also</span></span>

[<span data-ttu-id="5a044-282">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="5a044-282">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="5a044-283">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="5a044-283">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="5a044-284">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5a044-284">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5a044-285">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5a044-285">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5a044-286">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="5a044-286">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="5a044-287">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="5a044-287">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="5a044-288">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="5a044-288">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="5a044-289">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="5a044-289">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="5a044-290">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="5a044-290">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="5a044-291">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="5a044-291">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="5a044-292">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="5a044-292">JetUpdate</span></span>](./jetupdate-function.md)
