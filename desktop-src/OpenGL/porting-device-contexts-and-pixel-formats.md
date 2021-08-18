---
title: Portieren von Gerätekontexten und Pixelformaten
description: Portieren von Gerätekontexten und Pixelformaten
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- Portieren zu OpenGL, Pixel
- OpenGL-Portierung, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b292fb3f27eb2ed888a4db94198944f41a8571114b38c5c90b994cdd1cb6367f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144083"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Portieren von Gerätekontexten und Pixelformaten

Jedes Fenster in der Microsoft-Implementierung von OpenGL für Windows hat ein eigenes aktuelles Pixelformat. Ein Pixelformat wird durch eine [**PIXELFORMATDESCRIPTOR-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) definiert. Da jedes Fenster ein eigenes Pixelformat aufweist, erhalten Sie einen Gerätekontext, legen das Pixelformat des Gerätekontexts fest und erstellen dann einen OpenGL-Renderingkontext für den Gerätekontext. Der Renderingkontext verwendet automatisch das Pixelformat seines Gerätekontexts.

Das X-Fenstersystem verwendet auch die Datenstruktur **XVisualInfo,** um die Eigenschaften von Pixeln in einem Fenster anzugeben. **XVisualInfo-Strukturen** enthalten eine **visuelle** Datenstruktur, die beschreibt, wie Farbressourcen auf einem bestimmten Bildschirm verwendet werden.

Im X-Fenstersystem wird **XVisualInfo** verwendet, um ein Fenster zu erstellen, indem das Fenster auf das gewünschte Pixelformat festgelegt wird. Die zurückgegebene -Struktur wird verwendet, um das Fenster und einen Renderingkontext zu erstellen. In Windows erstellen Sie zunächst ein Fenster und erhalten ein Handle für einen Gerätekontext (HDC) des Fensters. Der HDC wird dann verwendet, um das Pixelformat für das Fenster festzulegen. Der Renderingkontext verwendet das Pixelformat des Fensters.

In der folgenden Tabelle werden die visuellen Funktionen X Window System und GLX mit ihren entsprechenden Windows Pixelformatfunktionen verglichen.



| Visuelle X-Fenster-/GLX-Funktion                                                                                     | Windows Pixelformatfunktion                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**( Display *\* dpy*,int *screen*,int *\* attribList*)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\* ppfd*)                                      |
| int **glXGetConfig**( anzeigen *\* dpy*,XVisualInfo *\* vis*,int *\* attribList*,int *\* value*)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*) |
| XVisualInfo \* **XGetVisualInfo**( Display *\* dpy*,long *vinfo \_ mask*,XVisualInfo *\* vinfo \_ templ*,int *\* nitems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)                                                                           |
| Das von **glxChooseVisual** zurückgegebene *Visual* wird verwendet, wenn ein Fenster erstellt wird.                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\* ppfd*)                        |



 

Die folgenden Abschnitte enthalten Beispiele für Codefragmente im Pixelformat für ein X-Fenstersystemprogramm und den gleichen Code, nachdem er zu Windows portiert wurde.

-   [GLX-Pixelformatcodebeispiel](glx-pixel-format-code-sample.md)
-   [Windows Pixelformatcodebeispiel](win32-pixel-format-code-sample.md)

Weitere Informationen zu Pixelformaten finden Sie unter [Pixelformate.](pixel-formats.md)

 

 




