---
title: Peerzwischenspeicherung
description: Ab Background Intelligent Transfer Service (BITS) 4.0 wurde der BITS-Dienst erweitert, um peerzwischenspeichern auf Subnetzebene für heruntergeladene URL-Daten mit Windows BranchCache zu ermöglichen.
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: cf48a71c87aa27199578f5efe693cb941fbb3d7820a61c7e8766958b3d090952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173345"
---
# <a name="peer-caching"></a>Peerzwischenspeicherung

Ab Background Intelligent Transfer Service (BITS) 4.0 wurde der BITS-Dienst erweitert, um peerzwischenspeichern auf Subnetzebene für heruntergeladene URL-Daten mit Windows BranchCache zu ermöglichen. BITS-Clients können Daten von anderen Computern in ihrem eigenen Subnetz abrufen, die die Daten bereits heruntergeladen haben, anstatt die Daten von Remoteservern abzurufen. Weitere Informationen zu Windows BranchCache finden Sie in der [BranchCache-Übersicht.](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))

Wenn ein Administrator Windows BranchCache auf Client- und Servercomputern in einer Organisation über eine Gruppenrichtlinie oder lokale Konfigurationseinstellungen aktiviert, verwendet BITS Windows BranchCache für Datenübertragungen.

-   [Konfiguration für BITS 4.0-Peerzwischenspeicherung](#configuration-for-bits-40-peer-caching)
-   [Deaktivieren von Windows BranchCache](#disabling-windows-branchcache)
-   [Überprüfung und Überwachung](#verification-and-monitoring)
-   [Peerzwischenspeicherung in BITS 3.0](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>Konfiguration für BITS 4.0-Peerzwischenspeicherung

Die folgende Konfiguration ist für die Peerzwischenspeicherung in BITS 4.0 erforderlich, damit sie funktioniert:

-   Windows BranchCache muss auf dem Client über eine Gruppenrichtlinie oder lokale Konfigurationseinstellungen aktiviert werden. Weitere Informationen finden Sie unter [BranchCache-Clientkonfiguration.](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10))
    > [!Note]  
    > Die Windows BranchCache-Funktion ist standardmäßig deaktiviert.

     

-   Die Windows BranchCache-Funktion ist eine optionale Komponente, die auf dem Server installiert werden muss. Weitere Informationen finden Sie unter [BranchCache-Serverkonfiguration.](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10))
-   Der Server muss auch die Windows BranchCache-Funktion über Gruppenrichtlinien- oder lokale Konfigurationseinstellungen aktivieren. Weitere Informationen finden Sie unter [BranchCache-Serverkonfiguration.](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10))
    > [!Note]  
    > Die Windows BranchCache-Funktion ist standardmäßig deaktiviert.

     

Die BITS-Standardgruppenrichtlinie ermöglicht das Peerzwischenspeichern. Wenn Windows BranchCache global auf einem Computer aktiviert ist, ist dieses Feature auch für BITS-Übertragungsaufträge aktiviert. Weitere Informationen zu den BITS-spezifischen Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien.](group-policies.md)

## <a name="disabling-windows-branchcache"></a>Deaktivieren von Windows BranchCache

Ein Administrator kann eine Gruppenrichtlinie verwenden, um die Verwendung des Windows BranchCache zu deaktivieren. (Siehe [Gruppenrichtlinien](group-policies.md).) Wenn die Windows BranchCache deaktiviert ist, rufen BITS-Clients nur Daten von Remoteservern ab.

Eine Anwendung kann die Windows BranchCache auch auftragsbezogen deaktivieren, indem sie die [**IBackgroundCopyJob4::SetPeerCachingFlags-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) aufruft und das **FLAG BG DISABLE BRANCH \_ \_ \_ CACHE** festlegt.

> [!Note]  
> Diese Einstellungen wirken sich nicht auf die Verwendung von Windows BranchCache durch andere Anwendungen als BITS aus. Diese Einstellungen gelten nicht für BITS-Übertragungen über SMB. BITS steuert keine Einstellungen für Windows BranchCache-Übertragungen über SMB.

 

## <a name="verification-and-monitoring"></a>Überprüfung und Überwachung

Es gibt eine Reihe von Möglichkeiten zum Überprüfen und Überwachen von Peerzwischenspeicherungsstatistiken. Administratoren können die [**IBackgroundCopyFile4::GetPeerDownloadStats-Methode**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) aufrufen, um die Datenmenge abzufragen, die von Peers und Ursprungsservern heruntergeladen wurde. Administratoren können auch das Ereignisprotokoll auf [Ereignis-ID 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10))überprüfen, das auftragsspezifische Informationen bereitstellt.

Das Feature Windows BranchCache bietet auch eine Reihe von Mechanismen zum Überprüfen und Überwachen von Peerzwischenspeicherungsstatistiken. Weitere Informationen finden Sie unter [Überprüfung und Überwachung](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) und [Leistungsindikatoren.](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10))

