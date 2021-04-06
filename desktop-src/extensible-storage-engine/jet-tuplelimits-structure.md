---
description: 'Weitere Informationen finden Sie hier: JET_TUPLELIMITS Struktur'
title: JET_TUPLELIMITS Struktur
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960863"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="5ec4e-103">JET_TUPLELIMITS Struktur</span><span class="sxs-lookup"><span data-stu-id="5ec4e-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="5ec4e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5ec4e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="5ec4e-105">JET_TUPLELIMITS Struktur</span><span class="sxs-lookup"><span data-stu-id="5ec4e-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="5ec4e-106">Die **JET_TUPLELIMITS** -Struktur ermöglicht die Anpassung der tupelindexmerkmale auf Index Basis und nicht pro Instanz mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ec4e-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="5ec4e-107">**Windows Server 2003:** Die **JET_TUPLELIMITS** Struktur wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="5ec4e-108">Member</span><span class="sxs-lookup"><span data-stu-id="5ec4e-108">Members</span></span>

<span data-ttu-id="5ec4e-109">**chverlängert**</span><span class="sxs-lookup"><span data-stu-id="5ec4e-109">**chLengthMin**</span></span>

<span data-ttu-id="5ec4e-110">Die minimale Länge eines Tupels.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-110">The minimum length of a tuple.</span></span> <span data-ttu-id="5ec4e-111">Der Standardwert ist 3.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-111">The default value is 3.</span></span>

<span data-ttu-id="5ec4e-112">**chlängen Max**</span><span class="sxs-lookup"><span data-stu-id="5ec4e-112">**chLengthMax**</span></span>

<span data-ttu-id="5ec4e-113">Die maximale Länge eines Tupels.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-113">The maximum length of a tuple.</span></span> <span data-ttu-id="5ec4e-114">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-114">The default value is 10.</span></span>

<span data-ttu-id="5ec4e-115">**Chum indexmax**</span><span class="sxs-lookup"><span data-stu-id="5ec4e-115">**chToIndexMax**</span></span>

<span data-ttu-id="5ec4e-116">Die maximale Länge einer Zeichenfolge, die indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-116">The maximum length of a string to index.</span></span> <span data-ttu-id="5ec4e-117">Wenn eine Spalte z. b. 100 Zeichen lang ist und **chchanindexmax** auf 60 festgelegt ist, werden nur die ersten 60 Zeichen der Spalte indiziert.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="5ec4e-118">Der Standardwert ist 32767.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-118">The default value is 32767.</span></span>

<span data-ttu-id="5ec4e-119">**cchincrement**</span><span class="sxs-lookup"><span data-stu-id="5ec4e-119">**cchIncrement**</span></span>

<span data-ttu-id="5ec4e-120">Dadurch kann der Stride auf Index Basis konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="5ec4e-121">**Windows Vista:** Der **cchincrement** -Member wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="5ec4e-122">Vor Windows Vista war der Betrag zum Verschieben des Fensters ("stride") immer 1, wie im Beispiel im Abschnitt "Hinweise" gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="5ec4e-123">**ichstart**</span><span class="sxs-lookup"><span data-stu-id="5ec4e-123">**ichStart**</span></span>

<span data-ttu-id="5ec4e-124">Der Offset im Wert, mit dem das Abrufen von Tupeln aus dem Wert begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="5ec4e-125">**Windows Vista:** Das Mitglied " **ichstart** " wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="5ec4e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ec4e-126">Remarks</span></span>

