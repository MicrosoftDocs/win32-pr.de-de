---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: PrintTicket-Schema und Dokument Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe386638a7f119c52982f1911d602691455343f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219075"
---
# <a name="printticket-schema-and-document-construction"></a>PrintTicket-Schema und Dokument Erstellung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Die aktuelle Methode zum Angeben von Geräte Konfigurationsinformationen mithilfe einer DEVMODE-Struktur hat mehrere Einschränkungen. Zuerst ist die DEVMODE-Struktur eine binäre Struktur, die zu Problemen unterschiedlicher Versionen führen kann. Zweitens wird Sie in einen nicht erweiterbaren öffentlichen Teil und einen privaten Teil aufgeteilt, auf den nur von Treibern zugegriffen werden kann, und nur durch den spezifischen Treiber, von dem Sie erstellt wurde. Das PrintTicket-Format drückt Konfigurationsinformationen mithilfe des XML-basierten Print Schema-Frameworks aus, wodurch diese Mängel der DEVMODE-Struktur beseitigt werden.

Das PrintTicket-Schema wird für jedes der beiden soeben erwähnten Probleme adressiert. Zuerst ist das PrintTicket-Schema eine XML-basierte Textdatei, sodass Probleme mit Erweiterbarkeit und Versionsverwaltung beseitigt werden. Zweitens sind Konfigurationsinformationen für alle Clients verfügbar. Dies bedeutet, dass jeder Client oder Anbieter alle in einem PrintTicket enthaltenen Informationen speichern und abrufen kann. Optionen werden mit dem gleichen Verfahren beschrieben, das auch vom Druck Schema Framework und dem abgeleiteten printfunktionalitäten-Dokument verwendet wird. Aus diesem Grund stellt das PrintTicket alle möglichen Portabilitäts Vorteile des Options Definitions Modells bereit, die erkannt werden können. Weitere Informationen finden Sie unter [Print Schema Framework](print-schema-framework.md) . Die Zielgruppe für diesen Abschnitt umfasst die folgenden Gruppen:

-   Implementierer einer PrintTicket/printfunktionalitäten-Anbieter Schnittstelle

-   Consumer von PrintTicket

-   Clients einer PrintTicket/printfunktionalitäten-Anbieter Schnittstelle

Die Mitglieder der ersten Kategorie in der vorangehenden Liste werden im restlichen Teil dieses Abschnitts als PrintTicket-Anbieter bezeichnet. Mitglieder der letzten beiden Kategorien werden als PrintTicket-Consumer bezeichnet.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Beziehung zum Druck Schema und zum printfunktionalitäten-Schema

Die PrintTicket-und printfunktionalitäten-Schemas sind beide spezialisierte Teile des Druck Schemas. Die wesentlichen strukturellen Unterschiede zwischen diesen Teilmengen des Druck Schemas besteht darin, dass das PrintTicket-Schema Eigenschaften-und parameterinit-Instanzen enthält, die nicht im printfunktionalitäten-Schema enthalten sind, während das printfunktionalitäten-Schema Eigenschaften-und ParameterDef-Instanzen enthält, die nicht im PrintTicket-Schema enthalten sind. Mit Ausnahme dieser Unterschiede spiegeln sich die Schemas "printfähigkeiten" und "PrintTicket" im allgemeinen gegenseitig in den Instanzen "Content", "Sharing Feature", "Option", "ScoredProperty" Alle freigegebenen Inhalte müssen auf dem neuesten Stand gehalten werden. Wenn beispielsweise eine Änderung an der mediasize-Funktion im printfunktionsschema vorgenommen wird, muss die gleiche Änderung im PrintTicket-Schema vorgenommen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



