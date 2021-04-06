---
title: Video Puffer
description: Video Puffer
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712582"
---
# <a name="video-buffers"></a>Video Puffer

Die mit der Video Erfassung verwendeten Puffer befinden sich im Arbeitsspeicher Heap. Die Anzahl von Puffern, die bei einem Aufzeichnungs Vorgang verwendet werden, kann variieren und hängt vom Wert des **wnumvideorequused** -Members der [**captuprojektmappenstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) und des verfügbaren System Speichers ab.

Sie können den aktuellen Wert der angeforderten Video Puffer abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden. Die aktuell angeforderte Anzahl von Video Puffern wird im **wnumvideorequtzig** -Member der **captuprojektstruktur** -Struktur gespeichert. Sie können die Platzierung und die Anzahl der Puffer anfordern, indem Sie dieses Element aktualisieren, und dann die aktualisierte **captuprojektmappenstruktur** [**mithilfe der**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Setup-Nachricht der [**WM-Cap-Set- \_ \_ \_ Sequenz \_**](wm-cap-set-sequence-setup.md) an das Aufzeichnungs Fenster senden.

 

 




