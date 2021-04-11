---
title: Binden mit Verschlüsselung
description: Sensible Daten, die über ein Netzwerk ausgetauscht werden, sollten verschlüsselt werden.
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindung mit Verschlüsselung
- Binden mit Verschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf19747a8356459f4ab50c0aa409f69b58eb224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947356"
---
# <a name="binding-with-encryption"></a>Binden mit Verschlüsselung

Sensible Daten, die über ein Netzwerk ausgetauscht werden, sollten verschlüsselt werden. Um dies zuzulassen, unterstützt ADSI zwei Arten von Verschlüsselung: Kerberos und Secure Sockets Layer (SSL). Beide Verschlüsselungstypen erfordern die Verwendung von [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) für die Bindung.

" **GetObject** " und " [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) " können in diesem Fall nicht für die Bindung verwendet werden, da diese Funktionen bewirken, dass die von ADSI verwendeten LDAP-Anforderungen und die vom Verzeichnisserver zurückgegebenen Daten als Klartext über das Netzwerk übertragen werden. Zu Debuggingzwecken ist es hilfreich, die Verschlüsselung zu deaktivieren, sodass die Netzwerkmonitor zum Anzeigen der LDAP-Anforderungen und-Daten zwischen dem Client und dem Verzeichnisserver verwendet werden kann.

## <a name="kerberos-based-encryption"></a>Kerberos-basierte Verschlüsselung

Wenn Sie die Kerberos-basierte Verschlüsselung verwenden möchten, geben Sie beim Aufrufen von [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)das Flag zum **\_ \_ versiegeln von anzeigen** an. Das Flag " **ADS \_ use \_ versiegelt** " kann auch verwendet werden, um die Datenintegrität zu überprüfen, d. h. um sicherzustellen, dass die empfangenen Daten mit den gesendeten Daten identisch sind. Wenn das Flag für die **Werbeeinblendungen \_ verwendet \_** wird, wird automatisch auch das Flag zum **\_ \_ Signieren von anzeigen** angegeben. Für beide Flags ist die Kerberos-Authentifizierung erforderlich, die nur unter den folgenden Bedingungen funktioniert:

-   Der Client Computer muss bei der Windows-Domäne oder in einer Domäne angemeldet sein, die von einer Windows-Domäne als vertrauenswürdig eingestuft wird.
-   [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) muss mit NULL-Anmelde Informationen aufgerufen werden. Das heißt, es können keine alternativen Anmelde Informationen angegeben werden.

## <a name="ssl-based-encryption"></a>SSL-basierte Verschlüsselung

Wenn Sie die SSL-basierte Verschlüsselung verwenden möchten, geben Sie beim Aufrufen von [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)das Flag zum **\_ Verwenden des \_ SSL** -Kennzeichens an. Wenn nur die **ADS \_ \_ SSL** -Flag verwenden angegeben ist, öffnet ADSI den SSL-Port 636 und führt dann eine einfache Bindung über diesen SSL-Kanal aus. Wenn die **\_ sichere \_ Authentifizierung** und die Werbung **\_ \_ SSL** -Flags verwenden, ist das Bindungsverhalten vom Client abhängig, von dem der-Befehl stammt. Bei nicht unterstützten Versionen von Windows öffnet ADSI zuerst einen SSL-Kanal und führt eine einfache Bindung mit dem angegebenen Benutzernamen und Kennwort oder dem aktuellen Benutzer Kontext durch, wenn sowohl der Benutzername als auch das Kennwort NULL sind. Unter den unterstützten Versionen von Windows führt ADSI eine sichere Authentifizierung anstelle einer einfachen Bindung aus.

Zur Verwendung der SSL-basierten Verschlüsselung bei der Kommunikation mit Active Directory muss Active Directory die Public Key-Infrastruktur (PKI) aktivieren. PKI kann aktiviert werden, indem Sie eine Unternehmens Zertifizierungsstelle auf einem der Server in Active Directory einrichten, einschließlich eines der Active Directory Server selbst. Das Einrichten einer Unternehmens Zertifizierungsstelle bewirkt, dass ein Active Directory Server ein Serverzertifikat erhält, das dann für die SSL-basierte Verschlüsselung verwendet werden kann.

 

 




