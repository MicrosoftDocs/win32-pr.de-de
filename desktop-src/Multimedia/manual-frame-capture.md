---
title: Manuelle Frame Erfassung
description: Manuelle Frame Erfassung
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN Meldung
- WM_CAP_SINGLE_FRAME Meldung
- WM_CAP_SINGLE_FRAME_CLOSE Meldung
- capcapturesingleframeopen-Makro
- capcapturesingleframe-Makro
- capcapturesingleframeclose-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855867"
---
# <a name="manual-frame-capture"></a>Manuelle Frame Erfassung

Wenn Sie die zu erfassenden Frames einzeln in einem Videostream angeben möchten, können Sie die Reihenfolge steuern, indem Sie die Makros zum Schließen eines einzelnen Frames vom Typ " [**WM \_ \_ \_ \_**](wm-cap-single-frame-open.md)", " [**WM \_ Cap \_ \_**](wm-cap-single-frame.md)Single Frame" und " [**WM Cap Single Frame \_ \_ \_ \_ Close**](wm-cap-single-frame-close.md) " (oder die Makros [**capcapturesingleframeopen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capcapturesingleframe**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)und [**capcapturesingleframeclose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ) verwenden. In der Regel werden diese Nachrichten verwendet, um eine Animation zu erstellen, indem einzelne Frames an die Erfassungs Datei angehängt werden. WM-Abdeckung \_ \_ Single \_ Frame \_ Open öffnet eine Datei für einen manuell betriebenen Aufzeichnungs Vorgang. Der \_ \_ einzelne \_ Rahmen der WM-Abdeckung erfasst einen einzelnen Frame und fügt ihn an die Erfassungs Datei an. WM \_ - \_ Cap \_ : einzelner Frame \_ schließt die Datei, die für die manuelle Frame Erfassung verwendet wird.

> [!Note]  
> Diese Aufzeichnungsmethode unterstützt keine gleichzeitige Audioerfassung mit Video Erfassung.

 

 

 




