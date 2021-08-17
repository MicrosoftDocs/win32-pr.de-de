---
description: Das SSPI-Modell (Security Support Provider Interface) stellt eine einzelne Schnittstelle für eine Client-/Servertransportanwendung bereit, die die verschiedenen Sicherheitspakete verwendet, die auf einem Computer oder Netzwerk verfügbar sind.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Verfahren, die mit den meisten Sicherheitspaketen und Protokollen verwendet werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611ecbf7f2a124ea9352a71c7197d298f30a43391e3692303fcd3f7bc533cc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920749"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Verfahren, die mit den meisten Sicherheitspaketen und Protokollen verwendet werden

Das SSPI-Modell [*(Security Support Provider Interface)*](../secgloss/s-gly.md) stellt eine einzelne Schnittstelle [](../secgloss/s-gly.md) für eine Client-/Servertransportanwendung bereit, die die verschiedenen Sicherheitspakete verwendet, die auf einem Computer oder Netzwerk verfügbar sind. SSPI ermöglicht einer Anwendung die Verwendung eines Sicherheitspakets, ohne sich mit den zugrunde liegenden [*Sicherheitsprotokollen des*](../secgloss/s-gly.md) Pakets zu beschäftigen. Gleichzeitig ermöglicht SSPI komplexen, sicherheitsorientierten Anwendungen die Nutzung der erweiterten Funktionen bestimmter Sicherheitspakete.

Anwendungen initialisieren SSPI mithilfe der folgenden Schritte, um eine Netzwerkverbindung für die meisten Sicherheitspakete zu sichern:

-   [Verwenden von SecBufferDesc und SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Initialisieren von SSPI](initializing-sspi.md)
-   [Herstellen einer sicheren Verbindung mit Authentifizierung](establishing-a-secure-connection-with-authentication.md)
-   [Sicherstellen der Kommunikationsintegrität während der Exchange](ensuring-communication-integrity-during-message-exchange.md)
-   [Beenden einer SSPI-Sitzung](ending-an-sspi-session.md)

 

 
