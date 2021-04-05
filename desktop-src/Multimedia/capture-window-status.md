---
title: Status des Aufzeichnungs Fensters
description: Status des Aufzeichnungs Fensters
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS Meldung
- capgetstatus-Makro
- Capstatus-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037356"
---
# <a name="capture-window-status"></a>Status des Aufzeichnungs Fensters

Sie können den aktuellen Status eines Aufzeichnungs Fensters abrufen, indem Sie die [**\_ \_ \_ Status**](wm-cap-get-status.md) Meldung "WM-Abdeckung abrufen" (oder das " [**capgetstatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) "-Makro) verwenden. Diese Meldung Ruft eine Kopie der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur mit den aktuellen Werten der zugehörigen Member ab. Die **capstatus** -Struktur enthält Informationen über die Abmessungen des Bilds, die Scrollposition und ob die Überlagerung oder die Vorschau des Bilds aktiviert ist. Da die in **capstatus** dargestellten Informationen dynamisch sind, sollte Ihre Anwendung den Inhalt der Struktur immer dann aktualisieren, wenn sich die Größe oder das Format des aufgezeichneten Videostreams geändert hat (z. b. nach dem Anzeigen des Video Formats des Aufzeichnungs Treibers).

Das Ändern der Abmessungen des Aufzeichnungs Fensters wirkt sich nicht auf die Dimensionen des tatsächlich aufgezeichneten Videostreams aus. Im Dialogfeld Format, das vom Gerätetreiber für die Video Erfassung angezeigt wird, werden die Dimensionen des aufgezeichneten Videostreams gesteuert.

 

 




