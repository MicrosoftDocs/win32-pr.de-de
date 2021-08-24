---
title: RAS-Benutzerverwaltung
description: Ein RAS-Server verwendet eine Benutzerkontodatenbank, die Informationen zu einer Gruppe von Benutzerkonten enthält.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- RAS-Verwaltung RRAS , Benutzerverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e4916a9cf6138ebb6c201e9301feacbe332649036e7eb18075df621512a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028640"
---
# <a name="ras-user-administration"></a>RAS-Benutzerverwaltung

Ein RAS-Server verwendet eine Benutzerkontodatenbank, die Informationen zu einer Gruppe von Benutzerkonten enthält. Die Informationen umfassen die RAS-Berechtigungen eines Benutzers. Dabei handelt es sich um eine Reihe von Bitflags, die bestimmen, wie der RAS-Server reagiert, wenn der Benutzer aufruft, um eine Verbindung herzustellen. Die RAS-Serververwaltungsfunktionen suchen die Benutzerkontodatenbank und erhalten und legen die RAS-Berechtigungen für Benutzerkonten fest.

Ein RAS-Server kann Teil einer Betriebssystemdomäne oder ein eigenständiger Computer sein, auf dem der Server oder die professionelle Version des Betriebssystems ausgeführt wird. Bei einem Server, der Teil einer Domäne ist, wird die Benutzerkontodatenbank auf dem Server gespeichert, der der primäre Domänencontroller (PDC) ist. Ein eigenständiger Server speichert seine eigene lokale Benutzerkontodatenbank. Um den Namen des Servers abzurufen, auf dem die von einem angegebenen RAS-Server verwendete Benutzerkontodatenbank gespeichert wird, können Sie die [**MprAdminGetPDCServer-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) aufrufen. Sie können dann den Namen des Benutzerkontoservers in einem Aufruf der [**NetQueryDisplayInformation-Funktion**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) verwenden, um die Benutzer in einer Benutzerkontodatenbank aufzuzählen. Sie können den Servernamen auch in Aufrufen der Funktionen [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) und [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) verwenden, um die RAS-Berechtigungen für ein angegebenes Benutzerkonto abzurufen und festzulegen.

Die Funktionen [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) und [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) verwenden die [**RAS USER \_ \_ 0-Struktur,**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) um die RAS-Berechtigungen und die Rückruftelefonnummer eines Benutzers anzugeben. Die RAS-Berechtigungen geben die folgenden Informationen an:

-   Gibt an, ob der Benutzer eine Remoteverbindung mit dem Server oder der Domäne herstellen kann, zu der der Server gehört.
-   Gibt an, ob der Benutzer eine Verbindung über einen Rückruf herstellt, in dem der RAS-Server hängt und dann den Benutzer zurückruft, um die Verbindung herzustellen.

Jedes Benutzerkonto gibt eines der folgenden Flags an, um die Rückrufberechtigungen des Benutzers anzugeben.



| Wert                      | Bedeutung                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | Der RAS-Server ruft den Benutzer nicht zurück, um eine Verbindung herzustellen.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Wenn der Benutzer aufruft, hängt der RAS-Server auf und ruft eine voreingestellte Rückruftelefonnummer auf, die in der Benutzerkontodatenbank gespeichert ist. Das **szPhoneNumber-Element** der [**RAS USER \_ \_ 0-Struktur**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) enthält die Rückruftelefonnummer des Benutzers.                       |
| RASPRIV \_ CallerSetCallback | Wenn der Benutzer anruft, bietet der RAS-Server die Möglichkeit, eine Telefonnummer anzugeben, unter der der Benutzer zurückruft. Der Benutzer kann auch ohne Rückruf sofort eine Verbindung herstellen. Das **szPhoneNumber-Element** enthält eine Standardnummer, die der Benutzer überschreiben kann. |



 

 

 