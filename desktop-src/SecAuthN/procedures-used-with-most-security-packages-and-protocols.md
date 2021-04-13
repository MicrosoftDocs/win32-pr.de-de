---
description: Das SSPI-Modell (Security Support Provider Interface) bietet eine einzige Schnittstelle für eine Client/Server-Transport Anwendung, die die verschiedenen auf einem Computer oder Netzwerk verfügbaren Sicherheitspakete verwendet.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Prozeduren für die meisten Sicherheitspakete und Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525853"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Prozeduren für die meisten Sicherheitspakete und Protokolle

Das SSPI-Modell ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) bietet eine einzige Schnittstelle für eine Client/Server-Transport Anwendung, die die verschiedenen auf einem Computer oder Netzwerk verfügbaren [*Sicherheitspakete*](../secgloss/s-gly.md) verwendet. SSPI ermöglicht einer Anwendung die Verwendung eines Sicherheitspakets, ohne die zugrunde liegenden [*Sicherheitsprotokolle*](../secgloss/s-gly.md) des Pakets zu behandeln. Gleichzeitig ermöglicht SSPI auch anspruchsvolle, sicherheitsbewusste Anwendungen, um die erweiterten Funktionen bestimmter Sicherheitspakete nutzen zu können.

Anwendungen initialisieren SSPI mithilfe der folgenden Schritte, um eine Netzwerkverbindung für die meisten Sicherheitspakete zu sichern:

-   [Verwenden von secbufferde SC und secbuffer](using-secbufferdesc-and-secbuffer.md)
-   [SSPI wird initialisiert.](initializing-sspi.md)
-   [Einrichten einer sicheren Verbindung mit der Authentifizierung](establishing-a-secure-connection-with-authentication.md)
-   [Sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs](ensuring-communication-integrity-during-message-exchange.md)
-   [Beenden einer SSPI-Sitzung](ending-an-sspi-session.md)

 

 
