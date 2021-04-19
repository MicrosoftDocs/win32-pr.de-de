---
description: Listet die Sicherheitspakete auf, die mit SSPI verwendet werden können.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Verwenden von Sicherheitspaketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360716"
---
# <a name="using-security-packages"></a>Verwenden von Sicherheitspaketen

Die [*Security Support Provider-Schnittstelle*](../secgloss/s-gly.md) (SSPI) kann mit den folgenden [*Sicherheitspaketen*](../secgloss/s-gly.md)verwendet werden:

-   [Kerberos-Sicherheitspaket](#kerberos-security-package)
-   [NTLM-Sicherheitspaket](#ntlm-security-package)

Die [*Kerberos*](../secgloss/k-gly.md) -und NTLM-Protokolle werden als Sicherheitspakete von der Secur32.dll [*Security Support Provider*](../secgloss/s-gly.md) (SSP) implementiert, die mit dem Betriebssystem bereitgestellt werden. Standardmäßig wird die Unterstützung für die Kerberos-und NTLM-Authentifizierung von der [*lokalen Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) auf einem Computer geladen, wenn das System gestartet wird. In Windows Server-oder Windows-Domänen können beide Pakete zum Authentifizieren von Netzwerk Anmeldungen und Client-/Serververbindungen verwendet werden. Welches verwendet wird, hängt von den Funktionen des Computers auf der anderen Seite der Verbindung ab. Das Kerberos-Protokoll wird immer bevorzugt, falls verfügbar.

Nachdem ein Sicherheitskontext für einen interaktiven Benutzer eingerichtet wurde, kann eine andere Instanz des Kerberos-oder NTLM-Pakets von einem Prozess geladen werden, der im Sicherheitskontext des Benutzers ausgeführt wird, um das austauschen, signieren, überprüfen, verschlüsseln und Entschlüsseln von Nachrichten zu unterstützen. Es ist jedoch nicht zulässig, dass der andere Prozess als die LSA den Zugriff auf die [*Sitzungsschlüssel*](../secgloss/s-gly.md) oder Tickets im Anmelde Informations Cache gestattet.

System Dienste und Anwendungen auf Transport Ebene greifen über SSPI auf einen SSP zu, der Funktionen zum Auflisten der auf einem System verfügbaren Sicherheitspakete, zum Auswählen eines Pakets und zum Verwenden dieses Pakets zum Abrufen einer authentifizierten Verbindung bietet.

Die Methoden in SSPI sind generische Routinen, die Entwickler verwenden können, ohne die Details eines bestimmten [*Sicherheitsprotokolls*](../secgloss/s-gly.md)kennen zu müssen. Wenn z. b. eine Client-/Serververbindung authentifiziert wird:

1.  Die Anwendung auf der Clientseite der Verbindung sendet mithilfe der SSPI-Funktion [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) [*Anmelde*](../secgloss/c-gly.md) Informationen an den Server.
2.  Die Anwendung auf der Serverseite der Verbindung antwortet mit der SSPI-Funktion [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).
3.  Nachdem die Verbindung authentifiziert wurde, werden von der LSA auf dem Server Informationen vom Client verwendet, um ein [*Zugriffs Token*](../secgloss/a-gly.md)zu erstellen.
4.  Der Server kann dann die SSPI-Funktion mit dem Identitätsnachweis [**atesecuritycontext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) aufrufen, um das Zugriffs Token an einen Identitätswechsel Thread für den Dienst anzufügen.

## <a name="kerberos-security-package"></a>Kerberos-Sicherheitspaket

Das Kerberos- [*Sicherheitspaket*](../secgloss/s-gly.md) basiert auf dem [*Kerberos-Authentifizierungsprotokoll*](../secgloss/k-gly.md).

Wenn das Kerberos-Protokoll verwendet wird, um eine Client/Server-Verbindung zu authentifizieren, generiert [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) eine GSSAPI-Nachricht, die eine krb \_ AP- \_ req-Nachricht vom Client enthält. " [**Accept-SecurityContext" (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) generiert dann eine GSSAPI-Nachricht, die eine krb \_ AP Rep- \_ Nachricht vom Server enthält.

Hintergrundinformationen zu den Schritten, die im Hintergrund in der Implementierung eines Kerberos-Protokolls stattfinden, finden Sie unter [Microsoft Kerberos](microsoft-kerberos.md).

Alle verteilten Dienste verwenden SSPI für den Zugriff auf das Kerberos-Protokoll. Eine partielle Liste der Methoden, mit denen das Kerberos-Protokoll für die Authentifizierung verwendet wird, umfasst Folgendes:

-   Druckspoolerdienste
-   CIFS/SMB-Remote Dateizugriff
-   [*LDAP*](../secgloss/l-gly.md) -Abfragen für den Active Directory
-   Verteilte Dateisystem Verwaltung und-Verweise
-   Authentifizierung der IPSec-Host-zu-Host-Sicherheits Autorität
-   Reservierungs Anforderungen für Netzwerk Quality of Service
-   Intranetauthentifizierung zum Internetinformationsdienste
-   Remote Server-oder Arbeitsstations Verwaltung mithilfe von authentifizierter RPC
-   [*Zertifikat Anforderungen*](../secgloss/c-gly.md) an Zertifikat Dienste für Domänen Benutzer und-Computer

## <a name="ntlm-security-package"></a>NTLM-Sicherheitspaket

Das NTLM-Sicherheitspaket basiert auf dem NTLM-Authentifizierungsprotokoll.

 

 
