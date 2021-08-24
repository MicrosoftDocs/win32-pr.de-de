---
description: 'Konzeptionelles Modell: Anwendungsanforderungen'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'Konzeptionelles Modell: Anwendungsanforderungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19c69f8da7179765242815c4d01760c36b94e95714188f7db772600826d0416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853920"
---
# <a name="the-conceptual-model-application-requirements"></a>Konzeptionelles Modell: Anwendungsanforderungen

Beim Entwerfen des konzeptionellen Modells müssen Sie die Geschäftsprobleme und die Funktionen definieren, die zum Lösen dieser Probleme erforderlich sind. Ein bewährter Ansatz besteht im Sprechen mit Personen, die die Anwendung tatsächlich verwenden, mit einer vielzahl von Benutzern zusammentreffen und so viele Geschäfts- oder Benutzerszenarien wie möglich umfassen. Bestimmen Sie die Identitäten und die Anzahl der potenziellen Benutzer des Systems sowie die Größe und den Umfang der beteiligten Daten. Obwohl das Sammeln dieser Informationen der am wenigsten technische Aspekt des Entwurfsprozesses sein kann, ist es einer der wichtigsten. Um eine erfolgreiche Anwendung zu entwickeln, benötigen Sie ein klares Verständnis der Geschäftsprobleme und -prozesse, die behandelt werden müssen.

Beachten Sie beim Ermitteln der Anwendungsanforderungen die folgenden Überlegungen:

-   Leistungsanforderungen. Wie lange ist die erwartete Antwortzeit für Anwendungsaufgaben? Welche Failoverunterstützung für Ausfallserver ist erforderlich? Wie hoch sind die Verfügbarkeitszeiten?
-   Umgebung. Welche Server sind verfügbar? Sind zusätzliche Server geplant, um Skalierungsanforderungen zu erfüllen?
-   Bereitstellung. Wie wird die Anwendung in ein aktuelles System integriert? Mit welchen anderen Systemen interagiert die Anwendung? Welche Betriebssysteme verwenden die anderen Systeme? Welche Kommunikationsprotokolle sollten unterstützt werden? Welche API können Sie für die Interaktion mit den anderen Systemen verwenden? Wo befinden sich die anderen Systeme im Netzwerk? Welche Einschränkungen gelten für die Computernutzung? Für welche Benutzerkonten ist der Zugriff zulässig?
-   Der Standort. Wo befinden sich die Daten in Bezug auf den Client? Wird remote auf die Daten zugegriffen, oder handelt es sich um lokale Daten?
-   Sicherheit. Gibt es Verschlüsselungs- oder Integritätsüberprüfungsanforderungen? Gibt es Authentifizierungs- oder Datenschutzanforderungen?
-   Zugriffsrechte. Gibt es Einschränkungen, wer bestimmte Vorgänge ausführen darf? Wenn ja, sollten Sie zuerst dokumentieren, welche Vorgänge eine Autorisierung erfordern, und dann die Typen von Benutzern dokumentieren, die über Autorisierung verfügen können. Diese Anforderungen können einen großen Einfluss darauf haben, wie Teile der Anwendung implementiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Logisches Modell: Anwendungsdefinition und -planung](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[Das physische Modell: Anwendungsarchitektur](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



