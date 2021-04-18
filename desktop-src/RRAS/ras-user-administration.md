---
title: RAS-Benutzerverwaltung
description: Ein RAS-Server verwendet eine Benutzerkonten Datenbank, die Informationen zu einem Satz von Benutzerkonten enthält.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- RAS-Verwaltung-RRAS, Benutzerverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3e357ef813a60c67f991b6e5829879d3e1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337460"
---
# <a name="ras-user-administration"></a>RAS-Benutzerverwaltung

Ein RAS-Server verwendet eine Benutzerkonten Datenbank, die Informationen zu einem Satz von Benutzerkonten enthält. Die Informationen beinhalten die RAS-Berechtigungen eines Benutzers, bei denen es sich um einen Satz von Bitflags handelt, die bestimmen, wie der RAS-Server reagiert, wenn der Benutzer eine Verbindung aufruft. Die RAS-Server-Verwaltungsfunktionen suchen die Benutzerkonten Datenbank und erhalten und legen die RAS-Berechtigungen für Benutzerkonten fest.

Ein RAS-Server kann Teil einer Betriebssystem Domäne sein, oder es kann sich um einen eigenständigen Computer handeln, auf dem die Server-oder Professional-Version des Betriebssystems ausgeführt wird. Bei einem Server, der Teil einer Domäne ist, wird die Datenbank des Benutzerkontos auf dem Server gespeichert, der als primärer Domänen Controller (PDC) verwendet wird. Ein eigenständiger Server speichert seine eigene lokale Benutzerkonten Datenbank. Zum Abrufen des Namens des Servers, auf dem die Benutzerkonten Datenbank gespeichert ist, die von einem angegebenen RAS-Server verwendet wird, können Sie die [**mpradmingetpdcserver**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) -Funktion aufrufen. Anschließend können Sie den Namen des Benutzerkonto Servers in einem aufzurufenden Befehl der [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) -Funktion verwenden, um die Benutzer in einer Benutzerkonten Datenbank aufzulisten. Sie können auch den Servernamen in Aufrufen der [**mpradminusergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) -und [**mpradminusersetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) -Funktionen verwenden, um die RAS-Berechtigungen für ein bestimmtes Benutzerkonto zu erhalten und festzulegen.

Die [**mpradminusergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) -und [**mpradminuserminfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) -Funktionen verwenden die [**RAS-Benutzer- \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) -Struktur, um die RAS-Berechtigungen und die Rückruf Telefonnummer eines Benutzers anzugeben. Die RAS-Berechtigungen geben die folgenden Informationen an:

-   Gibt an, ob der Benutzer eine Remote Verbindung mit dem Server oder der Domäne herstellen kann, zu der der Server gehört.
-   Gibt an, ob der Benutzer über einen Rückruf eine Verbindung herstellt, in der der RAS-Server nicht mehr aktiv ist, und ruft dann den Benutzer zum Herstellen der Verbindung zurück.

Jedes Benutzerkonto gibt eines der folgenden Flags an, um die Rückruf Berechtigungen des Benutzers anzugeben.



| Wert                      | Bedeutung                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Raspriv \_ NoCallback        | Der RAS-Server Ruft den Benutzer nicht zurück, um eine Verbindung herzustellen.                                                                                                                                                                                                          |
| Raspriv \_ adminsetcallback  | Wenn der Benutzer aufruft, reagiert der RAS-Server und ruft eine voreingestellte Telefonnummer auf, die in der Benutzerkonten Datenbank gespeichert ist. Der **szphonenumber** -Member der [**RAS- \_ Benutzer- \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) -Struktur enthält die Rückruf Telefonnummer des Benutzers.                       |
| Raspriv \_ callersetcallback | Wenn der Benutzer aufruft, bietet der RAS-Server die Möglichkeit, eine Telefonnummer anzugeben, bei der der Benutzer aufgerufen werden soll. Der Benutzer kann auch ohne Rückrufe sofort eine Verbindung herstellen. Der **szphonenumber** -Member enthält eine Standardzahl, die der Benutzer überschreiben kann. |



 

 

 