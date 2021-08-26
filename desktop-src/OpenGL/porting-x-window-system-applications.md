---
title: Portieren von X-Fenstersystemanwendungen
description: Portieren von X-Fenstersystemanwendungen
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL auf Windows,Portierung
- Portieren zu OpenGL,X Window System
- OpenGL-Portierung,X-Fenstersystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07a20de68df3806da40629252246f176beece0a4c3951180d484d9fadc6b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034760"
---
# <a name="porting-x-window-system-applications"></a>Portieren von X-Fenstersystemanwendungen

Wie Windows ist das X-Fenstersystem ein meldungsbasiertes Ereignisbehandlungssystem, das Fenstersteuerelemente und Menüs verwendet. Der OpenGL-Code in Ihrer X Window System-Anwendung befindet sich wahrscheinlich in Bereichen, die ungefähr dem Ort entsprechen, an dem er angezeigt wird, wenn Sie ihn zu Windows portieren. Der größte Teil ihres OpenGL-Codes ändert sich nicht, sie müssen jedoch codespezifisch für das X-Fenstersystem umschreiben.

**Verwenden Sie das folgende allgemeine Verfahren, um Ihre OpenGL-Programme des X-Fenstersystems zu Windows**

1.  Schreiben Sie den X-Fenstersystem-spezifischen Code mit entsprechendem Windows Code um. Suchen Sie nach Code für die Fenstererstellung und Ereignisbehandlung. Das X-Fenstersystem und Windows sind meldungsbasierte Ereignisbehandlungssysteme, die es einfacher machen, zu bestimmen, wo die entsprechenden Änderungen vorgenommen werden sollen. (Insbesondere bei großen Anwendungen kann das Umschreiben einer Anwendung von einem Betriebssystem in ein anderes jedoch eine komplexe und schwierige Aufgabe sein.)
2.  Suchen Sie nach code, der GLX-Funktionen verwendet. Dies sind die Funktionen, die Sie in die entsprechenden Windows Funktionen übersetzen.
3.  Übersetzen Sie GLX-Pixelformatfunktionen und Visual/Drawable-Funktionen in die entsprechenden Windows/OpenGL-Pixelformat- und Gerätekontextfunktionen.
4.  Übersetzen von GLX-Renderingkontextfunktionen in Windows/OpenGL-Renderingkontextfunktionen.
5.  Übersetzen sie GLX Pixmap-Funktionen in entsprechende Windows Funktionen.
6.  Übersetzen Sie GLX-Framepuffer und andere GLX-Funktionen in die entsprechenden Windows Funktionen.

 

 




