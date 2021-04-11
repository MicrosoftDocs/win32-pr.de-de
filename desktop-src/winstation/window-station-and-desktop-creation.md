---
title: Fenster Station und Desktop Erstellung
description: Das System erstellt automatisch die interaktive Fenster Station.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315141"
---
# <a name="window-station-and-desktop-creation"></a>Fenster Station und Desktop Erstellung

Das System erstellt automatisch die interaktive Fenster Station. Wenn sich ein interaktiver Benutzer anmeldet, ordnet das System die interaktive Fenster Station der Benutzer Anmelde Sitzung zu. Das System erstellt außerdem den standardmäßigen Eingabe Desktop für die interaktive Fenster Station (Winsta0 \\ Standard). Prozesse, die vom angemeldeten Benutzer gestartet wurden, werden dem Winsta0 \\ -Standard Desktop zugeordnet.

Ein Prozess kann mit der Funktion "Funktion erstellen" eine neue Fenster Station erstellen, und mit [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) up **Desktop** " oder " [**kreatedesktopex**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) " können Sie einen neuen Desktop erstellen. Die Anzahl der Desktops, die erstellt werden können, ist durch die Größe des System Desktop Heaps beschränkt. Weitere Informationen finden Sie unter " [**kreatedesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)".

Wenn ein nicht interaktiver Prozess (z. b. eine Dienst Anwendung) versucht, eine Verbindung mit einer Fenster Station herzustellen, und keine Fenster Station für die Prozess Anmelde Sitzung vorhanden ist, versucht das System, eine Fenster Station und einen Desktop für die Sitzung zu erstellen. Der Name der erstellten Fenster Station basiert auf dem Anmelde Sitzungs Bezeichner, und der Desktop hat den Namen Default, wie hier beschrieben:

-   Wenn ein Dienst im Sicherheitskontext des Kontos "LocalSystem" ausgeführt wird, aber nicht das interaktive Prozess Attribut des Diensts enthält \_ \_ , werden die folgende Fenster Station und der Desktop verwendet: Service-0x0-3e7 $ \\ default. Diese Fenster Station ist nicht interaktiv, sodass der Dienst keine Benutzeroberfläche anzeigen kann. Außerdem können vom Dienst erstellte Prozesse keine Benutzeroberfläche anzeigen.
-   Wenn der Dienst im Sicherheitskontext eines Benutzerkontos ausgeführt wird, basiert der Name der Fenster Station auf der Benutzer-SID-Dienst-0x *Z1* - *Z2*$, wobei " *Z1* " der hohe Teil der Anmelde-SID und " *Z2* " der niedrige Teil der Anmelde-SID ist. Da eine sid für die Anmelde Sitzung eindeutig ist, erhalten zwei Dienste, die im selben Sicherheitskontext ausgeführt werden, eindeutige Fenster Stationen. Diese Fenster Stationen sind nicht interaktiv.

Die freigegebene Zugriffs Steuerungs Liste (DACL) für die Fenster Station und den Desktop umfasst die folgenden Zugriffsrechte für das Benutzerkonto des dienstanweises:

Fenster Station:

<dl> winsta \_ accessclipboard  
winsta \_ accessglobalatome  
winsta \_ -up-Desktop  
winsta- \_ exitwindows  
winsta- \_ Eigenschaften  
Standard \_ Rechte \_ erforderlich  
</dl>

Desktop:

<dl> desktopingdesktop \_  
Desktop- \_ kreatewindow  
Desktop \_ Aufzählung  
Desktop- \_ Hostingsteuerelement  
Desktop-Schreib \_ Objekte  
Desktop-Schreib \_ Objekte  
Standard \_ Rechte \_ erforderlich  
</dl>

 

 