<span data-ttu-id="5ec4e-127">Ein Tupelindex durchläuft eine Zeichenfolge und indiziert alle möglichen Teil Zeichenfolgen von **chlängen Max**.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="5ec4e-128">Am Ende der Zeichenfolge (oder an der Position **chinindexmax**, je nachdem, welcher Wert zuerst auftritt) werden die Teil Zeichenfolgen von mindestens **chlängen min** indiziert.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="5ec4e-129">Ein Tupelindex kann verwendet werden, um Zeichen folgen mit führenden und nachfolgenden Platzhaltern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="5ec4e-130">Wenn in einer Zeile mit dem Textfeld "Regen in Spanien \! " ein Tupelindex mit den Parametern " **chverlänmin**= 2" und " **chlängen Max**= 3" erstellt wird, werden die folgenden Einträge im Index erstellt:</span><span class="sxs-lookup"><span data-stu-id="5ec4e-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="5ec4e-131">Darstellt</span><span class="sxs-lookup"><span data-stu-id="5ec4e-131">"RAI"</span></span>  
<span data-ttu-id="5ec4e-132">Porzellan</span><span class="sxs-lookup"><span data-stu-id="5ec4e-132">"AIN"</span></span>  
<span data-ttu-id="5ec4e-133">IN</span><span class="sxs-lookup"><span data-stu-id="5ec4e-133">"IN "</span></span>  
<span data-ttu-id="5ec4e-134">"N I"</span><span class="sxs-lookup"><span data-stu-id="5ec4e-134">"N I"</span></span>  
<span data-ttu-id="5ec4e-135">IN</span><span class="sxs-lookup"><span data-stu-id="5ec4e-135">" IN"</span></span>  
<span data-ttu-id="5ec4e-136">IN</span><span class="sxs-lookup"><span data-stu-id="5ec4e-136">"IN "</span></span>  
<span data-ttu-id="5ec4e-137">"N S"</span><span class="sxs-lookup"><span data-stu-id="5ec4e-137">"N S"</span></span>  
<span data-ttu-id="5ec4e-138">El</span><span class="sxs-lookup"><span data-stu-id="5ec4e-138">" SP"</span></span>  
<span data-ttu-id="5ec4e-139">Hotel</span><span class="sxs-lookup"><span data-stu-id="5ec4e-139">"SPA"</span></span>  
<span data-ttu-id="5ec4e-140">Kampagnen</span><span class="sxs-lookup"><span data-stu-id="5ec4e-140">"PAI"</span></span>  
<span data-ttu-id="5ec4e-141">Porzellan</span><span class="sxs-lookup"><span data-stu-id="5ec4e-141">"AIN"</span></span>  
<span data-ttu-id="5ec4e-142">"In \! "</span><span class="sxs-lookup"><span data-stu-id="5ec4e-142">"IN\!"</span></span>  
<span data-ttu-id="5ec4e-143">"N \! "</span><span class="sxs-lookup"><span data-stu-id="5ec4e-143">"N\!"</span></span>

<span data-ttu-id="5ec4e-144">Beachten Sie, dass "in" zweimal auftritt und dass der letzte Eintrag ("N \! ") kürzer als 3 (**chlängen Max**) ist.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="5ec4e-145">Beachten Sie außerdem, dass der Teilungs Algorithmus keine Leerzeichen oder Wörter kennt und alle Zeichen identisch behandelt.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="5ec4e-146">**Windows XP:** Windows XP unterstützt tupelindizes, verfügt jedoch nicht über **JET_TUPLELIMITS**.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="5ec4e-147">Die Datenbank-Engine verwendet die Standardwerte (**chverlänmin**= 3, **chlängen Max**= 10, **chdeindexmax**= 32767).</span><span class="sxs-lookup"><span data-stu-id="5ec4e-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="5ec4e-148">Es ist immer noch möglich, diese Werte zu ändern, aber Sie werden auf instanzbasis mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)und [JET_paramIndexTuplesToIndexMax](./index-parameters.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="5ec4e-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ec4e-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ec4e-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5ec4e-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5ec4e-151">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ec4e-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5ec4e-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5ec4e-153">Erfordert Windows Server 2008, Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ec4e-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5ec4e-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5ec4e-155">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5ec4e-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5ec4e-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ec4e-156">See Also</span></span>

[<span data-ttu-id="5ec4e-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="5ec4e-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="5ec4e-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="5ec4e-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="5ec4e-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="5ec4e-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="5ec4e-160">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="5ec4e-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
