---
title: Dateiname erfassen
description: Dateiname erfassen
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE Meldung
- capFileSetCaptureFile-Makro
- WM_CAP_FILE_GET_CAPTURE_FILE Meldung
- capFileGetCaptureFile-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941595"
---
# <a name="capture-filename"></a>Dateiname erfassen

AVICap leitet standardmäßig Video- und Audiostreamdaten aus einem Erfassungsfenster an eine Datei mit dem Namen CAPTURE.AVI im Stammverzeichnis des aktuellen Laufwerks weiter. Sie können einen alternativen Dateinamen angeben, indem Sie die [**WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE-Nachricht**](wm-cap-file-set-capture-file.md) (oder das [**CapFileSetCaptureFile-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) an ein Erfassungsfenster senden. Diese Meldung gibt den Dateinamen an. Die Datei wird nicht erstellt, zugeordnet oder geöffnet. Sie können den aktuellen Erfassungsdateinamen abrufen, indem Sie die [**WM CAP FILE GET CAPTURE \_ \_ \_ \_ \_ FILE-Nachricht**](wm-cap-file-get-capture-file.md) (oder das [**CapFileGetCaptureFile-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) an ein Erfassungsfenster senden.

 

 




