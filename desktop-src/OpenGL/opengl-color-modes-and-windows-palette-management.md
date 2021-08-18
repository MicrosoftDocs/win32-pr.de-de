---
title: OpenGL-Farbmodi und Windows Palettenverwaltung
description: Die Microsoft-Implementierung von OpenGL in Windows unterstützt zwei Farbpixeldatenmodi RGBA und Farbindexmodi. Windows bieten zwei analoge Methoden zum Behandeln von Farb-True-Farbe und Palettenverwaltung.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL auf Windows,Farbmodi
- OpenGL auf Windows,Palettenverwaltung
- Palettenverwaltung OpenGL
- Farbmodi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf91ebb45e99368596cb48cb625f0eb6de025e6664144f104f6a9c17951a1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144133"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>OpenGL-Farbmodi und Windows Palettenverwaltung

Die Microsoft-Implementierung von OpenGL in Windows unterstützt zwei Farbpixel-Datenmodi: RGBA und Farbindexmodi. Windows bieten zwei analoge Methoden für die Behandlung von Farben: die Verwaltung von True Color und Palette.

Geräte mit true-Farben, die 16, 24 oder mehr Bits an Farbinformationen pro Pixel akzeptieren können, können Zehntausende, Dutzende Millionen oder mehr Farben gleichzeitig anzeigen. Komplexität entsteht jedoch, wenn eine Anwendung den RGBA- oder Farbindexmodus auf einem Palettengerät verwalten muss. Geräte vom Typ Palette, z. B. eine VGA-Anzeige mit 256 Farben, sind in der Anzahl der Farben beschränkt, die sie gleichzeitig anzeigen können. Anwendungen müssen eine Reihe von kniffligen Details verarbeiten, um Geräte vom Typ Palette erfolgreich zu verwenden. Da Programme im Farbindexmodus keine Hardwarepalette verwenden, sind sie schwieriger mit Geräten mit richtiger Farbe zu verwenden als Programme, die den RGBA-Modus verwenden.

 

 




