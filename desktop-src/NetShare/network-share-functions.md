---
description: Die Netzwerkfreigabe Funktionen steuern freigegebene Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. b. ein Datenträger Verzeichnis, Druck Gerät oder Named Pipe), auf die von Benutzern und Anwendungen im Netzwerk zugegriffen werden kann.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Netzwerkfreigabe Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356665"
---
# <a name="network-share-functions"></a>Netzwerkfreigabe Funktionen

Die Netzwerkfreigabe Funktionen steuern freigegebene Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. b. ein Datenträger Verzeichnis, Druck Gerät oder Named Pipe), auf die von Benutzern und Anwendungen im Netzwerk zugegriffen werden kann.

Die Freigabe Funktionen sind nachfolgend aufgeführt.



| Funktion                                   | BESCHREIBUNG                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | Gibt eine Ressource auf einem Server frei.                                       |
| [**Netsharecheck**](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | Fragt ab, ob ein Server ein Gerät gemeinsam verwendet.                        |
| [**Netsharedel**](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | Löscht einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers.       |
| [**Netshareaufumum**](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | Ruft Freigabe Informationen zu den einzelnen freigegebenen Ressourcen auf einem Server ab.  |
| [**NetShareGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | Ruft Informationen zu einer angegebenen freigegebenen Ressource auf einem Server ab. |
| [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | Legt die Parameter einer freigegebenen Ressource fest.                                 |



 

Die [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) -Funktion ermöglicht es einem Benutzer oder einer Anwendung, mithilfe des angegebenen Freigabe namens eine Ressource eines bestimmten Typs freizugeben. Die Funktion **NetShareAdd** erfordert, dass der Freigabe Name und der Name des lokalen Geräts die Ressource freigeben. Ein Benutzer oder eine Anwendung muss über ein Konto auf dem Server verfügen, um auf die Ressource zugreifen zu können.

Sie können auch eine Sicherheits Beschreibung angeben, die einer Freigabe zugeordnet werden soll. Sicherheits Deskriptoren geben an, welche Benutzer über die Freigabe auf Dateien zugreifen dürfen und mit welchem Zugriffstyp. Geben Sie [**eine Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) mit der Informationsebene [**Freigabe \_ Info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) an, wenn [**Sie NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) oder [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)aufrufen. **NetShareSetInfo** unterstützt die Informationsebene [**Freigabe \_ Info \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) . Weitere Informationen zu Sicherheits Beschreibungen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Die Netzwerk Verwaltungsfunktionen verwenden die folgenden speziellen Freigabe Namen für die prozessübergreifende Kommunikation (prozessübergreifende Communication, IPC) und die Remote Verwaltung des-Servers:

-   IPC $, für prozessübergreifende Kommunikation reserviert
-   ADMIN $, für Remote Verwaltung reserviert
-   A $, B $, C $ (und andere lokale Datenträger Namen, gefolgt von einem Dollarzeichen), die lokalen Datenträgern zugewiesen sind

Um alle Verbindungen aufzulisten, die mit einer freigegebenen Ressource auf einem Server hergestellt wurden, oder um alle Verbindungen aufzulisten, die von einem bestimmten Computer hergestellt wurden, nennen Sie die [**netconnectionenum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) -Funktion. Sie können **netconnectionenum** auf den Informationsebenen [**Connection \_ Info \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) und [**Connection \_ Info \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) aufzurufen.

Freigabe Funktionen sind auf den folgenden Informationsebenen verfügbar:

<dl>

[**Freigabe \_ Informationen \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[**Freigabe \_ Informationen \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[**Freigabe \_ Informationen \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[**Freigabe \_ Informationen \_ 501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[**Freigabe \_ Informationen \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[**Freigabe \_ Informationen \_ 1005**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

Die folgenden Informationsebenen sind nur für [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)gültig:

<dl>

[**Freigabe \_ Informationen \_ 1004**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[**Freigabe \_ Informationen \_ 1006**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[**Freigabe \_ Informationen \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungs Freigabe erreichen können. Weitere Informationen finden Sie unter [**iadsfileshare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 
