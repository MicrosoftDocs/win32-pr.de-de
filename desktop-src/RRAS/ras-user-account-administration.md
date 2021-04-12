---
title: RAS-Benutzerkonten Verwaltung
description: Ein Windows NT 4,0-RAS-Server verwendet eine Benutzerkonten Datenbank, die Informationen zu einem Satz von Benutzerkonten enthält.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d090fc16e7d731525b79493119f3c604e043c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315381"
---
# <a name="ras-user-account-administration"></a>RAS-Benutzerkonten Verwaltung

Ein Windows NT 4,0-RAS-Server verwendet eine Benutzerkonten Datenbank, die Informationen zu einem Satz von Benutzerkonten enthält. Die Informationen beinhalten die RAS-Berechtigungen eines Benutzers, bei denen es sich um einen Satz von Bitflags handelt, die bestimmen, wie der RAS-Server reagiert, wenn der Benutzer eine Verbindung aufruft. Mit den RAS-Server-Verwaltungsfunktionen können Sie die Benutzerkonten Datenbank suchen und die RAS-Berechtigungen für Benutzerkonten ermitteln und festlegen.

Ein Windows NT 4,0-RAS-Server kann Teil einer Windows NT/Windows 2000-Domäne sein, oder es kann sich um einen eigenständigen Windows NT-Server oder eine Arbeitsstation handeln, der nicht Teil einer Domäne ist. Bei einem Server, der Teil einer Domäne ist, wird die Datenbank des Benutzerkontos auf dem Server gespeichert, der als primärer Domänen Controller (PDC) verwendet wird. Ein eigenständiger Server speichert seine eigene lokale Benutzerkonten Datenbank. Zum Abrufen des Namens des Servers, auf dem die Benutzerkonten Datenbank gespeichert ist, die von einem angegebenen RAS-Server verwendet wird, können Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion aufrufen. Anschließend können Sie den Namen des Benutzerkonto Servers in einem aufzurufenden Befehl der [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) -Funktion verwenden, um die Benutzer in einer Benutzerkonten Datenbank aufzulisten. Sie können auch den Servernamen in Aufrufen der [**rasadminusergetinfo**](rasadminusergetinfo.md) -Funktion und der [**rasadminusersetinfo**](rasadminusersetinfo.md) -Funktion verwenden, um die RAS-Berechtigungen für ein angegebenes Benutzerkonto abzurufen und festzulegen.

Die [**rasadminusergetinfo**](rasadminusergetinfo.md) -und [**rasadminuserminfo**](rasadminusersetinfo.md) -Funktionen verwenden die [**RAS-Benutzer- \_ \_ 0**](ras-user-0-str.md) -Struktur, um die RAS-Berechtigungen und die Rückruf Telefonnummer eines Benutzers anzugeben. Die RAS-Berechtigungen geben die folgenden Informationen an:

-   Gibt an, ob der Benutzer eine Remote Verbindung mit dem Server oder der Domäne herstellen kann, zu der der Server gehört.
-   Gibt an, ob der Benutzer mithilfe eines Rückrufs eine Verbindung herstellen kann, in der der RAS-Server nicht mehr angezeigt wird, und ruft dann den Benutzer zum Herstellen der Verbindung zurück.

Jedes Benutzerkonto gibt eines der folgenden Flags an, um die Rückruf Berechtigung des Benutzers anzugeben.



| Wert                      | Bedeutung                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Raspriv \_ NoCallback        | Der RAS-Server Ruft den Benutzer nicht zurück, um eine Verbindung herzustellen.                                                                                                                                                                                        |
| Raspriv \_ adminsetcallback  | Wenn der Benutzer aufruft, reagiert der RAS-Server und ruft eine voreingestellte Telefonnummer auf, die in der Benutzerkonten Datenbank gespeichert ist. Der **szphonenumber** -Member der [**RAS- \_ Benutzer- \_ 0**](ras-user-0-str.md) -Struktur enthält die Rückruf Telefonnummer des Benutzers. |
| Raspriv \_ callersetcallback | Wenn der Benutzer aufruft, bietet der RAS-Server die Möglichkeit, eine Rückruf Telefonnummer anzugeben. Der Benutzer kann auch sofort eine Verbindung ohne Rückruf herstellen. Der **szphonenumber** -Member enthält eine Standardzahl, die der Benutzer überschreiben kann.      |



 

 

 