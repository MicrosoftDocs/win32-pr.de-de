---
title: Funktionen für die Anwendungs Wiederherstellung und Neustart
description: 'Anwendungs Wiederherstellung und Neustart definiert die folgenden Funktionen:'
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102035"
---
# <a name="application-recovery-and-restart-functions"></a>Funktionen für die Anwendungs Wiederherstellung und Neustart

Anwendungs Wiederherstellung und Neustart definiert die folgenden Funktionen:



| Funktion                                                                               | BESCHREIBUNG                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Applicationwiederherstellungsfertig**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Gibt an, dass die aufrufenden Anwendung die Datenwiederherstellung abgeschlossen hat.                    |
| [**Applicationwiederherstellungsinprogress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Gibt an, dass die aufrufende Anwendung weiterhin Daten wieder hergestellt.                      |
| [**Getapplicationwiederherstellungsrückruf**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Ruft einen Zeiger auf die Wiederherstellungs Rückruf Routine ab, die für den angegebenen Prozess registriert ist. |
| [**Getapplicationrestartsettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Ruft die für den angegebenen Prozess registrierten Neustart Informationen ab.                    |
| [**Registerapplicationwiederherstellungsrückruf**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registriert die aktive Instanz einer Anwendung für die Wiederherstellung.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registriert die aktive Instanz einer Anwendung für den Neustart.                               |
| [**Unregisterapplicationwiederherstellungsrückruf**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Entfernt die aktive Instanz einer Anwendung aus der Wiederherstellungs Liste.                      |
| [**Unregisterapplicationrestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Entfernt die aktive Instanz einer Anwendung aus der Neustart Liste.                       |



 

 

 