---
title: Sicherheitsrichtlinie
description: Es ist wichtig, den Benutzer über mögliche Sicherheitsprobleme auf dem Laufenden zu halten.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102110"
---
# <a name="security-guideline"></a>Sicherheitsrichtlinie

Es ist wichtig, den Benutzer über mögliche Sicherheitsprobleme auf dem Laufenden zu halten.

## <a name="notify-the-user-of-security-related-events"></a>Benachrichtigen des Benutzers über Security-Related-Ereignisse

Benachrichtigen Sie den Benutzer stets über jegliche Änderung der Sicherheit, ob es sich um einen sicherheitsbezogenen Fehler wie einen Zertifikat Fehler oder eine Änderung der Sicherheit des zugrunde liegenden Protokolls handelt, z. b. eine Änderung von einer HTTPS-Site zu einer HTTP-Site.

## <a name="notify-the-user-of-security-related-errors"></a>Benachrichtigen des Benutzers über Security-Related Fehler

Wenn Ihre Anwendung eine Fehlermeldung empfängt, die möglicherweise auf ein Sicherheitsproblem hinweist, stellt die **internetterrordlg** -Funktion eine standardmäßige, vertraute Schnittstelle zum Benachrichtigen des Benutzers in den meisten Fällen bereit.

Zu den Fehlern, die in diese Kategorie fallen, zählen die folgenden:

**Fehler " \_ Internet \_ http \_ zu https" \_ \_ beim \_ redir**

**Fehler beim \_ Internet \_ ungültige Zertifizierungsstelle \_**

**Fehler " \_ Internet \_ Post" \_ ist \_ nicht \_ sicher.**

**Fehler \_ Internet \_ Sek. \_ CERT- \_ Fehler**

**Fehler \_ Internet \_ sec \_ CERT \_ CN ist \_ ungültig.**

**Fehler \_ Internet \_ Sek. \_ CERT- \_ Datum \_ ungültig**

Ein Fehler bei der Benachrichtigung des Benutzers über Fehler, wie z. b. diese, kann den Benutzer für verschiedene Arten von Sicherheitsverletzungen verfügbar machen, einschließlich Spoofing-Angriffe oder unfreiwilligen Offenlegung von Informationen.

## <a name="notify-the-user-when-connection-security-changes"></a>Benutzer benachrichtigen, wenn sich die Verbindungssicherheit ändert

Benachrichtigen Sie den Benutzer immer, wenn die Sicherheit der Verbindung geändert wird, z. b. von HTTPS zu http. Andernfalls verbergen Sie die Risiken der Offenlegung unfreiwilliger Informationen, es sei denn, der Benutzer hat explizit entschieden, nicht über solche Änderungen benachrichtigt zu werden.

Zu den Funktionen, die eine solche Änderung der Verbindungssicherheit melden, gehören die **Internetstatus Callback** -Rückruffunktion und die **internetconfirmzonecrossing** -Funktion.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 