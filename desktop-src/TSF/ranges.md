---
title: Bereiche
description: Bereiche
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Text Dienst Framework (TSF), Bereiche
- TSF (Text Dienst Framework), Bereiche
- Text Dienste, Bereiche
- TSF-aktivierte Anwendungen, Bereiche
- ranges
- Text Dienst Framework (TSF), Anker
- TSF (Text Dienst Framework), Anker
- Text Dienste, Anker
- TSF-aktivierte Anwendungen, Anker
- Anker
- Text Dienst Framework (TSF), Klone
- TSF (Text Dienst Framework), Klone
- Text Dienste, Klone
- TSF-aktivierte Anwendungen, Klone
- klässler
- Text Dienst Framework (TSF), Sicherungen
- TSF (Text Dienst Framework), Sicherungen
- Text Dienste, Sicherungen
- TSF-aktivierte Anwendungen, Sicherungen
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948056"
---
# <a name="ranges"></a><span data-ttu-id="02765-123">Bereiche</span><span class="sxs-lookup"><span data-stu-id="02765-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="02765-124">Anchors</span><span class="sxs-lookup"><span data-stu-id="02765-124">Anchors</span></span>

<span data-ttu-id="02765-125">Ein Bereich wird durch zwei *Anker*, einen Start Anker und einen endanker getrennt.</span><span class="sxs-lookup"><span data-stu-id="02765-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="02765-126">Ein Anker ist in einem imaginären Slot zwischen zwei Zeichen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="02765-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="02765-127">Der Start Anker bezieht sich auf Text, der auf den Anker folgt, und der endanker bezieht sich auf Text, der dem Anker vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="02765-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="02765-128">Der Start-und der endanker können am gleichen Speicherort vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="02765-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="02765-129">In diesem Fall hat der Bereich eine Länge von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="02765-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="02765-130">Beginnen Sie z. b. mit folgendem Text:</span><span class="sxs-lookup"><span data-stu-id="02765-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="02765-131">Wenden Sie nun einen Bereich auf diesen Text mit dem Start-und endanker an Position 0 an.</span><span class="sxs-lookup"><span data-stu-id="02765-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="02765-132">Sie wird visuell wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="02765-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="02765-133">Die Anker beanspruchen keinen Platz im Text selbst.</span><span class="sxs-lookup"><span data-stu-id="02765-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="02765-134">Dies ist ein Bereich der Länge 0 (null), und der zugehörige Text ist leer.</span><span class="sxs-lookup"><span data-stu-id="02765-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="02765-135">Verschieben Sie nun die endanker + 3 Positionen.</span><span class="sxs-lookup"><span data-stu-id="02765-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="02765-136">Sie wird visuell wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="02765-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="02765-137">Der Start Anker wird direkt vor dem Zeichen an Position 0 positioniert, und der endananker wird direkt hinter das Zeichen an Position 3 positioniert, da der endenanchor an die drei Positionen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="02765-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="02765-138">Der Textbereich ist jetzt "Thi".</span><span class="sxs-lookup"><span data-stu-id="02765-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="02765-139">Darüber hinaus kann der Start Anker nicht so fest gemacht werden, dass er auf den Enden Anker folgt, und der endanker kann nicht vor dem Start Anker stehen.</span><span class="sxs-lookup"><span data-stu-id="02765-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="02765-140">Anker Schwergewicht</span><span class="sxs-lookup"><span data-stu-id="02765-140">Anchor Gravity</span></span>

<span data-ttu-id="02765-141">Jeder Anker verfügt über eine *schwere* Grad Einstellung, die bestimmt, wie der Anker antwortet, wenn Text an der Ankerposition in den Textstream eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="02765-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="02765-142">Wenn eine Einfügung an der Position eines Ankers erfolgt, muss an der Position des Ankers eine Anpassung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="02765-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="02765-143">Die Schwerkraft bestimmt, wie diese Anker Positions Anpassung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="02765-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="02765-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="02765-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="02765-145">Wenn das Wort "very" an der Bereichs Position eingefügt wird, kann der Start Anker entweder vor oder nach dem eingefügten Wort positioniert werden:</span><span class="sxs-lookup"><span data-stu-id="02765-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="02765-146">\- Oder –</span><span class="sxs-lookup"><span data-stu-id="02765-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="02765-147">Die Anker Gravitation gibt an, wie der Anker neu positioniert wird, wenn an seiner Position eine Einfügung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="02765-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="02765-148">Die Schwerkraft kann entweder *rückwärts* oder *Vorwärts* sein.</span><span class="sxs-lookup"><span data-stu-id="02765-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="02765-149">Wenn der Anker eine abwärts Gravitation hat, wird der Anker nach hinten verschoben, relativ zur Einfügemarke, sodass der eingefügte Text dem Anker folgt:</span><span class="sxs-lookup"><span data-stu-id="02765-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="02765-150">Wenn der Anker eine vorwärts Gravitation hat, wechselt der Anker (relativ zur Einfügemarke) beim Einfügen, sodass der eingefügte Text vor dem Anker liegt:</span><span class="sxs-lookup"><span data-stu-id="02765-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="02765-151">Klone und Sicherungen</span><span class="sxs-lookup"><span data-stu-id="02765-151">Clones and Backups</span></span>

