---
description: Wenn Sie eine Authentifizierungs Ebene für eine Anwendung festlegen, legen Sie fest, welcher Grad an Authentifizierung durchgeführt wird, wenn Clients die Anwendung anrufen.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Festlegen einer Authentifizierungs Ebene für eine Server Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345622"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Festlegen einer Authentifizierungs Ebene für eine Server Anwendung

Wenn Sie eine Authentifizierungs Ebene für eine Anwendung festlegen, legen Sie fest, welcher Grad an Authentifizierung durchgeführt wird, wenn Clients die Anwendung anrufen. Höhere Authentifizierungs Ebenen sorgen für eine höhere Sicherheit und Datenintegrität, auch wenn dies in der Regel zu Leistungseinbußen führen kann. Weitere Informationen finden Sie unter [Client Authentifizierung](client-authentication.md).

**So wählen Sie eine Authentifizierungs Ebene für eine Serveranwendung aus**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Authentifizierung festlegen, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Wählen Sie im Feld **Authentifizierungs Ebene für Anrufe** die entsprechende Ebene aus. Die folgenden Ebenen sind von der niedrigsten zur höchsten Sicherheit geordnet:

    -   **Keine**. Es erfolgt keine Authentifizierung.
    -   **Verbinden** Sie sich. Authentifiziert Anmeldeinformationen nur dann, wenn die Verbindung hergestellt wurde.
    -   **Aufgerufen** wird. Authentifiziert am Anfang jedes Aufrufs die Anmeldeinformationen.
    -   **Paket**. Authentifiziert Anmeldeinformationen und überprüft, ob alle Aufrufdaten empfangen wurden. Dies ist die Standardeinstellung für com+-Server Anwendungen.
    -   **Paketintegrität**. Authentifiziert Anmeldeinformationen und stellt sicher, dass während der Übertragung keine Aufrufdaten geändert wurden.
    -   **Paket Datenschutz**. Authentifiziert Anmeldeinformationen und verschlüsselt das Paket, einschließlich der Daten sowie der Identität und Signatur des Absenders.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



