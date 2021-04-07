---
title: Zugriffspunkt-und Authentifizierungsprotokoll Interaktion während der Authentifizierung
description: Die raseapmakemess-Funktion steuert die Mehrzahl der Interaktionen zwischen dem Authentifizierungsprotokoll und dem Zugriffspunkt (Access Point, AP).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e486e3a10e323f28bc2f6fef4c131acfc095b48
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038830"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Zugriffspunkt-und Authentifizierungsprotokoll Interaktion während der Authentifizierung

Die [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) -Funktion steuert die Mehrzahl der Interaktionen zwischen dem Authentifizierungsprotokoll und dem Zugriffspunkt (Access Point, AP). **Raseapmakemess** verarbeitet eingehende EAP-Pakete und erstellt EAP-Pakete für die Übertragung an den Remotepeer. Außerdem werden Ereignisse wie Timeouts und Abschluss der Authentifizierung verarbeitet.

Wenn vom Remotepeer eine Nachricht empfangen wird, ruft der AP-Authentifizierungsdienst [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))auf und übergibt dabei einen Zeiger auf die empfangene Nachricht im *preceivepacket* -Parameter.

Wenn der Dienst [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) aufruft, bei dem *preceivepacket* auf **null** festgelegt ist, initiiert der AP entweder den Dialog mit dem Authentifizierungsprotokoll oder fordert an, dass das Protokoll das letzte Paket erneut sendet. Das Authentifizierungsprotokoll sollte bestimmen, welche Aktion der Dienst basierend auf seinem Zustand und aus dem Nachrichten Kontext durch nimmt.

Bei der Rückgabe von [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))gibt der Wert des **Action** -Members der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Struktur an, welche Aktion (falls vorhanden) der Authentifizierungsdienst durchführt. Der **Action** -Member nimmt Werte aus dem enumerierten Typ der [**PPP- \_ EAP- \_ Aktion**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action) auf.

Wenn **Action** " **eapaction \_ Send**", " **eapaction \_ sendanddone**", " **eapaction \_ sendwithtimeout**" oder " **eapaction \_ sendwithtimeoutinteractive**" ist, überträgt der Dienst das Paket, auf das durch den *psendpacket* -Parameter verwiesen wird, an den Remotepeer.

Der **eapaction-Wert \_ sendwithtimeout** ermöglicht einen Timeout. Danach geht der Authentifizierungsdienst davon aus, dass der Link verloren gegangen ist, und trennt die Sitzung.

Der **eapaction-Wert \_ sendwithtimeoutinteractive** ermöglicht einen unendlichen Zeitaufwand. Der Authentifikator sollte diesen Wert verwenden, wenn Benutzereingaben auf dem Client erwartet werden. Dieses Timeout ermöglicht dem Benutzer eine nicht angegebene Zeitspanne, um die erforderliche Eingabe abzuschließen.

Wenn **Action** " **eapaction \_ sendwithtimeout** " oder " **eapaction \_ sendwithtimeoutinteractive**" ist, sollte das Authentifizierungsprotokoll den " **dwidexpzierte** "-Member der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Struktur auf den Bezeichner des nächsten Pakets festlegen, das vom Remotepeer erwartet wird. Unabhängig davon, ob das nächste vom Peer empfangene Paket mit diesem Wert übereinstimmt, übergibt der Authentifizierungsdienst das Paket in einem nachfolgenden Aufrufer von [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))an das Authentifizierungsprotokoll. Das Authentifizierungsprotokoll kann das Paket im Hintergrund verwerfen, indem es einfach das **\_ ungültige Fehler PPP- \_ \_ Paket** zurückgibt. Wenn ein Paket mit dem erwarteten Bezeichner nicht innerhalb des konfigurierten Timeout Zeitraums empfangen wird, ruft der Authentifizierungsdienst weiterhin **raseapmakemess** auf. In diesem Fall wird der-Befehl mit dem *preceivepacket* -Parameter auf **null** festgelegt, um anzugeben, dass das vorherige Paket erneut gesendet werden muss.

Wenn der **Aktionsmember** **eapaction \_ done** oder **eapaction \_ sendanddone** ist, untersucht der Authentifizierungsdienst den **dwauthresultcode** -Member der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Wenn **dwauthresultcode** keinen \_ Fehler hat, war die Authentifizierung erfolgreich. Wenn **dwauthresultcode** ein anderer Wert als No \_ Error ist, ist die Authentifizierung fehlgeschlagen. Der Fehlercode, der für den Fehlerfall zurückgegeben wird, sollte von "raserror. h", "mprerror. h" oder "Winerror. h" stammen. Mögliche Rückgabecodes sind u. a. die folgenden:

