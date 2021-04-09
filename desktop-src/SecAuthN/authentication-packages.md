---
description: Authentifizierungs Pakete sind in Dynamic Link Libraries enthalten.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Authentifizierungs Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff02017b653521d80741bcdf3c205ab924c4bceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866020"
---
# <a name="authentication-packages"></a>Authentifizierungs Pakete

[*Authentifizierungs Pakete*](/windows/desktop/SecGloss/a-gly) sind in Dynamic Link Libraries enthalten. Die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) lädt Authentifizierungs Pakete mithilfe von Konfigurationsinformationen, die in der Registrierung gespeichert sind. Durch das Laden mehrerer Authentifizierungs Pakete wird der LSA die Unterstützung mehrerer Anmelde Prozesse und mehrerer [*Sicherheitsprotokolle*](/windows/desktop/SecGloss/s-gly)ermöglicht.

Anmelde Prozesse verwenden Authentifizierungs Pakete, um Anmeldedaten zu analysieren. Neue Anmelde Prozesse werden einem System hinzugefügt, indem eine [*Gina*](/windows/desktop/SecGloss/g-gly) hinzugefügt wird, um die erforderlichen Anmeldedaten zu erfassen, und ggf. durch Hinzufügen eines neuen Authentifizierungs Pakets, um die Daten zu analysieren.

Sicherheitsprotokolle werden von Authentifizierungs Paketen implementiert. Ein Authentifizierungs Paket analysiert Anmeldedaten anhand der Regeln und Prozeduren, die in einem Sicherheitsprotokoll festgelegt sind.

Authentifizierungs Pakete sind für die folgenden Aufgaben verantwortlich:

-   Analysieren von Anmeldedaten, um zu bestimmen, ob sich ein [*Sicherheits Prinzipal*](/windows/desktop/SecGloss/s-gly) an einem System anmelden darf.
-   Einrichten einer neuen [*Anmelde Sitzung*](/windows/desktop/SecGloss/l-gly) und Erstellen eines eindeutigen [*Anmelde Bezeichners*](/windows/desktop/SecGloss/l-gly) für den erfolgreich authentifizierten Prinzipal.
-   Übergeben von Sicherheitsinformationen an die LSA für das Sicherheits Token des Prinzipals.

Wenn ein Benutzer versucht, eine interaktive Anmeldung durchzusetzen, ruft die LSA ein Authentifizierungs Paket auf, um zu bestimmen, ob der Benutzer sich anmelden darf. MSV1 \_ 0 ist beispielsweise ein Authentifizierungs Paket, das mit dem Betriebssystem Microsoft Windows installiert wird. Das \_ Paket MSV1 0 akzeptiert einen Benutzernamen und ein [](/windows/desktop/SecGloss/h-gly) Hash Kennwort. Die Kombination aus Benutzername und Hashwert des Kennworts wird in der Security Accounts Manager (Sam)-Datenbank nachgeschlagen. Wenn die Anmeldedaten mit den gespeicherten [*Anmelde*](/windows/desktop/SecGloss/c-gly)Informationen übereinstimmen, kann das Authentifizierungs Paket die Anmeldung erfolgreich durchführen.

Nachdem die Anmelde Informationen eines [*Sicherheits Prinzipals*](/windows/desktop/SecGloss/s-gly) erfolgreich authentifiziert wurden, ist ein Authentifizierungs Paket für das Erstellen einer neuen LSA-Anmelde Sitzung für den Prinzipal und die Zuordnung des [*Anmelde Bezeichners*](/windows/desktop/SecGloss/l-gly) verantwortlich, der die Anmelde Sitzung eindeutig identifiziert. Das Authentifizierungs Paket kann Anmelde Informationen in der Anmelde Sitzung für nachfolgende Authentifizierungsanforderungen zuordnen. Beispielsweise ordnet das \_ Authentifizierungs Paket MSV1 0 (von Microsoft bereitgestellt) den Benutzerkonto Namen und einen Hash des Benutzer Kennworts zu jeder Anmelde Sitzung zu.

Das Authentifizierungs Paket bietet auch eine Reihe von [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) und weitere Informationen, die für die Einbindung in das von der LSA erstellten Sicherheits Token geeignet sind. Dieses Token stellt den Sicherheits [*Kontext*](/windows/desktop/SecGloss/c-gly) des Prinzipals für den Zugriff auf Windows-Vorgänge dar.

Nachdem eine Anmelde Sitzung erstellt und einem Prinzipal zugeordnet wurde, werden nachfolgende Authentifizierungsanforderungen, die im Namen des Prinzipals erfolgen, anders behandelt als bei der ersten Anmeldung. Das Authentifizierungs Paket erstellt keine neue Anmelde Sitzung und gibt keine Informationen zum Erstellen eines Tokens zurück. Das Authentifizierungs Paket kann jedoch [*zusätzliche Anmelde*](/windows/desktop/SecGloss/s-gly) Informationen zuordnen, die während einer nachfolgenden Authentifizierung mit der vorhandenen Anmelde Sitzung des Prinzipals abgerufen wurden. Zusätzliche Anmelde Informationen werden abgerufen, wenn der Zugriff auf eine angeforderte Ressource über die Anmelde Informationen hinausgeht, die von der anfänglichen Anmeldung festgelegt wurden. Wenn ein angemeldeter Benutzer z. b. eine Novell-Netzwerk Anmeldung anfordert, kann ein Novell-spezifisches Authentifizierungs Paket aufgerufen werden, und Novell-spezifische Anmelde Informationen können authentifiziert und der Anmelde Sitzung zugeordnet werden. Diese Anmelde Informationen können von einem Novell Redirector (über das Novell-Authentifizierungs Paket) referenziert werden, wenn der Benutzer auf das Novell-Netzwerk zugreift.

In den folgenden Themen werden die verschiedenen Typen von [*Authentifizierungs Paketen*](/windows/desktop/SecGloss/a-gly)erläutert:

-   [Windows-Authentifizierungs Pakete](windows-authentication-packages.md)
-   [Anbieter für Sicherheitsunterstützung/Authentifizierungs Pakete](security-support-provider-authentication-packages.md)
-   [Von Microsoft bereitgestellte Authentifizierungs Pakete](authentication-packages-provided-by-microsoft.md)
-   [Unter Authentifizierungs Pakete](subauthentication-packages.md)

 

 
