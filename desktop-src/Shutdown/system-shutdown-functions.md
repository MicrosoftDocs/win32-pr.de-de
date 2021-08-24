---
description: Die folgenden Funktionen werden beim Herunterfahren des Systems verwendet.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funktionen zum Herunterfahren des Systems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664340"
---
# <a name="system-shutdown-functions"></a>Funktionen zum Herunterfahren des Systems

Die folgenden Funktionen werden beim Herunterfahren des Systems verwendet.



| Funktion                                                         | Beschreibung                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Beendet das Herunterfahren des Systems, das initiiert wurde.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Meldet den interaktiven Benutzer ab.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Meldet den interaktiven Benutzer ab, fährt das System herunter oder fährt das System herunter und startet es neu.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Initiiert das Herunterfahren und Neustarten des angegebenen Computers und startet alle Anwendungen neu, die für den Neustart registriert wurden.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Initiiert das Herunterfahren und den optionalen Neustart des angegebenen Computers.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Initiiert ein Herunterfahren und einen optionalen Neustart des angegebenen Computers und zeichnet optional den Grund für das Herunterfahren auf.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Sperrt die Anzeige der Arbeitsstation.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Gibt an, dass das System nicht heruntergefahren werden kann, und legt eine Ursachenzeichenfolge fest, die dem Benutzer angezeigt wird, wenn das Herunterfahren des Systems initiiert wird. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Gibt an, dass das System heruntergefahren werden kann, und gibt die Ursachenzeichenfolge frei.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Ruft die von der [**ShutdownBlockReasonCreate-Funktion**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) festgelegte Ursachenzeichenfolge ab.                     |



 

 

 



