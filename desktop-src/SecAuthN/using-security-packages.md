---
description: Listet die Sicherheitspakete auf, die mit SSPI verwendet werden können.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Verwenden von Sicherheitspaketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9253ee2ac4cec98e3c68a1f3dab80a71b216e6235af78722864ee0e0958897c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915192"
---
# <a name="using-security-packages"></a>Verwenden von Sicherheitspaketen

Die [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) kann mit den folgenden [*Sicherheitspaketen*](../secgloss/s-gly.md)verwendet werden:

-   [Kerberos-Sicherheitspaket](#kerberos-security-package)
-   [NTLM-Sicherheitspaket](#ntlm-security-package)

Die Kerberos- und [*NTLM-Protokolle*](../secgloss/k-gly.md) werden als Sicherheitspakete vom [*Secur32.dll-Sicherheitsunterstützungsanbieter (Security Support Provider,*](../secgloss/s-gly.md) SSP) implementiert, der mit dem Betriebssystem bereitgestellt wird. Standardmäßig wird die Unterstützung für kerberos- und NTLM-Authentifizierung von der [*lokalen Sicherheitsautorität*](../secgloss/l-gly.md) (LSA) auf einem Computer geladen, wenn das System gestartet wird. In Windows Server- oder Windows-Domänen können beide Pakete verwendet werden, um Netzwerkanmeldungen und Client-/Serververbindungen zu authentifizieren. Welche verwendet wird, hängt von den Funktionen des Computers auf der anderen Seite der Verbindung ab. Das Kerberos-Protokoll wird immer bevorzugt, sofern verfügbar.

Nachdem ein Sicherheitskontext für einen interaktiven Benutzer eingerichtet wurde, kann eine andere Instanz des Kerberos- oder NTLM-Pakets durch einen Prozess geladen werden, der im Sicherheitskontext des Benutzers ausgeführt wird, um das Austauschen, Signieren, Überprüfen, Verschlüsseln und Entschlüsseln von Nachrichten zu unterstützen. Allerdings wird kein anderer Prozess als der LSA jemals Zugriff auf [*Sitzungsschlüssel*](../secgloss/s-gly.md) oder Tickets im Cache für Anmeldeinformationen gewährt.

Systemdienste und Anwendungen auf Transportebene greifen über SSPI auf einen SSP zu, der Funktionen zum Aufzählen der auf einem System verfügbaren Sicherheitspakete, zum Auswählen eines Pakets und zum Verwenden dieses Pakets zum Abrufen einer authentifizierten Verbindung bereitstellt.

Die Methoden in SSPI sind generische Routinen, die Entwickler verwenden können, ohne die Details eines bestimmten [*Sicherheitsprotokolls*](../secgloss/s-gly.md)zu kennen. Wenn beispielsweise eine Client-/Serververbindung authentifiziert wird:

1.  Die Anwendung auf der Clientseite der Verbindung sendet [*Anmeldeinformationen*](../secgloss/c-gly.md) mithilfe der SSPI-Funktion [**InitializeSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)an den Server.
2.  Die Anwendung auf der Serverseite der Verbindung antwortet mit der SSPI-Funktion [**AcceptSecurityContext (Allgemein).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  Nachdem die Verbindung authentifiziert wurde, verwendet das LSA auf dem Server Informationen vom Client, um ein [*Zugriffstoken*](../secgloss/a-gly.md)zu erstellen.
4.  Der Server kann dann die SSPI-Funktion [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) aufrufen, um das Zugriffstoken an einen Identitätswechselthread für den Dienst anzufügen.

## <a name="kerberos-security-package"></a>Kerberos-Sicherheitspaket

Das [*Kerberos-Sicherheitspaket*](../secgloss/s-gly.md) basiert auf dem [*Kerberos-Authentifizierungsprotokoll*](../secgloss/k-gly.md).

Wenn das Kerberos-Protokoll zum Authentifizieren einer Client-/Serververbindung verwendet wird, generiert [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) eine GSSAPI-Nachricht, die eine KRB-AP-REQ-Nachricht \_ vom Client \_ enthält. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) generiert dann eine GSSAPI-Nachricht, die eine \_ KRB-AP-REP-Nachricht \_ vom Server enthält.

Hintergrundinformationen zu den Schritten, die im Hintergrund bei der Implementierung eines Kerberos-Protokolls erfolgen, finden Sie unter [Microsoft Kerberos](microsoft-kerberos.md).

Alle verteilten Dienste verwenden SSPI für den Zugriff auf das Kerberos-Protokoll. Eine partielle Liste der Methoden, mit denen das Kerberos-Protokoll für die Authentifizierung verwendet wird, umfasst Folgendes:

-   Druckspoolerdienste
-   CIFS/SMB-Remotedateizugriff
-   [*LDAP-Abfragen*](../secgloss/l-gly.md) an Active Directory
-   Verteilte Dateisystemverwaltung und Empfehlungen
-   IPsec-Authentifizierung zwischen Host- und Hostsicherheitsstellen
-   Reservierungsanforderungen für netzwerk Quality of Service
-   Intranetauthentifizierung bei Internetinformationsdienste
-   Remoteserver- oder Arbeitsstationsverwaltung mithilfe eines authentifizierten RPC
-   [*Zertifikatanforderungen*](../secgloss/c-gly.md) an Zertifikatdienste für Domänenbenutzer und Computer

## <a name="ntlm-security-package"></a>NTLM-Sicherheitspaket

Das NTLM-Sicherheitspaket basiert auf dem NTLM-Authentifizierungsprotokoll.

 

 
