---
title: Verbinden eines Aufzeichnungs Fensters mit einem Aufzeichnungs Treiber
description: Verbinden eines Aufzeichnungs Fensters mit einem Aufzeichnungs Treiber
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT Meldung
- capdriverconnect-Makro
- capgetdriverdescription-Funktion
- WM_CAP_DRIVER_GET_NAME Meldung
- capdrivergetname-Makro
- WM_CAP_DRIVER_GET_VERSION Meldung
- capdrivergetversion-Makro
- WM_CAP_DRIVER_DISCONNECT Meldung
- capdriverdisconnect-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710157"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Verbinden eines Aufzeichnungs Fensters mit einem Aufzeichnungs Treiber

Sie können ein Aufzeichnungs Fenster dynamisch verbinden oder mit einem Aufzeichnungs Treiber verbinden. Sie können ein Aufzeichnungs Fenster mithilfe der [**WM- \_ Cap-Treiber- \_ \_ Connect**](wm-cap-driver-connect.md) -Nachricht (oder dem [**capdriverconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) -Makro) mit einem Aufzeichnungs Treiber verbinden oder zuordnen. Nachdem ein Erfassungsfenster und ein Erfassungs Treiber verbunden sind, können Sie gerätespezifische Nachrichten an den mit einem Aufzeichnungs Fenster verknüpften Erfassungs Treiber senden.

Wenn Sie mehr als ein Erfassungsgerät auf einem System installiert haben, können Sie ein Aufzeichnungs Fenster mit einem bestimmten Gerätetreiber für die Video Erfassung verbinden, indem Sie eine ganze Zahl für den *wParam* -Parameter der WM- \_ Cap-Treiber- \_ \_ Verbindungs Nachricht angeben. Die ganze Zahl ist ein Index, der einen Video Erfassungs Treiber identifiziert, der in der Registrierung oder im \[ \] Abschnitt Drivers der SYSTEM.INI Datei aufgeführt ist. NULL für den ersten Index Eintrag verwenden.

Sie können den Namen und die Version eines installierten Erfassungs Treibers mithilfe der [**capgetdriverdescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) -Funktion abrufen. Die Anwendung kann diese Funktion zum Auflisten der installierten Erfassungsgeräte und Treiber verwenden, sodass der Benutzer ein Erfassungsgerät auswählen kann, um eine Verbindung mit einem Aufzeichnungs Fenster herzustellen.

Sie können den Namen des Erfassungsgeräte Treibers, der mit einem Aufzeichnungs Fenster verbunden ist, mit der " [**WM \_ Cap \_ Driver \_ get \_ Name**](wm-cap-driver-get-name.md) Message" (oder dem " [**capdrivergetname**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) "-Makro) abrufen. Um die Version eines installierten Erfassungs Treibers abzurufen, verwenden [**Sie die Version des WM- \_ Cap- \_ Treibers \_ get \_ Version**](wm-cap-driver-get-version.md) (oder das " [**capdrivergetversion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) "-Makro).

Sie können ein Erfassungsfenster von einem Aufzeichnungs Treiber trennen, indem Sie die " [**WM \_ Cap \_ Driver \_ Disconnect**](wm-cap-driver-disconnect.md) "-Nachricht (oder das " [**capdriverdisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) "-Makro) verwenden.

Wenn ein Erfassungsfenster zerstört wird, werden alle angeschlossenen Gerätetreiber für die Geräte Erfassung automatisch getrennt.

 

 




