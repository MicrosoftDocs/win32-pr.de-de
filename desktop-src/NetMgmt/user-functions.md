---
title: Benutzerfunktionen
description: Die Benutzerfunktionen der Netzwerkverwaltung steuern das Konto eines Benutzers in der Sicherheitsdatenbank, bei der es sich um die SAM-Datenbank (Security Accounts Manager) oder im Fall von Domänencontrollern um Active Directory handelt. Die Benutzerfunktionen sind im Folgenden aufgeführt.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796816"
---
# <a name="user-functions"></a>Benutzerfunktionen

Die Benutzerfunktionen der Netzwerkverwaltung steuern das Konto eines Benutzers in der Sicherheitsdatenbank, bei der es sich um die SAM-Datenbank (Security Accounts Manager) oder im Fall von Domänencontrollern um Active Directory handelt. Die Benutzerfunktionen sind im Folgenden aufgeführt.



| Funktion                                               | Beschreibung                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Fügt ein Benutzerkonto hinzu und weist eine Kennwort- und Berechtigungsebene zu.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Ändert das Kennwort eines Benutzers für einen angegebenen Netzwerkserver oder eine angegebene Domäne. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Löscht ein Benutzerkonto vom Server.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Listet alle Benutzerkonten auf einem Server auf.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Gibt eine Liste der globalen Gruppennamen zurück, zu denen ein Benutzer gehört.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Gibt Informationen zu einem bestimmten Benutzerkonto auf einem Server zurück.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Gibt eine Liste lokaler Gruppennamen zurück, zu denen ein Benutzer gehört.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Legt globale Gruppenmitgliedschaften für ein angegebenes Benutzerkonto fest.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Legt das Kennwort und andere Elemente eines Benutzerkontos fest.             |



 

Jeder Benutzer oder jede Anwendung, der bzw. die auf Netzwerkressourcen zutritt, muss über ein Konto in der Sicherheitsdatenbank verfügen. Die Verzeichnisdienste verwenden dieses Konto, um zu überprüfen, ob der Benutzer oder die Anwendung über die Berechtigung zum Herstellen einer Verbindung mit einer Ressource verfügt. Wenn ein Benutzer oder eine Anwendung Zugriff auf eine Ressource an fordert, sucht das Windows Sicherheitssystem nach einem geeigneten Benutzerkonto oder Gruppenkonto, um den Zugriff zu ermöglichen.

Nachdem Sie ein Benutzerkonto durch Aufrufen der [**NetUserDel-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) entfernt haben, kann der Benutzer nur noch über das Gastkonto auf den Server zugreifen.

Da das Kennwort eines Benutzers vertraulich ist, wird es nicht von der [**NetUserEnum-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) oder der [**NetUserGetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) zurückgegeben. Das Kennwort wird anfänglich zugewiesen, wenn Sie [**NetUserAdd aufrufen.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)

Benutzerkontoinformationen sind auf den folgenden Ebenen verfügbar:

-   [**BENUTZERINFORMATIONEN \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**BENUTZERINFORMATIONEN \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**BENUTZERINFORMATIONEN \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**BENUTZERINFORMATIONEN \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**BENUTZERINFORMATIONEN \_ \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**BENUTZERINFORMATIONEN \_ \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**BENUTZERINFORMATIONEN \_ \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**BENUTZERINFORMATIONEN \_ \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**BENUTZERINFORMATIONEN \_ \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**BENUTZERINFORMATIONEN \_ \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**BENUTZERINFORMATIONEN \_ \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Darüber hinaus sind die folgenden Informationsebenen gültig, wenn Sie die [**NetUserSetInfo-Funktion**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) aufrufen:

-   [**BENUTZERINFORMATIONEN \_ \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**BENUTZERINFORMATIONEN \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**BENUTZERINFORMATIONEN \_ \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**BENUTZERINFORMATIONEN \_ \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**BENUTZERINFORMATIONEN \_ \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**BENUTZERINFORMATIONEN \_ \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**BENUTZERINFORMATIONEN \_ \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**BENUTZERINFORMATIONEN \_ \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**BENUTZERINFORMATIONEN \_ \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**BENUTZERINFORMATIONEN \_ \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**BENUTZERINFORMATIONEN \_ \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**BENUTZERINFORMATIONEN \_ \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**BENUTZERINFORMATIONEN \_ \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**BENUTZERINFORMATIONEN \_ \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**BENUTZERINFORMATIONEN \_ \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**BENUTZERINFORMATIONEN \_ \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Mit den folgenden Funktionen können Anwendungen die Kennwortkonformität überprüfen.



| Funktion                                                               | Beschreibung                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Gibt den von der [**NetValidatePasswordPolicy-Funktion zugeordneten Arbeitsspeicher**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) frei. |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Überprüft, ob Kennwörter die Anforderungen an Komplexität, Altern, Mindestlänge und Verlaufswiederverwendung erfüllen.            |



 

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Benutzerfunktionen für die Netzwerkverwaltung erreichen können. Weitere Informationen finden Sie unter [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) und [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 