---
description: VMR-Betriebsmodi
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: VMR-Betriebsmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353170"
---
# <a name="vmr-modes-of-operation"></a>VMR-Betriebsmodi

Die Komponentenarchitektur von VMR ermöglicht es Anwendungen, diese auf verschiedene Weise zu konfigurieren, je nachdem, wie das Rendering durchgeführt werden soll. In der folgenden Tabelle werden die drei präsentationsmodi und die beiden-Mischungs Modi und die Komponenten aufgeführt, die für die einzelnen Konfigurationen vorhanden sind.



| Mode       | Einzelner Stream                                                                     | Mehrere Streams (Mischungs Modus)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Fenster   | Zuordnung-presentercore-Synchronisierungs Einheit<br/> Fenster-Manager<br/> | Mixercompositor\*<br/> Zuordnung-Presenter<br/> Core-Synchronisierungs Einheit<br/> Fenster-Manager<br/> |
| Fensterlose | Zuordnung-presentercore-Synchronisierungs Einheit<br/>                           | Mixercompositor\*<br/> Zuordnung-Presenter<br/> Core-Synchronisierungs Einheit<br/>                           |
| Renderlos | Zuordnung von "Zuweisung-Presenter" (von Anwendung bereitgestellt) Core-Synchronisierungs Einheit<br/> | Mixercompositor\*<br/> Zuordnung-Presenter (von Anwendung bereitgestellt)<br/> Core-Synchronisierungs Einheit<br/> |



 

\* Gibt an, dass die Anwendung über die Option verfügt, eine benutzerdefinierte Komponente bereitzustellen oder die Standardkomponente zu verwenden.

Bei allen Konfigurationen sollten Sie sich beim Erstellen von Filter Diagrammen mit der VMR nicht merken, dass Sie die VMR vor dem verbinden konfigurieren müssen.

Für alle Konfigurationen können Pins nicht dynamisch hinzugefügt oder entfernt werden, nachdem die VMR mit dem upstreamfilter verbunden ist, Sie können jedoch verbunden und getrennt werden. Wenn die Anwendung nicht sicher ist, wie viele Pins benötigt werden, sollte die VMR für die maximal benötigte Anzahl konfiguriert werden. Das vorhanden sein von nicht verwendeten Eingabe Pins für den Filter beeinträchtigt nicht die Renderingleistung. Im Gegensatz zum alten Überlagerungs-Mixer hat VMR keine Ausgabe-PIN, da es keinen separaten Filter für die Fensterverwaltung erfordert.

In den folgenden Abschnitten wird beschrieben, wie Sie den VMR für einen bestimmten Modus konfigurieren:

-   [VMR-Fenstermodus (Kompatibilitätsmodus)](vmr-windowed--compatibility--mode.md)
-   [Fensterloser VMR-Modus](vmr-windowless-mode.md)
-   [VMR mit mehreren Streams (Mischungs Modus)](vmr-with-multiple-streams--mixing-mode.md)
-   [YUV-Mischungs Modus](yuv-mixing-mode.md)
-   [Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Exklusiver DirectDraw-Modus](directdraw-exclusive-mode.md)

 

 




