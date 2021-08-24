---
title: Verbinden eines Erfassungsfensters mit einem Erfassungstreiber
description: Verbinden eines Erfassungsfensters mit einem Erfassungstreiber
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT Meldung
- capDriverConnect-Makro
- capGetDriverDescription-Funktion
- WM_CAP_DRIVER_GET_NAME Meldung
- capDriverGetName-Makro
- WM_CAP_DRIVER_GET_VERSION Meldung
- capDriverGetVersion-Makro
- WM_CAP_DRIVER_DISCONNECT Meldung
- capDriverDisconnect-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf74b5dc7cda0fdb73c8f9bd73f61de5ecefc157c20816c110d71e04bba6c196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144903"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Verbinden eines Erfassungsfensters mit einem Erfassungstreiber

Sie können ein Erfassungsfenster dynamisch mit einem Erfassungstreiber verbinden oder trennen. Sie können mithilfe der WM CAP DRIVER [**\_ \_ \_ CONNECT-Nachricht**](wm-cap-driver-connect.md) (oder des CapDriverConnect-Makros) eine Verbindung mit einem Erfassungstreiber herstellen oder einem [**Erfassungstreiber**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) zuordnen. Nachdem ein Erfassungsfenster und ein Erfassungstreiber verbunden wurden, können Sie gerätespezifische Nachrichten an den Erfassungstreiber senden, der einem Erfassungsfenster zugeordnet ist.

Wenn Sie mehr als ein Erfassungsgerät auf einem System installiert haben, können Sie ein Erfassungsfenster mit einem bestimmten Videoaufnahmegerätetreiber verbinden, indem Sie eine ganze Zahl für den *wParam-Parameter* der WM \_ CAP DRIVER \_ \_ CONNECT-Nachricht angeben. Die ganze Zahl ist ein Index, der einen video capture-Treiber identifiziert, der in der Registrierung oder im \[ \] Treiberabschnitt der SYSTEM.INI-Datei aufgeführt ist. Verwenden Sie 0 (null) für den ersten Indexeintrag.

Sie können den Namen und die Version eines installierten Erfassungstreibers mithilfe der [**capGetDriverDescription-Funktion**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) abrufen. Ihre Anwendung kann diese Funktion verwenden, um die installierten Erfassungsgeräte und Treiber aufzuzählen, sodass der Benutzer ein Erfassungsgerät auswählen kann, um eine Verbindung mit einem Erfassungsfenster herzustellen.

Sie können den Namen des Erfassungsgerätetreibers abrufen, der mit einem Erfassungsfenster verbunden ist, indem Sie die [**MELDUNG WM CAP DRIVER GET \_ \_ \_ \_ NAME**](wm-cap-driver-get-name.md) (oder das Makro [**capDriverGetName)**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) verwenden. Um die Version eines installierten Erfassungstreibers abzurufen, verwenden Sie die [**MELDUNG WM CAP DRIVER GET \_ \_ \_ \_ VERSION**](wm-cap-driver-get-version.md) (oder das Makro [**capDriverGetVersion).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion)

Sie können ein Erfassungsfenster mit einem Erfassungstreiber trennen, indem Sie die [**WM \_ CAP DRIVER \_ \_ DISCONNECT-Meldung**](wm-cap-driver-disconnect.md) (oder das [**CapDriverDisconnect-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) verwenden.

Wenn ein Aufzeichnungsfenster zerstört wird, werden alle verbundenen Gerätetreiber für die Videoaufzeichnung automatisch getrennt.

 

 




