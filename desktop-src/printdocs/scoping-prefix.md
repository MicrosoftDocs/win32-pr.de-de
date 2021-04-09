---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Bereichs Präfix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef74be192671124872e19e87973a266da4a09226
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869624"
---
# <a name="scoping-prefix"></a>Bereichs Präfix

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein Bereichs Präfix ist eine Text Bezeichnung, die an ein Schema Schlüsselwort angefügt wird, um einen kontextbezogenen Bereich bereitzustellen. Dies ermöglicht das Zuordnen eines bestimmten und gut verständlichen Kontexts zu Schlüsselwörtern auf vordefinierte Weise. Die Attribute "Print Schema Feature", "ParameterDef", "parameterinit" und "ParameterRef" und "Property Keywords" der Stamm Ebene müssen einen der folgenden Bereichs Präfixe aufweisen: "Job", "Document" oder "page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretation des Bereichs Präfixes mit PrintTicket-Inhalt

Print Ticket kann in drei Inhalts Ebenen aufgeteilt werden, die den auf hoher Ebene, die Dokumente im Auftrag und die Seiten in den einzelnen Dokumenten darstellen. Diese Ebenen werden entsprechend der Spezifizität sortiert. die Auftrags Ebene ist die allgemeinste, dann die Dokument Ebene und dann die Seitenebene. Ein Auftrag besteht aus einem oder mehreren Dokumenten, und ein Dokument besteht aus einer oder mehreren Seiten.

## <a name="job-level-prefix"></a>Präfix auf Auftrags Ebene

Ein Ticket auf Auftrags Ebene enthält alle Auftrags Formatierungs Einstellungen, die für den gesamten Auftrag gelten sollen. Alle Elemente mit den Bereichs Präfixen "Job", "Document" oder "page" sind in einem Ticket auf Auftrags Ebene zulässig.

Die in einem Ticket auf der Auftrags Ebene angegebenen Einstellungen für "Dokument" und "Seite" werden automatisch auf die Tickets auf Dokument-und Seitenebene angewendet.

## <a name="document-level-prefix"></a>Präfix auf Dokument Ebene

Das Ticket auf Dokument Ebene enthält alle Auftrags Formatierungs Einstellungen, die auf ein oder mehrere Dokumente in einem Auftrag angewendet werden sollen. Diese können Einstellungen enthalten, die zuvor im Ticket auf Auftrags Ebene angegeben wurden. Nur Elemente mit Bereichs Präfixen "Document" oder "page" sind in einem Ticket auf Dokument Ebene zulässig.

Ein Ticket auf Dokument Ebene kann zuvor durch das Ticket auf Auftrags Ebene angegebene Einstellungen für ein Dokument mit Präfix enthalten.

## <a name="page-level-prefix"></a>Präfix auf Seitenebene

Das Ticket auf Seitenebene umfasst alle Auftrags Formatierungs Einstellungen, die auf eine oder mehrere Seiten eines Auftrags angewendet werden sollen (nicht auf ein einzelnes Dokument beschränkt). Diese können Einstellungen enthalten, die zuvor im Ticket für die Auftrags-oder Dokument Ebene angegeben wurden. Nur Elemente mit Bereichs Präfixen "page" sind in einem Ticket auf Seitenebene zulässig.

Ein Ticket auf Seitenebene kann "page"-Einstellungen enthalten, die zuvor durch das Ticket auf Auftrags Ebene und/oder das Ticket auf Dokument Ebene festgelegt wurden.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Präfix Verwendung innerhalb eines PrintTicket-oder Druck Funktions Dokuments

Die Dokumente PrintTicket und Print-Funktionen dürfen nicht mehrere Schlüsselwörter enthalten, die sich nur im Bereichs Präfix unterscheiden. Beispielsweise darf für ein printfunktionalitäten-Dokument nicht sowohl "JobInputBin" als auch "paginput bin" angegeben werden. Für ein Dokument mit Druckfunktionen sind jedoch möglicherweise sowohl "jobduplexalldocumentscontiguron" als auch "DocumentDuplex" angegeben, da diese als verschiedene Merkmale angesehen werden, da Sie unterschiedliche Verhaltensweisen aufweisen? Dieses Beispiel gilt auch für ein einzelnes Print Ticket.

## <a name="prefix-conflict-management"></a>Präfix Konflikt Verwaltung

Ein Schlüsselwort Konflikt zwischen Einstellungen wird als definiert, das gleiche Druck Schema Element auf Stamm Ebene, das durch das XML-Attribut "Name" gekennzeichnet ist, das in Tickets mit mehreren Ebenen angezeigt wird. Wenn kein Konflikt vorliegt, kann ein Element mit Präfix Bereich von einem allgemeineren Ticket zu einem spezifischeren Ticket herunter geschoben oder geerbt werden. Tritt ein Konflikt auf, hat die Einstellung des spezifischsten Tickets Vorrang. Das heißt, pro Seiteneinstellungen in einem Ticket auf Seitenebene überschreiben die identischen Einstellungen pro Seite in einem Dokument oder auf einem Ticket auf Auftrags Ebene. Ebenso haben Dokument Einstellungen im Ticket auf Dokument Ebene Vorrang vor Dokument Einstellungen im Ticket auf Auftrags Ebene.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



