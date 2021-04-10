---
title: OpenGL-Farbmodi und Windows-Palettenverwaltung
description: Die Microsoft-Implementierung von OpenGL in Windows unterstützt zwei Farbpixel-Daten Modi RGBA und Color-Index-Modi. Windows bietet zwei analoge Möglichkeiten, Farben und Palettenverwaltung Farben zu verarbeiten.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL unter Windows, Farbmodi
- OpenGL unter Windows, Palettenverwaltung
- Palette Management OpenGL
- Farbmodi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309788"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>OpenGL-Farbmodi und Windows-Palettenverwaltung

Die Microsoft-Implementierung von OpenGL in Windows unterstützt zwei Farbpixel-Daten Modi: RGBA und Color-Index-Modi. Windows bietet zwei analoge Methoden zur Handhabung von Farben: echte Farb-und Palettenverwaltung.

Echte Farben Geräte, die in der Lage sind, 16, 24 oder mehr Bits von Farbinformationen pro Pixel zu akzeptieren, können Zehntausende, zehn Millionen oder mehr Farben gleichzeitig anzeigen. Komplexität entstehen jedoch, wenn eine Anwendung den RGBA-oder Farb Index Modus auf einem palettengerät verwalten muss. Palettengeräte, wie z. b. eine 256-farbige VGA-Anzeige, sind in der Anzahl von Farben, die Sie gleichzeitig anzeigen können, beschränkt. Anwendungen müssen eine Reihe komplizierter Details verarbeiten, um Geräte mit Palettentyp erfolgreich verwenden zu können. Da im farbindexmodusprogramm keine Hardware Palette verwendet wird, ist die Verwendung mit echten Farb Geräten schwieriger als Programme, die den RGBA-Modus verwenden.

 

 




