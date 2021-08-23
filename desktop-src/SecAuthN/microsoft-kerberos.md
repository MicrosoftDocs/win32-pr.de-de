---
description: Das Kerberos-Protokoll definiert, wie Clients mit einem Netzwerkauthentifizierungsdienst \[ (Platform Software Development Kit, SDK) \] interagieren.
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680a55581394d9d36da5b54cb2365d07384893069e26f9787163209daf2eabd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921792"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

Das [*Kerberos-Protokoll*](../secgloss/k-gly.md) definiert, wie Clients mit einem Netzwerkauthentifizierungsdienst interagieren. Clients erhalten Tickets vom Kerberos Key Distribution Center (KDC), die sie beim Herstellen einer Verbindung an den Server übergeben. Kerberos-Tickets stellen die [*Netzwerkanmeldeinformationen*](../secgloss/c-gly.md)des Clients dar.

Die Informationen in diesem Abschnitt bieten theoretischen Hintergrund zur Verwendung des Kerberos-Protokolls in einem Authentifizierungsprozess. Dies sind Hintergrundinformationen, die einem Entwickler das Verständnis der Vorgänge im Hintergrund in einem SSPI-Prozess hinzufügen können, der das Kerberos Version 5-Protokoll verwendet.

Das Kerberos-Authentifizierungsprotokoll bietet einen Mechanismus für die gegenseitige Authentifizierung zwischen Entitäten, bevor eine sichere Netzwerkverbindung hergestellt wird. In dieser Dokumentation werden die beiden Entitäten als Client und Server bezeichnet, obwohl sichere Netzwerkverbindungen zwischen Servern hergestellt werden können. Client und Server können auch als [*Sicherheitsprinzipale*](../secgloss/s-gly.md)bezeichnet werden.

Das Kerberos-Protokoll geht davon aus, dass Transaktionen zwischen Clients und Servern in einem offenen Netzwerk stattfinden, in dem die meisten Clients und viele Server physisch nicht sicher sind, und pakete, die über das Netzwerk übertragen werden, nach Belieben überwacht und geändert werden können. Die angenommene Umgebung ähnelt dem heutigen Internet, in dem sich ein Angreifer problemlos als Client oder Server darstellen und die Kommunikation zwischen legitimen Clients und Servern problemlos abhören oder manipulieren kann.

Dieser Abschnitt enthält folgende Informationen:

-   [Grundlegende Authentifizierungskonzepte](basic-authentication-concepts.md)
-   [Kerberos-Unterprotokollen](kerberos-subprotocols.md)
-   [Kerberos-Modell](kerberos-components.md)
-   [SSPI/Kerberos-Interoperabilität mit GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

Ihre Anwendung sollte nicht direkt auf das [*Kerberos-Sicherheitspaket*](../secgloss/s-gly.md) zugreifen. Stattdessen sollte das Sicherheitspaket [*Negotiate*](../secgloss/n-gly.md) verwendet werden. Negotiate ermöglicht Es Ihrer Anwendung, erweiterte [*Sicherheitsprotokolle*](../secgloss/s-gly.md) zu nutzen, wenn sie von den an der Authentifizierung beteiligten Systemen unterstützt werden. Derzeit wählt das Sicherheitspaket Negotiate zwischen [*Kerberos*](../secgloss/k-gly.md) und NTLM aus. Negotiate wählt Kerberos aus, es sei denn, es kann nicht von einem der an der Authentifizierung beteiligten Systeme verwendet werden.

 

 
