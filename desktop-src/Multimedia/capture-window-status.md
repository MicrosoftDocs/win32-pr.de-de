---
title: Status des Erfassungsfensters
description: Status des Erfassungsfensters
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS-Nachricht
- capGetStatus-Makro
- CAPSTATUS-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 367d35c3869adb6f4e960fa472e0cd6a22483c37fa981e886b3a78f0b7410029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375286"
---
# <a name="capture-window-status"></a>Status des Erfassungsfensters

Sie können den aktuellen Status eines Erfassungsfensters abrufen, indem Sie die [**WM \_ CAP GET \_ \_ STATUS-Meldung**](wm-cap-get-status.md) (oder das [**Makro capGetStatus)**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) verwenden. Diese Meldung ruft eine Kopie der [**CAPSTATUS-Struktur**](/windows/win32/api/vfw/ns-vfw-capstatus) mit den aktuellen Werten ihrer Member ab. Die **CAPSTATUS-Struktur** enthält Informationen über die Abmessungen des Bilds, die Scrollposition und darüber, ob die Überlagerung oder Vorschau des Bilds aktiviert ist. Da die in **CAPSTATUS** dargestellten Informationen dynamisch sind, sollte Ihre Anwendung den Inhalt der Struktur aktualisieren, wenn sich die Größe oder das Format des aufgezeichneten Videostreams geändert hat (z. B. nach dem Anzeigen des Videoformats des Erfassungstreibers).

Das Ändern der Dimensionen des Erfassungsfensters hat keine Auswirkungen auf die Dimensionen des tatsächlich erfassten Videostreams. Das Formatdialogfeld, das vom Gerätetreiber für die Videoaufzeichnung angezeigt wird, steuert die Abmessungen des erfassten Videostreams.

 

 




