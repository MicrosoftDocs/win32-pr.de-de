---
title: Auswählen zwischen RGBA und Color-Index Modus
description: Verwenden Sie im Allgemeinen den RGBA-Modus für Ihre OpenGL-Anwendungen. Sie bietet mehr Flexibilität als der Farb Index Modus für Effekte wie Schattierung, Beleuchtung, Farbzuordnung, Nebel, Antialiasing und Vermischung.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL unter Windows, RGBA-Modus
- OpenGL unter Windows, Farb Index Modus
- RGBA-Modus OpenGL
- Farb Index Modus OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710422"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Auswählen zwischen RGBA und Color-Index Modus

Verwenden Sie im Allgemeinen den RGBA-Modus für Ihre OpenGL-Anwendungen. Sie bietet mehr Flexibilität als der Farb Index Modus für Effekte wie Schattierung, Beleuchtung, Farbzuordnung, Nebel, Antialiasing und Vermischung.

In den folgenden Fällen sollten Sie den Farb Index Modus verwenden:

-   Wenn eine begrenzte Anzahl von bitflächen verfügbar ist, der Farb Index Modus kann weniger grobe Schattierung als der RGBA-Modus bewirken.
-   Wenn Sie sich keine Gedanken über die Verwendung von "Real"-Farben machen möchten, Beispielsweise können Sie verschiedene Farben in einer Topographic-Karte verwenden, um relative Erweiterungen festzulegen.
-   Wenn Sie eine vorhandene Anwendung portieren, die den Farb Index Modus ausgiebig verwendet.
-   Wenn Sie die Farb Zuordnungs Animation und-Effekte in der Anwendung verwenden möchten. (Dies ist auf echt Farben Geräten nicht möglich.)

 

 




