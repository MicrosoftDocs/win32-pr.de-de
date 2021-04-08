---
title: Lokale Gruppenfunktionen
description: Eine lokale Gruppe kann Benutzerkonten oder globale Gruppenkonten aus einer oder mehreren Domänen enthalten. (Globale Gruppen können Benutzer aus nur einer Domäne enthalten.) Eine lokale Gruppe nutzt gemeinsame Berechtigungen und Rechte nur innerhalb ihrer eigenen Domäne.
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727816"
---
# <a name="local-group-functions"></a>Lokale Gruppenfunktionen

Eine *lokale Gruppe* kann Benutzerkonten oder globale Gruppenkonten aus einer oder mehreren Domänen enthalten. (Globale Gruppen können Benutzer aus nur einer Domäne enthalten.) Eine lokale Gruppe nutzt gemeinsame Berechtigungen und Rechte nur innerhalb ihrer eigenen Domäne.

Die lokalen Gruppen von Netzwerk Verwaltungsfunktionen Steuern Mitglieder lokaler Gruppen so, dass die Funktionen nur lokal auf dem System aufgerufen werden können, auf dem die lokale Gruppe definiert ist. Auf einer Arbeitsstation oder auf einem Server, der kein Domänen Controller ist, können Sie nur eine lokale Gruppe verwenden, die auf diesem System definiert ist.

In Active Directory Domänen im einheitlichen Modus werden lokale Gruppen als lokale *Domänen Gruppen* bezeichnet. Lokale Domänen Gruppen sind auf allen Domänen Controllern, Mitglieds Servern und Arbeitsstationen verfügbar, die mit der Domäne verknüpft sind. Active Directory Domänen im gemischten Modus werden auf dem primären Domänen Controller definiert und auf allen anderen Domänen Controllern in der Domäne repliziert. Daher ist eine lokale Gruppe auf allen Domänen Controllern in der Domäne verfügbar, in der Sie erstellt wurde.

Die lokalen Gruppenfunktionen erstellen oder löschen lokale Gruppen und überprüfen oder ändern die Mitgliedschaften lokaler Gruppen. Diese Funktionen sind nachfolgend aufgeführt.



| Funktion                                                   | BESCHREIBUNG                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Erstellt eine lokale Gruppe.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Fügt einer vorhandenen lokalen Gruppe einen oder mehrere Benutzer oder globale Gruppen hinzu.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Löscht eine lokale Gruppe, wobei alle vorhandenen Mitglieder aus der Gruppe entfernt werden.    |
| [**Netlocalgroupdelta Members**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Entfernt mindestens ein Mitglied aus einer vorhandenen lokalen Gruppe.               |
| [**Netlocalgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Gibt Informationen zu den einzelnen lokalen Gruppenkonten auf einem Server zurück.         |
| [**Netlocalgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Gibt Informationen zu einem bestimmten lokalen Gruppenkonto auf einem Server zurück. |
| [**Netlocalgroupgetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Listet alle Mitglieder einer angegebenen lokalen Gruppe auf.                           |
| [**Netlocalgroupeintinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Legt allgemeine Informationen zu einer lokalen Gruppe fest.                           |
| [**Netlocalgroupsetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Weist Mitglieder einer lokalen Gruppe zu.                                       |



 

Sie können einer lokalen Gruppe ein Mitglied hinzufügen, indem Sie die Sicherheits-ID (SID) des Members angeben. Um einen Element Kontonamen in eine SID zu übersetzen, nennen Sie die [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) -Funktion.

Wenn Sie eine lokale Gruppe durch Aufrufen der [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) -Funktion erstellen, müssen Sie einen lokalen Gruppennamen angeben. Anfänglich hat die lokale Gruppe keine Mitglieder.

Informationen zu lokalen Gruppenkonten sind auf folgenden Ebenen verfügbar:

-   [**Localgroup- \_ Informationen \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**Localgroup- \_ Informationen \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**Localgroup- \_ Informationen \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

Informationen zu lokalen Gruppenmitgliedschaften sind auf den folgenden Informationsebenen verfügbar:

-   [**Localgroup- \_ Mitglieder \_ Info \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**Localgroup- \_ Mitglieder \_ Info \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**Localgroup- \_ Mitglieder \_ Info \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**Localgroup- \_ Mitglieder \_ Info \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

Sie können die Namen der lokalen Gruppen, zu denen ein Benutzer gehört, abrufen, indem Sie die Funktion " [**nettusergetlocalgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) " aufrufen, indem Sie die folgende Informationsebene angeben:

[**Localgroup- \_ Benutzer \_ Informationen \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

Weitere Informationen finden Sie in den Funktionen der Netzwerk Verwaltungs [Gruppe](group-functions.md).

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie erreichen können, indem Sie die lokalen Gruppenfunktionen der Netzwerkverwaltung aufrufen. Weitere Informationen finden Sie unter [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 