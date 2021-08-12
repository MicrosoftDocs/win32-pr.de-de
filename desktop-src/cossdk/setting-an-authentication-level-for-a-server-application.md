---
description: Wenn Sie eine Authentifizierungsebene für eine Anwendung festlegen, bestimmen Sie, welcher Authentifizierungsgrad ausgeführt wird, wenn Clients die Anwendung aufrufen.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Festlegen einer Authentifizierungsebene für eine Serveranwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6248574117a55420940fbaf24f88c5d3b2c8721e6fa022bad5923ba658bf5da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546254"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Festlegen einer Authentifizierungsebene für eine Serveranwendung

Wenn Sie eine Authentifizierungsebene für eine Anwendung festlegen, bestimmen Sie, welcher Authentifizierungsgrad ausgeführt wird, wenn Clients die Anwendung aufrufen. Höhere Authentifizierungsebenen sorgen für mehr Sicherheit und Datenintegrität, allerdings in der Regel mit leistungsschädigungen. Weitere Informationen finden Sie unter [Clientauthentifizierung](client-authentication.md).

**So wählen Sie eine Authentifizierungsebene für eine Serveranwendung aus**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Authentifizierung festlegen, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die **Registerkarte** Sicherheit.

3.  Wählen Sie **im Feld Authentifizierungsebene für** Aufrufe die entsprechende Ebene aus. Die Ebenen sind wie folgt und von der niedrigsten zur höchsten Sicherheit geordnet:

    -   **Keine**. Es erfolgt keine Authentifizierung.
    -   **Verbinden**. Authentifiziert Anmeldeinformationen nur dann, wenn die Verbindung hergestellt wurde.
    -   **Rufen Sie auf.** Authentifiziert am Anfang jedes Aufrufs die Anmeldeinformationen.
    -   **Paket**. Authentifiziert Anmeldeinformationen und überprüft, ob alle Aufrufdaten empfangen wurden. Dies ist die Standardeinstellung für COM+-Serveranwendungen.
    -   **Paketintegrität.** Authentifiziert Anmeldeinformationen und stellt sicher, dass während der Übertragung keine Aufrufdaten geändert wurden.
    -   **Paketschutz**. Authentifiziert Anmeldeinformationen und verschlüsselt das Paket, einschließlich der Daten sowie der Identität und Signatur des Absenders.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren der Authentifizierung für eine Bibliotheksanwendung](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



