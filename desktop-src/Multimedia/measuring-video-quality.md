---
title: Messen der Video Qualität
description: Messen der Video Qualität
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036888"
---
# <a name="measuring-video-quality"></a>Messen der Video Qualität

Eine Möglichkeit zum Messen der Videoqualität besteht darin, die Anzahl der aufgezeichneten Frames einzuschränken, die während des Aufzeichnungs Vorgangs verworfen wurden. Wenn die streamingerfassung abgeschlossen ist, wird der Qualitäts Wert mit dem Verhältnis der verworfenen Frames zu den Gesamtrahmen verglichen. Wenn der Prozentsatz der gelöschten Frames größer ist als der Wert des **wprozdropforerror** -Members der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) , sendet avicap bei der Installation eine Fehlermeldung an die Fehler Rückruffunktion.

Sie können das aktuelle Limit von gelöschten Frames (ausgedrückt als Prozentsatz) mithilfe der [**\_ \_ get \_ Sequence- \_ Setup**](wm-cap-get-sequence-setup.md) Nachricht der WM-Abdeckung abrufen (oder das-Makro [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Sie können eine neue Grenze festlegen, indem Sie einen Prozentwert als Wert des **wprozentudropforerror** -Members der **captuprojektstruktur** angeben und dann die aktualisierte Struktur mithilfe der [**\_ \_ \_ \_ Setup**](wm-cap-set-sequence-setup.md) -Nachricht für die WM-Abdeckung (oder das [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) an das Aufzeichnungs Fenster senden. Der Standardwert von **wprozdropforerror** ist 10 Prozent.

 

 




