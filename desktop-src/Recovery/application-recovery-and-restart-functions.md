---
title: Anwendungswiederherstellungs- und Neustartfunktionen
description: Anwendungswiederherstellung und Neustart definiert die folgenden Funktionen.
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024620"
---
# <a name="application-recovery-and-restart-functions"></a>Anwendungswiederherstellungs- und Neustartfunktionen

Anwendungswiederherstellung und Neustart definieren die folgenden Funktionen:



| Funktion                                                                               | BESCHREIBUNG                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Gibt an, dass die aufrufende Anwendung die Datenwiederherstellung abgeschlossen hat.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Gibt an, dass die aufrufende Anwendung weiterhin Daten wiederherstellt.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Ruft einen Zeiger auf die Für den angegebenen Prozess registrierte Wiederherstellungsrückrufroutine ab. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Ruft die für den angegebenen Prozess registrierten Neustartinformationen ab.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registriert die aktive Instanz einer Anwendung für die Wiederherstellung.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registriert die aktive Instanz einer Anwendung für den Neustart.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Entfernt die aktive Instanz einer Anwendung aus der Wiederherstellungsliste.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Entfernt die aktive Instanz einer Anwendung aus der Neustartliste.                       |



 

 

 