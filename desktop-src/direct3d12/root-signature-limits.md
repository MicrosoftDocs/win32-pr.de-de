---
title: Stamm Signatur Limits
description: Bei der Stamm Signatur handelt es sich um Primzahlen, und es sind strikte Grenzwerte und Kosten zu beachten.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104146"
---
# <a name="root-signature-limits"></a>Stamm Signatur Limits

Bei der Stamm Signatur handelt es sich um Primzahlen, und es sind strikte Grenzwerte und Kosten zu beachten.

-   [Arbeitsspeicher Grenzwerte und-Kosten](#memory-limits-and-costs)
-   [Leistungskosten](#performance-costs)
-   [Statische Samplern](#static-samplers)
-   [Verwandte Themen](#related-topics)

## <a name="memory-limits-and-costs"></a>Arbeitsspeicher Grenzwerte und-Kosten

Die maximale Größe einer Stamm Signatur beträgt 64 DWORDs.

Diese maximale Größe wird ausgewählt, um den Missbrauch der Stamm Signatur als Möglichkeit zum Speichern von Massendaten zu verhindern. Jeder Eintrag in der Stamm Signatur hat eine Kosten für dieses 64 DWORD-Limit:

-   Deskriptortabellen Kosten jeweils 1 DWORD.
-   Stamm konstanten Kosten jeweils 1 DWORD, da es sich um 32-Bit-Werte handelt.
-   Stamm Deskriptoren (64-Bit-GPU-virtuelle Adressen) Kosten 2 DWords jeweils.

Statische Samplern haben keine Kosten in der Größe der Stamm Signatur.

## <a name="performance-costs"></a>Leistungskosten

Die Leistungseinbußen (im Hinblick auf dereferenzierungsstufen) sind für eine Stamm Konstante (1 für einen Stamm Deskriptor und 2 für eine Deskriptortabelle) gleich 0 (null). Wenn eine Stamm Signatur groß ist und aus dem schnellsten Arbeitsspeicher zu einem etwas langsameren Arbeitsspeicher fließt (was auf Hardware auftreten kann), fügen Sie den Leistungskosten für die überfließenden Elemente am Ende der Stamm Signatur 1 hinzu.

Ein Überlauf kann auf Hardware auftreten, die z. b. eine festgelegte Größe von 16 DWords für das Root-Argument Raum aufweisen könnte. Diese Beschränkung wird möglicherweise um 1 reduziert, wenn der Eingabe Assembler verwendet wird. In diesem Fall gibt es einen Überlauf in etwas langsameren Arbeitsspeicher, wenn die Stamm Signatur für den 15-oder 16-ten DWORD-Speicher zu groß ist. In anderer Hardware gibt es keinen systeminternen Stamm Argument Speicher (d. h., die Überlauf Situation tritt nie auf).

Wenn sich ein root-Argument ändert, muss der Treiber für alle Hardware eine Version aller root-Argumente verwalten (im Gegensatz zu anderen speichern, wie z. b. deskriptorheaps und Puffer Ressourcen, die nicht vom Treiber versioniert werden). Bei der Hardware, bei der eine Überlauf Situation auftritt, muss nur der systemeigene oder Überlauf Bereich mit Versions Angabe versehen werden, je nachdem, wo die Änderung aufgetreten ist. Der Umfang der Versionsverwaltung sollte offensichtlich auf das erforderliche Minimum beschränkt werden.

Im Allgemeinen sollten Sie die folgenden Richtlinien beachten:

-   Verwenden Sie bei Bedarf eine kleine Stamm Signatur, aber ausgleichen Sie dies mit der Flexibilität einer größeren Stamm Signatur.
-   Anordnen von Parametern in einer großen Stamm Signatur, sodass die Parameter wahrscheinlich häufig geändert werden oder wenn eine geringe Zugriffs Latenz für einen bestimmten Parameter wichtig ist, treten zuerst auf.
-   Verwenden Sie ggf. Stamm Konstanten oder Stamm Konstanten-Puffer Sichten, um konstante Puffer Sichten in einem deskriptorheap zu platzieren.

## <a name="static-samplers"></a>Statische Samplern

Statische Samplern (Samplern, bei denen der Zustand vollständig definiert und unveränderlich ist) sind Teil der Stamm Signaturen, werden jedoch nicht in Bezug auf das 64 DWORD-Limit gezählt. Wenn ein Sampler als statisch definiert werden kann, ist es nicht erforderlich, dass der Sampler Teil eines deskriptorheaps ist.

Es gibt keine Leistungseinbußen bei der Verwendung statischer Samplern, und eine Stamm Signatur kann eine Mischung aus statischen Samplern (gespeichert in der Stamm Signatur oder in reserviertem Speicherplatz auf Hardware) und dynamischen Samplern (die in einem Sampler-deskriptorheap gespeichert sind) enthalten. Samplern in einem deskriptorheap können dynamisch zugewiesen und indiziert werden, welche statischen Samplern nicht.

Statische samplz können als Teil der Stamm Signatur in HLSL-Shadern geschrieben werden (Weitere Informationen finden Sie unter Angeben von Stamm [Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 




