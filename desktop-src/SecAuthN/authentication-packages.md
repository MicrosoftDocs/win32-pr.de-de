---
description: Authentifizierungspakete sind in Dynamic Link-Bibliotheken enthalten.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Authentifizierungspakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d556489d520ebf45224e3e9b8a5526cc4debcf1c7e7ab95028ecd9e35a6de217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141363"
---
# <a name="authentication-packages"></a>Authentifizierungspakete

[*Authentifizierungspakete*](/windows/desktop/SecGloss/a-gly) sind in Dynamic Link-Bibliotheken enthalten. Die lokale Sicherheitsstelle (Local [*Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) lädt Authentifizierungspakete mithilfe der in der Registrierung gespeicherten Konfigurationsinformationen. Durch das Laden mehrerer Authentifizierungspakete kann das LSA mehrere Anmeldeprozesse und mehrere [*Sicherheitsprotokolle unterstützen.*](/windows/desktop/SecGloss/s-gly)

Anmeldeprozesse verwenden Authentifizierungspakete, um Anmeldedaten zu analysieren. Neue Anmeldeprozesse werden einem System hinzugefügt, indem eine [*GINA*](/windows/desktop/SecGloss/g-gly) hinzugefügt wird, um die erforderlichen Anmeldedaten zu sammeln, und bei Bedarf durch Hinzufügen eines neuen Authentifizierungspakets zum Analysieren der Daten.

Sicherheitsprotokolle werden durch Authentifizierungspakete implementiert. Ein Authentifizierungspaket analysiert Anmeldedaten, indem die in einem Sicherheitsprotokoll festgelegten Regeln und Verfahren befolgen.

Authentifizierungspakete sind für die folgenden Aufgaben verantwortlich:

-   Analysieren von Anmeldedaten, um zu bestimmen, ob [*sich*](/windows/desktop/SecGloss/s-gly) ein Sicherheitsprinzipal bei einem System anmelden darf.
-   Einrichten einer neuen [*Anmeldesitzung*](/windows/desktop/SecGloss/l-gly) und Erstellen eines eindeutigen [*Anmeldebezeichners*](/windows/desktop/SecGloss/l-gly) für den erfolgreich authentifizierten Prinzipal.
-   Übergeben von Sicherheitsinformationen an das LSA für das Sicherheitstoken des Prinzipals.

Wenn ein Benutzer eine interaktive Anmeldung versucht, ruft die LSA ein Authentifizierungspaket auf, um zu bestimmen, ob der Benutzer sich anmelden kann. MSV1 0 ist beispielsweise ein Authentifizierungspaket, das mit dem Microsoft Windows \_ installiert wird. Das MSV1 \_ 0-Paket akzeptiert einen Benutzernamen und ein [*Hashkennwort.*](/windows/desktop/SecGloss/h-gly) Er sucht die Kombination aus Benutzername und Kennworthash in der SAM-Datenbank (Security Accounts Manager). Wenn die Anmeldedaten den gespeicherten Anmeldeinformationen [*entspricht,*](/windows/desktop/SecGloss/c-gly)lässt das Authentifizierungspaket zu, dass die Anmeldung erfolgreich ist.

Nach der erfolgreichen Authentifizierung der Anmeldeinformationen eines Sicherheitsprinzipals ist ein Authentifizierungspaket dafür [](/windows/desktop/SecGloss/l-gly) verantwortlich, eine neue LSA-Anmeldesitzung für den Prinzipal zu erstellen und den Anmeldebezeichner zu zuordnen, der die Anmeldesitzung eindeutig identifiziert. [](/windows/desktop/SecGloss/s-gly) Das Authentifizierungspaket kann der Anmeldesitzung Anmeldeinformationen für nachfolgende Authentifizierungsanforderungen zuordnen. Beispielsweise ordnet das Authentifizierungspaket MSV1 0 (von Microsoft bereitgestellt) den Benutzernamen und einen Hash des Kennworts des Benutzers jeder \_ Anmeldesitzung zu.

Das [*Authentifizierungspaket*](/windows/desktop/SecGloss/s-gly) stellt auch eine Reihe von Sicherheits-IDs (SIDs) und andere Informationen zur Verfügung, die für die Aufnahme in das vom LSA erstellte Sicherheitstoken geeignet sind. Dieses Token stellt den Sicherheitskontext des Prinzipals [*für den Zugriff*](/windows/desktop/SecGloss/c-gly) auf Windows dar.

Nachdem eine Anmeldesitzung erstellt und einem Prinzipal zugeordnet wurde, werden nachfolgende Authentifizierungsanforderungen, die im Auftrag des Prinzipals vorgenommen werden, anders behandelt als die erste Anmeldung. Das Authentifizierungspaket erstellt keine neue Anmeldesitzung und gibt keine Informationen zum Erstellen eines Tokens zurück. Das Authentifizierungspaket kann [](/windows/desktop/SecGloss/s-gly) jedoch zusätzliche Anmeldeinformationen, die während einer nachfolgenden Authentifizierung erhalten wurden, der vorhandenen Anmeldesitzung des Prinzipals zuordnen. Zusätzliche Anmeldeinformationen werden erhalten, wenn für den Zugriff auf eine angeforderte Ressource Informationen erforderlich sind, die über die anmeldeinformationen hinausgehen, die bei der ersten Anmeldung festgelegt wurden. Wenn ein angemeldeter Benutzer z. B. eine Anmeldung über das Netzwerk anklangt, kann ein Protokoll-spezifisches Authentifizierungspaket aufgerufen werden, und Es können anmeldespezifische Anmeldeinformationen authentifiziert und der Anmeldesitzung zugeordnet werden. Auf diese Anmeldeinformationen kann (über dasKtor-Authentifizierungspaket) von einem Bein-Redirector verwiesen werden, wenn der Benutzer auf das Netzwerk vonAuthent zutritt.

In den folgenden Themen werden die verschiedenen Typen von [*Authentifizierungspaketen behandelt:*](/windows/desktop/SecGloss/a-gly)

-   [Windows Authentifizierungspakete](windows-authentication-packages.md)
-   [Sicherheitssupportanbieter/Authentifizierungspakete](security-support-provider-authentication-packages.md)
-   [Von Microsoft bereitgestellte Authentifizierungspakete](authentication-packages-provided-by-microsoft.md)
-   [Unterauthentifizierungspakete](subauthentication-packages.md)

 

 