-   Fehler " \_ keine \_ Dialin- \_ Berechtigung"
-   Fehler " \_ passwd" \_ abgelaufen
-   Fehler beim \_ \_ Deaktivieren
-   Fehler beim \_ Einschränken der \_ Anmelde \_ Zeiten.
-   Fehler Authentifizierung ( \_ \_ intern)

Wenn **Action** **eapaction \_ done** oder **eapaction \_ sendanddone** ist, sollte der **puserattribute** -Member auf Attribute verweisen, die Attribute desselben Typs überschreiben, die im-Befehl von [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))an den Server weitergegeben wurden.

Das Authentifizierungsprotokoll auf dem Server kann anfordern, dass der Authentifizierungsdienst den aktuellen Authentifizierungs Anbieter aufruft, indem er **eapaction- \_ Authentifizieren** im **Aktions** Mitglied in der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)zurückgibt. In diesem Fall zeigt der **puserattribute** -Zeiger in der **PPP- \_ EAP- \_ Ausgabe** nur auf Attribute, die vom Authentifizierungsprotokoll auf dem Server generiert wurden. Es enthält keines der Attribute, die beim aufzurufen von [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))an den Server übermittelt wurden. Der Authentifizierungs Anbieter benötigt diese anfänglichen Attribute nicht, da sich die Anmelde Informationen der Authentifizierung innerhalb der EAP-Nachricht selbst befinden, nicht in einem separaten RADIUS-Attribut. Wenn der Authentifizierungsdienst auf die **\_ Authenticate-Aktion von eapaction** antwortet, zeigt **puserattribute** bei der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)auf alle Attribute, die während der Authentifizierung generiert werden. Diese Attribute werden an das Authentifizierungsprotokoll auf dem Client zurückgegeben.

Wenn das Authentifizierungsprotokoll **eapaction \_ Authenticate** verwendet, führt der Authentifizierungs Anbieter entweder PAP oder MD5-CHAP aus. Diese Authentifizierungsmethode kann nur für Windows-Clients verwendet werden.

Wenn das Authentifizierungsprotokoll den Benutzer authentifiziert, ohne sich auf einen Authentifizierungs Anbieter zu verlassen, ist es nicht erforderlich, dass das Protokoll jemals die **Aktion** " **eapaction" \_ authentifiziert**. Ein Beispiel für diesen Fall ist EAP-Transport Layer Security (TLS).

Das EAP-Erfolgs Paket ist ein nicht bestätigter Paket. Daher kann der Server verloren gehen und nicht erneut vom Server gesendet werden. Wenn der Authentifizierungsdienst auf dem Client ein NCP-Paket (Network Control Protocol) empfängt, wird der serverseitige Authentifizierungsdienst so weiter ausgeführt, als ob die Authentifizierung erfolgreich war. Dies liegt daran, dass der Server zur NCP-Phase von PPP gewechselt ist. Entsprechend ruft der Authentifizierungsdienst [**raseapmakemesage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) auf, wobei das **ferfolgreispacket-** Member der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur auf **true** festgelegt ist.

Im Verlauf der Authentifizierungs Sitzung ist für das Authentifizierungsprotokoll möglicherweise eine direkte Interaktion mit dem Benutzer auf dem Client erforderlich. Der Authentifizierungsprotokoll Anbieter kann zu diesem Zweck eine interaktive Benutzeroberfläche bereitstellen. Das Authentifizierungsprotokoll kann anfordern, dass der Dienst die interaktive Benutzeroberfläche anzeigt, indem die Elemente **finvokeinteractiveui**, **puicontextdata** und **dwsizeofuicontextdata** in der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Struktur festgelegt werden. Weitere Informationen zur Verwendung einer interaktiven Benutzeroberfläche finden Sie unter [interaktive Benutzeroberfläche](interactive-user-interface.md).

Das Authentifizierungsprotokoll sollte nur über den unter [interaktive Benutzeroberfläche](interactive-user-interface.md)beschriebenen Mechanismus eine Benutzeroberfläche anzeigen. Wenn das Authentifizierungsprotokoll selbst die Benutzeroberfläche anzeigt, wird der PPP-Thread blockiert, bis die Benutzeroberfläche verworfen wird.

Wenn während des Authentifizierungsprozesses der Wert für [**raseapmakemess**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) einen anderen Wert als **No \_ Error** oder **Error \_ PPP \_ invalid \_ Packet** zurückgibt, wird die Sitzung getrennt, und der Fehler wird protokolliert (auf dem Server) oder für den Benutzer angezeigt (auf dem Client).

 

 