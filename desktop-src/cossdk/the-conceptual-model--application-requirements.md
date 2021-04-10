---
description: 'Das konzeptionelle Modell: Anwendungsanforderungen'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'Das konzeptionelle Modell: Anwendungsanforderungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a287ff940f154bf104bbb50f6362bf573d9223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127136"
---
# <a name="the-conceptual-model-application-requirements"></a>Das konzeptionelle Modell: Anwendungsanforderungen

Beim Entwerfen des konzeptionellen Modells müssen Sie die geschäftlichen Probleme und die zum Lösen dieser Probleme erforderlichen Funktionen definieren. Ein bewährter Ansatz besteht darin, mit Personen zu kommunizieren, die die Anwendung tatsächlich verwenden, eine Vielzahl von Benutzern treffen und so viele Geschäfts-oder Benutzer Szenarien wie möglich einschließen. Bestimmen Sie die Identitäten und die Anzahl der potenziellen Benutzer des Systems sowie die Größe und den Umfang der beteiligten Daten. Obwohl das Sammeln dieser Informationen der am wenigsten technische Aspekt des Entwurfsprozesses sein kann, ist es eine der wichtigsten. Zum Entwickeln einer erfolgreichen Anwendung benötigen Sie ein klares Verständnis der geschäftlichen Probleme und Prozesse, die angegangen werden müssen.

Beachten Sie beim Bestimmen der Anwendungsanforderungen die folgenden Punkte:

-   Leistungsanforderungen. Wie sieht die erwartete Reaktionszeit für Anwendungsaufgaben aus? Welche Failoverunterstützung für Downstreamserver ist erforderlich? Welche Stunden sind verfügbar?
-   Umgebung. Welche Server sind verfügbar? Sind zusätzliche Server für die Handhabung von Skalierungs Anforderungen geplant?
-   Bereitstellung. Wie wird die Anwendung in ein aktuelles System integriert? Mit welchen anderen Systemen interagieren die Anwendungen? Welche Betriebssysteme werden von den anderen Systemen verwendet? Welche Kommunikationsprotokolle sollten unterstützt werden? Welche API können Sie verwenden, um mit den anderen Systemen zu interagieren? Wo befinden sich die anderen Systeme im Netzwerk? Welche Einschränkungen gelten für die Verwendung durch den Computer? Für welche Benutzerkonten ist der Zugriff zulässig?
-   Der Standort. Wo befinden sich die Daten in Bezug auf den Client? Ist der Remote Zugriff auf die Daten erfolgt oder ist Sie lokal?
-   Sicherheit. Gibt es Verschlüsselungs-oder Integritäts Überprüfungsanforderungen? Gibt es Authentifizierungs-oder Datenschutzanforderungen?
-   Zugriffsrechte. Gibt es Einschränkungen für den Benutzer, der bestimmte Vorgänge ausführen darf? Wenn dies der Fall ist, sollten Sie zuerst dokumentieren, welche Vorgänge eine Autorisierung erfordern, und dann die Typen von Benutzern dokumentieren, die Autorisierung haben können. Diese Anforderungen können eine große Auswirkung darauf haben, wie Teile der Anwendung implementiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das logische Modell: Anwendungs Definition und-Planung](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[Das physische Modell: Anwendungsarchitektur](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



