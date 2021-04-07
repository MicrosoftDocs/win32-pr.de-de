---
title: Fenster Station-und Desktop Funktionen
description: Anwendungen können die folgenden Funktionen mit Fenster Station-Objekten verwenden.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6665f52de1f7f57930105edb0063c4512e375ac3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727353"
---
# <a name="window-station-and-desktop-functions"></a>Fenster Station-und Desktop Funktionen

Anwendungen können die folgenden Funktionen mit [Fenster Station](window-stations.md) -Objekten verwenden.



| Funktion                                                     | BESCHREIBUNG                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Closewindowstation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Schließt ein geöffnetes Fenster Station-handle.                                                                           |
| [**"Up Windows Station"**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Erstellt ein Fenster Station-Objekt, ordnet es dem aktuellen Prozess zu und weist es der aktuellen Sitzung zu. |
| [**Aufgelisteten Stationen**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Listet alle Fenster Stationen in der aktuellen Sitzung auf.                                                          |
| [**Getprocesswindowstation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Ruft ein Handle für die aktuelle Fenster Station für den aufrufenden Prozess ab.                                       |
| [**Getuserobjectinformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Ruft Informationen über die angegebene Fenster Station oder das angegebene Desktop Objekt ab.                                     |
| [**Getuserobjectsecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Ruft Sicherheitsinformationen für die angegebene Fenster Station oder das angegebene Desktop Objekt ab.                              |
| [**Openwindowstation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Öffnet die angegebene Fenster Station.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Weist dem aufrufenden Prozess die angegebene Fenster Station zu.                                                    |
| [**Setuserobjectinformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Legt Informationen über die angegebene Fenster Station oder das angegebene Desktop Objekt fest.                                          |
| [**Setuserobjectsecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Legt Sicherheitsinformationen für die angegebene Fenster Station oder das angegebene Desktop Objekt fest.                                   |



 

Anwendungen können die folgenden Funktionen mit [Desktop](desktops.md) Objekten verwenden.



| Funktion                                                     | BESCHREIBUNG                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Closedesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Schließt ein geöffnetes Handle für ein Desktop Objekt.                                                                                         |
| [**Mit dem Desktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Erstellt einen neuen Desktop, ordnet ihn der aktuellen Fenster Station des aufrufenden Prozesses zu und weist ihn dem aufrufenden Thread zu. |
| [**"Kreatedesktopex"**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Erstellt einen neuen Desktop, ordnet ihn der aktuellen Fenster Station des aufrufenden Prozesses zu und weist ihn dem aufrufenden Thread zu. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Listet alle Desktops auf, die der aktuellen Fenster Station des aufrufenden Prozesses zugeordnet sind.                                         |
| [**Enumdesktopwindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Listet alle Fenster der obersten Ebene auf, die dem angegebenen Desktop zugeordnet sind.                                                            |
| [**Getthreaddesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Ruft ein Handle für den Desktop ab, der dem angegebenen Thread zugewiesen ist.                                                                |
| [**Getuserobjectinformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Ruft Informationen zu einer Fenster Station oder einem Desktop Objekt ab.                                                                         |
| [**Getuserobjectsecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Ruft Sicherheitsinformationen für eine Fenster Station oder ein Desktop Objekt ab.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Öffnet das angegebene Desktop Objekt.                                                                                                |
| [**Openinputdesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Öffnet den Desktop, der Benutzereingaben empfängt.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Weist den angegebenen Desktop dem aufrufenden Thread zu.                                                                               |
| [**Setuserobjectinformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Legt Informationen zu einer Fenster Station oder einem Desktop Objekt fest.                                                                         |
| [**Setuserobjectsecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Legt Sicherheitsinformationen für eine Fenster Station oder ein Desktop Objekt fest.                                                                  |
| [**Switchdesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Macht einen Desktop sichtbar und aktiviert ihn. Dadurch kann der Desktop Eingaben vom Benutzer empfangen.                                 |



 

 

 