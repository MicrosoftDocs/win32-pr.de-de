---
title: Benutzer und Netzwerkverbindungen
description: Bits überträgt Dateien nur, wenn der Besitzer des Auftrags angemeldet ist und eine Netzwerkverbindung hergestellt wird.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- Netzwerkverbindungen (Bits)
- Übertragen von Auftrags Bits, Besitz
- Übertragen von Auftrags Bits, Besitz, Benutzerkonto
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7f841e3bf92004b62f3bbb576f71a45ac6b4a6bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102238"
---
# <a name="users-and-network-connections"></a>Benutzer und Netzwerkverbindungen

Bits überträgt Dateien nur, wenn der Besitzer des Auftrags angemeldet ist und eine Netzwerkverbindung hergestellt wird. Bits verarbeitet den Übertragungs Auftrag unter Verwendung des Sicherheits Kontexts des Auftrags Besitzers. Der Benutzer, der den Auftrag erstellt hat, wird als Besitzer des Auftrags angesehen. Ein Benutzer mit Administratorrechten kann jedoch den Besitz des Auftrags eines anderen Benutzers [**übernehmen**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) .

Bits hält einen Auftrag an, wenn der Besitzer sich abmeldet oder wenn die Netzwerkverbindung verloren geht (die Netzwerkverbindung wird von Bits nicht erzwungen). Bits setzt den Auftrag fort, wenn sich der Besitzer wieder anmeldet und eine Netzwerkverbindung hergestellt wird. Nachdem die Netzwerkverbindung hergestellt wurde, kann eine kurze Verzögerung auftreten, bevor Bits mit der Datenübertragung beginnt.

Wenn die Netzwerkverbindung unterbrochen wird, werden alle Aufträge, deren Status der BG-Auftragsstatus in der [**\_ \_ \_ Warteschlange**](/windows/desktop/api/Bits/ne-bits-bg_job_state) ist, bzw. die über **\_ \_ \_ Tragung des BG-Auftrags** Zustands in den Status "BG-Auftragsstatus **\_ \_ \_ vorübergehender \_ Fehler** " mit dem Fehlercode " [BG \_ E \_ Network \_](bits-return-values.md) Wenn eine Netzwerkverbindung hergestellt wird, werden alle Aufträge in einem Status **\_ \_ \_ vorübergehender \_ Status eines BG-Auftrags** , der ggf. einen beliebigen Fehlercode enthalten kann, in den Status des Status der BG-Auftragsstatus in **\_ \_ \_ Warteschlange** verschoben.

Damit Bits erkennen kann, dass ein Benutzer angemeldet ist, muss der Benutzer eine der folgenden interaktiven Anmelde Optionen verwenden:

-   Melden Sie sich über den Willkommensbildschirm an.
-   Melden Sie sich bei einem [Terminaldienst](../termserv/terminal-services-portal.md) Client an.
-   Verwenden Sie die [schnelle Benutzerumschaltung](../shell/fast-user-switching.md).
-   Ab Windows 10, Version 1607, melden Sie sich über die Remote-PowerShell von einem anderen Gerät an. Weitere Informationen finden [Sie unter So verwalten Sie PowerShell-Remote Sitzungen](using-windows-powershell-to-create-bits-transfer-jobs.md) .

Das Ausführen einer Anwendung als ein anderer Benutzer (mit dem Befehl **runas** ) ist keine interaktive Anmeldung. Bits führt keine Aufträge aus, die dem angegebenen Benutzer zugeordnet sind.

Die Systemkonten "LocalSystem", "LocalService" und "NetworkService" sind immer angemeldet. aus diesem Grund werden Aufträge, die von einem Dienst übermittelt werden, immer ausgeführt. Informationen und Einschränkungen bei der Verwendung von Dienst Konten finden Sie unter [Dienst Konten und Bits](service-accounts-and-bits.md).

Auftrags Besitzer können ein Hilfstoken bereitstellen, das in Situationen verwendet wird, in denen mehrere Token zum Durchführen einer Übertragung benötigt werden, z. b. für die Authentifizierung mit einem Remote Host. Weitere Informationen finden Sie unter [hilfsprogrammtoken für Bits-Übertragungs Aufträge](helper-tokens-for-bits-transfer-jobs.md) . In früheren Versionen von Windows musste der Besitzer des Auftrags über Administratorrechte verfügen, um einen Auftrag zu starten, der ein Hilfsobjekt verwendet hat. In Windows 10, Version 1607, ist es für einen Bits-Auftrags Besitzer nun möglich, Hilfstoken ohne Administratorrechte festzulegen, solange das Hilfsobjekt keine Administrator Funktionen hat. Dadurch werden Sicherheitsrisiken von Tools für Hintergrunddownloads oder -aktualisierungen gemindert, da diese Tools nicht unter einem Konto mit Administratorrechten, sondern unter dem NetworkService-Konto mit niedrigeren Berechtigungen ausgeführt werden.

Benutzer mit [eingeschränktem Token](../secauthz/restricted-tokens.md) (ein Token, das Einschränkende SIDs enthält) können keine Aufträge erstellen oder ändern.
 

 