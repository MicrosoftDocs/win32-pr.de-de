---
description: Ein Bereichspräfix ist eine Textbezeichnung, die einem Schemaschlüsselwort vorangestellt ist, um einen kontextbezogenen Bereich bereitzustellen, einschließlich Auftrag, Dokument und Seite.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Bereichspräfix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c027de94fda403eb58905e536d8c6256cb2d6c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404903"
---
# <a name="scoping-prefix"></a>Bereichspräfix

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Bereichspräfix ist eine Textbezeichnung, die einem Schemaschlüsselwort vorangestellt ist, um einen kontextbezogenen Bereich bereitzustellen. Dies ermöglicht das Abonnieren eines bestimmten und wohlverstandenen Kontexts für Schlüsselwörter auf vordefinierte Weise. Druckschemafunktion, ParameterDef, ParameterInit und ParameterRef und Eigenschaftsschlüsselwortelemente auf Stammebene MÜSSEN eines der folgenden Bereichspräfixe aufweisen: "Job", "Document" oder "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretation des Bereichspräfixes mit PrintTicket-Inhalt

Das PrintTicket kann in drei Inhaltsebenen unterteilt werden, die den Auftrag auf hoher Ebene, die Dokumente im Auftrag und die Seiten in den einzelnen Dokumenten darstellen. Diese Ebenen werden nach Spezifität eingestuft. Die Auftragsebene ist am allgemeinsten, dann die Dokumentebene und dann die Seitenebene am spezifischsten. Ein Auftrag besteht aus einem oder mehreren Dokumenten und ein Dokument aus mindestens einer Seite.

## <a name="job-level-prefix"></a>Präfix auf Auftragsebene

Ein Ticket auf Auftragsebene enthält alle Einstellungen für die Auftragsformatierung, die für einen gesamten Auftrag gelten sollen. Alle Elemente mit Bereichspräfixen "Job", "Document" oder "Page" sind in einem Ticket auf Auftragsebene zulässig.

Die in einem Auftragsebenenticket angegebenen Einstellungen mit dem Präfix "Dokument" und "Seite" werden automatisch auf die Tickets auf Dokument- und Seitenebene angewendet.

## <a name="document-level-prefix"></a>Präfix auf Dokumentebene

Das Ticket auf Dokumentebene enthält alle Einstellungen für die Auftragsformatierung, die für ein oder mehrere Dokumente in einem Auftrag gelten sollen. Dazu können Einstellungen gehören, die zuvor im Ticket für die Auftragsebene angegeben wurden. Nur Elemente mit Bereichspräfixen "Dokument" oder "Seite" sind in einem Ticket auf Dokumentebene zulässig.

Ein Ticket auf Dokumentebene kann Einstellungen mit Dokumentpräfix enthalten, die zuvor vom Ticket auf Auftragsebene angegeben wurden.

## <a name="page-level-prefix"></a>Präfix auf Seitenebene

Das Ticket auf Seitenebene enthält alle Einstellungen für die Auftragsformatierung, die für eine oder mehrere Seiten eines Auftrags gelten sollen (nicht auf ein einzelnes Dokument beschränkt). Dies können Einstellungen sein, die zuvor im Auftrags- oder Dokumentebenenticket angegeben wurden. In einem Ticket auf Seitenebene sind nur Elemente mit Bereichspräfixen von "Page" zulässig.

Ein Ticket auf Seitenebene kann Einstellungen mit dem Präfix "Page" enthalten, die zuvor durch das Ticket auf Auftragsebene und/oder das Ticket auf Dokumentebene angegeben wurden.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Präfixverwendung in einem PrintTicket- oder Print Capabilities-Dokument

PrintTicket- und PrintCapabilities-Dokumente DÜRFEN NICHT mehrere Schlüsselwörter enthalten, die sich nur im Bereichspräfix unterscheiden. Beispielsweise DARF für ein PrintCapabilities-Dokument NICHT sowohl JobInputBin als auch PageInputBin angegeben sein. Für ein Dokument mit Druckfunktionen können jedoch sowohl JobDuplexAllDocumentsContiguously als auch DocumentDuplex angegeben werden, da diese als unterschiedliche Features betrachtet werden, da sie ein abweichendes Verhalten aufweisen. Dieses Beispiel gilt auch für ein einzelnes PrintTicket.

## <a name="prefix-conflict-management"></a>Präfixkonfliktverwaltung

Ein Schlüsselwortkonflikt zwischen Einstellungen wird als dasselbe Druckschemaelement auf Stammebene definiert, das durch das XML-Attribut "Name" bezeichnet wird und in mehreren Level-Tickets angezeigt wird. Wenn kein Konflikt vorliegt, kann ein präfixbezogenes Element von einem allgemeineren Ticket auf ein spezifischeres Ticket gepusht oder geerbt werden. Wenn ein Konflikt vorliegt, hat die Einstellung des spezifischsten Tickets Vorrang. Das heißt, dass die Einstellungen pro Seite in einem Ticket auf Seitenebene die identischen Einstellungen pro Seite in einem Dokument- oder Auftragsebenenticket überschreiben. Auf ähnliche Weise haben Dokumenteinstellungen im Ticket auf Dokumentebene Vorrang vor Dokumenteinstellungen im Auftragsebenenticket.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



