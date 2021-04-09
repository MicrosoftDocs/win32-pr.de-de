---
description: Das Kerberos-Protokoll definiert, wie Clients mit einem Netzwerk Authentifizierungsdienst \[ Platform Software Development Kit (SDK) interagieren \] .
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958874"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

Das [*Kerberos-Protokoll*](../secgloss/k-gly.md) definiert, wie Clients mit einem Netzwerk Authentifizierungsdienst interagieren. Clients erhalten Tickets vom Kerberos Key Distribution Center (KDC), die sie beim Herstellen einer Verbindung an den Server übergeben. Kerberos-Tickets stellen die Netzwerk [*Anmelde*](../secgloss/c-gly.md)Informationen des Clients dar.

Die Informationen in diesem Abschnitt bieten einen theoretischen Hintergrund zur Verwendung des Kerberos-Protokolls bei einem Authentifizierungsprozess. Dabei handelt es sich um Hintergrundinformationen, mit denen Entwickler wissen, was im Hintergrund in einem SSPI-Prozess passiert, der das Kerberos 5-Protokoll verwendet.

Das Kerberos-Authentifizierungsprotokoll bietet einen Mechanismus für die gegenseitige Authentifizierung zwischen Entitäten, bevor eine sichere Netzwerkverbindung hergestellt wird. In dieser Dokumentation werden die beiden Entitäten als Client und Server bezeichnet, obwohl sichere Netzwerkverbindungen zwischen Servern hergestellt werden können. Sowohl der Client als auch der Server können auch als [*Sicherheits Prinzipale*](../secgloss/s-gly.md)bezeichnet werden.

Das Kerberos-Protokoll geht davon aus, dass Transaktionen zwischen Clients und Servern in einem geöffneten Netzwerk stattfinden, in dem die meisten Clients und viele Server nicht physisch sicher sind, und die Pakete, die über das Netzwerk übertragen werden, können überwacht und geändert werden. Die übernommene Umgebung ähnelt dem heutigen Internet, bei dem ein Angreifer sich problemlos als Client oder Server darstellen kann und die Kommunikation zwischen legitimen Clients und Servern problemlos auslassen oder manipulieren kann.

Dieser Abschnitt enthält folgende Informationen:

-   [Grundlegende Authentifizierungs Konzepte](basic-authentication-concepts.md)
-   [Kerberos-Unterprotokolle](kerberos-subprotocols.md)
-   [Kerberos-Modell](kerberos-components.md)
-   [SSPI/Kerberos-Interoperabilität mit GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

Ihre Anwendung sollte nicht direkt auf das Kerberos- [*Sicherheitspaket*](../secgloss/s-gly.md) zugreifen. Stattdessen sollte das [*Aushandlungs*](../secgloss/n-gly.md) Sicherheitspaket verwendet werden. Aushandeln ermöglicht der Anwendung die Nutzung erweiterter [*Sicherheitsprotokolle*](../secgloss/s-gly.md) , wenn Sie von den Systemen, die an der Authentifizierung beteiligt sind, unterstützt werden. Derzeit wählt das Aushandlungs Sicherheitspaket zwischen [*Kerberos*](../secgloss/k-gly.md) und NTLM aus. Aushandeln wählt Kerberos aus, es sei denn, Sie kann von einem der an der Authentifizierung beteiligten Systeme verwendet werden.

 

 
