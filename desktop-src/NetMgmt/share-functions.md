---
title: Freigabefunktionen
description: Die Funktionen der Netzwerkverwaltungsfreigabe steuern freigegebene Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. B. ein Datenträgerverzeichnis, ein Druckgerät oder eine Named Pipe), auf die Benutzer und Anwendungen im Netzwerk zugreifen können.
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97dc4570c3ef1300322bdf9bd4c9616176e31661319ac77378c61a71667523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064290"
---
# <a name="share-functions"></a>Freigabefunktionen

Die Funktionen der Netzwerkverwaltungsfreigabe steuern freigegebene Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. B. ein Datenträgerverzeichnis, ein Druckgerät oder eine Named Pipe), auf die Benutzer und Anwendungen im Netzwerk zugreifen können.

Die Freigabefunktionen sind im Folgenden aufgeführt.



| Funktion                                  | Beschreibung                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | Gibt eine Ressource auf einem Server wieder.                                       |
| [**NetShareCheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | Fragt ab, ob ein Server ein Gerät gemeinsam verwendet.                        |
| [**NetShareDel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | Löscht einen Freigabenamen aus der Liste der freigegebenen Ressourcen eines Servers.       |
| [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | Ruft Freigabeinformationen zu jeder freigegebenen Ressource auf einem Server ab.  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | Ruft Informationen zu einer angegebenen freigegebenen Ressource auf einem Server ab. |
| [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | Legt die Parameter einer freigegebenen Ressource fest.                                 |



 

Diese Freigabefunktion gilt nur für Freigaben auf einem Server Message Block (LAN Manager)-Server. Diese Freigabefunktionen unterstützen keine verteiltes Dateisystem (DFS) Freigaben. Beispielsweise kann die [**NetShareGetInfo-Funktion**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) nur Informationen für eine angegebene Freigaberessource auf einem SMB-Server abrufen. Verwenden Sie die [**WNetGetConnection-Funktion,**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) um Informationen für eine Freigabe mithilfe eines anderen Netzwerkanbieters (z. B. WebDAV oder DFS-Freigabe) abzurufen.

Die [**NetShareAdd-Funktion**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) ermöglicht es einem Benutzer oder einer Anwendung, eine Ressource eines bestimmten Typs unter Verwendung des angegebenen Freigabenamens gemeinsam zu nutzen. Die **NetShareAdd-Funktion** erfordert den Freigabenamen und den Namen des lokalen Geräts, um die Ressource gemeinsam nutzen zu können. Ein Benutzer oder eine Anwendung muss über ein Konto auf dem Server verfügen, um auf die Ressource zugreifen zu können.

Sie können auch einen Sicherheitsdeskriptor angeben, der einer Freigabe zugeordnet werden soll. Sicherheitsdeskriptoren geben an, welche Benutzer über die Freigabe auf Dateien zugreifen dürfen und mit welchem Zugriffstyp. Geben Sie beim Aufrufen von **NetShareAdd** oder [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo)einen [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) mit der [**Informationsebene SHARE \_ INFO \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) an. **NetShareSetInfo unterstützt** die [**Informationsebene SHARE \_ INFO \_ 1501.**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) Weitere Informationen zu Sicherheitsdeskriptoren finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Die Netzwerkverwaltungsfunktionen verwenden die folgenden speziellen Freigabenamen für die prozessübergreifende Kommunikation (Interprocess Communication, IPC) und die Remoteverwaltung des Servers:

-   IPC$, reserviert für prozessübergreifende Kommunikation
-   ADMIN$, reserviert für die Remoteverwaltung
-   A$, B$, C$ (und andere lokale Datenträgernamen gefolgt von einem Dollarzeichen), die lokalen Datenträgergeräten zugewiesen sind

Rufen Sie die [**NetConnectionEnum-Funktion**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) auf, um alle Verbindungen, die mit einer freigegebenen Ressource auf einem Server hergestellt wurden, oder alle von einem bestimmten Computer hergestellten Verbindungen auflisten zu können. Sie können **NetConnectionEnum auf** den Informationsebenen [**CONNECTION INFO \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) und [**CONNECTION INFO \_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1) aufrufen.

Freigabefunktionen sind auf den folgenden Informationsebenen verfügbar, obwohl einige Freigabeebenen nur für einige der Freigabefunktionen gelten:

-   [**FREIGEBEN \_ VON INFORMATIONEN \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**FREIGEBEN \_ VON INFORMATIONEN \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**FREIGEBEN \_ VON INFORMATIONEN \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**FREIGABEINFORMATIONEN \_ \_ 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**FREIGEBEN \_ VON INFO \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**FREIGEBEN \_ VON INFO \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**FREIGEBEN \_ VON INFO \_ 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**FREIGEBEN \_ VON INFO \_ 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**FREIGEBEN \_ VON INFO \_ 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**FREIGABEINFORMATIONEN \_ \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

Weitere Informationen finden Sie in der Dokumentation zu einer bestimmten Freigabefunktion.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Netzwerkverwaltungsfreigabefunktionen erreichen können. Weitere Informationen finden Sie unter [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 