---
description: Um böswillige Angriffe zu verhindern, bestimmen Sie, ob Ihre Anwendung Administratorrechte erfordert. Erstellen Sie für Funktionen, die Administratorberechtigungen erfordern, eine separate Anwendung, und verwenden Sie den Befehlszeilenbefehl Windows RunAs.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Ausführen mit Administratorrechten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87533e71fbce613ff01ec2cf4670f1632d46786eb2a5b77900f950357a9eaa8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622720"
---
# <a name="running-with-administrator-privileges"></a>Ausführen mit Administratorrechten

Der erste Schritt beim Festlegen des Kontotyps, unter dem Ihre Anwendung ausgeführt werden muss, besteht darin, zu untersuchen, welche Ressourcen von der Anwendung verwendet werden und welche privilegierten APIs aufgerufen werden. Sie stellen möglicherweise fest, dass die Anwendung oder große Teile davon keine Administratorrechte erfordern. *Writing Secure Code*, von Michael Fly und David LeBlanc bietet eine hervorragende Beschreibung der Durchführung dieser Bewertung und wird dringend empfohlen. (Diese Ressource ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

Sie können die Berechtigungen, die Ihre Anwendung benötigt, mit einem der folgenden Ansätze bereitstellen, um böswilligen Angriffen weniger ausgesetzt zu sein:

-   Führen Sie unter einem Konto mit weniger Berechtigungen aus. Eine Möglichkeit hierzu ist die Verwendung von [**PrivilegeCheck,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) um zu bestimmen, welche Berechtigungen in einem Token aktiviert sind. Wenn die verfügbaren Berechtigungen für den aktuellen Vorgang nicht ausreichen, können Sie diesen Code deaktivieren und den Benutzer bitten, sich bei einem Konto mit Administratorrechten zu anmelden.
-   Untergliedern Sie sich in separate Anwendungsfunktionen, die Administratorberechtigungen erfordern. Sie können dem Benutzer eine Verknüpfung bereitstellen, die den RunAs-Befehl ausführt. Ausführliche Anweisungen zum Einrichten der Verknüpfung finden Sie unter "runas" in der Hilfe. Programmgesteuert können Sie den [RunAs-Befehl](/windows/desktop/com/runas) unter dem Registrierungsschlüssel des [AppId-Schlüssels](/windows/desktop/com/appid-key) für Ihre Anwendung konfigurieren.
-   Authentifizieren Sie den Benutzer, indem [**Sie CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) oder [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (Befehlszeile) aufrufen, um Benutzername und Kennwort abzurufen. Ein Beispiel finden Sie unter [Fragen des Benutzers nach Anmeldeinformationen.](asking-the-user-for-credentials.md)
-   Identität des Benutzers annehmen. Ein Prozess, der unter einem Konto mit hohen Berechtigungen wie System gestartet wird, kann die Identität eines Benutzerkontos annehmen, indem [**impersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) oder ähnliche Identitätswechselfunktionen aufgerufen werden, wodurch die Berechtigungsstufe verringert wird. Wenn jedoch ein Aufruf von [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) in den Thread eingefügt wird, kehrt der Prozess zu den ursprünglichen Systemberechtigungen zurück.

Wenn Sie festgestellt haben, dass Ihre Anwendung unter einem Konto mit Administratorrechten ausgeführt werden muss und dass ein Administratorkennwort im Softwaresystem gespeichert werden muss, finden Sie unter Behandeln von [Kennwörtern](handling-passwords.md) Informationen zu sicheren Vorgehensweisen.

 

 
