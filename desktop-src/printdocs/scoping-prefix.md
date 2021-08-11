---
description: Ein Bereichspräfix ist eine Textbezeichnung, die einem Schemaschlüsselwort vorangestellt ist, um einen kontextbezogenen Bereich, einschließlich Auftrag, Dokument und Seite, zu bieten.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Bereichspräfix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad23369d2b2c60c00752e4f5be31f6ad605e2814d0b7502d42ff79baa10977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234093"
---
# <a name="scoping-prefix"></a>Bereichspräfix

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein Bereichspräfix ist eine Textbezeichnung, die einem Schemaschlüsselwort vorangestellt ist, um einen kontextbezogenen Bereich zu bieten. Dies ermöglicht das Abonnieren eines bestimmten und gut verständlichen Kontexts für Schlüsselwörter auf vordefinierte Weise. Druckschemafeature, ParameterDef, ParameterInit und ParameterRef sowie Property-Schlüsselwortelemente auf Stammebene MÜSSEN eines der folgenden Bereichspräfixe aufweisen: "Job", "Document" oder "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretation des Bereichspräfixes mit PrintTicket-Inhalt

Das PrintTicket kann in drei Inhaltsebenen unterbrochen werden, die den Auftrag auf hoher Ebene, die Dokumente im Auftrag und die Seiten in jedem Dokument darstellen. Diese Ebenen werden nach Spezifizität eingestuft. Die Auftragsebene ist am allgemeinsten, dann die Dokumentebene und dann die Seitenebene am spezifischsten. Ein Auftrag besteht aus einem oder mehreren Dokumenten, und ein Dokument besteht aus mindestens einer Seite.

## <a name="job-level-prefix"></a>Präfix auf Auftragsebene

Ein Ticket auf Auftragsebene enthält alle Auftragsformatierungseinstellungen, die für einen gesamten Auftrag gelten sollen. Alle Elemente mit bereichspräfixen "Job", "Document" oder "Page" sind in einem Ticket auf Auftragsebene zulässig.

Die in einem Ticket auf Auftragsebene angegebenen Einstellungen "Dokument" und "Seite" werden automatisch auf die Tickets auf Dokument- und Seitenebene angewendet.

## <a name="document-level-prefix"></a>Präfix auf Dokumentebene

Das Dokumentebenenticket enthält alle Auftragsformatierungseinstellungen, die für ein oder mehrere Dokumente in einem Auftrag gelten sollen. Dies kann Einstellungen enthalten, die zuvor im Ticket auf Auftragsebene angegeben wurden. Nur Elemente mit bereichspräfixen "Document" oder "Page" sind in einem Ticket auf Dokumentebene zulässig.

Ein Dokumentebenenticket kann Einstellungen mit Dokumentpräfix enthalten, die zuvor durch das Ticket auf Auftragsebene angegeben wurden.

## <a name="page-level-prefix"></a>Präfix auf Seitenebene

Das Ticket auf Seitenebene enthält alle Einstellungen für die Auftragsformatierung, die auf eine oder mehrere Seiten eines Auftrags angewendet werden sollen (nicht auf ein einzelnes Dokument beschränkt). Dies kann Einstellungen enthalten, die zuvor im Ticket auf Auftrags- oder Dokumentebene angegeben wurden. Nur Elemente mit Bereichspräfixen von "Page" sind in einem Ticket auf Seitenebene zulässig.

Ein Ticket auf Seitenebene kann Einstellungen mit dem Präfix "Page" enthalten, die zuvor durch das Ticket auf Auftragsebene und/oder das Ticket auf Dokumentebene angegeben wurden.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Präfixverwendung in einem PrintTicket- oder Druckfunktionendokument

PrintTicket- und PrintCapabilities-Dokumente DÜRFEN NICHT mehrere Schlüsselwörter enthalten, die sich nur im Bereichspräfix unterscheiden. Für ein PrintCapabilities-Dokument DÜRFEN z. B. NICHT sowohl JobInputBin als auch PageInputBin angegeben sein. In einem Dokument mit Druckfunktionen können jedoch sowohl JobDuplexAllDocumentsContiguously als auch DocumentDuplex angegeben werden, da diese als unterschiedliche Features betrachtet werden, da sie ein abweichendes Verhalten zeigen.? Dieses Beispiel gilt auch für ein einzelnes PrintTicket.

## <a name="prefix-conflict-management"></a>Präfixkonfliktverwaltung

Ein Schlüsselwortkonflikt zwischen Einstellungen wird als definiert, das gleiche Print Schema-Element auf Stammebene, das durch das XML-Attribut "name" bezeichnet wird und in mehreren Leveltickets angezeigt wird. Wenn kein Konflikt besteht, kann ein Element mit Präfixbereich von einem allgemeineren Ticket an ein spezifischeres Ticket vererbt oder vererbt werden. Bei einem Konflikt hat die Einstellung aus dem spezifischsten Ticket Vorrang. Das heißt, dass die Einstellungen pro Seite in einem Ticket auf Seitenebene die identischen Einstellungen pro Seite in einem Dokument- oder Auftragsebenenticket überschreiben. Auf ähnliche Weise haben Dokumenteinstellungen im Dokumentebenenticket Vorrang vor Dokumenteinstellungen im Ticket auf Auftragsebene.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



