---
title: Modale Benutzerfunktionen
description: Die modalen Benutzerfunktionen der Netzwerkverwaltung erhalten systemweite Parameter im Zusammenhang mit dem Sicherheitssystemverhalten und legen diese fest.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addea3c76d79cbcdb0e359424be154893d2c436c1f6d45157ecf50e748fc9417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796796"
---
# <a name="user-modal-functions"></a>Modale Benutzerfunktionen

Die modalen Benutzerfunktionen der Netzwerkverwaltung erhalten systemweite Parameter im Zusammenhang mit dem Sicherheitssystemverhalten und legen diese fest.

Die modalen Benutzerfunktionen sind im Folgenden aufgeführt.



| Funktion                                     | Beschreibung                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Gibt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank zurück, bei denen es sich um die SAM-Datenbank (Security Accounts Manager) oder im Fall von Domänencontrollern um Active Directory handelt. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Legt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank fest.                                                                                                                       |



 

Die Funktionen **NetUserModalsGet** und **NetUserModalsSet** untersuchen und ändern die modalen Einstellungen. Dabei handelt es sich um globale Parameter, die sich auf jedes Konto in der Sicherheitsdatenbank auswirken (z. B. die minimale zulässige Kennwortlänge). Alle modalen Einstellungen können durch Aufrufen von **NetUserModalsSet** geändert werden. Die meisten Modalen können auch mit dem Befehl **net accounts** geändert werden. Die modalen Funktionen des Netzwerkverwaltungsbenutzers erfordern keine Sicherheit auf Benutzerebene für den Server.

Modale Benutzerinformationen sind auf den folgenden Ebenen verfügbar:

-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

Die folgenden Informationsebenen sind nur für [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) gültig und ersetzen die ältere Methode der Übergabe eines *Parmnums,* um ein bestimmtes Feld festzulegen:

-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**BENUTZER \_ MODALE \_ INFORMATIONEN \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der modalen Funktionen des Netzwerkverwaltungsbenutzers erreichen können. Weitere Informationen finden Sie unter [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 