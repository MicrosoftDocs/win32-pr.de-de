---
title: Einschränkungen
description: Einschränkungen
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL unter Windows, Einschränkungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709725"
---
# <a name="limitations"></a>Einschränkungen

Die generische Implementierung weist die folgenden Einschränkungen auf:

-   Drucken.

    Sie können ein OpenGL-Bild direkt mit Metadateien an einen Drucker drucken. Weitere Informationen finden Sie unter [Drucken eines OpenGL-Bilds](printing-an-opengl-image.md).

-   OpenGL-und GDI-Grafiken können nicht in einem Fenster mit doppelter puffert gemischt werden.

    Eine Anwendung kann sowohl OpenGL-Grafiken als auch GDI-Grafiken direkt in ein nur-gepuffertes Fenster, aber nicht in ein Fenster mit doppelter puffert zeichnen.

-   Es sind keine Hardware Farbpaletten pro Fenster vorhanden.

    Windows verfügt über eine einzelne System Hardware-Farbpalette, die für den gesamten Bildschirm gilt. Ein OpenGL-Fenster kann nicht über eine eigene Hardware Palette verfügen, kann aber über eine eigene logische Palette verfügen. Zu diesem Zweck muss Sie zu einer palettenfähigen Anwendung werden. Weitere Informationen finden Sie unter [OpenGL-Farbmodi und Windows-Palettenverwaltung](opengl-color-modes-and-windows-palette-management.md).

-   Es gibt keine direkte Unterstützung für die Zwischenablage, den dynamischen Datenaustausch (DDE) oder OLE.

    Ein Fenster mit OpenGL-Grafiken unterstützt diese Windows-Funktionen nicht direkt. Es gibt jedoch Problem Umgehungen für die Verwendung der Zwischenablage. Weitere Informationen finden Sie unter [Kopieren eines OpenGL-Bilds in die Zwischenablage](copying-an-opengl-image-to-the-clipboard.md).

-   Die C++-Klassenbibliothek von Inventor 2,0 ist nicht enthalten.

    Die Erfinder Klassenbibliothek, die auf OpenGL basiert, bietet Konstrukte höherer Ebene für die Programmierung von 3D-Grafiken. Sie ist nicht in der aktuellen Version der Microsoft-Implementierung von OpenGL für Windows enthalten.

-   Es gibt keine Unterstützung für die folgenden Pixel Format Features: Stereotyp, Alpha bitplane und hilfspuffer.

    Es gibt jedoch Unterstützung für mehrere zusätzliche Puffer, einschließlich Schablonen Puffer, Akkumulations Puffer, Hintergrund Puffer (doppelte Pufferung), über Lagerungs-und unterebenenpuffer und tiefen Puffer (z-Achse).

 

 




