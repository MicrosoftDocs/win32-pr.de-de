---
description: VMR-Betriebsmodi
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: VMR-Betriebsmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e7a1fa378ff781a712f71c877c32991cf19683a81daa10ff9b2fbbea40e7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049370"
---
# <a name="vmr-modes-of-operation"></a>VMR-Betriebsmodi

Die Komponentenarchitektur der VMR ermöglicht Es Anwendungen, sie auf verschiedene Weise zu konfigurieren, je nachdem, wie das Rendering durchgeführt werden soll. Die folgende Tabelle zeigt die drei Präsentationsmodi und die beiden Mischungsmodi sowie die Komponenten, die für jede Konfiguration vorhanden sind.



| Mode       | Einzelner Stream                                                                     | Mehrere Streams (Gemischter Modus)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Fenstermodus   | Allocator-presenterCore Synchronization Unit<br/> Fenster-Manager<br/> | MixerCompositor\*<br/> Allocator-Presenter<br/> Kernsynchronisierungseinheit<br/> Fenster-Manager<br/> |
| Fensterlosen | Allocator-presenterCore Synchronization Unit<br/>                           | MixerCompositor\*<br/> Allocator-Presenter<br/> Kernsynchronisierungseinheit<br/>                           |
| Renderlos | Allocator-Presenter (von Anwendung bereitgestellt)Core Synchronization Unit<br/> | MixerCompositor\*<br/> Allocator-Presenter (bereitgestellt von der Anwendung)<br/> Kernsynchronisierungseinheit<br/> |



 

\* Gibt an, dass die Anwendung über die Option verfügt, eine benutzerdefinierte Komponente bereitzustellen oder die Standardkomponente zu verwenden.

In allen Konfigurationen ist der wichtigste Punkt, den Sie beim Erstellen von Filterdiagrammen mit der VMR beachten sollten, dass Sie die VMR konfigurieren müssen, bevor Sie eine Verbindung herstellen.

Für alle Konfigurationen können Pins nicht dynamisch hinzugefügt oder entfernt werden, nachdem die VMR mit dem Upstreamfilter verbunden wurde, aber sie können verbunden und getrennt werden. Wenn die Anwendung nicht sicher ist, wie viele Pins benötigt werden, sollte sie die VMR für die maximal erforderliche Anzahl konfigurieren. Das Vorhandensein von nicht verwendeten Eingabepins im Filter beeinträchtigt nicht die Renderingleistung. Im Gegensatz zum alten Overlay-Mixer verfügt die VMR über keinen Ausgabepin, da kein separater Filter für die Fensterverwaltung erforderlich ist.

In den folgenden Abschnitten wird beschrieben, wie Sie die VMR für einen bestimmten Modus konfigurieren:

-   [VMR-Fenstermodus (Kompatibilität)](vmr-windowed--compatibility--mode.md)
-   [VMR-Modus ohne Fenster](vmr-windowless-mode.md)
-   [VMR mit mehreren Streams (Gemischter Modus)](vmr-with-multiple-streams--mixing-mode.md)
-   [YUV-Gemischtmodus](yuv-mixing-mode.md)
-   [Positionieren und Verschieben von Videorechtecke im Kompositionsbereich](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [VMR Renderless Playback Mode (Custom Allocator-Presenters)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Exklusiver DirectDraw-Modus](directdraw-exclusive-mode.md)

 

 




