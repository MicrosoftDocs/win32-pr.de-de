---
title: Einschränkungen
description: Einschränkungen
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL für Windows,Einschränkungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d058570c049f471dcf6e92c4eb55eb1365948d581127c68a46deb8d863ccc34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937417"
---
# <a name="limitations"></a>Einschränkungen

Die generische Implementierung weist die folgenden Einschränkungen auf:

-   Drucken.

    Sie können ein OpenGL-Image nur mithilfe von Metadateien direkt auf einem Drucker drucken. Weitere Informationen finden Sie unter [Drucken eines OpenGL-Bilds.](printing-an-opengl-image.md)

-   OpenGL- und GDI-Grafiken können nicht in einem doppelt gepufferten Fenster gemischt werden.

    Eine Anwendung kann Sowohl OpenGL-Grafiken als auch GDI-Grafiken direkt in ein einzelnes gepuffertes Fenster, jedoch nicht in ein doppelt gepuffertes Fenster zeichnen.

-   Es gibt keine Hardwarefarbpaletten pro Fenster.

    Windows verfügt über eine einzelne Systemhardwarefarbpalette, die für den gesamten Bildschirm gilt. Ein OpenGL-Fenster kann nicht über eine eigene Hardwarepalette, aber über eine eigene logische Palette verfügen. Dazu muss sie zu einer palettenfähigen Anwendung werden. Weitere Informationen finden Sie unter [OpenGL-Farbmodi und Windows Palettenverwaltung.](opengl-color-modes-and-windows-palette-management.md)

-   Es gibt keine direkte Unterstützung für die Zwischenablage, den dynamischen Datenaustausch (Dynamic Data Exchange, DDE) oder OLE.

    Ein Fenster mit OpenGL-Grafiken unterstützt diese Windows Funktionen nicht direkt. Es gibt jedoch Problemumgehungen für die Verwendung der Zwischenablage. Weitere Informationen finden Sie unter [Kopieren eines OpenGL-Images in die Zwischenablage.](copying-an-opengl-image-to-the-clipboard.md)

-   Die C++-Klassenbibliothek "Redistribut 2.0" ist nicht enthalten.

    Die Auf der Grundlage von OpenGL aufgebaute Class Library Von Der Class Library von "Class" stellt Konstrukte auf höherer Ebene für die Programmierung von 3D-Grafiken bereit. Sie ist nicht in der aktuellen Version der Microsoft-Implementierung von OpenGL für Windows enthalten.

-   Die folgenden Pixelformatfeatures werden nicht unterstützt: Stereobilder, Alphabitebenen und Hilfspuffer.

    Es gibt jedoch Unterstützung für mehrere Hilfspuffer, einschließlich Schablonenpuffer, Akkumulationspuffer, Hintergrundpuffer (doppelte Pufferung), Überlagerungs- und Hintergrundebenenpuffer und Tiefenpuffer (Z-Achse).

 

 




