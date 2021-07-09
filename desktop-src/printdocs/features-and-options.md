---
description: Erfahren Sie mehr über Features und Optionen in einem PrintCapabilities-Dokument. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Features und Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae6d0918b6237885c2c7240efb0dc0f982b882f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549408"
---
# <a name="features-and-options"></a>Features und Optionen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Feature-/Options- und Parameterkonstrukte werden in einem PrintCapabilities-Dokument verwendet, um Geräteattribute darzustellen, die zur Definition der Gerätekonfiguration beitragen. Ein Beispiel für ein Feature-/Optionskonstrukt ist ein Druckgerät, das in mehreren Auflösungen drucken kann. Das Geräteattribut, das die Auflösung definiert, kann als Funktionsinstanz dargestellt werden, wobei jeder der möglichen Ausgabeauflösungswerte als einzelne Option-Instanz dargestellt wird. Eine Optionsinstanz kann eine Auflösung von 300 dpi darstellen, eine andere eine Auflösung von 600 dpi usw.

Beachten Sie, dass das Druckschema erfordert, dass die Liste der Feature-, Options- und ParameterDef-Instanzen, die in jedem PrintCapabilities-Dokument gemeldet werden, unabhängig von der Konfiguration konstant bleiben muss. Dadurch können Konfigurationen und Abhängigkeiten von Konfigurationen eindeutig ausgedrückt werden. Dies hat zur Folge, dass jedes Feature und jede Untergeordnete Funktion über eine klar definierte Einstellung verfügen muss, unabhängig von der Einstellung eines anderen Features oder Unterfeatures. Daher muss jedes Unterfeature über eine Option verfügen, die einer No-Op-Einstellung entspricht (einstellung Off, Disabled oder None), die automatisch für alle Unterfeatures ausgewählt wird, wenn der Benutzer die No-Op-Option im übergeordneten Feature auswählt. Wenn dagegen eines der Untergeordneten Features auf eine aktivierte Option festgelegt ist, werden auch das übergeordnete Feature und andere zugehörige Unterfeatures aktiviert. In der Zwischenzeit muss der PrintTicket-Anbieter (während der PrintTicket-Überprüfung) sicherstellen, dass Einstellungen für alle Feature- und Unterfeatureinstanzen unabhängig von der Gerätekonfiguration definiert werden und dass die Einstellungen der untergeordneten Features mit den Einstellungen des übergeordneten Features übereinstimmen. Dadurch wird sichergestellt, dass dem Gerät kein inkonsistentes PrintTicket angezeigt wird, bei dem einige Unterfeatures darauf hinweisen, dass z. B. das Stapling aktiviert ist, während andere Unterfeatures darauf hinweisen, dass das Stapling deaktiviert ist.

Beachten Sie, dass PrintCapabilities-Autoren die Schachtelungsfunktionen von Featureelementen nicht nutzen müssen. Wenn sie möchten, können sie alle Funktionsinstanzen in einer flachen Struktur als gleichgeordnete Elemente darstellen. Beachten Sie auch, dass eine geschachtelte Sammlung von Featureinstanzen vereinfacht werden kann, indem einfach alle Untergeordneten Features auf die Stammebene verschoben werden. Die einzige Vorsichtsmaßnahme besteht darin, sicherzustellen, dass die Namensattribute dieser Featureinstanzen eindeutig sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



