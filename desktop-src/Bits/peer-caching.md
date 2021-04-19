---
title: Peer Caching
description: Beginnend mit Background Intelligent Transfer Service (Bits) 4,0 wurde der BITS-Dienst erweitert, um das Peer Caching auf Subnetzebene für heruntergeladene URL-Daten mithilfe von Windows BranchCache zuzulassen.
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337444"
---
# <a name="peer-caching"></a>Peer Caching

Beginnend mit Background Intelligent Transfer Service (Bits) 4,0 wurde der BITS-Dienst erweitert, um das Peer Caching auf Subnetzebene für heruntergeladene URL-Daten mithilfe von Windows BranchCache zuzulassen. BITS-Clients können Daten von anderen Computern in Ihrem eigenen Subnetz abrufen, die die Daten bereits heruntergeladen haben, anstatt die Daten von Remote Servern abzurufen. Weitere Informationen zu Windows BranchCache finden Sie unter [BranchCache: Übersicht](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Wenn ein Administrator Windows BranchCache auf Client-und Server Computern in einer Organisation über eine Gruppenrichtlinie oder lokale Konfigurationseinstellungen aktiviert, verwendet Bits Windows BranchCache für Datenübertragungen.

-   [Konfiguration für Bits 4,0-Peer Caching](#configuration-for-bits-40-peer-caching)
-   [Deaktivieren von Windows BranchCache](#disabling-windows-branchcache)
-   [Überprüfung und Überwachung](#verification-and-monitoring)
-   [Peer Caching in Bits 3,0](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>Konfiguration für Bits 4,0-Peer Caching

Die folgende Konfiguration ist erforderlich, damit das Peer Caching in Bits 4,0 funktioniert:

-   Windows BranchCache muss auf dem Client über eine Gruppenrichtlinie oder lokale Konfigurationseinstellungen aktiviert werden. Weitere Informationen finden Sie unter [BranchCache-Client Konfiguration](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10)).
    > [!Note]  
    > Das Windows BranchCache-Feature ist standardmäßig deaktiviert.

     

-   Das Windows BranchCache-Feature ist eine optionale Komponente, die auf dem-Server installiert werden muss. Weitere Informationen finden Sie unter [BranchCache-Serverkonfiguration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
-   Der Server muss das Windows BranchCache-Feature auch über Gruppenrichtlinien oder lokale Konfigurationseinstellungen aktivieren. Weitere Informationen finden Sie unter [BranchCache-Serverkonfiguration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
    > [!Note]  
    > Das Windows BranchCache-Feature ist standardmäßig deaktiviert.

     

Die standardmäßige Bits-Gruppenrichtlinie ermöglicht Peer Zwischenspeicherung. Wenn Windows BranchCache Global auf einem Computer aktiviert ist, ist dieses Feature auch für Bits-Übertragungs Aufträge aktiviert. Weitere Informationen zu den Bits-spezifischen Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien](group-policies.md).

## <a name="disabling-windows-branchcache"></a>Deaktivieren von Windows BranchCache

Ein Administrator kann eine Gruppenrichtlinie verwenden, um die Verwendung von Windows BranchCache zu deaktivieren. (Weitere Informationen finden Sie unter [Gruppenrichtlinien](group-policies.md).) Wenn Windows BranchCache deaktiviert ist, werden von BITS-Clients nur Daten von Remote Servern abgerufen.

Eine Anwendung kann Windows BranchCache auch pro Auftrag deaktivieren, indem Sie die [**IBackgroundCopyJob4:: setpeercachingflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) -Methode aufruft und das Flag " **BG \_ - \_ Branch- \_ Cache deaktivieren** " festlegt.

> [!Note]  
> Diese Einstellungen wirken sich nicht auf die Verwendung von Windows BranchCache durch andere Anwendungen als Bits aus. Diese Einstellungen gelten nicht für BITS-Übertragungen über SMB. Bits steuert keine Einstellungen für Windows BranchCache-Übertragungen über SMB.

 

## <a name="verification-and-monitoring"></a>Überprüfung und Überwachung

Es gibt eine Reihe von Möglichkeiten, Peer Cache Statistiken zu überprüfen und zu überwachen. Administratoren können die [**IBackgroundCopyFile4:: getpeerdownloadstats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) -Methode aufrufen, um die Menge der Daten abzufragen, die von Peers und Ursprungs Servern heruntergeladen wurden. Administratoren können auch das Ereignisprotokoll auf [Ereignis-ID 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10))überprüfen, das auftragsspezifische Informationen bereitstellt.

Das Windows BranchCache-Feature bietet auch eine Reihe von Mechanismen zum Überprüfen und Überwachen von Peer Cache Statistiken. Weitere Informationen finden Sie unter über [Prüfung und Überwachung](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) und [Leistungsindikatoren](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10)).

Das Peer Caching-Modell, das Windows BranchCache verwendet, ersetzt das in Bits 3,0 verwendete Peer Cache Modell. Weitere Informationen zu Windows BranchCache finden Sie in den folgenden Bereichen:

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [BranchCache Overview](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Windows 7-Dienste](../win7devguide/services.md)
-   [Peer Verteilungs-API](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>Peer Caching in Bits 3,0

> [!Note]  
> Ab Windows 7 ist das Peer Caching-Modell von Bits 3,0 veraltet. Wenn BITS 4,0 installiert ist, ist das Peer Cache Modell Bits 3,0 nicht verfügbar.

 

Wenn der Administrator Peer Caching aktiviert und der Auftrag das Herunterladen von Inhalten von einem Peer zulässt, versucht Bits, den Inhalt von einem oder mehreren Peers herunterzuladen. Das Herunterladen von einem Peer ist viel schneller als das Herunterladen von Inhalten aus dem Internet. Peer Caching ist standardmäßig deaktiviert, und Aufträge müssen explizit das Herunterladen von Inhalten von Peers zulassen. Ein Administrator kann eine Gruppenrichtlinie verwenden, um Peer Caching zu aktivieren. Nachdem Sie das Peer Caching aktiviert haben, kann der Administrator entweder das Herunterladen von einem Peer oder das Bereitstellung von Inhalten an einen Peer deaktivieren.

Eine Anwendung kann das Peer Caching auch durch Aufrufen der [**ibitspeercacheadministration:: setconfigurationflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) -Methode aktivieren. Diese Einstellungen werden jedoch von den Gruppenrichtlinien Einstellungen überschrieben, sofern festgelegt.

Wenn Peer Caching aktiviert ist, erstellt Bits eine Liste von Peers, die sich im gleichen Subnetz befinden und derselben Domäne angehören. Die Liste enthält keine Peers aus einer vertrauenswürdigen Domäne. Peer Caching kann nur in einer Domänen Umgebung aktiviert werden.

Bits ermittelt die Peers wie folgt:

-   Lauschen auf Peer Server, die sich selbst ankündigen. Ein Peer Server kündigt sich an, wenn er gestartet wird. Bits fügt den Peer Server der Liste hinzu, wenn der Client mehr Peers in der Liste benötigt.
-   Sendet eine Anforderung für Peer Server, wenn mehr Peers in der Peer Liste benötigt werden. Peer Server, die zur Bereitstellung von Inhalten verfügbar sind, reagieren auf die Anforderung.

Bits entfernt Peer Server aus der Peer Liste, wenn der Server folgende Aktionen durchführt:

-   Fehler bei der Authentifizierung
-   Ist zu lange Offline (nicht verfügbar)
-   Stellt ein Zertifikat mit Fehlern bereit.

Wenn ein Auftrag Inhalt von einem Peer anfordert, wählt Bits nach dem Zufallsprinzip eine Teilmenge der Peers aus der Peer Liste aus und fragt Sie, ob Sie über den Inhalt verfügen. Bits kann Inhalte nur von authentifizierten Peer Servern herunterladen. Der Client und der Server authentifizieren sich anfänglich gegenseitig mithilfe von Kerberos und tauschen bei der Inhalts Ermittlung und dem Download selbst signierte Zertifikate für die Authentifizierung aus.

Bits lädt den Inhalt des ersten authentifizierten Peers herunter, um auf die Anforderung zu reagieren. Wenn ein Peer nicht den gesamten Inhalt enthält, lädt Bits den Inhalt von einem oder mehreren Peers herunter, bevor der Rest vom Ursprungsserver heruntergeladen wird. Wenn keiner der Peers den Inhalt aufweist oder beim Herunterladen von einem Peer ein Fehler auftritt, lädt Bits den Inhalt vom Ursprungsserver herunter.

Die heruntergeladenen Inhalte können nur für andere Peers bereitgestellt werden, nachdem die Anwendung den Inhalt der Dateien überprüft hat. Wenn die Datei nicht explizit von der Anwendung überprüft wird, wird die Datei implizit überprüft, wenn die Anwendung den Auftrag abschließt.

Standardmäßig kann ein Peer Server Inhalte nur an drei Clients gleichzeitig verarbeiten. Wenn der Server derzeit mit der Bewältigung von drei Clients ausgelastet ist, kommt es zu einer Verzögerung bei der Reaktion auf andere Anforderungen. Bits schränkt die Bandbreite für die Bereitstellung von Inhalten auf 1 Mbit/s ein. Verwenden Sie die Gruppenrichtlinie " [maxbandwidthserved](group-policies.md) ", um den Grenzwert zu ändern.

> [!Note]  
> Diese Funktion wird nur in Domänen Netzwerken unterstützt. Peer Caching wird für Arbeitsgruppen oder Heimnetzwerke nicht unterstützt.

Siehe auch [Verwalten des Peer Caches](/windows/desktop/Bits/administering-the-peer-cache)
 

 

 