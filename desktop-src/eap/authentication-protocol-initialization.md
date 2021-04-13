---
title: Initialisierung des Authentifizierungs Protokolls
description: Die von EAP gesicherte Verbindung wird auf der Basis von Client und Server auf ähnliche Weise für RAS-und drahtlose Clients (802.1 x) initialisiert.
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856bd173ef617fb272460f874fa1d2087322c8b4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390225"
---
# <a name="authentication-protocol-initialization"></a>Initialisierung des Authentifizierungs Protokolls

Die von EAP gesicherte Verbindung wird auf der Basis von Client und Server auf ähnliche Weise für RAS-und drahtlose Clients (802.1 x) initialisiert.

## <a name="client"></a>Client

Wenn der Client versucht, die Verbindung herzustellen, erhält der Authentifizierungsdienst [Identitätsinformationen](obtaining-identity-information.md) für den Benutzer. Wenn der **RAS- \_ EAP \_ valueName- \_ \_ namedlg** -Wert in der Registrierung für dieses Authentifizierungsprotokoll vorhanden ist und dieser Wert auf 0 (null) festgelegt ist, ruft der Authentifizierungsdienst [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)auf. Diese Funktion zeigt in der Regel eine Benutzeroberfläche an, die es ermöglicht, dass Identitätsinformationen von einem Typ sind, der für das Authentifizierungsprotokoll spezifisch ist. z. b. ein Zertifikat oder eine numerische ID. Wenn **RAS- \_ EAP- \_ valueName " \_ \_ namedlg aufrufen** " nicht vorhanden oder auf "1" festgelegt ist, zeigt der Authentifizierungsdienst das Standard Dialogfeld "Systembenutzer Name" an.

Nachdem der Authentifizierungsdienst die Identitätsinformationen für den Benutzer abgerufen hat, ruft er die Implementierung von [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))des Authentifizierungs Protokolls auf. Dieser Aufruf ermöglicht dem Authentifizierungsprotokoll das zuordnen und Initialisieren eines Arbeits Puffers, den der Dienst bei nachfolgenden Aufrufen von [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) und [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85))übergibt. Der Arbeits Puffer ist für den Dienst nicht transparent und greift nie auf den Inhalt des Arbeits Puffers zu. Wenn das Authentifizierungsprotokoll für jede EAP-Sitzung einen eindeutigen Arbeits Puffer erstellt, ist der Arbeits Puffer Sitzungs-und Thread sicher. Da das Authentifizierungsprotokoll den Arbeitsspeicher für den Arbeits Puffer zuordnet, sollte das Authentifizierungsprotokoll auch diesen Speicher mithilfe der [**raseapfreememory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) -Funktion freigeben.

Beim Aufrufen von [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))übergibt der Dienst außerdem eine PPP- [**\_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur, die Zeiger auf die Konfigurationsinformationen für die Verbindung und die Identitätsinformationen für den Benutzer enthält. Der Dienst übergibt immer einen Wert für den **pszidentity** -Member der **PPP- \_ EAP- \_ Eingabe**. Allerdings kann das **pszpassword** -Mitglied der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) **null** sein.

Innerhalb der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur gibt der **fauthenticator** -Member an, ob das Authentifizierungsprotokoll zum Authentifizieren (auf dem Client) oder als Authentifikator (auf dem Server) aufgerufen wird.

## <a name="server"></a>Server

Auf dem Server gibt das **binitialid-** Mitglied der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) die ID an, die der Server für das erste EAP-Paket verwendet. Der Server erhöht diese ID für nachfolgende Pakete.

Auf dem Server zeigt der **puserattribute** -Zeiger in der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) auf ein Array von Attributen des RAS-Authentifizierungs [**\_ \_ \_ Attributtyps**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) . Dies sind Attribute für den Benutzer, die vom Client abgerufen wurden.

Wenn der [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) -Rückruf einen anderen Wert als " **No \_ Error**" zurückgibt, wird die Sitzung getrennt. Der zurückgegebene Fehler wird (auf dem Server) protokolliert oder für den Benutzer (auf dem Client) angezeigt.

 

 