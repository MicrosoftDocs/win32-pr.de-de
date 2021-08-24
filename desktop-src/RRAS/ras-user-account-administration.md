---
title: RAS-Benutzerkontoverwaltung
description: Ein Windows NT 4.0 RAS-Server verwendet eine Benutzerkontodatenbank, die Informationen zu einer Gruppe von Benutzerkonten enthält.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6254a2d4066c6b4b4e1f1167ec842cd86c07d8122b0683c985cbea0a8ca7f2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028730"
---
# <a name="ras-user-account-administration"></a>RAS-Benutzerkontoverwaltung

Ein Windows NT 4.0 RAS-Server verwendet eine Benutzerkontodatenbank, die Informationen zu einer Gruppe von Benutzerkonten enthält. Die Informationen umfassen die RAS-Berechtigungen eines Benutzers. Dabei handelt es sich um eine Reihe von Bitflags, die bestimmen, wie der RAS-Server reagiert, wenn der Benutzer aufruft, um eine Verbindung herzustellen. Mit den RAS-Serververwaltungsfunktionen können Sie die Benutzerkontodatenbank suchen und die RAS-Berechtigungen für Benutzerkonten abrufen und festlegen.

Ein Windows NT 4.0-RAS-Server kann Teil einer Windows NT/Windows 2000-Domäne oder ein eigenständiger Windows NT-Server oder einer Arbeitsstation sein, die nicht Teil einer Domäne ist. Bei einem Server, der Teil einer Domäne ist, wird die Benutzerkontodatenbank auf dem Server gespeichert, der der primäre Domänencontroller (PDC) ist. Ein eigenständiger Server speichert seine eigene lokale Benutzerkontodatenbank. Um den Namen des Servers abzurufen, auf dem die von einem angegebenen RAS-Server verwendete Benutzerkontodatenbank gespeichert wird, können Sie die [**RasAdminGetUserAccountServer-Funktion**](rasadmingetuseraccountserver.md) aufrufen. Sie können dann den Namen des Benutzerkontoservers in einem Aufruf der [**NetQueryDisplayInformation-Funktion**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) verwenden, um die Benutzer in einer Benutzerkontodatenbank aufzuzählen. Sie können den Servernamen auch in Aufrufen der [**Funktionen RasAdminUserGetInfo**](rasadminusergetinfo.md) und [**RasAdminUserSetInfo**](rasadminusersetinfo.md) verwenden, um die RAS-Berechtigungen für ein angegebenes Benutzerkonto abzurufen und festzulegen.

Die Funktionen [**RasAdminUserGetInfo**](rasadminusergetinfo.md) und [**RasAdminUserSetInfo**](rasadminusersetinfo.md) verwenden die [**RAS USER \_ \_ 0-Struktur,**](ras-user-0-str.md) um die RAS-Berechtigungen und die Rückruftelefonnummer eines Benutzers anzugeben. Die RAS-Berechtigungen geben die folgenden Informationen an:

-   Gibt an, ob der Benutzer eine Remoteverbindung mit dem Server oder der Domäne herstellen kann, zu der der Server gehört.
-   Gibt an, ob der Benutzer eine Verbindung über einen Rückruf herstellen kann, in dem der RAS-Server hängt und dann den Benutzer zurückruft, um die Verbindung herzustellen.

Jedes Benutzerkonto gibt eines der folgenden Flags an, um die Rückrufberechtigung des Benutzers anzugeben.



| Wert                      | Bedeutung                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | Der RAS-Server ruft den Benutzer nicht zurück, um eine Verbindung herzustellen.                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | Wenn der Benutzer aufruft, hängt der RAS-Server auf und ruft eine voreingestellte Rückruftelefonnummer auf, die in der Benutzerkontodatenbank gespeichert ist. Das **szPhoneNumber-Element** der [**RAS USER \_ \_ 0-Struktur**](ras-user-0-str.md) enthält die Rückruftelefonnummer des Benutzers. |
| RASPRIV \_ CallerSetCallback | Wenn der Benutzer anruft, bietet der RAS-Server die Möglichkeit, eine Rückruftelefonnummer anzugeben. Der Benutzer kann auch auswählen, dass die Verbindung sofort ohne Rückruf hergestellt werden soll. Das **szPhoneNumber-Element** enthält eine Standardnummer, die der Benutzer überschreiben kann.      |



 

 

 