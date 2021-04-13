---
description: Windows Challenge/Response (NTLM) ist das Authentifizierungsprotokoll, das in Netzwerken verwendet wird, die Systeme mit dem Betriebssystem Windows und eigenständigen Systemen enthalten.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft-NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525862"
---
# <a name="microsoft-ntlm"></a>Microsoft-NTLM

Windows Challenge/Response (NTLM) ist das Authentifizierungsprotokoll, das in Netzwerken verwendet wird, die Systeme mit dem Betriebssystem Windows und eigenständigen Systemen enthalten.

Das Microsoft [*Kerberos*](../secgloss/k-gly.md) - [*Sicherheitspaket*](../secgloss/s-gly.md) erhöht die Sicherheit von NTLM zu Systemen in einem Netzwerk. Obwohl es sich bei Microsoft *Kerberos* um das Protokoll der Wahl handelt, wird NTLM weiterhin unterstützt. NTLM muss auch für die Anmelde Authentifizierung auf eigenständigen Systemen verwendet werden. Weitere Informationen zu Kerberos finden Sie unter [Microsoft Kerberos](microsoft-kerberos.md).

NTLM-Anmelde Informationen basieren auf Daten, die während des interaktiven Anmeldevorgangs abgerufen werden. Sie bestehen aus einem Domänen Namen, einem Benutzernamen und einem unidirektionalen [*Hash*](../secgloss/h-gly.md) des Benutzer Kennworts. NTLM verwendet ein verschlüsseltes Challenge/Response-Protokoll, um einen Benutzer zu authentifizieren, ohne das Kennwort des Benutzers über das Netzwerk zu senden. Stattdessen muss das System, das eine Authentifizierung anfordert, eine Berechnung durchführen, die bestätigt, dass es Zugriff auf die gesicherten NTLM-Anmelde Informationen

Die interaktive NTLM-Authentifizierung über ein Netzwerk umfasst in der Regel zwei Systeme: ein Client System, in dem der Benutzer eine Authentifizierung anfordert, und einen Domänen Controller, auf dem Informationen im Zusammenhang mit dem Kennwort des Benutzers aufbewahrt werden. Die nicht interaktive Authentifizierung, die möglicherweise erforderlich ist, um einem bereits angemeldeten Benutzer den Zugriff auf eine Ressource wie z. b. eine Serveranwendung zu gestatten, umfasst in der Regel drei Systeme: einen Client, einen Server und einen Domänen Controller, der die Authentifizierungs Berechnungen für den Server ausführt.

Die folgenden Schritte zeigen eine Übersicht über die nicht interaktive NTLM-Authentifizierung. Der erste Schritt stellt die NTLM-Anmelde Informationen des Benutzers bereit und tritt nur im Rahmen des interaktiven Authentifizierungs Vorgangs (Logon) auf.

1.  (Nur interaktive Authentifizierung) Ein Benutzer greift auf einen Client Computer zu und stellt einen Domänen Namen, einen Benutzernamen und ein Kennwort bereit. Der Client berechnet einen kryptografischen [*Hash*](../secgloss/h-gly.md) des Kennworts und verwirft das tatsächliche Kennwort.
2.  Der Client sendet den Benutzernamen an den Server (als [*Klartext).*](../secgloss/p-gly.md)
3.  Der Server generiert eine 16-Byte-Zufallszahl, die als " *Challenge* " oder " [*Nonce*](../secgloss/n-gly.md)" bezeichnet wird, und sendet Sie an den Client.
4.  Der Client verschlüsselt diese Aufforderung mit dem Hashwert des Benutzer Kennworts und gibt das Ergebnis an den Server zurück. Dies wird *als Antwort* bezeichnet.
5.  Der Server sendet die folgenden drei Elemente an den Domänen Controller:

    -   Benutzername
    -   Die Anforderung wurde an den Client gesendet.
    -   Vom Client empfangene Antwort

6.  Der Domänen Controller verwendet den Benutzernamen, um den Hash des Benutzer Kennworts aus der Security Account Manager-Datenbank abzurufen. Dieser Kenn Wort Hash wird verwendet, um die Abfrage zu verschlüsseln.
7.  Der Domänen Controller vergleicht die verschlüsselte, berechnete Abfrage (in Schritt 6) mit der vom Client berechneten Antwort (in Schritt 4). Wenn Sie identisch sind, ist die Authentifizierung erfolgreich.

Die Anwendung sollte nicht direkt auf das NTLM- [*Sicherheitspaket*](../secgloss/s-gly.md) zugreifen. Stattdessen sollte das [*Aushandlungs*](../secgloss/n-gly.md) Sicherheitspaket verwendet werden. Aushandeln ermöglicht der Anwendung die Nutzung erweiterter [*Sicherheitsprotokolle*](../secgloss/s-gly.md) , wenn Sie von den Systemen, die an der Authentifizierung beteiligt sind, unterstützt werden. Derzeit wählt das Aushandlungs Sicherheitspaket zwischen [*Kerberos*](../secgloss/k-gly.md) und NTLM aus. Aushandeln wählt Kerberos aus, es sei denn, Sie kann von einem der an der Authentifizierung beteiligten Systeme verwendet werden.

 

 
