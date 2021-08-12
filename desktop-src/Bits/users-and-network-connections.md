---
title: Benutzer und Netzwerkverbindungen
description: BITS überträgt Dateien nur, wenn der Auftragsbesitzer angemeldet ist und eine Netzwerkverbindung hergestellt wird.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- Bits für Netzwerkverbindungen
- Übertragungsauftrag BITS , Besitz
- Übertragungsauftrag BITS , Besitz, Benutzerkonto
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 54e346590cac90b8d896a9a45c86aee5ae241d7d299bb055cf9ff55db88b8668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679882"
---
# <a name="users-and-network-connections"></a>Benutzer und Netzwerkverbindungen

BITS überträgt Dateien nur, wenn der Auftragsbesitzer angemeldet ist und eine Netzwerkverbindung hergestellt wird. BITS verarbeitet den Übertragungsauftrag mithilfe des Sicherheitskontexts des Auftragsbesitzers. Der Benutzer, der den Auftrag erstellt hat, wird als Besitzer des Auftrags betrachtet. Ein Benutzer mit Administratorrechten kann jedoch [**den Besitz des**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) Auftrags eines anderen Benutzers übernehmen.

BITS unterzieht einen Auftrag, wenn sich der Besitzer abmelden oder die Netzwerkverbindung unterbrochen wird (BITS erzwingen keine Netzwerkverbindung). BITS setzt den Auftrag wieder auf, wenn sich der Besitzer wieder anmeldet und eine Netzwerkverbindung hergestellt wird. Nachdem die Netzwerkverbindung hergestellt wurde, kann es zu einer kurzen Verzögerung kommen, bevor BITS mit der Übertragung von Daten beginnt.

Wenn die Netzwerkverbindung unterbrochen wird, werden alle Aufträge, deren Status [**BG \_ JOB STATE \_ \_ QUEUED**](/windows/desktop/api/Bits/ne-bits-bg_job_state) oder **BG JOB STATE \_ \_ \_ TRANSFERRING** ist, mit einem [BG E NETWORK \_ \_ \_ DISCONNECTED-Fehlercode](bits-return-values.md) in den **Status BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR** verschoben. Wenn eine Netzwerkverbindung hergestellt wird, werden alle Aufträge in einem **BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR-Zustand,** der fehlercodes enthalten kann, in den Status BG JOB STATE **\_ \_ \_ QUEUED** verschoben.

Damit BITS erkennt, dass ein Benutzer angemeldet ist, muss der Benutzer eine der folgenden optionen für die interaktive Anmeldung verwenden:

-   Melden Sie sich über den Willkommensbildschirm an.
-   Melden Sie sich bei einem [Terminaldienstclient](../termserv/terminal-services-portal.md) an.
-   Verwenden Sie [den schnellen Benutzerwechsel.](../shell/fast-user-switching.md)
-   Ab Windows 10 Version 1607 melden Sie sich über Remote PowerShell von einem anderen Gerät aus an. Weitere [Informationen finden Sie unter So verwalten Sie PowerShell-Remotesitzungen.](using-windows-powershell-to-create-bits-transfer-jobs.md)

Das Ausführen einer Anwendung als anderer Benutzer (mithilfe des **Befehls RunAs)** ist keine interaktive Anmeldung. BITS führen keine Aufträge aus, die dem angegebenen Benutzer zugeordnet sind.

Die Systemkonten LocalSystem, LocalService und NetworkService sind immer angemeldet. Daher werden aufträge, die von einem Dienst mit diesen Konten übermittelt werden, immer ausgeführt. Informationen und Einschränkungen zur Verwendung von Dienstkonten finden Sie unter [Dienstkonten und BITS](service-accounts-and-bits.md).

Auftragsbesitzer können ein Hilfstoken bereitstellen, das in Situationen verwendet werden kann, in denen mehrere Token zum Abschließen einer Übertragung erforderlich sind, z. B. für die Authentifizierung bei einem Remotehost. Weitere [Informationen finden Sie unter Hilfstoken für BITS-Übertragungsaufträge.](helper-tokens-for-bits-transfer-jobs.md) In früheren Versionen von Windows musste der Auftragsbesitzer effektiv über Administratorrechte verfügen, um einen Auftrag zu starten, der ein Hilfstoken verwendet hat. In Windows 10 Version 1607 ist es jetzt möglich, dass ein BITS-Auftragsbesitzer Hilfstoken ohne Administratorrechte festgelegt, solange das Hilfstoken nicht über Administratorfunktionen verfügt. Dadurch werden Sicherheitsrisiken von Tools für Hintergrunddownloads oder -aktualisierungen gemindert, da diese Tools nicht unter einem Konto mit Administratorrechten, sondern unter dem NetworkService-Konto mit niedrigeren Berechtigungen ausgeführt werden.

Benutzer mit einem [eingeschränkten Token](../secauthz/restricted-tokens.md) (ein Token, das einschränkende SIDs enthält) können keine Aufträge erstellen oder ändern.
 

 