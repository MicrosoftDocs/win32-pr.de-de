---
title: Modale Benutzer Funktionen
description: Die modalen Funktionen der Netzwerk Verwaltungs Benutzer erhalten und legen systemweite Parameter fest, die sich auf das Verhalten des Sicherheitssystems beziehen.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949048"
---
# <a name="user-modal-functions"></a>Modale Benutzer Funktionen

Die modalen Funktionen der Netzwerk Verwaltungs Benutzer erhalten und legen systemweite Parameter fest, die sich auf das Verhalten des Sicherheitssystems beziehen.

Die modalen Benutzer Funktionen sind nachfolgend aufgeführt.



| Funktion                                     | BESCHREIBUNG                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Nettusermodalsget"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Gibt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank zurück, bei der es sich um die SAM-Datenbank (Security Accounts Manager) handelt, oder, im Fall von Domänen Controllern, die Active Directory. |
| [**"Nettusermodalsset"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Legt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank fest.                                                                                                                       |



 

Die Funktionen " **nettusermodalsget** " und " **nettusermodalsset** " überprüfen und ändern die modalen Einstellungen, bei denen es sich um globale Parameter handelt, die sich auf jedes Konto in der Sicherheitsdatenbank auswirken (z. b. die minimal zulässige Kenn Wort Länge Alle modalen Einstellungen können durch Aufrufen von " **nettusermodalsset**" geändert werden. Die meisten modale können auch mit dem Befehl **net Accounts** geändert werden. Die modalen Funktionen der Netzwerk Verwaltungs Benutzer erfordern nicht, dass der Server über Sicherheit auf Benutzerebene verfügt.

Benutzer modale Informationen sind auf folgenden Ebenen verfügbar:

-   [**Benutzer \_ modals \_ Info \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**Benutzer \_ modals \_ Info \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**Benutzer- \_ modals \_ Info \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**Benutzer \_ modals \_ Info \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

Die folgenden Informationsebenen sind nur für ' [**nettusermodalsset**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) ' gültig und ersetzen die ältere Methode zum Übergeben eines *Parametern* zum Festlegen eines bestimmten Felds:

-   [**Benutzer- \_ modals- \_ Informationen \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**Benutzer- \_ modals- \_ Informationen \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**Benutzer- \_ modals- \_ Informationen \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**Benutzer- \_ modals- \_ Informationen \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**Benutzer- \_ modals- \_ Informationen \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**Benutzer- \_ modals- \_ Informationen \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**Benutzer- \_ modals- \_ Informationen \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um dieselbe Funktionalität zu erreichen, die Sie erreichen können, indem Sie die modalen Funktionen der Netzwerk Verwaltungs Benutzer aufrufen. Weitere Informationen finden Sie unter [**iadsdomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 