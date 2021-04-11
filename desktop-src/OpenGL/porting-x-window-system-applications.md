---
title: Portieren von System Anwendungen für X-Fenster
description: Portieren von System Anwendungen für X-Fenster
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL unter Windows, portieren
- Portieren auf OpenGL, X Window System
- OpenGL-Portierung, X-Fenster System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206856"
---
# <a name="porting-x-window-system-applications"></a>Portieren von System Anwendungen für X-Fenster

Wie bei Windows ist das X-Fenstersystem ein Nachrichten basiertes System, das Fenster Steuerelemente und Menüs verwendet. Der OpenGL-Code in der X-Fenster System Anwendung befindet sich wahrscheinlich in Bereichen, die in etwa so aussehen, wo Sie angezeigt werden, wenn Sie Sie in Windows portieren. Der größte Teil Ihres OpenGL-Codes ändert sich nicht, aber Sie müssen jeden Code neu schreiben, der für das X-Fenster System spezifisch ist.

**Verwenden Sie das folgende allgemeine Verfahren, um die OpenGL-Programme des X-Fensters auf Windows zu portieren.**

1.  Schreiben Sie den System spezifischen Code des X-Fensters mit dem entsprechenden Windows-Code um. Suchen Sie den Code zum Erstellen von Fenstern und zur Ereignis Behandlung. Das X-Fenster System und Windows sind Ereignis Behandlung, Nachrichten basierte windowingsysteme, mit denen Sie leichter bestimmen können, wo die entsprechenden Änderungen vorgenommen werden. (Insbesondere bei großen Anwendungen kann das Umschreiben einer Anwendung von einem Betriebssystem zu einem anderen eine komplexe und schwierige Aufgabe darstellen.)
2.  Suchen Sie nach Code, der glx-Funktionen verwendet. Dabei handelt es sich um die Funktionen, die Sie in die entsprechenden Windows-Funktionen übersetzen.
3.  Übersetzen Sie glx-Pixel Formatfunktionen und visuelle/drawable-Funktionen in entsprechende Windows/OpenGL-Pixel Formate und Gerätekontext Funktionen.
4.  Übersetzt die glx-renderingkontextfunktionen in Windows/OpenGL-Rendering-Kontextfunktionen
5.  Übersetzt die glx-pixmap-Funktionen in äquivalente Windows-Funktionen.
6.  Übersetzen Sie glx Frame Puffer und andere glx-Funktionen in die entsprechenden Windows-Funktionen.

 

 




