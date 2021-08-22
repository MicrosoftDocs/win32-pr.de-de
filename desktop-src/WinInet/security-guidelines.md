---
title: Sicherheitsrichtlinie
description: Es ist wichtig, den Benutzer über mögliche Sicherheitsprobleme auf dem Laufenden zu halten.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0870ecb13e195b226fbbd6e69c3c81fec256d7b35edcf2304167877e154a1dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386140"
---
# <a name="security-guideline"></a>Sicherheitsrichtlinie

Es ist wichtig, den Benutzer über mögliche Sicherheitsprobleme auf dem Laufenden zu halten.

## <a name="notify-the-user-of-security-related-events"></a>Benachrichtigen des Benutzers über Security-Related Ereignisse

Benachrichtigen Sie den Benutzer immer über jede Sicherheitsänderung, unabhängig davon, ob es sich um einen sicherheitsbezogenen Fehler handelt, z. B. einen Zertifikatfehler oder eine Änderung der Sicherheit des zugrunde liegenden Protokolls, z. B. eine Änderung von einer HTTPS-Website zu einer HTTP-Website.

## <a name="notify-the-user-of-security-related-errors"></a>Benachrichtigen des Benutzers über Security-Related Fehler

Wenn Ihre Anwendung eine Fehlermeldung empfängt, die auf ein Sicherheitsproblem hindeuten kann, stellt die **InternetErrorDlg-Funktion** eine standardmäßige, vertraute Schnittstelle zum Benachrichtigen des Benutzers in den meisten Fällen bereit.

Zu den Fehlern, die in diese Kategorie fallen, zählen:

**FEHLER \_ INTERNET HTTP TO HTTPS ON \_ \_ \_ \_ \_ REDIR**

**FEHLER \_ INTERNET \_ UNGÜLTIGE \_ ZERTIFIZIERUNGSSTELLE**

**FEHLER \_ \_ INTERNETBEITRAG \_ IST \_ NICHT \_ SICHER**

**FEHLER \_ INTERNET \_ SEC \_ CERT \_ ERRORS**

**FEHLER \_ INTERNET \_ SEC \_ CERT \_ CN \_ INVALID**

**FEHLER \_ INTERNET \_ SEC \_ CERT DATE \_ \_ INVALID**

Wenn der Benutzer nicht über solche Fehler informiert wird, kann dies dazu führen, dass der Benutzer verschiedene Arten von Sicherheitsverletzungen aussetzen kann, z. B. Spoofingangriffe oder unfreiwillige Offenlegung von Informationen.

## <a name="notify-the-user-when-connection-security-changes"></a>Benachrichtigen des Benutzers, wenn sich die Verbindungssicherheit ändert

Benachrichtigen Sie den Benutzer immer, wenn sich die Sicherheit der Verbindung ändert, z. B. von HTTPS in HTTP. Andernfalls verbergen Sie das Risiko einer unfreiwilligen Veröffentlichung von Informationen, es sei denn, der Benutzer hat sich explizit dafür entschieden, nicht über solche Änderungen benachrichtigt zu werden.

Zu den Funktionen, die eine solche Änderung der Verbindungssicherheit melden, gehören die **Rückruffunktion InternetStatusCallback** und die **InternetConfirmZoneCrossing-Funktion.**

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 