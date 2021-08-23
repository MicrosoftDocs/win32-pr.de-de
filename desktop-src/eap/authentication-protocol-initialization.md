---
title: Initialisierung des Authentifizierungsprotokolls
description: Die EAP-gesicherte Verbindung wird für RAS- und Drahtlosclients (802.1X) auf ähnliche Weise zwischen Client und Server initialisiert.
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d53643718f747e1f39aaf68393f92a0577455041ec765ca19bea710f2c3aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984460"
---
# <a name="authentication-protocol-initialization"></a>Initialisierung des Authentifizierungsprotokolls

Die EAP-gesicherte Verbindung wird für RAS- und Drahtlosclients (802.1X) auf ähnliche Weise zwischen Client und Server initialisiert.

## <a name="client"></a>Client

Wenn der Client versucht, die Verbindung herzustellen, ruft der Authentifizierungsdienst [Identitätsinformationen](obtaining-identity-information.md) für den Benutzer ab. Wenn der **RAS \_ EAP \_ VALUENAME \_ INVOKE \_ NAMEDLG-Wert** in der Registrierung für dieses Authentifizierungsprotokoll vorhanden ist und dieser Wert auf 0 (null) festgelegt ist, ruft der Authentifizierungsdienst [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)auf. Diese Funktion zeigt in der Regel eine Benutzeroberfläche an, die es ermöglicht, dass die Identitätsinformationen einen für das Authentifizierungsprotokoll spezifischen Typ aufweisen. z. B. ein Zertifikat oder eine numerische ID. Wenn **RAS \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG** nicht vorhanden ist oder auf 1 festgelegt ist, zeigt der Authentifizierungsdienst das Dialogfeld Standardsystembenutzername an.

Sobald der Authentifizierungsdienst die Identitätsinformationen für den Benutzer abgerufen hat, ruft er die Implementierung des Authentifizierungsprotokolls von [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))auf. Mit diesem Aufruf kann das Authentifizierungsprotokoll einen Arbeitspuffer zuordnen und initialisieren, den der Dienst bei nachfolgenden Aufrufen von [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) und [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85))übergibt. Der Arbeitspuffer ist für den Dienst nicht transparent und greift nie auf den Inhalt des Arbeitspuffers zu. Wenn das Authentifizierungsprotokoll einen eigenen Arbeitspuffer für jede EAP-Sitzung erstellt, ist der Arbeitspuffer sitzungs- und threadsicher. Da das Authentifizierungsprotokoll den Arbeitsspeicher für den Arbeitspuffer zuordnet, sollte das Authentifizierungsprotokoll diesen Arbeitsspeicher auch mithilfe der [**RasEapFreeMemory-Funktion**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) freigeben.

Beim Aufruf von [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))übergibt der Dienst auch eine [**\_ PPS-EAP-EINGABEstruktur, \_**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) die Zeiger auf die Konfigurationsinformationen für die Verbindung und die Identitätsinformationen für den Benutzer enthält. Der Dienst übergibt immer einen Wert für den **pszIdentity-Member** von **EMAILS \_ EAP \_ INPUT**. Der **pszPassword-Member** von [**\_ PPEAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) kann jedoch **NULL** sein.

Innerhalb der [**\_ EAP \_ INPUT-Struktur von PPS**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) gibt der **fAuthenticator-Member** an, ob das Authentifizierungsprotokoll für die Authentifizierung (auf dem Client) oder als Authenticator (auf dem Server) aufgerufen wird.

## <a name="server"></a>Server

Auf dem Server gibt das **bInitialID-Mitglied** von [**\_ EQEAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) die ID an, die der Server für das erste EAP-Paket verwendet. Der Server erhöht diese ID für nachfolgende Pakete.

Auch auf dem Server zeigt der **pUserAttributes-Zeiger** in [**DER \_ \_ EAP-EINGABE für DEN CURSOR**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) auf ein Array von Attributen des TYPS RAS [**\_ AUTH ATTRIBUTE \_ \_ TYPE.**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) Dies sind Attribute für den Benutzer, die vom Client abgerufen wurden.

Wenn der [**RasEapBegin-Aufruf**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) einen anderen Wert als **NO \_ ERROR** zurückgibt, wird die Sitzung getrennt. Der zurückgegebene Fehler wird protokolliert (auf dem Server) oder dem Benutzer (auf dem Client) angezeigt.

 

 