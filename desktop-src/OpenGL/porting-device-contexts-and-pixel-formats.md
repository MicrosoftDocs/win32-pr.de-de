---
title: Portieren von Geräte Kontexten und Pixel Formaten
description: Portieren von Geräte Kontexten und Pixel Formaten
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- Portieren auf OpenGL, Pixel
- OpenGL-portieren, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338977"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Portieren von Geräte Kontexten und Pixel Formaten

Jedes Fenster in der Microsoft-Implementierung von OpenGL für Windows verfügt über ein eigenes Aktuelles Pixel Format. Ein Pixel Format wird durch eine [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur definiert. Da jedes Fenster über ein eigenes Pixel Format verfügt, erhalten Sie einen Gerätekontext, legen Sie das Pixel Format des Geräte Kontexts fest, und erstellen Sie dann einen OpenGL-renderingkontext für den Gerätekontext. Der renderingkontext verwendet automatisch das Pixel Format des Geräte Kontexts.

Das X-Fenster System verwendet auch eine Datenstruktur, **xvisualinfo**, um die Eigenschaften der Pixel in einem Fenster anzugeben. **Xvisualinfo** -Strukturen enthalten eine **visuelle** Datenstruktur, die beschreibt, wie Farb Ressourcen in einem bestimmten Bildschirm verwendet werden.

Im X-Fenster System wird **xvisualinfo** zum Erstellen eines Fensters verwendet, indem das Fenster auf das gewünschte Pixel Format festgelegt wird. Die zurückgegebene-Struktur wird verwendet, um das Fenster und einen renderingkontext zu erstellen. In Windows erstellen Sie zunächst ein Fenster und erhalten ein Handle für einen Gerätekontext (HDC) des Fensters. Der HDC wird dann verwendet, um das Pixel Format für das Fenster festzulegen. Der renderingkontext verwendet das Pixel Format des Fensters.

In der folgenden Tabelle werden die X-Fenster System-und glx-visuellen Funktionen mit ihren entsprechenden Windows-Pixel Formatfunktionen verglichen.



| X Fenster/glx-Funktion                                                                                     | Windows-Pixel Format-Funktion                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Xvisualinfo \* **glxchoosevisual**(Display *\* dpy*, int *Screen*, int *\* atzst*)                               | int [**Choice Pixel Format**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *hdc*, pixelformatdescriptor *\* ppfd*)                                      |
| int **glxgetconfig**(Display *\* dpy*, xvisualinfo *\* VIS*, int *\* atzst*, int *\* Wert*)                      | int [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *hdc*, int *ipixelformat*, uint *nbytes*, lppixelformatdescriptor *ppfd*) |
| Xvisualinfo \* **xgetvisualinfo**(Display *\* dpy*, Long *vinfo \_ Mask*, xvisualinfo *\* vinfo \_ Templ*, int *\* nitems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *hdc*)                                                                           |
| Die von **glxchoosevisual** zurückgegebene *Visualisierung* wird verwendet, wenn ein Fenster erstellt wird.                                   | Bool [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *hdc*, int *ipixelformat*, pixelformatdescriptor *\* ppfd*)                        |



 

In den folgenden Abschnitten finden Sie Beispiele für Pixel Format-Code Fragmente für ein X-Fenster System Programm und denselben Code, nachdem er zu Windows portiert wurde.

-   [Code Beispiel für das glx-Pixel Format](glx-pixel-format-code-sample.md)
-   [Code Beispiel für Windows-Pixel Format](win32-pixel-format-code-sample.md)

Weitere Informationen zu Pixel Formaten finden Sie unter [Pixel Formate](pixel-formats.md).

 

 




