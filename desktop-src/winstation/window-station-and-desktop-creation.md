---
title: Fensterstation und Desktoperstellung
description: Das System erstellt automatisch die interaktive Fensterstation.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52a3cc85a3194bea6c8eaea00a7ce794901426e794c962e1b23713561f8fc744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030516"
---
# <a name="window-station-and-desktop-creation"></a>Fensterstation und Desktoperstellung

Das System erstellt automatisch die interaktive Fensterstation. Wenn sich ein interaktiver Benutzer anmeldet, ordnet das System die interaktive Fensterstation der Benutzeranmeldungssitzung zu. Das System erstellt auch den Standardeingabedesktop für die interaktive Fensterstation (Winsta0-Standard). \\ Prozesse, die vom angemeldeten Benutzer gestartet werden, sind dem \\ Winsta0-Standarddesktop zugeordnet.

Ein Prozess kann die [**CreateWindowStation-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) verwenden, um eine neue Fensterstation zu erstellen, und die **CreateDesktop-** oder [**CreateDesktopEx-Funktion,**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) um einen neuen Desktop zu erstellen. Die Anzahl der Desktops, die erstellt werden können, wird durch die Größe des Systemdesktop-Heaps beschränkt. Weitere Informationen finden Sie unter [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).

Wenn ein nicht inaktiver Prozess wie eine Dienstanwendung versucht, eine Verbindung mit einer Fensterstation herzustellen, und keine Fensterstation für die Prozessanmeldungssitzung vorhanden ist, versucht das System, eine Fensterstation und einen Desktop für die Sitzung zu erstellen. Der Name der erstellten Fensterstation basiert auf dem Anmeldesitzungsbezeichner, und der Desktop hat den Namen default, wie hier beschrieben:

-   Wenn ein Dienst im Sicherheitskontext des LocalSystem-Kontos ausgeführt wird, aber nicht das ATTRIBUT SERVICE INTERACTIVE PROCESS enthält, verwendet er die folgende Fensterstation und den folgenden \_ \_ Desktop: Service-0x0-3e7$ \\ default. Diese Fensterstation ist nicht interaktiv, sodass der Dienst keine Benutzeroberfläche anzeigen kann. Darüber hinaus können vom Dienst erstellte Prozesse keine Benutzeroberfläche anzeigen.
-   Wenn der Dienst im Sicherheitskontext eines Benutzerkontos ausgeführt wird, basiert der Name der Fensterstation auf der Benutzer-SID Service-0x *Z1* - *Z2*$, wobei *Z1* der hohe Teil der Anmelde-SID und *Z2* der untere Teil der Anmelde-SID ist. Da eine SID für die Anmeldesitzung eindeutig ist, erhalten zwei Dienste, die im gleichen Sicherheitskontext ausgeführt werden, eindeutige Fensterstationen. Diese Fensterstationen sind nicht interaktiv.

Die DACL (Discretionary Access Control List) für die Fensterstation und den Desktop umfasst die folgenden Zugriffsrechte für das Benutzerkonto des Diensts:

Fensterstation:

<dl> WINSTA \_ ACCESSCLIPBOARD  
WINSTA \_ ACCESSGLOBALATOMS  
WINSTA \_ CREATEDESKTOP  
WINSTA \_ EXITWINDOWS  
WINSTA \_ READATTRIBUTES  
STANDARDRECHTE \_ \_ ERFORDERLICH  
</dl>

Desktop:

<dl> DESKTOP \_ CREATEMENU  
DESKTOP \_ CREATEWINDOW  
DESKTOP \_ ENUMERATE  
DESKTOP \_ HOOKCONTROL  
DESKTOP \_ READOBJECTS  
DESKTOP \_ WRITEOBJECTS  
STANDARDRECHTE \_ \_ ERFORDERLICH  
</dl>

 

 