---
title: Anforderungen an die Netzwerk Verwaltungsfunktionen auf Active Directory-Domäne Controllern
description: Wenn Sie eine der in diesem Thema aufgeführten Netzwerk Verwaltungsfunktionen auf einem Domänen Controller aufrufen, auf dem Active Directory ausgeführt wird, wird der Zugriff auf ein Sicherungs fähiges Objekt basierend auf der Zugriffs Steuerungs Liste (Access Control List, ACL) für das Objekt zugelassen oder verweigert.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858311"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Anforderungen an die Netzwerk Verwaltungsfunktionen auf Active Directory-Domäne Controllern

Wenn Sie eine der in diesem Thema aufgeführten Netzwerk Verwaltungsfunktionen auf einem Domänen Controller aufrufen, auf dem Active Directory ausgeführt wird, wird der Zugriff auf ein Sicherungs [fähiges Objekt](/windows/desktop/SecAuthZ/securable-objects) basierend auf der [Zugriffs Steuerungs Liste (Access Control List](/windows/desktop/SecAuthZ/access-control-lists) , ACL) für das Objekt zugelassen oder verweigert. (ACLs werden im Verzeichnis angegeben.)

Andere Zugriffs Anforderungen gelten für Informations Abfragen und Informations Aktualisierungen.

## <a name="queries"></a>Abfragen

Bei Abfragen können alle authentifizierten Benutzer und Mitglieder der Gruppe "[Pre-Windows 2000 Compatible Access](/windows/desktop/SecAuthZ/allowing-anonymous-access)" in der Standard-ACL Informationen lesen und auflisten. Die folgenden Funktionen sind betroffen:

-   [**Netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**netgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**netgroupgetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**Netlocalgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**netlocalgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**netlocalgroupgetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   " [**Nettessiongetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) " (nur Stufen 1 und 2)
-   [**Netshareaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (nur Ebenen 2 und 502)
-   " [**Nettuserenum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)", " [**nettusergetgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)", " [**nettusergetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)", " [**nettusergetlocalgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups)", " [**nettusermodalsget**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) "
-   [**Netwkstagetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **netwkstausererium**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Der anonyme Zugriff auf Gruppeninformationen erfordert, dass der anonyme Benutzer explizit der "Pre-Windows 2000 Compatible Access"-Gruppe hinzugefügt wird. Dies liegt daran, dass anonyme Token nicht die Gruppen-SID "jeder" enthalten.

**Windows 2000:** Standardmäßig enthält die Gruppe "Pre-Windows 2000 Compatible Access" alle als Mitglied. Dies ermöglicht den anonymen Zugriff (anonyme Anmeldung), um Informationen zu erhalten, wenn das System den anonymen Zugriff zulässt. Administratoren können jederzeit alle Benutzer aus der Gruppe "Pre-Windows 2000 Compatible Access" entfernen. Wenn Sie alle Benutzer aus der Gruppe entfernen, wird der Zugriff auf Informationen nur auf authentifizierte Benutzer beschränkt Weitere Informationen über den anonymen Zugriff finden Sie unter [Sicherheits](/windows/desktop/SecAuthZ/security-identifiers) -IDs und [Bekannte SIDs](/windows/desktop/SecAuthZ/well-known-sids).

Sie können den Standardwert des Systems überschreiben, indem Sie den folgenden Schlüssel in der Registrierung auf den Wert 1 festlegen:

**HKEY \_ Lokales \_ Computer \\ System \\ CurrentControlSet- \\ Steuerelement \\ LSA** \\ **everyoneincludezs\1**

Weitere Informationen über den anonymen Zugriff auf Gruppeninformationen beim Aufrufen dieser beiden Funktionen finden Sie unter [**netwkstagetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) und [**netwkstauserenum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) .

## <a name="updates"></a>Aktualisierungen

Bei Updates können von der Standard-ACL nur Domänen Administratoren und Konto Operatoren Informationen schreiben. Eine Ausnahme besteht darin, dass Benutzer ihr eigenes Kennwort ändern und das Feld für die Verwendung von "USA, usr" festlegen können \* \_ \_ . Eine weitere Ausnahme ist, dass Konto Betreiber Verwaltungs Konten nicht ändern können. Die folgenden Funktionen sind betroffen:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**netgroupadduser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**netgroupdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**netgroupdeluser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**netgroupsetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**netgroupsetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**netlocalgroupsetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**netlocalgroupsetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**Netmessagebuffersend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   " [**Nettuseradd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)", " [**nettuserchangepassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword)", " [**nettuserdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)", " [**nettusermodalsset**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset)", " [**nettusersetgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)", " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

In der Regel benötigen Aufrufer Schreibzugriff auf das gesamte Objekt, damit Aufrufe an " [**nettusermodalsset**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset)", " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)", " [**netgroupsetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) " und " [**netlocalgroupsetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) " erfolgreich ausgeführt werden können. Für eine präzisere Zugriffs Steuerung sollten Sie die Verwendung von ADSI in Erwägung gezogen. Weitere Informationen zu ADSI finden Sie unter [Active Directory-Dienst Schnittstellen](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Weitere Informationen zum Steuern des Zugriffs auf Sicherungs fähige Objekte finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control), [Berechtigungen](/windows/desktop/SecAuthZ/privileges)und Sicherungs [fähige Objekte](/windows/desktop/SecAuthZ/securable-objects). Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

 

 