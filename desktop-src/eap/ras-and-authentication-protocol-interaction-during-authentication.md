---
title: Interaktion von Zugriffspunkt und Authentifizierungsprotokoll während der Authentifizierung
description: Die RasEapMakeMessage-Funktion steuert den Großteil der Interaktion zwischen dem Authentifizierungsprotokoll und dem Zugriffspunkt (ACCESS POINT, AP).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea18883225a2a34e592b73e0cdc93b019c1bf466124976f01851febb2a17d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117770"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interaktion von Zugriffspunkt und Authentifizierungsprotokoll während der Authentifizierung

Die [**RasEapMakeMessage-Funktion**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) steuert den Großteil der Interaktion zwischen dem Authentifizierungsprotokoll und dem Zugriffspunkt (ACCESS POINT, AP). **RasEapMakeMessage** verarbeitet eingehende EAP-Pakete und erstellt EAP-Pakete für die Übertragung an den Remotespeer. Außerdem werden Ereignisse wie Time outs und Authentifizierungsabschluss verarbeitet.

Wenn eine Nachricht vom Remotespeer empfangen wird, ruft der AP-Authentifizierungsdienst [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))auf und übergibt einen Zeiger auf die empfangene Nachricht im *pReceivePacket-Parameter.*

Wenn der Dienst [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) aufruft, wobei *pReceivePacket* auf **NULL** festgelegt ist, initiiert die AP entweder das Dialogfeld mit dem Authentifizierungsprotokoll oder fordert an, dass das Protokoll das letzte Paket erneut senden soll. Das Authentifizierungsprotokoll sollte anhand des Status und des Nachrichtenkontexts bestimmen, welche Aktion vom Dienst ergriffen wird.

Bei der Rückgabe von [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))gibt der Wert des **Action-Members** der [**\_ EAP \_ OUTPUT-Struktur von PPAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) an, welche Aktion ggf. vom Authentifizierungsdienst durchgeführt wird. Der **Action-Member** übernimmt Werte aus dem [**ENUMERATIONS-EAP \_ \_ ACTION-Typ.**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action)

Wenn **Action** **EAPACTION \_ Send**, **EAPACTION \_ SendAndDone,** **EAPACTION \_ SendWithTimeout** oder **EAPACTION \_ SendWithTimeoutInteractive** ist, überträgt der Dienst das Paket, auf das vom *pSendPacket-Parameter* verwiesen wird, an den Remotespeer.

Der **\_ EAPACTION-Wert SendWithTimeout** ermöglicht ein Timeout. Danach geht der Authentifizierungsdienst davon aus, dass der Link verloren gegangen ist, und trennt die Sitzung.

Der **\_ EAPACTION-Wert SendWithTimeoutInteractive** ermöglicht ein unendliches Timeout. Der Authentifikator sollte diesen Wert verwenden, wenn er Benutzereingaben auf dem Client erwartet. Dieses Time out ermöglicht dem Benutzer eine nicht angegebene Zeitspanne, um die erforderliche Eingabe abzuschließen.

Wenn **Action** **EAPACTION \_ SendWithTimeout** oder **EAPACTION \_ SendWithTimeoutInteractive** ist, sollte das Authentifizierungsprotokoll den **dwIdExpected-Member** der [**EQ \_ EAP \_ OUTPUT-Struktur**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) auf den Bezeichner des nächsten Pakets festlegen, das vom Remotespeer erwartet wird. Unabhängig davon, ob das nächste vom Peer empfangene Paket mit diesem Wert übereinstimmt, übergibt der Authentifizierungsdienst das Paket in einem nachfolgenden Aufruf von [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))an das Authentifizierungsprotokoll. Das Authentifizierungsprotokoll verwirft das Paket möglicherweise im Hintergrund, indem einfach **ERROR \_ INVALID \_ \_ PACKET ZURÜCKGEGEBEN** wird. Wenn ein Paket mit dem erwarteten Bezeichner nicht innerhalb des konfigurierten Time out-Zeitraums empfangen wird, ruft der Authentifizierungsdienst **weiterhin RasEapMakeMessage** auf. In diesem Fall wird der Aufruf mit dem *pReceivePacket-Parameter* durchgeführt, der auf **NULL** festgelegt ist, um anzugeben, dass das vorherige Paket erneut gesendet werden muss.