Das Peerzwischenspeichermodell, das Windows BranchCache verwendet, ersetzt das in BITS 3.0 verwendete Peerzwischenspeicherungsmodell. Weitere Informationen zu Windows BranchCache finden Sie in den folgenden Themen:

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [BranchCache Overview](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Windows 7 Dienste](../win7devguide/services.md)
-   [Peerverteilungs-API](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>Peerzwischenspeicherung in BITS 3.0

> [!Note]  
> Ab Windows 7 ist das BITS 3.0-Peerzwischenspeichermodell veraltet. Wenn BITS 4.0 installiert ist, ist das BITS 3.0-Peercachemodell nicht verfügbar.

 

Wenn der Administrator die Peerzwischenspeicherung aktiviert und der Auftrag das Herunterladen von Inhalten von einem Peer zulässt, versucht BITS, den Inhalt von einem oder mehreren Peers herunterzuladen. Das Herunterladen von einem Peer ist viel schneller als das Herunterladen von Inhalten aus dem Internet. Peerzwischenspeicherung ist standardmäßig deaktiviert, und Aufträge müssen das Herunterladen von Inhalten von Peers explizit zulassen. Ein Administrator kann eine Gruppenrichtlinie zum Aktivieren der Peerzwischenspeicherung verwenden. Nach dem Aktivieren der Peerzwischenspeicherung kann der Administrator entweder das Herunterladen von einem Peer oder die Bereitstellung von Inhalten für einen Peer deaktivieren.

Eine Anwendung kann auch die Peerzwischenspeicherung aktivieren, indem sie die [**IBitsPeerCacheAdministration::SetConfigurationFlags-Methode aufruft.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) Diese Einstellungen werden jedoch von den Gruppenrichtlinieneinstellungen überschrieben, sofern festgelegt.

Wenn die Peerzwischenspeicherung aktiviert ist, erstellt BITS eine Liste von Peers, die sich im selben Subnetz befinden und zur gleichen Domäne gehören. Die Liste enthält keine Peers aus einer vertrauenswürdigen Domäne. Peerzwischenspeicherung kann nur in einer Domänenumgebung aktiviert werden.

BITS ermittelt die Peers wie folgt:

-   Lauschen auf Peerserver, die sich selbst ankündigen. Ein Peerserver kündigt sich selbst an, wenn er gestartet wird. BITS fügt den Peerserver der Liste hinzu, wenn der Client mehr Peers in seiner Liste benötigt.
-   Senden einer Anforderung für Peerserver, wenn mehr Peers in der Peerliste benötigt werden. Peerserver, die zum Bereitstellen von Inhalten verfügbar sind, reagieren auf die Anforderung.

BITS entfernt Peerserver aus der Peerliste, wenn der Server Folgendes tut:

-   Fehler bei der Authentifizierung
-   Ist zu lange offline (nicht verfügbar)
-   Stellt ein Zertifikat mit Fehlern bereit.

Wenn ein Auftrag Inhalte von einem Peer anfordert, wählt BITS nach dem Zufallsprinzip eine Teilmenge der Peers aus der Peerliste aus und fragt sie, ob sie über den Inhalt verfügen. BITS kann Inhalte nur von authentifizierten Peerservern herunterladen. Der Client und der Server authentifizieren sich zunächst gegenseitig mit Kerberos und tauschen dann während der Inhaltsermittlung und des Downloads selbstsignte Zertifikate für die Authentifizierung aus.

BITS lädt den Inhalt vom ersten authentifizierten Peer herunter, um auf die Anforderung zu reagieren. Wenn ein Peer nicht den gesamten Inhalt enthält, lädt BITS das, was er kann, von einem oder mehreren peers herunter, bevor der Rest vom Ursprungsserver heruntergeladen wird. Wenn keiner der Peers den Inhalt aufweist oder beim Herunterladen von einem Peer ein Fehler auftritt, lädt BITS den Inhalt vom Ursprungsserver herunter.

Der heruntergeladene Inhalt wird erst dann für andere Peers verfügbar, wenn die Anwendung den Inhalt der Dateien überprüft hat. Wenn die Anwendung die Datei nicht explizit überprüft, wird die Datei implizit überprüft, wenn die Anwendung den Auftrag abschließt.

Standardmäßig kann ein Peerserver Inhalte nur für drei Clients gleichzeitig verarbeiten. Wenn der Server derzeit mit der Bereitstellung von drei Clients ausgelastet ist, kommt es zu einer Verzögerung bei der Reaktion auf andere Anforderungen. BITS begrenzt die Bandbreite, die zum Bedienen von Inhalten verwendet wird, auf 1 MBit/s. Sie können die [MaxBandwidthServed-Gruppenrichtlinie](group-policies.md) verwenden, um den Grenzwert zu ändern.

> [!Note]  
> Dieses Feature wird nur in Domänennetzwerken unterstützt. Peerzwischenspeicherung wird in Arbeitsgruppen oder Heimnetzwerken nicht unterstützt.

Siehe auch [Verwalten des Peercaches.](/windows/desktop/Bits/administering-the-peer-cache)
 

 

 