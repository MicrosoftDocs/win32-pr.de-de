---
description: Die nicht interaktive Authentifizierung kann nur verwendet werden, nachdem eine interaktive Authentifizierung stattfindet. Während der nicht interaktiven Authentifizierung wird der Benutzer nicht zur Eingabe von Anmeldedaten verwendet. stattdessen werden zuvor festgelegte Anmelde Informationen verwendet.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Nicht interaktive Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658cba212403da2f970e056d7bacc1bc1bcaa559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958872"
---
# <a name="noninteractive-authentication"></a>Nicht interaktive Authentifizierung

Die nicht interaktive Authentifizierung kann nur verwendet werden, nachdem eine [interaktive Authentifizierung](interactive-authentication.md) stattfindet. Während der nicht interaktiven Authentifizierung wird der Benutzer nicht zur Eingabe von [*Anmeldedaten*](../secgloss/l-gly.md)verwendet. stattdessen werden zuvor festgelegte [*Anmelde*](../secgloss/c-gly.md) Informationen verwendet.

Die nicht interaktive Authentifizierung wird ausgeführt, wenn eine Anwendung die [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI) und ein Sicherheitspaket verwendet, um eine sichere Netzwerkverbindung herzustellen. Die nicht interaktive Authentifizierung ist der Mechanismus bei der Arbeit, wenn ein Benutzer eine Verbindung mit mehreren Computern in einem Netzwerk herstellt, ohne die Anmelde Informationen für jeden Computer erneut eingeben zu müssen. Wenn eine Anwendung z. b. einen sicheren Ordner auf einem Remote Computer öffnen muss und der Anwendungs Benutzer bereits interaktiv bei einem Domänen Konto angemeldet ist, ist es für die Anwendung nicht erforderlich, dass der Benutzer erneut Anmeldedaten bereitstellt. Stattdessen kann die Anwendung mithilfe von SSPI eine nicht interaktive Authentifizierung anfordern, um die zuvor eingerichteten Sicherheitsinformationen an ein Sicherheitspaket zu übergeben. Das Sicherheitspaket verwendet dann LSA-Funktionen, um die [*Anmelde*](../secgloss/c-gly.md)Informationen zu überprüfen. Dieses Verfahren wird im folgenden Diagramm veranschaulicht.

![nicht interaktive Authentifizierung](images/lsasspi2.png)

Im vorangehenden Diagramm initiiert die Client Anwendung einen SSPI-Aufrufe, um eine authentifizierte Netzwerkverbindung anzufordern. SSPI übergibt die Anforderung des Clients an ein Sicherheitspaket zur Verarbeitung. Das Sicherheitspaket authentifiziert den Benutzer durch Aufrufen der [*lokalen Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) und durch Angabe eines [*Authentifizierungs Pakets*](../secgloss/a-gly.md) und Bereitstellen der vorhandenen Anmelde Informationen des Benutzers.

Das Authentifizierungs Ergebnis wird vom [*Authentifizierungs Paket*](../secgloss/a-gly.md)über die LSA an das [*Sicherheitspaket*](../secgloss/s-gly.md)und schließlich an SSPI übermittelt. SSPI benachrichtigt die Client Anwendung über das Ergebnis der Anforderung.

Weitere Informationen zu SSPI finden Sie [unter Security Support Provider Interface](sspi.md).

 

 