Wenn das **Action-Element** **EAPACTION \_ Done** oder **EAPACTION \_ SendAndDone** ist, überprüft der Authentifizierungsdienst das **dwAuthResultCode-Element** von [**TG \_ EAP \_ OUTPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Wenn **dwAuthResultCode** NO ERROR ist, war \_ die Authentifizierung erfolgreich. Wenn **dwAuthResultCode** ein anderer Wert als NO \_ ERROR ist, ist die Authentifizierung fehlgeschlagen. Der für den Fehlerfall zurückgegebene Fehlercode sollte von "Raserror.h", "Mprerror.h" oder "Winerror.h" stammen. Mögliche Rückgabecodes sind u. a. Folgende:

-   FEHLER \_ KEINE \_ \_ DIALIN-BERECHTIGUNG
-   FEHLER \_ PASSWD \_ ABGELAUFEN
-   FEHLER \_ ACCT \_ DISABLED
-   FEHLER \_ EINGESCHRÄNKTE \_ \_ ANMELDESTUNDEN
-   FEHLER \_ BEI \_ DER AUTHENTIFIZIERUNG INTERN

Wenn **Action** **EAPACTION \_ Done** oder **EAPACTION \_ SendAndDone** ist, sollte der **pUserAttributes-Member** auf Attribute verweisen, die Attribute desselben Typs überschreiben, die beim Aufruf von [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))an den Server übergeben wurden.

Das Authentifizierungsprotokoll auf dem Server kann anfordern, dass der Authentifizierungsdienst den aktuellen Authentifizierungsanbieter aufruft, indem **EAPACTION \_ Authenticate** im **Action-Member** in [**DER \_ EAP \_ OUTPUT-AKTION**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)zurückgegeben wird. In diesem Fall verweist der **pUserAttributes-Zeiger** in **DER \_ EAP \_ OUTPUT-Datei nur** auf Attribute, die vom Authentifizierungsprotokoll auf dem Server generiert wurden. Sie enthält keines der Attribute, die beim Aufruf von [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))an den Server übergeben wurden. Der Authentifizierungsanbieter benötigt diese anfänglichen Attribute nicht, da sich die Anmeldeinformationen für die Authentifizierung in der EAP-Nachricht selbst und nicht in einem separaten RADIUS-Attribut befinden. Wenn der Authentifizierungsdienst auf die **\_ EAPACTION-Authentifizierungsaktion** antwortet, zeigt **pUserAttributes** in [**DER \_ EAP \_ INPUT-Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)des Authentifizierungsdiensts auf alle Attribute, die während der Authentifizierung generiert wurden. Diese Attribute werden an das Authentifizierungsprotokoll auf dem Client zurückgegeben.

Wenn das Authentifizierungsprotokoll **EAPACTION \_ Authenticate** verwendet, führt der Authentifizierungsanbieter entweder PAP oder MD5-CHAP aus. Diese Authentifizierungsmethode kann nur mit Windows Clients verwendet werden.

Wenn das Authentifizierungsprotokoll den Benutzer authentifiziert, ohne sich auf einen Authentifizierungsanbieter zu verlassen, ist es nicht erforderlich, dass das Protokoll **action** auf **EAPACTION \_ Authenticate** festgelegt hat. Ein Beispiel für diesen Fall ist EAP-Transport Layer Security (TLS).

Das EAP-Erfolgspaket ist ein nicht bestätigtes Paket. Daher kann er verlorengehen und nicht vom Server erneut gesendet werden. Wenn der Authentifizierungsdienst auf dem Client ein NCP-Paket (Network Control Protocol) empfängt, wird der serverseitige Authentifizierungsdienst so fortgesetzt, als ob die Authentifizierung erfolgreich war. Dies liegt daran, dass der Server in die NCP-Phase von CSV gewechselt ist. Entsprechend ruft der Authentifizierungsdienst [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) auf, wobei der **Member fSuccessPacketReceived** der [**PPUS \_ EAP \_ INPUT-Struktur**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) auf TRUE festgelegt **ist.**

Während der Authentifizierungssitzung erfordert das Authentifizierungsprotokoll möglicherweise eine direkte Interaktion mit dem Benutzer auf dem Client. Der Anbieter des Authentifizierungsprotokolls kann zu diesem Zweck eine interaktive Benutzeroberfläche bereitstellen. Das Authentifizierungsprotokoll kann anfordern, dass der Dienst die interaktive Benutzeroberfläche anzeigt, indem es die Member **fInvokeInteractiveUI,** **pUIContextData** und **dwSizeOfUIContextData** in der [**\_ EAP \_ OUTPUT-Struktur von PPWWfestlegt.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Weitere Informationen zur Verwendung einer interaktiven Benutzeroberfläche finden Sie unter [Interactive Benutzeroberfläche](interactive-user-interface.md).

Das Authentifizierungsprotokoll sollte eine Benutzeroberfläche nur über den unter [Interactive Benutzeroberfläche](interactive-user-interface.md)beschriebenen Mechanismus anzeigen. Wenn im Authentifizierungsprotokoll selbst die Benutzeroberfläche angezeigt wird, blockiert der THREAD THREADS, bis die Benutzeroberfläche verworfen wird.

Wenn [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) während des Authentifizierungsprozesses einen anderen Wert als **NO \_ ERROR** oder **ERROR INVALID \_ \_ \_ PACKET** zurückgibt, wird die Sitzung getrennt, und der Fehler wird protokolliert (auf dem Server) oder dem Benutzer (auf dem Client) angezeigt.

 

 