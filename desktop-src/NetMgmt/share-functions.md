---
title: Freigabe Funktionen
description: Die Funktionen der Netzwerk Verwaltungs Freigabe steuern gemeinsam genutzte Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. b. ein Datenträger Verzeichnis, Druck Gerät oder Named Pipe), auf die von Benutzern und Anwendungen im Netzwerk zugegriffen werden kann.
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5034d46e233ebb7ed4de691bd79942a3ecdf5263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390871"
---
# <a name="share-functions"></a>Freigabe Funktionen

Die Funktionen der Netzwerk Verwaltungs Freigabe steuern gemeinsam genutzte Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. b. ein Datenträger Verzeichnis, Druck Gerät oder Named Pipe), auf die von Benutzern und Anwendungen im Netzwerk zugegriffen werden kann.

Die Freigabe Funktionen sind nachfolgend aufgeführt.



| Funktion                                  | BESCHREIBUNG                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | Gibt eine Ressource auf einem Server frei.                                       |
| [**Netsharecheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | Fragt ab, ob ein Server ein Gerät gemeinsam verwendet.                        |
| [**Netsharedel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | Löscht einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers.       |
| [**Netshareaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | Ruft Freigabe Informationen zu den einzelnen freigegebenen Ressourcen auf einem Server ab.  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | Ruft Informationen zu einer angegebenen freigegebenen Ressource auf einem Server ab. |
| [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | Legt die Parameter einer freigegebenen Ressource fest.                                 |



 

Diese Freigabe Funktion gilt nur für Freigaben auf einem Server Message Block-Server (LAN-Manager). Diese Freigabe Funktionen unterstützen keine verteiltes Dateisystem (DFS)-Freigaben. Beispielsweise kann die [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) -Funktion nur Informationen für eine angegebene Freigabe Ressource auf einem SMB-Server abrufen. Wenn Sie Informationen für eine Freigabe mithilfe eines anderen Netzwerk Anbieters (z. b. WebDAV oder eine DFS-Freigabe) abrufen möchten, verwenden Sie die [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) -Funktion.

Die [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) -Funktion ermöglicht es einem Benutzer oder einer Anwendung, mithilfe des angegebenen Freigabe namens eine Ressource eines bestimmten Typs freizugeben. Die Funktion **NetShareAdd** erfordert, dass der Freigabe Name und der Name des lokalen Geräts die Ressource freigeben. Ein Benutzer oder eine Anwendung muss über ein Konto auf dem Server verfügen, um auf die Ressource zugreifen zu können.

Sie können auch eine Sicherheits Beschreibung angeben, die einer Freigabe zugeordnet werden soll. Sicherheits Deskriptoren geben an, welche Benutzer über die Freigabe auf Dateien zugreifen dürfen und mit welchem Zugriffstyp. Geben Sie [**eine Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) mit der Informationsebene [**Freigabe \_ Info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) an, wenn **Sie NetShareAdd** oder [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo)aufrufen. **NetShareSetInfo** unterstützt die Informationsebene [**Freigabe \_ Info \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) . Weitere Informationen zu Sicherheits Beschreibungen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Die Netzwerk Verwaltungsfunktionen verwenden die folgenden speziellen Freigabe Namen für die prozessübergreifende Kommunikation (prozessübergreifende Communication, IPC) und die Remote Verwaltung des-Servers:

-   IPC $, für prozessübergreifende Kommunikation reserviert
-   ADMIN $, für Remote Verwaltung reserviert
-   A $, B $, C $ (und andere lokale Datenträger Namen, gefolgt von einem Dollarzeichen), die lokalen Datenträgern zugewiesen sind

Um alle Verbindungen aufzulisten, die mit einer freigegebenen Ressource auf einem Server hergestellt wurden, oder um alle Verbindungen aufzulisten, die von einem bestimmten Computer hergestellt wurden, nennen Sie die [**netconnectionenum**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) -Funktion. Sie können **netconnectionenum** auf den Informationsebenen [**Connection \_ Info \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) und [**Connection \_ Info \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1) aufzurufen.

Freigabe Funktionen sind auf den folgenden Informationsebenen verfügbar, obwohl einige Freigabe Ebenen nur auf einige der Freigabe Funktionen anwendbar sind:

-   [**Freigabe \_ Informationen \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**Freigabe \_ Informationen \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**Freigabe \_ Informationen \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**Freigabe \_ Informationen \_ 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**Freigabe \_ Informationen \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**Freigabe \_ Informationen \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**Freigabe \_ Informationen \_ 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**Freigabe \_ Informationen \_ 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**Freigabe \_ Informationen \_ 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**Freigabe \_ Informationen \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

Ausführliche Informationen finden Sie in der Dokumentation zu einer bestimmten Freigabe Funktion.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungs Freigabe erreichen können. Weitere Informationen finden Sie unter [**iadsfileshare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 