---
description: Die Semantik für Datagramm oder verbindungslose Kontexte unterscheidet sich geringfügig von denen für Verbindungs orientierte Kontexte.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Datagramm-Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129928"
---
# <a name="datagram-contexts"></a>Datagramm-Kontexte

Die Semantik für [*Datagramm*](/windows/desktop/SecGloss/d-gly)oder verbindungslose Kontexte unterscheidet sich geringfügig von denen für Verbindungs orientierte Kontexte. Im Verbindungs losen [*Kontext*](/windows/desktop/SecGloss/c-gly)eines Datagramms kann ein Server nicht bestimmen, wann die Verbindung vom Client heruntergefahren oder anderweitig beendet wurde. Anders ausgedrückt: Es wird keine Abbruch Mitteilung von der Transport Anwendung an den Server übermittelt, wie es in einem Verbindungs orientierten Kontext der Fall wäre.

Um einen Datagramm-Kontext zu verwenden, legt ein Client das ISC \_ req- \_ Datagramm-Flag im-Befehl der [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion fest.

> [!IMPORTANT]
> Das [Microsoft Kerberos](microsoft-kerberos.md) -Paket unterstützt keine datagrammkontexte im Benutzer-zu-Benutzer-Modus.

 

Um einige Modelle besser zu unterstützen, insbesondere RPC im DCE-Format, gelten die folgenden Regeln, wenn der Client einen Datagramm-Kontext verwendet:

-   Das [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) erzeugt beim ersten [**InitializeSecurityContext-Befehl (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)kein Authentifizierungs- [*BLOB*](/windows/desktop/SecGloss/b-gly) (Binary Large Object). Der Client kann jedoch den zurückgegebenen Sicherheitskontext in einem Rückruf der [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion verwenden, um eine Signatur für eine Nachricht zu generieren.
-   Das Sicherheitspaket muss zulassen, dass der Kontext mehrmals wieder hergestellt wird, damit der Server die Verbindung ohne vorherige Ankündigung löschen kann. Dies impliziert, dass alle in den Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) verwendeten Schlüssel in einen konsistenten [*Zustand*](/windows/desktop/SecGloss/s-gly)versetzt werden können.
-   Das Sicherheitspaket ermöglicht dem Aufrufer, Sequenz Informationen anzugeben, und stellt diese Sequenz Informationen auf Empfängerseite bereit. Dies gilt zusätzlich zu den vom Paket verwalteten Sequenz Informationen.

Ein Sicherheitspaket legt das Datagramm-Flag "secpkg Flag" fest, \_ \_ um anzugeben, dass es datagrammsemantik unterstützt

 

 
