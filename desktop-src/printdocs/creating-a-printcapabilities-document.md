---
description: Nachdem ein PrintTicket überprüft wurde, kann es verwendet werden, um eine Momentaufnahme der PrintCapabilities zu erstellen.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Erstellen eines PrintCapabilities-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a01395df674b683349bd4a5f42fe1bd57ef2768ef4d967ba3aeda7734f5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950200"
---
# <a name="creating-a-printcapabilities-document"></a>Erstellen eines PrintCapabilities-Dokuments

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Nachdem ein PrintTicket überprüft wurde, kann es verwendet werden, um eine Momentaufnahme der PrintCapabilities zu erstellen. Der Anbieter muss über eine interne Darstellung für jede Eigenschaft verfügen, deren Wert von der Gerätekonfiguration abhängt. Wenn SpotDiameter beispielsweise eine Eigenschaft ist, die sowohl von den Auflösungs- als auch von mediaType-Features abhängig ist, kann eine interne Darstellung von SpotDiameter in Bezug auf die verschiedenen Werte für Auflösung und MediaType wie in der folgenden Tabelle angezeigt werden:



| Lösung      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Bindung<br/>   | 520<br/> |
| 300<br/>  | Glänzend<br/> | 350<br/> |
| 600<br/>  | Bindung<br/>   | 330<br/> |
| 600<br/>  | Glänzend<br/> | 180<br/> |
| 1200<br/> | Bindung<br/>   | 250<br/> |
| 1200<br/> | Glänzend<br/> | 100<br/> |



 

In diesem Beispiel muss der PrintCapabilities-Anbieter das bereitgestellte PrintTicket verwenden, um den richtigen Eintrag aus der internen Tabelle auszuwählen und diesen als Wert für die SpotDiameter-Eigenschaft zu melden. Dieser Prozess wird für jede mehrwertige Eigenschaft wiederholt (für jede Eigenschaft, deren Wert von der Konfiguration abhängig ist). Im Abschnitt [PrintCapabilities Schema and Document Construction (PrintCapabilities-Schema und Dokumenterstellung)](printcapabilities-schema-and-document-construction.md) werden die anderen Schritte beschrieben, die beim Erstellen einer Momentaufnahme von PrintCapabilities erforderlich sind.

Um eine Momentaufnahme des PrintCapabilities-Standarddokuments zu erstellen, geben Sie ein PrintTicket-Standardticket (anstelle eines beliebigen PrintTicket) für die Methode an, die PrintCapabilities-Dokumente erstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




