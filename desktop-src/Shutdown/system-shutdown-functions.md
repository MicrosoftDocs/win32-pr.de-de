---
description: Die folgenden Funktionen werden mit dem Herunterfahren des Systems verwendet.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: SystemShutdown-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959856"
---
# <a name="system-shutdown-functions"></a>SystemShutdown-Funktionen

Die folgenden Funktionen werden mit dem Herunterfahren des Systems verwendet.



| Funktion                                                         | BESCHREIBUNG                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Abortsystemshutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Beendet das Herunterfahren eines Systems, das initiiert wurde.                                                                                    |
| [**Exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Protokolliert den interaktiven Benutzer.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Hiermit wird der interaktive Benutzer protokolliert, das System heruntergefahren oder das System heruntergefahren und neu gestartet.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Initiiert das Herunterfahren und Neustarten des angegebenen Computers und startet alle Anwendungen neu, die für den Neustart registriert wurden.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Initiiert ein Herunterfahren und einen optionalen Neustart des angegebenen Computers.                                                                |
| [**Initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Initiiert ein Herunterfahren und einen optionalen Neustart des angegebenen Computers und zeichnet optional den Grund für das Herunterfahren auf.            |
| [**Lock Workstation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Sperrt die Anzeige der Arbeitsstation.                                                                                                    |
| [**Shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Gibt an, dass das System nicht heruntergefahren werden kann, und legt eine Grund Zeichenfolge fest, die dem Benutzer angezeigt wird, wenn das System heruntergefahren wird. |
| [**Shutdownblockreasondestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Gibt an, dass das System heruntergefahren werden kann, und gibt die Grund Zeichenfolge frei.                                                             |
| [**Shutdownblockreasonquery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Ruft die von der [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) -Funktion festgelegte Grund Zeichenfolge ab.                     |



 

 

 



