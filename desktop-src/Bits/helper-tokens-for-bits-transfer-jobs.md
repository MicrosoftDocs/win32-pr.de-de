---
title: Hilfstoken für BITS-Übertragungsaufträge
description: Hilfstoken für BITS-Übertragungsaufträge
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a22708b11bd07165166f647454c05663d59f6cfeddde659a9bb5903d5a9606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528680"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Hilfstoken für BITS-Übertragungsaufträge

In Windows Vista ermöglicht der Background Intelligent Transfer Service-Dienst (BITS) einer Anwendung, einem BITS-Übertragungsauftrag ein einzelnes Sicherheitstoken zuzuordnen. Der BITS-Übertragungsauftrag verwendet dieses Token dann für die Authentifizierung und den Zugriff auf lokale und Remoteressourcen.

In Windows 7 ordnet der BITS-Dienst einem BITS-Übertragungsauftrag ein zusätzliches Token zu. Der BITS-Übertragungsauftrag kann mit einem zusätzlichen Sicherheitstoken konfiguriert werden. Dabei handelt es sich um ein Identitätswechseltoken, das von einer Anwendung erstellt wird, die die BITS COM-API aufruft. Mit diesem Hilfstokenmodell können Anwendungen gleichzeitig zwei verschiedene Sicherheitstoken verwenden, um auf lokale Dateien, clientseitige Zertifikate, Remotedateien und Proxys zuzugreifen. Beispielsweise wird ein BITS-Übertragungsauftrag erstellt, der die heruntergeladenen Daten in ein privilegiertes lokales Verzeichnis schreibt und dann eine Domänenidentität mit geringen Rechten für den HTTP-Server und den Proxyserver darstellt.

Eine Anwendung, in der Regel ein Windows Dienst, gibt ein Hilfstoken an, indem die neue Schnittstelle [**IBitsTokenOptions verwendet**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)wird. Diese Schnittstelle wird vom BITS-Auftragsobjekt implementiert. Die Anwendung ruft [**IBackgroundCopyJob::QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) auf, um den Schnittstellenzeiger abzurufen. Die Anwendung nimmt die Identität der Hilfsfunktion an und ruft [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) auf, um das Token an den BITS-Dienst zu übergeben. Anschließend gibt die Anwendung die Ressourcen an, auf die das Token angewendet wird, indem ein Satz von Bitflags mit [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags)übergeben wird. Die Anwendung löscht alle Flags (mit **setHelperTokenFlags** erneut), um das Verhalten rückgängig zu machen. Der BITS-Dienst speichert die Bitflags und das Token im BITS-Übertragungsauftrag.

Wenn sich der Besitzer der BITS-Übertragungsaufträge abmeldet, verwirft der BITS-Dienst alle Hilfstoken, die dem Übertragungsauftrag zugeordnet sind. Wenn die Übertragung nicht abgeschlossen ist, platziert der BITS-Dienst den Auftrag mit dem Fehlercode **BG \_ E TOKEN \_ \_ REQUIRED** in einen Fehlerzustand und verwirft das Hilfstoken. Die Clientanwendung kann das Token durch Aufrufen von [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) aktualisieren und dann den BITS-Übertragungsauftrag fortsetzen. Alternativ kann die Clientanwendung die Hilfstokenflags mit [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) löschen und dann den Übertragungsauftrag ohne Hilfstoken fortsetzen.

Wenn sich der Besitzer einer Terminaldienstsitzung abmeldet, muss der BITS-Dienst alle Hilfstoken aus dieser Sitzung verwerfen und die betroffenen Übertragungsaufträge mit dem Fehlercode **BG \_ E TOKEN \_ \_ REQUIRED** in einen Fehlerzustand setzen.

Das Hilfstokenmodell erfordert eine Änderung der BITS-Zugriffssteuerungsrichtlinie. In früheren Versionen von BITS wurden Zugriffsüberprüfungen für jeden Methodenaufruf implementiert. Ab Windows 7 muss die Zugriffsüberprüfung innerhalb des [**Aufrufs IBackgroundCopyJob::QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ausgeführt werden. Andernfalls hat das Hilfstoken möglicherweise keinen Zugriff auf den Übertragungsauftrag.

> [!Note]  
> Bei älteren Implementierungen mussten BITS-Benutzer über Administratorrechte verfügen, um Hilfstoken festzulegen. Ab Windows 10 Version 1607 können BITS-Benutzer ohne Administratorrechte [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) verwenden, um Hilfstoken ohne Administratorrechte für BITS-Aufträge festzulegen, deren Eigentümer sie sind. Durch diese Änderung können BITS-Benutzer ohne Administratorrechte (z. B. Hintergrunddownloaddienste, die unter dem [NetworkService-Konto](/windows/desktop/Services/networkservice-account)ausgeführt werden) Hilfstoken festlegen.
>
> Insbesondere wurde die Implementierung so geändert, dass Benutzer ohne Administratorrechte Hilfstoken festlegen können, solange die folgenden Bedingungen erfüllt sind:
>
> -   während des [**Aufrufs IBackgroundCopyJob::QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ist die SID des Threadtokens des Aufrufers mit der SID des Benutzerkontos des Auftragsbesitzers identisch.
> -   Wenn [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) aufgerufen wird, ist die Administrator-SID **(DOMAIN ALIAS RID \_ \_ \_ ADMINS)** für das Hilfstoken nicht aktiviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 