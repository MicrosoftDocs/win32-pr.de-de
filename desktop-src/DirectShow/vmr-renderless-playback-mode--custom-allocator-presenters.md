---
description: VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757668"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)

Im renderlosen Wiedergabemodus führt VMR das Rendering nicht aus. Stattdessen wird eine von der Anwendung bereitgestellte benutzerdefinierte Zuordnung verwendet. Dieser Modus ist nützlich für Spiele und andere Arten von Anwendungen, die über anspruchsvolle Video Effekte verfügen. Der renderlose Wiedergabemodus ermöglicht es den Anwendungen, ihre eigene DirectDraw-Oberfläche (VMR-7) oder Direct3D Surface (VMR-9) zu erstellen und zu steuern und zum Zeitpunkt der Präsentation auf die Video Bits zuzugreifen.

Im renderlosen Modus lädt VMR-9 seine Mischungs Komponente nicht automatisch.

Im renderlosen Wiedergabemodus führt die Anwendung die folgenden Aufgaben aus:

-   Verwaltet das Wiedergabe Fenster.
-   Ordnet das DirectDraw-oder Direct3D-Objekt und den abschließenden Frame Puffer zu.
-   Benachrichtigt den Rest des Wiedergabe Systems des verwendeten Objekts.
-   Stellt den Frame Puffer zur richtigen Zeit dar.
-   Behandelt alle Änderungen im Auflösungsmodus, überwachen Änderungen und Oberflächen Verluste. Er muss das restliche Wiedergabe System dieser Ereignisse informieren.

Die VMR führt folgende Schritte aus:

-   Behandelt alle Zeitüberschreitungen im Zusammenhang mit der Darstellung des Video Frames.
-   Stellt Qualitäts Steuerungsinformationen für die Anwendung und den Rest des Wiedergabe Systems bereit.
-   Stellt eine konsistente Schnittstelle zu den Upstreamkomponenten des Wiedergabe Systems dar, die nicht wissen, dass die Anwendung die Frame Puffer Zuordnung bereitstellt und das Rendering ausführt.
-   Bietet eine beliebige Mischung aus Videostreams, die vor dem Rendering erforderlich sein können.

Da Deinterlacing durch den Mixer ausgeführt wird, hat der zuordnerpräsentator immer Deinterlacing-Frames empfangen. Weitere Informationen finden Sie unter [Festlegen von deinterlace-Einstellungen](setting-deinterlace-preferences.md).

Weitere Informationen zum Bereitstellen einer benutzerdefinierten Zuweisung finden Sie in den folgenden Themen:

-   [Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [Synchronisieren von VMR mit der Aktualisierungs Rate des Monitors](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



