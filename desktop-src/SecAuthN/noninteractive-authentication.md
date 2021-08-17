---
description: Die nicht interaktive Authentifizierung kann nur verwendet werden, nachdem eine interaktive Authentifizierung durchgeführt wurde. Während der nichtinteraktiven Authentifizierung gibt der Benutzer keine Anmeldedaten ein, stattdessen werden zuvor eingerichtete Anmeldeinformationen verwendet.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Nichtinteraktive Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e259a2b14d48f4d7109966fa01f6fbd6a505a1343e90ea312c557ebfb9c84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786613"
---
# <a name="noninteractive-authentication"></a>Nichtinteraktive Authentifizierung

Die nicht interaktive Authentifizierung kann nur verwendet werden, nachdem eine [interaktive Authentifizierung](interactive-authentication.md) durchgeführt wurde. Während der nicht interaktiven Authentifizierung gibt der Benutzer keine [*Anmeldedaten*](../secgloss/l-gly.md)ein, stattdessen werden zuvor [*eingerichtete Anmeldeinformationen*](../secgloss/c-gly.md) verwendet.

Die nicht interaktive Authentifizierung wird ausgeführt, wenn eine Anwendung die [*SSPI (Security Support Provider Interface)*](../secgloss/s-gly.md) und ein Sicherheitspaket verwendet, um eine sichere Netzwerkverbindung herzustellen. Die nicht interaktive Authentifizierung ist der Mechanismus bei der Arbeit, wenn ein Benutzer eine Verbindung mit mehreren Computern in einem Netzwerk herstellt, ohne erneut Anmeldeinformationen für jeden Computer eingeben zu müssen. Wenn eine Anwendung beispielsweise einen sicheren Ordner auf einem Remotecomputer öffnen muss und der Anwendungsbenutzer bereits interaktiv bei einem Domänenkonto angemeldet ist, benötigt die Anwendung nicht, dass der Benutzer erneut Anmeldedaten angibt. Stattdessen kann die Anwendung mithilfe von SSPI eine nicht interaktive Authentifizierung anfordern, um die zuvor eingerichteten Sicherheitsinformationen an ein Sicherheitspaket zu übergeben. Das Sicherheitspaket verwendet dann LSA-Funktionen, um die [*Anmeldeinformationen*](../secgloss/c-gly.md)zu überprüfen. Das folgende Diagramm veranschaulicht dieses Verfahren.

![Nichtinteraktive Authentifizierung](images/lsasspi2.png)

Im obigen Diagramm initiiert die Clientanwendung einen Aufruf von SSPI, um eine authentifizierte Netzwerkverbindung anzufordern. SSPI übergibt die Anforderung des Clients zur Verarbeitung an ein Sicherheitspaket. Das Sicherheitspaket authentifiziert den Benutzer, indem es die [*lokale Sicherheitsautorität (Local Security Authority,*](../secgloss/l-gly.md) LSA) aufruft, ein [*Authentifizierungspaket*](../secgloss/a-gly.md) angibt und die vorhandenen Anmeldeinformationen des Benutzers bereitstellt.

Das Authentifizierungsergebnis wird vom [*Authentifizierungspaket*](../secgloss/a-gly.md)über das LSA, an das [*Sicherheitspaket*](../secgloss/s-gly.md)und schließlich an SSPI übergeben. SSPI benachrichtigt die Clientanwendung über das Ergebnis der Anforderung.

Weitere Informationen zu SSPI finden Sie unter [Security Support Provider Interface](sspi.md).

 

 
