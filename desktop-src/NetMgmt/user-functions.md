---
title: Benutzer Funktionen
description: Die Benutzer Funktionen der Netzwerkverwaltung steuern das Konto eines Benutzers in der Sicherheitsdatenbank, bei der es sich um die SAM-Datenbank (Security Accounts Manager) handelt, oder, im Fall von Domänen Controllern, die Active Directory. Die Benutzer Funktionen sind nachfolgend aufgeführt.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a3349673d09e42fbfe7a5dc949d1bcff53b828
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339510"
---
# <a name="user-functions"></a>Benutzer Funktionen

Die Benutzer Funktionen der Netzwerkverwaltung steuern das Konto eines Benutzers in der Sicherheitsdatenbank, bei der es sich um die SAM-Datenbank (Security Accounts Manager) handelt, oder, im Fall von Domänen Controllern, die Active Directory. Die Benutzer Funktionen sind nachfolgend aufgeführt.



| Funktion                                               | BESCHREIBUNG                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**"Nettuseradd"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Fügt ein Benutzerkonto hinzu und weist ein Kennwort und eine Berechtigungsebene zu.     |
| [**"Nettuserchangepassword"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Ändert das Kennwort eines Benutzers für einen angegebenen Netzwerkserver oder eine angegebene Domäne. |
| [**"Nettuserdel"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Löscht ein Benutzerkonto auf dem Server.                             |
| [**"Nettuserenum"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Listet alle Benutzerkonten auf einem Server auf.                                |
| [**"Nettusergetgroups"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Gibt eine Liste der globalen Gruppennamen zurück, zu denen ein Benutzer gehört.       |
| [**"Nettusergetinfo"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Gibt Informationen zu einem bestimmten Benutzerkonto auf einem Server zurück.    |
| [**"Nettusergetlocalgroups"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Gibt eine Liste der lokalen Gruppennamen zurück, zu denen ein Benutzer gehört.        |
| [**"Nettusersetgroups"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Legt globale Gruppenmitgliedschaften für ein angegebenes Benutzerkonto fest.         |
| [**"Nettusersetinfo"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Legt das Kennwort und andere Elemente eines Benutzerkontos fest.             |



 

Jeder Benutzer oder jede Anwendung, der auf Netzwerkressourcen zugreift, muss über ein Konto in der Sicherheitsdatenbank verfügen. Die Verzeichnisdienste verwenden dieses Konto, um sicherzustellen, dass der Benutzer oder die Anwendung über die Berechtigung zum Herstellen einer Verbindung mit einer Ressource verfügt. Wenn ein Benutzer oder eine Anwendung den Zugriff auf eine Ressource anfordert, wird vom Windows-Sicherheitssystem nach einem entsprechenden Benutzerkonto oder Gruppenkonto gesucht, um den Zugriff zuzulassen.

Wenn Sie ein Benutzerkonto durch Aufrufen der Funktion " [**nettuserdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) " entfernen, kann der Benutzer nicht mehr auf den Server zugreifen, es sei denn, Sie verwenden das Gastkonto.

Da das Kennwort eines Benutzers vertraulich ist, wird es nicht von der Funktion " [**nettuserenum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) " oder der Funktion " [**nettusergetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) " zurückgegeben. Das Kennwort wird anfänglich zugewiesen, wenn Sie " [**nettuseradd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)" aufrufen.

Die Benutzerkontoinformationen sind auf folgenden Ebenen verfügbar:

-   [**Benutzer \_ Informationen \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**Benutzer \_ Informationen \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**Benutzer \_ Informationen \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**Benutzer \_ Informationen \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**Benutzer \_ Informationen \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**Benutzer \_ Informationen \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**Benutzer \_ Informationen \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**Benutzer \_ Informationen \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**Benutzer \_ Informationen \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**Benutzer \_ Informationen \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**Benutzer \_ Informationen \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Außerdem sind die folgenden Informationsebenen gültig, wenn Sie die Funktion " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " aufrufen:

-   [**Benutzer \_ Informationen \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**Benutzer \_ Informationen \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**Benutzer \_ Informationen \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**Benutzer \_ Informationen \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**Benutzer \_ Informationen \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**Benutzer \_ Informationen \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**Benutzer \_ Informationen \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**Benutzer \_ Informationen \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**Benutzer \_ Informationen \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**Benutzer \_ Informationen \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**Benutzer \_ Informationen \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**Benutzer \_ Informationen \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**Benutzer \_ Informationen \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**Benutzer \_ Informationen \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**Benutzer \_ Informationen \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**Benutzer \_ Informationen \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Mit den folgenden Funktionen können Anwendungen die Kenn Wort Konformität überprüfen.



| Funktion                                                               | BESCHREIBUNG                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Netvalidatepasswordpolicyfree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Gibt den von der [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) -Funktion belegten Arbeitsspeicher frei. |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Mit dieser Option wird überprüft, ob Kenn Wörter die Anforderungen für Komplexität, Alterung, minimale Länge und Versions Wiederverwendung erfüllen.            |



 

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Netzwerk Verwaltungs Benutzer Funktionen erreichen können. Weitere Informationen finden Sie unter [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) und [**iadscomputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 