---
description: Erläutert, wie ein benutzerdefiniertes Sicherheitspaket erstellt wird.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Erstellen von benutzerdefinierten Sicherheitspaketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866016"
---
# <a name="creating-custom-security-packages"></a>Erstellen von benutzerdefinierten Sicherheitspaketen

## <a name="ssp-security-packages"></a>SSP-Sicherheitspakete

Wenn ein Sicherheitspaket für benutzerdefinierte Security Support Provider (SSP) ausschließlich für die Unterstützung von Client-/Serversicherheit verwendet wird, kann es die Microsoft [Security Support Provider-Schnittstelle](sspi.md)implementieren.

Das sampssp-Beispiel, das im Platform Software Development Kit (SDK) enthalten ist, enthält ein Beispiel für eine SSP-Sicherheitspaket Implementierung.

## <a name="sspap-security-packages"></a>SSP/AP-Sicherheitspakete

Benutzerdefinierte [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) / [*Authentifizierungs Pakete*](/windows/desktop/SecGloss/a-gly) (SSP/APS) enthalten Sicherheitspakete, die als Authentifizierungs Pakete (APS) und Security Support Provider (SSPs) fungieren. Diese Pakete implementieren separate APIs, um die einzelnen Rollen zu unterstützen.

Da es als AP fungiert, muss ein benutzerdefiniertes SSP/AP- [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) Implementierungen für alle Funktionen bereitstellen, die [von Authentifizierungs Paketen implementiert](authentication-functions.md)werden.

Zum Bereitstellen integrierter Sicherheitsunterstützung muss ein benutzerdefiniertes SSP/AP-Sicherheitspaket Implementierungen für die [von SSP/APS implementierten Funktionen](authentication-functions.md)bereitstellen. [LSA-Funktionen, die von SSP/APS aufgerufen werden](authentication-functions.md) , beschreiben die Unterstützungsfunktionen, die für die SSP/AP-Entwickler zur Verfügung stehen, die mit der LSA interagieren möchten.

SSP/AP-Sicherheitspakete, die sowohl als AP als auch als SSP ausgeführt werden, können als Teil des Betriebssystems und als Teil einer Benutzeranwendung ausgeführt werden. Diese zwei Ausführungsmodi werden als LSA-Modus bzw. Benutzermodus bezeichnet. Ausführliche Informationen zu benutzerdefinierten Sicherheitspaketen im LSA-Modus finden Sie unter [LSA Mode Initialization](lsa-mode-initialization.md). Ausführliche Informationen zum Benutzermodus finden Sie unter [benutzermodusinitialisierung](user-mode-initialization.md).

Wenn ein benutzerdefiniertes SSP/AP-Sicherheitspaket Dienste für Client/Server-Anwendungen bereitstellt, sollte es Implementierungen für die Funktionen bereitstellen, die unter [von Benutzermodus-SSP/APS implementierte](authentication-functions.md)Funktionen beschrieben werden. [LSA-Funktionen, die vom benutzermodussp/APS aufgerufen werden](authentication-functions.md) , beschreiben die Unterstützungsfunktionen, die für eine SSP/AP-Ausführung in einem Client-oder Server Prozess verfügbar sind.

Informationen zum Registrieren einer SSP/AP-dll finden Sie unter [Registrieren von SSP/AP-DLLs](registering-ssp-ap-dlls.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
