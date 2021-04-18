---
description: Bestimmen Sie, ob Ihre Anwendung Administratorrechte erfordert, um böswillige Angriffe zu verhindern. Erstellen Sie für Funktionen, für die Administrator Berechtigungen erforderlich sind, eine separate Anwendung, und verwenden Sie den Befehlszeilen Befehl Windows runas.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Ausführen mit Administrator Rechten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc28843195e9b5cabadc13aa2317b0bdd8058ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351084"
---
# <a name="running-with-administrator-privileges"></a>Ausführen mit Administrator Rechten

Der erste Schritt beim Einrichten des Kontos, unter dem Ihre Anwendung ausgeführt werden muss, besteht darin, zu überprüfen, welche Ressourcen von der Anwendung verwendet werden und welche privilegierten APIs Sie aufruft. Möglicherweise stellen Sie fest, dass die Anwendung oder große Teile davon keine Administratorrechte erfordern. Das *Schreiben von sicherem Code* von Michael Howard und David LeBlanc bietet eine ausgezeichnete Beschreibung, wie diese Bewertung durchgeführt werden kann, und es wird dringend empfohlen. (Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)

Mithilfe eines der folgenden Ansätze können Sie die von Ihrer Anwendung benötigten Berechtigungen mit weniger Anfälligkeit für böswillige Angriffe bereitstellen:

-   Führen Sie unter einem Konto mit weniger Berechtigungen aus. Eine Möglichkeit hierfür ist die Verwendung von [**privilegecheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) , um zu bestimmen, welche Berechtigungen in einem Token aktiviert werden. Wenn die verfügbaren Berechtigungen für den aktuellen Vorgang nicht ausreichen, können Sie diesen Code deaktivieren und den Benutzer bitten, sich bei einem Konto mit Administratorrechten anzumelden.
-   Unterbrechen Sie separate Anwendungsfunktionen, für die Administrator Berechtigungen erforderlich sind. Sie können für den Benutzer eine Verknüpfung bereitstellen, die den runas-Befehl ausführt. Ausführliche Anweisungen zum Einrichten der Verknüpfung finden Sie unter "runas" in der Hilfe. Programm gesteuert können Sie den Befehl [runas](/windows/desktop/com/runas) unter dem Schlüssel Registrierungsschlüssel [AppID](/windows/desktop/com/appid-key) für Ihre Anwendung konfigurieren.
-   Authentifizieren Sie den Benutzer durch Aufrufen von [**creduipromptforanmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Informationen (GUI) oder [**creduicmdlinepromptforanmelde**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) Informationen (Befehlszeile), um den Benutzernamen und das Kennwort zu erhalten. Ein Beispiel finden Sie unter [anfordern von Anmelde Informationen für den Benutzer](asking-the-user-for-credentials.md).
-   Nimmt die Identität des Benutzers an. Ein Prozess, der unter einem Konto mit weitreichenden Berechtigungen wie dem System gestartet wird, kann die Identität eines Benutzerkontos annehmen, indem er den Wert von "Identität [**ateloggedonuser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) " oder ähnliche Identitätswechsel Funktionen annimmt Wenn jedoch ein Rückruf von [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) in den Thread eingefügt wird, wird der Prozess zu den ursprünglichen System Privilegien zurückgegeben.

Wenn Sie festgestellt haben, dass Ihre Anwendung unter einem Konto mit Administratorrechten ausgeführt werden muss und dass ein Administrator Kennwort im Softwaresystem gespeichert werden muss, finden Sie weitere Informationen unter Behandeln von Kenn [Wörtern](handling-passwords.md) für eine sichere Vorgehensweise.

 

 
