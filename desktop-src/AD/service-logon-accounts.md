---
title: Dienst Anmeldekonten
description: Ein Dienst hat wie ein beliebiger Prozess eine primäre Sicherheitsidentität, die die gewährten Zugriffsrechte und Berechtigungen für lokale und Netzwerkressourcen bestimmt.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory mithilfe von, Dienst Anmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855383"
---
# <a name="service-logon-accounts"></a>Dienst Anmeldekonten

Ein Dienst hat wie ein beliebiger Prozess eine primäre Sicherheitsidentität, die die gewährten Zugriffsrechte und Berechtigungen für lokale und Netzwerkressourcen bestimmt. Diese Sicherheitsidentität oder der Sicherheitskontext bestimmt auch das Potenzial, das der Dienst für schädliche lokale Ressourcen und Netzwerkressourcen hat.

Der Sicherheitskontext für einen Microsoft Win32-Dienst wird durch das Anmelde Konto bestimmt, das zum Starten des Diensts verwendet wird. In diesem Abschnitt werden Programmierprobleme und bewährte Methoden im Zusammenhang mit dem Dienst Anmelde Konto erläutert, das von Win32-Diensten verwendet wird, wobei der Schwerpunkt auf Verzeichnis aktivierten Diensten liegt. Dieser Abschnitt schließt folgende Themen ein:

-   [Informationen zu Dienst Anmeldekonten](about-service-logon-accounts.md)– eine Übersicht über Dienst Anmeldekonten und Probleme beim Programmieren von Sicherheits Kontexten für einen Win32-Dienst.
-   [Richtlinien für das Auswählen eines Dienst Anmelde Kontos](guidelines-for-selecting-a-service-logon-account.md) für einen Win32-Dienst.
-   [Einrichten des Benutzerkontos eines Dienstanbieter](setting-up-a-serviceampaposs-user-account.md).
-   [Installieren eines Diensts auf einem Host Computer](installing-a-service-on-a-host-computer.md) und angeben des Dienst Anmelde Kontos.
-   Gewähren der Berechtigung " [Anmelden als Dienst" auf dem Host Computer](granting-logon-as-service-right-on-the-host-computer.md)– gewähren des Benutzerkontos "Anmelden als Dienst" auf dem Host Computer für das Benutzerkonto des Diensts.
-   [Testen, ob auf einem Domänen Controller ausgeführt](testing-whether-running-on-a-domain-controller.md)wird – erkennen, ob die Dienst Instanz auf einem Domänen Controller installiert ist.
-   [Erteilen von Zugriffsrechten für das Dienst Anmelde Konto](granting-access-rights-to-the-service-logon-account.md)– festlegen und Verwalten von ACEs und Gruppenmitgliedschaften, um sicherzustellen, dass das System dem laufenden Dienst Zugriff auf die erforderlichen lokalen Ressourcen und Netzwerkressourcen gewährt.
-   [Ändern des Kennworts für das Benutzerkonto eines Diensts](changing-the-password-on-a-serviceampaposs-user-account.md)– Ändern des Kennworts für das Benutzerkonto eines Diensts und gleichzeitigem Aktualisieren des Kennworts, das mit dem Dienststeuerungs-Manager auf jedem Host Server registriert ist, auf dem der Dienst installiert ist.
-   [Gegenseitige Authentifizierung mithilfe von Kerberos](mutual-authentication-using-kerberos.md)– Wartung der Dienst Prinzipal Namen-Registrierung (SPN) für das Verzeichnis Objekt, das dem Anmelde Konto der einzelnen Instanzen Ihres Diensts zugeordnet ist. Mithilfe von SPNs können Clients einen Dienst mithilfe der gegenseitigen Kerberos-Authentifizierung authentifizieren.
-   Das [Umrechnen von Domänen Konto-namens Formaten](converting-domain-account-name-formats.md)– z. b. das Umbenennen eines Distinguished Name in das *Domänen ***\\*** Benutzernamen* Format und umgekehrt

 

 




