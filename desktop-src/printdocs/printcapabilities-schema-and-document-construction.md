---
title: Printfunktionalitäten-Schemas und-Dokumente
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1b8e2827e451fd8b1df477c33fe18d6203d10c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106367281"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Printfunktionalitäten-Schema und Dokument Erstellung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Die aktuellen Win32 devcaps-Funktionen (wie z. b. GetDeviceCaps oder devicecapabili, die in der Microsoft Platform Software Development Kit (SDK)-Dokumentation beschrieben werden) schränken den Typ der Informationen, die nicht-Treiber Komponenten erhalten können, in Bezug auf die Funktionen und Eigenschaften von Druckgeräten erheblich ein. Es gibt keine Unterstützung für das Veröffentlichen der Funktionen von Druck Prozessoren. es gibt auch keine Methode zum Auflisten nicht standardmäßiger Features. Folglich gibt es keine Möglichkeit für eine andere Komponente als einen Treiber, eine komplette Benutzeroberfläche zu erstellen. Darüber hinaus kann der Client oder die Anwendung die Funktionen von Geräten oder Druck Warteschlangen nicht vollständig ermitteln, die über die Funktionen der Win32 devcaps-Funktionen hinausgehen. Die aktuellen Funktionen sind nicht erweiterbar, sodass Geräte keine neuen Eigenschaften oder Features veröffentlichen können.

Das printfunctions-Schema soll viele Einschränkungen der Win32 devcaps-Funktionen vermeiden, indem es eine Obermenge der von diesen Funktionen gewährten Funktionen bereitstellt. Wenn mehr Funktionalität benötigt wird, kann ein Anbieter des Printworks-Dokuments die Druck Schema Schlüsselwörter innerhalb der Einschränkungen des Druck Schema-Frameworks durch Hinzufügen von Privat definierten Element Instanzen erweitern. Aufgrund der Abhängigkeit von XML als Mittel des Austauschs kann jeder Consumer eines printoperations-Dokuments ohne Einschränkung auf alle Daten im Dokument zugreifen, ohne dass die Kompatibilität mit verschiedenen Betriebssystemversionen berücksichtigt werden muss. In diesem Abschnitt werden das printfunktionalitäten-Schema beschrieben und seine Verwendung ausführlich erläutert.

Die Zielgruppe für diesen Abschnitt umfasst die folgenden Gruppen:

-   Implementierer der PrintTicket/printfunktionalitäten-Anbieter Schnittstelle

-   Consumer von Print-Funktionen

-   Clients der PrintTicket/printfunktionalitäten-Anbieter Schnittstelle

Die erste Kategorie in der vorangehenden Liste wird im restlichen Teil dieses Abschnitts als Print-Funktionen bezeichnet. Die zweite und dritte Kategorie werden als Print-Funktionen Consumer bezeichnet.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Beziehung zum Druck Schema und zum PrintTicket-Schema

Die printfunktionalitäten-und PrintTicket-Schemas sind beide spezialisierte Teile des Druck Schemas. Die wesentlichen strukturellen Unterschiede zwischen diesen Teilmengen des Druck Schemas besteht darin, dass das Printworks-Schema Eigenschaften-und ParameterDef-Instanzen enthält, die nicht im PrintTicket-Schema enthalten sind, während das PrintTicket-Schema Eigenschaften-und parameterinit-Instanzen enthält, die nicht im printfunktionalitäten-Schema enthalten sind. Mit Ausnahme dieser Unterschiede spiegeln sich die Schemas "printfähigkeiten" und "PrintTicket" im allgemeinen gegenseitig in den Instanzen "Content", "Sharing Feature", "Option", "ScoredProperty" Alle freigegebenen Inhalte müssen auf dem neuesten Stand gehalten werden. Wenn z. b. im printfunktionsschema eine Änderung an der PageMediaSize-Funktion vorgenommen wird, muss im PrintTicket-Schema dieselbe Änderung vorgenommen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



