---
title: Festlegen und Ändern von Benutzer Kennwörtern mit dem LDAP-Anbieter
description: Verwenden Sie die IADsUser. SetPassword-Methode, um ein Benutzer Kennwort festzulegen.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- LDAP-Anbieter-ADSI, Benutzerobjekt, Festlegen von Kenn Wörtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5488146de271ac1108a904cd85163fad9d7dd205
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316443"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Festlegen und Ändern von Benutzer Kennwörtern mit dem LDAP-Anbieter

Verwenden Sie die [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) -Methode, um ein Benutzer Kennwort festzulegen.

Der LDAP-Anbieter für Active Directory verwendet einen von drei Prozessen, um das Kennwort festzulegen (LDAP-Verzeichnisse von Drittanbietern, z. b. iPlanet verwenden diesen Prozess zur Kenn Wort Authentifizierung nicht). Die Methode kann je nach Netzwerkkonfiguration variieren. Die Methoden zum Festlegen des Kennworts treten in der folgenden Reihenfolge auf:

-   Zuerst versucht der LDAP-Anbieter, LDAP über eine 128-Bit-SSL-Verbindung zu verwenden. Damit LDAP-SSL erfolgreich ausgeführt werden kann, muss auf dem LDAP-Server das geeignete Server Authentifizierungszertifikat installiert sein, und die Clients, auf denen der ADSI-Code ausgeführt wird, müssen der Zertifizierungsstelle vertrauen, die diese Zertifikate Sowohl der Server als auch der Client müssen die 128-Bit-Verschlüsselung unterstützen.
-   Zweitens: Wenn die SSL-Verbindung nicht erfolgreich ist, versucht der LDAP-Anbieter, Kerberos zu verwenden. Unter Windows 2000 unterstützt Kerberos möglicherweise keine Gesamtstruktur übergreifende Authentifizierung. Spätere Erweiterungen für Kerberos unterstützen die Gesamtstruktur übergreifende Authentifizierung.
-   Drittens, wenn Kerberos nicht erfolgreich ist, versucht der LDAP-Anbieter, einen [**nettusersetinfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) -API-aufzurufen. In früheren Versionen hieß ADSI " **netusersetinfo** " im Sicherheitskontext, in dem der Thread ausgeführt wurde, und nicht der Sicherheitskontext, der im Aufruf von [**iadsopendsobject. opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)angegeben wurde. In späteren Versionen wurde dies geändert, sodass der ADSI LDAP-Anbieter die Identität des im **opendsobject** -Aufruf angegebenen Benutzers annimmt, wenn er **netusersetinfo** aufruft.

Verwenden Sie die [**IADsUser. ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) -Methode, um ein Benutzer Kennwort zu ändern. Wie bei [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)kann diese Methode mehrere Prozesse verwenden, um das Kennwort zu ändern. Die Methode zum Ändern von Kenn Wörtern erfolgt in der folgenden Reihenfolge:

-   Zuerst versucht der LDAP-Anbieter, LDAP über eine 128-Bit-SSL-Verbindung zu verwenden.
-   Zweitens: Wenn die 128-SSL-Verbindung nicht hergestellt werden kann, versucht der LDAP-Anbieter, einen [**nettuserchangepassword**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) -API-Befehl zu erhalten. Wie bei [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)nimmt der ADSI LDAP-Anbieter in früheren Versionen die Identität der Benutzer Anmelde Informationen an, die mithilfe der [**iadsopendsobject. opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode oder der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion weitergegeben wurden.

 

 