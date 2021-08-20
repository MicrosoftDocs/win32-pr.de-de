---
title: Bindung mit Verschlüsselung
description: Sensible Daten, die über ein Netzwerk ausgetauscht werden, sollten verschlüsselt werden.
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , mit, Bindung mit Verschlüsselung
- Bindung mit Verschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268bc384228f6cb11b9de7b0112f9613aabfb5f50ddfa09545c97b96fe61ddc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017927"
---
# <a name="binding-with-encryption"></a>Bindung mit Verschlüsselung

Sensible Daten, die über ein Netzwerk ausgetauscht werden, sollten verschlüsselt werden. Um dies zu ermöglichen, unterstützt ADSI zwei Verschlüsselungstypen: Kerberos und Secure Sockets Layer (SSL). Beide Verschlüsselungstypen erfordern die Verwendung von [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) für die Bindung.

**GetObject** und [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) können in diesem Fall nicht für die Bindung verwendet werden, da diese Funktionen dazu führen, dass die von ADSI verwendeten LDAP-Anforderungen und die vom Verzeichnisserver zurückgegebenen Daten als Klartext über das Netzwerk übertragen werden. Zu Debugzwecken ist es hilfreich, die Verschlüsselung zu deaktivieren, damit die Netzwerkmonitor zum Anzeigen der LDAP-Anforderungen und -Daten zwischen dem Client und dem Verzeichnisserver verwendet werden kann.

## <a name="kerberos-based-encryption"></a>Kerberos-basierte Verschlüsselung

Um die Kerberos-basierte Verschlüsselung zu verwenden, geben Sie beim Aufrufen von [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)das **FLAG ADS USE \_ \_ ARMOR** an. The **ADS\_USE\_SEALING** flag can also be used to verify data integrity, that is, to ensure the data received is the same as the data sent. Wenn das **FLAG ADS USE \_ \_ VERSIEGELT** angegeben ist, wird automatisch auch das **FLAG ADS USE \_ \_ SIGNING** angegeben. Beide Flags erfordern die Kerberos-Authentifizierung, die nur unter den folgenden Bedingungen funktioniert:

-   Der Clientcomputer muss bei der Windows Domäne oder bei einer Domäne angemeldet sein, die von einer Windows wird.
-   [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) muss mit NULL-Anmeldeinformationen aufgerufen werden. Das heißt, alternative Anmeldeinformationen können nicht angegeben werden.

## <a name="ssl-based-encryption"></a>SSL-basierte Verschlüsselung

Geben Sie zum Verwenden der SSL-basierten Verschlüsselung das **ADS \_ USE \_ SSL-Flag** an, wenn [**Sie ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**IADsOpenDSObject::OpenDSObject aufrufen.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) Wenn nur das **ADS \_ USE \_ SSL-Flag** angegeben ist, öffnet ADSI SSL-Port 636 und führt dann eine einfache Bindung über diesen SSL-Kanal aus. Wenn sowohl die **ADS \_ SECURE \_ AUTHENTICATION-** als auch **die ADS USE \_ \_ SSL-Flags** angegeben sind, hängt das Bindungsverhalten vom Client ab, von dem der Aufruf erfolgt. Bei nicht unterstützten Versionen von Windows öffnete ADSI zuerst einen SSL-Kanal und führt eine einfache Bindung mit dem angegebenen Benutzernamen und Kennwort oder dem aktuellen Benutzerkontext aus, wenn benutzername und kennwort null sind. Bei unterstützten Versionen von Windows ADSI eine sichere Authentifizierung anstelle einer einfachen Bindung.

Für die Verwendung der SSL-basierten Verschlüsselung bei der Kommunikation mit Active Directory muss für Active Directory die Public Key-Infrastruktur (PKI) aktiviert sein. PKI kann aktiviert werden, indem eine Unternehmenszertifizierungsstelle auf einem der Server in Active Directory eingerichtet wird, einschließlich eines der Active Directory-Server selbst. Das Einrichten einer Unternehmenszertifizierungsstelle bewirkt, dass ein Active Directory-Server ein Serverzertifikat bekommt, das dann für die SSL-basierte Verschlüsselung verwendet werden kann.

 

 




