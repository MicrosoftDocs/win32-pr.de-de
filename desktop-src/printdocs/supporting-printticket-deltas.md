---
description: Erfahren Sie mehr über die Unterstützung von PrintTicket-Deltas. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Unterstützen von PrintTicket Deltas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548779"
---
# <a name="supporting-printticket-deltas"></a>Unterstützen von PrintTicket Deltas

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Die PrintTicket-Anbieterschnittstelle verfügt über Methoden, mit denen inkrementelle Änderungen an einem vorhandenen PrintTicket vorgenommen werden können. Die inkrementellen PrintTicket-Änderungen können in einem partiellen PrintTicket angegeben werden, das als PrintTicket-Delta bezeichnet wird. Ein überarbeitetes PrintTicket wird erstellt, indem ein PrintTicket-Delta mit einem vorhandenen PrintTicket zusammengeführt wird. Weitere Informationen zu Methoden im Zusammenhang mit PrintTicket-Deltas finden Sie im bevorstehenden Dokument PrintTicket Provider Interface ( PrintTicket-Anbieterschnittstelle).

Wenn ein PrintTicket-Delta verarbeitet wird, müssen die folgenden Schritte ausgeführt werden.

1.  Identifizieren Sie Feature- oder ParameterInit-Instanzen, die sowohl dem vorhandenen PrintTicket (dem PrintTicket-Ziel) als auch dem PrintTicket-Delta gemeinsam sind.

    -   Ersetzen Sie für jedes Feature, das sowohl dem PrintTicket-Ziel als auch dem PrintTicket-Delta gemeinsam ist, das Feature im PrintTicket-Ziel durch das entsprechende Feature im PrintTicket-Delta.

    -   Ersetzen Sie für jeden ParameterInit, der sowohl für das PrintTicket-Ziel als auch für das PrintTicket-Delta gilt, die ParameterInit im PrintTicket-Ziel durch die entsprechende ParameterInit im PrintTicket-Delta.

2.  Kopieren Sie alle verbleibenden Feature- und ParameterInit-Instanzen im PrintTicket-Delta auf das PrintTicket-Ziel.

3.  Wenn Ihr Konfliktlösungsalgorithmus die Angabe von Prioritäten im PrintTicket selbst zulässt, können Sie die Prioritäten der Im PrintTicket-Delta benannten Feature- und ParameterInit-Instanzen erhöhen.

4.  Führen Sie die PrintTicket-Überprüfung wie unter Prüfliste für [die PrintTicket-Überprüfung](printticket-validation-checklist.md)beschrieben durch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



