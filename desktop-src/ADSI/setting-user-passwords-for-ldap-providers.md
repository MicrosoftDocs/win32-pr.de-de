---
title: Festlegen und Ändern von Benutzerpasswörtern mit dem LDAP-Anbieter
description: Um ein Benutzerkennwort festzulegen, verwenden Sie die IADsUser.SetPassword-Methode.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- LDAP-Anbieter ADSI, Benutzerobjekt, Festlegen von Kennwörtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbbd0439a011575fbc9278dbe506d46db2210ce03d807ea74097499cb764b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690525"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Festlegen und Ändern von Benutzerpasswörtern mit dem LDAP-Anbieter

Um ein Benutzerkennwort festzulegen, verwenden Sie die [**IADsUser.SetPassword-Methode.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)

Der LDAP-Anbieter für Active Directory verwendet einen von drei Prozessen zum Festlegen des Kennworts (LDAP-Verzeichnisse von Drittanbietern wie iEinander verwenden diesen Kennwortauthentifizierungsprozess nicht). Die Methode kann je nach Netzwerkkonfiguration variieren. Die methoden zum Festlegen von Kennwörtern erfolgen in der folgenden Reihenfolge:

-   Zunächst versucht der LDAP-Anbieter, LDAP über eine 128-Bit-SSL-Verbindung zu verwenden. Damit LDAP SSL erfolgreich funktioniert, muss auf dem LDAP-Server das entsprechende Serverauthentifizierungszertifikat installiert sein, und die Clients, auf denen der ADSI-Code ausgeführt wird, müssen der Zertifizierungsstelle vertrauen, die diese Zertifikate ausgestellt hat. Sowohl der Server als auch der Client müssen die 128-Bit-Verschlüsselung unterstützen.
-   Zweitens versucht der LDAP-Anbieter, Kerberos zu verwenden, wenn die SSL-Verbindung nicht erfolgreich ist. Ab Windows 2000 unterstützt Kerberos möglicherweise keine gesamtstrukturübergreifende Authentifizierung. Spätere Verbesserungen von Kerberos unterstützen die gesamtstrukturübergreifende Authentifizierung.
-   Drittens: Wenn Kerberos nicht erfolgreich ist, versucht der LDAP-Anbieter einen [**NetUserSetInfo-API-Aufruf.**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) In früheren Releases hat ADSI **NetUserSetInfo** im Sicherheitskontext aufgerufen, in dem der Thread ausgeführt wurde, und nicht den Sicherheitskontext, der im Aufruf von [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)angegeben wurde. In späteren Versionen wurde dies geändert, sodass der ADSI-LDAP-Anbieter beim Aufrufen von **NetUserSetInfo** die Identität des im **OpenDSObject-Aufruf** angegebenen Benutzers annehmen würde.

Um ein Benutzerkennwort zu ändern, verwenden Sie die [**IADsUser.ChangePassword-Methode.**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) Wie [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)kann diese Methode mehrere Prozesse verwenden, um das Kennwort zu ändern. Die Methoden zum Ändern von Kennwörtern erfolgen in der folgenden Reihenfolge:

-   Zunächst versucht der LDAP-Anbieter, LDAP über eine 128-Bit-SSL-Verbindung zu verwenden.
-   Zweitens: Wenn die 128-SSL-Verbindung nicht erfolgreich ist, versucht der LDAP-Anbieter einen [**NetUserChangePassword-API-Aufruf.**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) Wie [**setPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)nimmt der ADSI-LDAP-Anbieter in früheren Versionen die Identität der Benutzeranmeldeinformationen an, die mit der [**IADsOpenDSObject.OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) oder der [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) übergeben wurden.

 

 