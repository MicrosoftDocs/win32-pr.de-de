---
title: Dateiname erfassen
description: Dateiname erfassen
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE Meldung
- capfilesetcapturefile-Makro
- WM_CAP_FILE_GET_CAPTURE_FILE Meldung
- capfilegetcapturefile-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342269"
---
# <a name="capture-filename"></a>Dateiname erfassen

Avicap leitet standardmäßig Video-und audiostreamdaten aus einem Erfassungsfenster in eine Datei mit dem Namen CAPTURE.AVI im Stammverzeichnis des aktuellen Laufwerks. Sie können einen alternativen Dateinamen angeben, indem Sie die [**\_ \_ Datei \_ Set \_ Capture \_**](wm-cap-file-set-capture-file.md) -Datei für die WM-Abdeckung (oder das Makro [**capfilesetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) an ein Aufzeichnungs Fenster senden. Diese Meldung gibt den Dateinamen an. die Datei wird nicht erstellt, neu erstellt oder geöffnet. Sie können den aktuellen Aufzeichnungs Dateinamen abrufen, indem Sie die [**WM- \_ Cap-Datei " \_ \_ get \_ Capture \_ File**](wm-cap-file-get-capture-file.md) " (oder das Makro " [**capfilegetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ") an ein Erfassungsfenster senden.

 

 




