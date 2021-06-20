---
title: PrintCapabilities-Schemas und -Dokumente
description: Das PrintCapabilities-Schema soll viele der Einschränkungen der Win32 DevCaps-Funktionen beseitigen.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21347fae1c9824df4a8355f8dd26de37eeac4604
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407073"
---
# <a name="printcapabilities-schema-and-document-construction"></a>PrintCapabilities-Schema und Dokumenterstellung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Die aktuellen Win32 DevCaps-Funktionen (z. B. GetDeviceCaps oder DeviceCapabilities, beide in der Dokumentation zum Microsoft Platform Software Development Kit (SDK) beschrieben) beschränken die Art der Informationen, die Nichttreiberkomponenten abrufen können, im Hinblick auf die Funktionen und Eigenschaften von Druckgeräten stark. Es gibt keine Unterstützung für die Veröffentlichung der Funktionen von Druckprozessoren, und es gibt auch keine Methode zum Aufzählen nicht standardmäßiger Features. Daher gibt es für eine Komponente außer einem Treiber keine Möglichkeit, eine vollständige Benutzeroberfläche zu erstellen. Darüber hinaus kann der Client oder die Anwendung die Funktionen von Geräten oder Druckwarteschlangen nicht vollständig bestimmen, die über die funktionen von Win32 DevCaps hinausgehen. Die aktuellen Funktionen sind nicht erweiterbar, sodass Geräte keine neuen Eigenschaften oder Features veröffentlichen können.

Das PrintCapabilities-Schema soll viele der Einschränkungen der Win32 DevCaps-Funktionen beseitigen, indem es eine Obermenge der Funktionen bereitstellt, die von diesen Funktionen geboten werden. Wenn mehr Funktionalität erforderlich ist, kann ein Anbieter des PrintCapabilities-Dokuments die Schlüsselwörter des Druckschemas innerhalb der Einschränkungen des Druckschemaframeworks erweitern, indem er privat definierte Elementinstanzen hinzufügt. Aufgrund der Abhängigkeit von XML als Austauschmedium kann jeder Consumer eines PrintCapabilities-Dokuments uneingeschränkt und ohne Bedenken hinsichtlich der Kompatibilität mit verschiedenen Betriebssystemversionen auf alle Daten im Dokument zugreifen. In diesem Abschnitt wird das PrintCapabilities-Schema beschrieben und seine Verwendung ausführlich erläutert.

Die zielgruppe für diesen Abschnitt umfasst die folgenden Gruppen:

-   Implementierer der PrintTicket/PrintCapabilities-Anbieterschnittstelle

-   Consumer von PrintCapabilities

-   Clients der PrintTicket/PrintCapabilities-Anbieterschnittstelle

Die erste Kategorie in der vorherigen Liste wird im restlichen Teil dieses Abschnitts als PrintCapabilities-Anbieter bezeichnet. Die zweite und dritte Kategorie werden als PrintCapabilities-Consumer bezeichnet.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Beziehung zu Druckschema und PrintTicket-Schema

Die PrintCapabilities- und PrintTicket-Schemas sind jeweils spezialisierte Teile des Druckschemas. Die wichtigsten strukturellen Unterschiede zwischen diesen Teilmengen des Druckschemas bestehen darin, dass das PrintCapabilities-Schema Property- und ParameterDef-Instanzen enthält, die nicht im PrintTicket-Schema enthalten sind, während das PrintTicket-Schema Property- und ParameterInit-Instanzen enthält, die nicht im PrintCapabilities-Schema enthalten sind. Mit Ausnahme dieser Unterschiede spiegeln sich die PrintCapabilities- und PrintTicket-Schemas in der Regel in den Instanzen Inhalt, Freigabefeature, Option, ScoredProperty und Wert gegenseitig wider. Solche freigegebenen Inhalte müssen auf dem neuesten Stand gehalten werden. Wenn beispielsweise eine Änderung an der PageMediaSize-Funktion im PrintCapabilities-Schema vorgenommen wird, muss die gleiche Änderung im PrintTicket-Schema vorgenommen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



