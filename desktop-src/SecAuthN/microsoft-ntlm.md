---
description: Windows Challenge/Response (NTLM) ist das Authentifizierungsprotokoll, das in Netzwerken verwendet wird, die Systeme enthalten, auf denen das Windows Betriebssystem ausgeführt wird, und auf eigenständigen Systemen.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb3d7f272c831c6bf9ac5efd30b8fa67bc7ad27d78d43794e5110fb63d1fe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921691"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Windows Challenge/Response (NTLM) ist das Authentifizierungsprotokoll, das in Netzwerken verwendet wird, die Systeme enthalten, auf denen das Windows Betriebssystem ausgeführt wird, und auf eigenständigen Systemen.

Das Microsoft [*Kerberos-Sicherheitspaket*](../secgloss/k-gly.md) [](../secgloss/s-gly.md) erhöht die Sicherheit von Systemen in einem Netzwerk gegenüber NTLM. Obwohl Microsoft *Kerberos* das Protokoll der Wahl ist, wird NTLM weiterhin unterstützt. NTLM muss auch für die Anmeldeauthentifizierung auf eigenständigen Systemen verwendet werden. Weitere Informationen zu Kerberos finden Sie unter [Microsoft Kerberos.](microsoft-kerberos.md)

NTLM-Anmeldeinformationen basieren auf Daten, die während des interaktiven Anmeldevorgangs abgerufen wurden, und bestehen aus einem Domänennamen, einem Benutzernamen und einem einseitigen [*Hash*](../secgloss/h-gly.md) des Benutzerkennworts. NTLM verwendet ein verschlüsseltes Abfrage-/Antwortprotokoll, um einen Benutzer zu authentifizieren, ohne das Kennwort des Benutzers über das Kabel zu senden. Stattdessen muss das System, das die Authentifizierung anfordert, eine Berechnung durchführen, die nachweist, dass es Zugriff auf die gesicherten NTLM-Anmeldeinformationen hat.

Die interaktive NTLM-Authentifizierung über ein Netzwerk umfasst in der Regel zwei Systeme: ein Clientsystem, in dem der Benutzer die Authentifizierung anfordert, und einen Domänencontroller, auf dem Informationen zum Benutzerkennwort gespeichert werden. Die nicht interaktive Authentifizierung, die möglicherweise erforderlich ist, um einem bereits angemeldeten Benutzer den Zugriff auf eine Ressource wie eine Serveranwendung zu gestatten, umfasst in der Regel drei Systeme: einen Client, einen Server und einen Domänencontroller, der die Authentifizierungsberechnungen im Auftrag des Servers durchführt.

In den folgenden Schritten wird die nichtinteraktive NTLM-Authentifizierung beschrieben. Der erste Schritt stellt die NTLM-Anmeldeinformationen des Benutzers bereit und tritt nur im Rahmen des interaktiven Authentifizierungsprozesses (Anmeldung) auf.

1.  (Nur interaktive Authentifizierung) Ein Benutzer greift auf einen Clientcomputer zu und stellt einen Domänennamen, einen Benutzernamen und ein Kennwort bereit. Der Client berechnet einen kryptografischen [*Hash*](../secgloss/h-gly.md) des Kennworts und verwirft das tatsächliche Kennwort.
2.  Der Client sendet den Benutzernamen an den Server (im [*Klartext*](../secgloss/p-gly.md)).
3.  Der Server generiert eine 16-Byte-Zufallszahl, die als *Abfrage* oder [*Nonce*](../secgloss/n-gly.md)bezeichnet wird, und sendet sie an den Client.
4.  Der Client verschlüsselt diese Abfrage mit dem Hash des Kennworts des Benutzers und gibt das Ergebnis an den Server zurück. Dies wird als *Antwort* bezeichnet.
5.  Der Server sendet die folgenden drei Elemente an den Domänencontroller:

    -   Benutzername
    -   An den Client gesendete Abfrage
    -   Vom Client empfangene Antwort

6.  Der Domänencontroller verwendet den Benutzernamen, um den Hash des Kennworts des Benutzers aus der Security Account Manager-Datenbank abzurufen. Dieser Kennworthash wird verwendet, um die Abfrage zu verschlüsseln.
7.  Der Domänencontroller vergleicht die berechnete verschlüsselte Abfrage (in Schritt 6) mit der Antwort, die vom Client (in Schritt 4) berechnet wurde. Wenn sie identisch sind, ist die Authentifizierung erfolgreich.

Ihre Anwendung sollte nicht direkt auf das [*NTLM-Sicherheitspaket*](../secgloss/s-gly.md) zugreifen. Stattdessen sollte das Sicherheitspaket [*Negotiate*](../secgloss/n-gly.md) verwendet werden. Negotiate ermöglicht Es Ihrer Anwendung, erweiterte [*Sicherheitsprotokolle*](../secgloss/s-gly.md) zu nutzen, wenn sie von den an der Authentifizierung beteiligten Systemen unterstützt werden. Derzeit wählt das Sicherheitspaket Negotiate zwischen [*Kerberos*](../secgloss/k-gly.md) und NTLM aus. Negotiate wählt Kerberos aus, es sei denn, es kann nicht von einem der an der Authentifizierung beteiligten Systeme verwendet werden.

 

 
