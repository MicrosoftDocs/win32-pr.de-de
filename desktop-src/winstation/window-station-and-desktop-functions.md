---
title: Window Station and Desktop Functions
description: Anwendungen können die folgenden Funktionen mit Fensterstationsobjekten verwenden.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccda67841508081444f7025e457c9a778195b99d0ab67ebb585362d7a3b22cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810400"
---
# <a name="window-station-and-desktop-functions"></a>Window Station and Desktop Functions

Anwendungen können die folgenden Funktionen mit [Fensterstationsobjekten](window-stations.md) verwenden.



| Funktion                                                     | Beschreibung                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Schließt ein geöffnetes Fensterstationshandle.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Erstellt ein Fensterstationsobjekt, ordnet es dem aktuellen Prozess zu und weist es der aktuellen Sitzung zu. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Listet alle Fensterstationen in der aktuellen Sitzung auf.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Ruft ein Handle für die aktuelle Fensterstation für den aufrufenden Prozess ab.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Ruft Informationen über die angegebene Fensterstation oder das angegebene Desktopobjekt ab.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Ruft Sicherheitsinformationen für die angegebene Fensterstation oder das angegebene Desktopobjekt ab.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Öffnet die angegebene Fensterstation.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Weist dem aufrufenden Prozess die angegebene Fensterstation zu.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Legt Informationen über die angegebene Fensterstation oder das angegebene Desktopobjekt fest.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Legt Sicherheitsinformationen für die angegebene Fensterstation oder das angegebene Desktopobjekt fest.                                   |



 

Anwendungen können die folgenden Funktionen mit [Desktopobjekten](desktops.md) verwenden.



| Funktion                                                     | Beschreibung                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Schließt ein geöffnetes Handle für ein Desktopobjekt.                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Erstellt einen neuen Desktop, ordnet ihn der aktuellen Fensterstation des aufrufenden Prozesses zu und weist ihn dem aufrufenden Thread zu. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Erstellt einen neuen Desktop, ordnet ihn der aktuellen Fensterstation des aufrufenden Prozesses zu und weist ihn dem aufrufenden Thread zu. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Listet alle Desktops auf, die der aktuellen Fensterstation des aufrufenden Prozesses zugeordnet sind.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Listet alle Fenster der obersten Ebene auf, die dem angegebenen Desktop zugeordnet sind.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Ruft ein Handle für den Desktop ab, der dem angegebenen Thread zugewiesen ist.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Ruft Informationen zu einer Fensterstation oder einem Desktopobjekt ab.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Ruft Sicherheitsinformationen für eine Fensterstation oder ein Desktopobjekt ab.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Öffnet das angegebene Desktopobjekt.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Öffnet den Desktop, der Benutzereingaben empfängt.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Weist dem aufrufenden Thread den angegebenen Desktop zu.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Legt Informationen zu einer Fensterstation oder einem Desktopobjekt fest.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Legt Sicherheitsinformationen für eine Fensterstation oder ein Desktopobjekt fest.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Macht einen Desktop sichtbar und aktiviert ihn. Dadurch kann der Desktop Eingaben vom Benutzer empfangen.                                 |



 

 

 