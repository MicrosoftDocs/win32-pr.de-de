---
description: Microsoft ClearType antialiasing ist eine Glättungsmethode, die die Schriftanzeigeauflösung gegenüber herkömmlichen Antialiasing verbessert.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType-Antialiasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc8444c1e1b594559f9c5b7f96529a0db00b20c6a10e560bc1dcb4574e079d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888095"
---
# <a name="cleartype-antialiasing"></a>ClearType-Antialiasing

Microsoft ClearType antialiasing ist eine Glättungsmethode, die die Schriftanzeigeauflösung gegenüber herkömmlichen Antialiasing verbessert. Es verbessert die Lesbarkeit auf Farbmonitoren mit EINER digitalen Schnittstelle erheblich, z. B. bei Laptops und hochwertigen flachen Desktopanzeigen. Die Lesbarkeit auf CRT-Bildschirmen wurde ebenfalls etwas verbessert.

ClearType ist jedoch von der Ausrichtung und Reihenfolge der STRIPE-Stripes abhängig. Derzeit wird ClearType nur für LCDs mit vertikalen Stripes implementiert, die RGB-geordnet sind. Dies betrifft insbesondere Tablet-PCs, bei denen die Anzeige in beliebiger Richtung ausgerichtet werden kann, sowie die Bildschirme, die von Querformat zu Hochformat umgeschaltet werden können.

ClearType-Antialiasing ist zulässig:

-   Für 16-, 24- und 32-Bit-Farben (für 256 Farben oder weniger deaktiviert)
-   Für Bildschirm-DC und Arbeitsspeicher-DC (nicht für Druckerdomänencontroller)
-   Für TrueType-Schriftarten und OpenType-Schriftarten mit TrueType-Konturen

Das ClearType-Antialiasing ist deaktiviert:

-   Unter Terminalserverclient
-   Für Bitmapschriftarten, Vektorschriftarten, Geräteschriftarten, Schriftarten vom Typ 1 oder Postscript OpenType-Schriftarten ohne TrueType-Konturen
-   Wenn die Schriftart eingebettete Bitmaps optimiert hat, nur für die Schriftgrößen, die eingebettete Bitmaps enthalten

Rufen Sie zum Aktivieren des [**ClearType-Antialiasings einmal SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) auf, um die Schriftartglättung zu aktivieren, und legen Sie dann ein zweites Mal den Glättungstyp auf FE \_ FONTSMOOTHINGCLEARTYPE fest, wie im folgenden Codebeispiel gezeigt:


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Sie können die Darstellung von Text anpassen, indem Sie den im ClearType-Algorithmus verwendeten Kontrastwert ändern. Der Standardwert ist 1.400, kann aber ein beliebiger Wert zwischen 1.000 und 2.200 sein. Je nach Anzeigegerät und der Empfindlichkeit des Benutzers gegenüber Farben kann ein höherer oder niedrigerer Kontrastwert die Lesbarkeit verbessern. Um den Kontrast zu ändern, rufen [**Sie SystemParametersInfo mit**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) SPI \_ SETFONTSMOOTHINGCONTRAST auf. Der folgende Code legt den Kontrastwert auf 1.600 fest.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Beachten Sie die folgenden Details zur Anwendungskompatibilität:

-   Das Textrendering mit ClearType ist etwas langsamer als bei Standard-Antialiasing.
-   Anwendungen sollten XOR nicht verwenden, um ausgewählten Text anzuzeigen. Anwendungen sollten die Hintergrundfarbe festlegen und den ausgewählten Text erneut anzeigen.
-   Anwendungen sollten nicht denselben Text über sich selbst im transparenten Modus zeichnen. Wenn dies der Fall ist, werden die Ränderpixel, die antialiasiert werden, mit sich selbst und nicht mit der Hintergrundfarbe zusammengeführt. Dies führt zu dunklen und farbigen Kanten.
-   Anwendungen sollten keinen Text zeichnen, indem sie die Zeichen einzeln zeichnen, wenn sie sich im nicht transparenten Modus befinden, da der Rand eines Zeichens durch das folgende Zeichen abgeschnitten werden kann. Dies liegt daran, dass ein Zeichen, das mit ClearType geglättet wird, eine negative Breite von A oder C haben kann, bei der das reguläre Zeichen eine positive Breite von A oder C hat. Es wird garantiert, dass nur die B-Breite des Zeichens identisch ist. Ebenso sollten Anwendungen vorsichtig sein, wenn sich geglätteter Text neben nichtmoothiertem Text befindet.
-   Wenn eine Anwendung Text rendert und dann die Bitmap bearbeitet, sollte die Schriftartglättung deaktiviert werden, indem der **lfQuality-Member** der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) auf NONANTIALIASED \_ QUALITY festlegen. Beispielsweise kann ein Spiel einen Bitmapschatteneffekt hinzufügen, oder in eine Bitmap gerenderter Text kann skaliert werden, um eine Fingerabdruckansicht zu erzeugen.
-   Wenn der Benutzer im Hochformatmodus ausgeführt wird (d. h. monitor striping ist horizontal), sollte das ClearType-Antialiasing deaktiviert werden.

Der *fdwQuality-Parameter* in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) und das **lfQuality-Member** von [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) akzeptieren das CLEARTYPE \_ QUALITY-Flag. Bei der Rasterung von Schriftarten, die mit diesem Flag erstellt wurden, wird der ClearType-Rasterizer verwendet. Dieses Flag hat keine Auswirkungen auf frühere Versionen des Betriebssystems.

 

 
