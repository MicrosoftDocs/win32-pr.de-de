---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Unterstützen von PrintTicket-Delta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351861"
---
# <a name="supporting-printticket-deltas"></a>Unterstützen von PrintTicket-Delta

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Die PrintTicket-Anbieter Schnittstelle verfügt über Methoden, die verwendet werden können, um inkrementelle Änderungen an einem vorhandenen PrintTicket vorzunehmen. Die inkrementellen PrintTicket-Änderungen können in einem PrintTicket-Teil angegeben werden, das als PrintTicket-Delta bezeichnet wird. Ein überarbeitetes PrintTicket wird durch Zusammenführen eines PrintTicket-Deltas mit einem vorhandenen PrintTicket erstellt. Weitere Informationen zu Methoden, die PrintTicket-Delta betreffen, finden Sie im bevorstehenden Dokument der PrintTicket-Anbieter Schnittstelle.

Wenn ein PrintTicket-Delta verarbeitet wird, müssen die folgenden Schritte ausgeführt werden.

1.  Identifizieren Sie Feature-oder parameterinit-Instanzen, die sowohl für das vorhandene PrintTicket (das PrintTicket-Ziel) als auch für das PrintTicket-Delta gemeinsam sind.

    -   Ersetzen Sie für jedes Feature, das sowohl für das PrintTicket-Ziel als auch für das PrintTicket-Delta üblich ist, die Funktion im PrintTicket-Ziel durch die entsprechende Funktion im PrintTicket-Delta.

    -   Ersetzen Sie für jede parameterinit, die sowohl für das PrintTicket-Ziel als auch für das PrintTicket-Delta üblich ist, den Parameter "parameterinit" im PrintTicket-Ziel durch die entsprechende parameterinit im PrintTicket-Delta.

2.  Kopieren Sie alle verbleibenden Feature-und parameterinit-Instanzen im PrintTicket-Delta in das PrintTicket-Ziel.

3.  Wenn der Konflikt Auflösungs Algorithmus das Festlegen von Prioritäten im PrintTicket selbst ermöglicht, können Sie die Prioritäten der Funktionen und parameterinit-Instanzen im PrintTicket-Delta erhöhen.

4.  Führen Sie die PrintTicket-Überprüfung wie in der [PrintTicket-Überprüfungs Checkliste](printticket-validation-checklist.md)beschrieben

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