<span data-ttu-id="02765-152">Es gibt zwei Möglichkeiten, eine "Kopie" eines Range-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02765-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="02765-153">Der erste besteht darin, einen *Klon* des Bereichs mithilfe von " [itfrange:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone)" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02765-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="02765-154">Die zweite besteht darin, eine *Sicherung* des Bereichs mithilfe von [ITfContext:: "" ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup)"" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02765-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="02765-155">Ein Klon ist eine Kopie eines Bereichs, der keine statischen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="02765-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="02765-156">Die Anker des Bereichs werden kopiert, aber der Klon deckt weiterhin einen Textbereich innerhalb des Kontexts ab.</span><span class="sxs-lookup"><span data-stu-id="02765-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="02765-157">Ein Klon ist in jeder Hinsicht ein Bereichs Objekt.</span><span class="sxs-lookup"><span data-stu-id="02765-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="02765-158">Dies bedeutet, dass der Text und die Eigenschaften für einen geklonten Bereich dynamisch sind und sich ändern, wenn sich der Text und/oder die Eigenschaften des vom Klon abgedeckten Bereichs ändern.</span><span class="sxs-lookup"><span data-stu-id="02765-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="02765-159">Eine Sicherung speichert den Text und die Eigenschaften eines Bereichs zu dem Zeitpunkt, zu dem die Sicherung als statische Daten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="02765-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="02765-160">Eine Sicherung klont auch den ursprünglichen Bereich, sodass Änderungen an der Größe und Position des ursprünglichen Bereichs nachverfolgt werden können.</span><span class="sxs-lookup"><span data-stu-id="02765-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="02765-161">Dies bedeutet, dass der Text und die Eigenschaften für einen gesicherten Bereich statisch sind und sich nicht ändern, wenn sich der Text und/oder die Eigenschaften des von der Sicherung behandelten Bereichs ändern.</span><span class="sxs-lookup"><span data-stu-id="02765-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="02765-162">Beispielsweise der folgende Bereich (Prange) innerhalb des Kontexts:</span><span class="sxs-lookup"><span data-stu-id="02765-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="02765-163">Erstellen Sie jetzt einen Klon und eine Sicherung dieses Bereichs:</span><span class="sxs-lookup"><span data-stu-id="02765-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="02765-164">Nun enthalten die Objekte Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02765-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="02765-165">Ändern Sie nun den Text von Prange:</span><span class="sxs-lookup"><span data-stu-id="02765-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="02765-166">Nun enthalten die Objekte Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02765-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="02765-167">Das Festlegen des Texts hat bewirkt, dass der Text im Kontext geändert wird.</span><span class="sxs-lookup"><span data-stu-id="02765-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="02765-168">Außerdem wurde die Änderung des enden Ankers von Prange und pclone bewirkt.</span><span class="sxs-lookup"><span data-stu-id="02765-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="02765-169">pclone enthält jetzt "andere Wörter", da sich der Text innerhalb des Bereichs geändert hat und diese Änderungen von allen Bereichen nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="02765-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="02765-170">Wenn sich der von "Prange" und "pclone" behandelte Text geändert hat, wurde auch der Text des pclone geändert.</span><span class="sxs-lookup"><span data-stu-id="02765-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="02765-171">Der Text in pbackup wurde nicht vom ursprünglichen Prange geändert, da die Daten (Text und Eigenschaften) in der Sicherung nicht mit dem Kontext verknüpft sind und separat gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="02765-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="02765-172">Der in der Sicherung enthaltene Klon ändert sich tatsächlich, aber die Daten sind statisch.</span><span class="sxs-lookup"><span data-stu-id="02765-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="02765-173">Beim Wiederherstellen einer Sicherung kann die Sicherung auf den Klon innerhalb der Sicherung oder auf einen anderen Bereich vollständig angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="02765-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="02765-174">Um die Sicherung auf den Klon innerhalb der Sicherung anzuwenden, übergeben Sie **null** an [itfrangebackup:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , wie im folgenden Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="02765-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="02765-175">Nun enthalten die Objekte Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02765-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="02765-176">Wenn Sie die Sicherung in einem anderen Bereich wiederherstellen möchten, übergeben Sie beim Aufrufen von **itfrangebackup:: Restore** einen Zeiger auf das Bereichs Objekt.</span><span class="sxs-lookup"><span data-stu-id="02765-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="02765-177">Der gesicherte Text und die Eigenschaften werden auf den neuen Bereich angewendet.</span><span class="sxs-lookup"><span data-stu-id="02765-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="02765-178">Beispielsweise wird für die Verwendung des obigen Beispiels vor dem **Wiederherstellungs** Vorgang Prange geändert, um Folgendes zu veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="02765-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="02765-179">Nun enthalten die Objekte Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02765-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="02765-180">Wenn der endanker von Prange an zwei Stellen verschoben wurde, hat sich der Endpunkt des pclone nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="02765-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="02765-181">Stellen Sie nun die Sicherung mithilfe von Prange mit dem folgenden Codebeispiel wieder her:</span><span class="sxs-lookup"><span data-stu-id="02765-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="02765-182">Nun enthalten die Objekte Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02765-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="02765-183">Der von Prange abgedeckte Text wurde durch "Text" ersetzt, ein Teil des von pclone abgedeckten Texts hat sich geändert, und pbackup ändert sich entsprechend der Prange.</span><span class="sxs-lookup"><span data-stu-id="02765-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 




