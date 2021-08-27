---
description: Erläutert das Erstellen eines benutzerdefinierten Sicherheitspakets.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Erstellen benutzerdefinierter Sicherheitspakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88093ba7faed1ac2287c2a54391015984e83d4ad3878a60453978a9924706f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008848"
---
# <a name="creating-custom-security-packages"></a>Erstellen benutzerdefinierter Sicherheitspakete

## <a name="ssp-security-packages"></a>SSP-Sicherheitspakete

Wenn ein benutzerdefiniertes Sicherheitsunterstützungspaket (Security Support Provider, SSP) ausschließlich für die Client-/Serversicherheitsunterstützung verwendet wird, kann es die Schnittstelle des [Microsoft-Sicherheitssupportanbieters](sspi.md)implementieren.

Das im Lieferumfang des Platform Software Development Kit (SDK) enthaltene SampSSP-Beispiel enthält eine SSP-Beispiel-Sicherheitspaketimplementierungen.

## <a name="sspap-security-packages"></a>SSP-/AP-Sicherheitspakete

Benutzerdefinierte [*Sicherheitsunterstützungsanbieter-Authentifizierungspakete*](/windows/desktop/SecGloss/s-gly) / [](/windows/desktop/SecGloss/a-gly) (SSP/APs) enthalten Sicherheitspakete, die als Authentifizierungspakete (APs) und Sicherheitsunterstützungsanbieter (Security Support Providers, SSPs) fungieren. Diese Pakete implementieren separate APIs, um jede Rolle zu unterstützen.

Da es als AP funktioniert, muss ein [](/windows/desktop/SecGloss/s-gly) benutzerdefiniertes SSP/AP-Sicherheitspaket Implementierungen für alle Funktionen bereitstellen, die [von Authentifizierungspaketen implementiert werden.](authentication-functions.md)

Um integrierte Sicherheitsunterstützung bereitzustellen, muss ein benutzerdefiniertes SSP/AP-Sicherheitspaket Implementierungen für die [von SSP/APs implementierten Funktionen](authentication-functions.md)bereitstellen. [LSA-Funktionen, die von SSP/APs aufgerufen werden,](authentication-functions.md) beschreibt die Supportfunktionen, die den SSP/AP-Entwicklern zur Verfügung stehen, die mit dem LSA interagieren möchten.

SSP-/AP-Sicherheitspakete können sowohl als AP als auch als SSP als Teil des Betriebssystems und als Teil einer Benutzeranwendung ausgeführt werden. Diese beiden Ausführungsmodi werden als LSA-Modus bzw. Benutzermodus bezeichnet. Ausführliche Informationen zu benutzerdefinierten Sicherheitspaketen im LSA-Modus finden Sie unter Initialisierung des [LSA-Modus.](lsa-mode-initialization.md) Weitere Informationen zum Benutzermodus finden Sie unter [Benutzermodusinitialisierung.](user-mode-initialization.md)

Wenn ein benutzerdefiniertes SSP/AP-Sicherheitspaket Dienste für Client-/Serveranwendungen anbietet, sollte es Implementierungen für die Funktionen bereitstellen, die unter [Von SSP/APs im Benutzermodus implementierte](authentication-functions.md)Funktionen beschrieben sind. [LSA-Funktionen, die von SSP/APs im Benutzermodus aufgerufen werden,](authentication-functions.md) beschreiben die Supportfunktionen, die für einen SSP/AP verfügbar sind, der in einem Client- oder Serverprozess ausgeführt wird.

Informationen zum Registrieren einer SSP/AP-DLL finden Sie unter [Registrieren von SSP-/AP-DLLs.](registering-ssp-ap-dlls.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Registrieren und Installieren eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
