---
description: Erfahren Sie mehr über das PrintTicket-Format, das Konfigurationsinformationen mithilfe des XML-basierten Druckschemaframework ausdrückt.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: PrintTicket-Schema und Dokumentkonstruktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6de44ad04e9e39a516af0842bfaaca5b081191cb322b2f3a96f919590c64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824440"
---
# <a name="printticket-schema-and-document-construction"></a>PrintTicket-Schema und Dokumentkonstruktion

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Die aktuelle Methode zum Angeben von Gerätekonfigurationsinformationen mithilfe einer DEVMODE-Struktur hat mehrere Einschränkungen. Erstens ist die DEVMODE-Struktur eine binäre Struktur, die zu Problemen unterschiedlicher Versionen führen kann. Zweitens ist es in einen nicht mehr ersätzbaren öffentlichen Teil und einen privaten Teil unterteilt, auf den nur Treiber zugreifen können, und erst dann durch den spezifischen Treiber, der ihn erstellt hat. Das PrintTicket-Format drückt Konfigurationsinformationen mithilfe des XML-basierten Druckschemaframework aus, wodurch diese Mängel der DEVMODE-Struktur beseitigt werden.

Das PrintTicket-Schema behandelt jedes der beiden oben erwähnten Probleme. Erstens ist das PrintTicket-Schema eine XML-basierte Textdatei, sodass Probleme mit der Erweiterbarkeit und Versionsänderung beseitigt werden. Zweitens sind Konfigurationsinformationen für alle Clients verfügbar. Dies bedeutet, dass jeder Client oder Anbieter alle in einem PrintTicket enthaltenen Informationen speichern und abrufen kann. Optionen werden mit demselben Verfahren beschrieben, das auch vom Print Schema Framework und dem abgeleiteten PrintCapabilities-Dokument verwendet wird. Aus diesem Grund bietet PrintTicket alle potenziellen Portabilitätsvorteile des Optionsdefinitionsmodells, das realisiert werden soll. Weitere [Informationen finden Sie unter Druckschemaframework.](print-schema-framework.md) Die zielgruppe für diesen Abschnitt umfasst die folgenden Gruppen:

-   Implementierer einer PrintTicket-/PrintCapabilities-Anbieterschnittstelle

-   Consumers of the PrintTicket

-   Clients einer PrintTicket-/PrintCapabilities-Anbieterschnittstelle

Mitglieder der ersten Kategorie in der vorherigen Liste werden im restlichen Teil dieses Abschnitts als PrintTicket-Anbieter bezeichnet. Mitglieder der letzten beiden Kategorien werden als PrintTicket-Kunden bezeichnet.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Beziehung zu Druckschema und PrintCapabilities-Schema

Die PrintTicket- und PrintCapabilities-Schemas sind beide spezielle Teile des Druckschemas. Die wichtigsten strukturellen Unterschiede zwischen diesen Teilmengen des Druckschemas sind, dass das PrintTicket-Schema Property- und ParameterInit-Instanzen enthält, die nicht im PrintCapabilities-Schema enthalten sind, während das PrintCapabilities-Schema Property- und ParameterDef-Instanzen enthält, die nicht im PrintTicket-Schema enthalten sind. Abgesehen von diesen Unterschieden spiegeln sich die PrintCapabilities- und PrintTicket-Schemas in der Regel in Inhalts-, Freigabefeature-, Option-, ScoredProperty- und Value-Instanzen. Alle solchen freigegebenen Inhalte müssen auf dem neuesten Stand gehalten werden. Wenn beispielsweise eine Änderung am MediaSize-Feature im PrintCapabilities-Schema vorgenommen wird, muss die gleiche Änderung im PrintTicket-Schema vorgenommen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



