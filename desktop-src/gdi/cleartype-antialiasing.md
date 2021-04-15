---
description: Das Microsoft ClearType-Antialiasing ist eine Glättungs Methode, die die Auflösung der Schriftart Anzeige gegenüber herkömmlichem Antialiasing verbessert.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType-Antialiasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978776"
---
# <a name="cleartype-antialiasing"></a>ClearType-Antialiasing

Das Microsoft ClearType-Antialiasing ist eine Glättungs Methode, die die Auflösung der Schriftart Anzeige gegenüber herkömmlichem Antialiasing verbessert. Dadurch wird die Lesbarkeit von Farb-LCD-Monitoren mit einer digitalen Oberfläche, wie z. b. den Laptops und hochwertigen flatdesktopdarstellungen, deutlich verbessert. Die Lesbarkeit von CRT-Bildschirmen wird ebenfalls verbessert.

ClearType ist jedoch von der Ausrichtung und Reihenfolge der LCD-Streifen abhängig. ClearType wird zurzeit nur für LCDs mit vertikalen Streifen implementiert, die in der RGB-Form angeordnet sind. Dies betrifft insbesondere Tablet PCs, bei denen die Anzeige in beliebiger Richtung ausgerichtet werden kann, und die Bildschirme, die von Landscape zu Hochformat geschaltet werden können.

ClearType-Antialiasing ist zulässig:

-   Für 16-, 24-und 32-Bit-Farbe (deaktiviert für 256 Farben oder weniger)
-   Für den Bildschirm-DC und den Speichercontroller (nicht für den Drucker-DC)
-   Für TrueType-Schriftarten und OpenType-Schriftarten mit TrueType-Gliederungen

ClearType-Antialiasing ist deaktiviert:

-   Unter Terminal Server Client
-   Für Bitmap-Schriftarten, Vektor Schriftarten, Geräte Schriftarten, Type 1-Schriftarten oder PostScript OpenType-Schriftarten ohne TrueType-Gliederungen
-   Wenn die Schriftart eingebettete Bitmaps optimiert hat, nur für die Schrift Grade, die eingebettete Bitmaps enthalten.

Um das ClearType-Antialiasing zu aktivieren, müssen Sie [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) einmal aufrufen, um die Schriftart Glättung zu aktivieren, und dann ein zweites Mal, um den Glättungstyp auf FE \_ fonungmuothingcleartype festzulegen, wie im folgenden Codebeispiel gezeigt:


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



Sie können die Darstellung von Text anpassen, indem Sie den im ClearType-Algorithmus verwendeten Kontrastwert ändern. Der Standardwert ist 1.400, aber es kann sich um einen beliebigen Wert zwischen 1.000 und 2.200 handeln. Abhängig vom Anzeigegerät und der Empfindlichkeit des Benutzers bei Farben kann ein höherer oder niedrigerer Kontrastwert die Lesbarkeit verbessern. Um den Kontrast zu ändern, wenden Sie [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ setfonstistingcontrast an. Der folgende Code legt den Kontrastwert auf 1.600 fest.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Beachten Sie die folgenden Details zur Anwendungs Kompatibilität:

-   Das Rendern von Text mit ClearType ist etwas langsamer als bei Standard-Antialiasing.
-   Anwendungen sollten nicht XOR zum Anzeigen von ausgewähltem Text verwenden. Anwendungen sollten die Hintergrundfarbe festlegen und den ausgewählten Text neu anzeigen.
-   Anwendungen sollten nicht denselben Text im transparenten Modus selbst zeichnen. Wenn dies der Fall ist, werden die edgepixel, bei denen ein Antialiasing durchgeführt wird, farblich anstelle der Hintergrundfarbe mit sich selbst zusammengeführt. Dies führt zu einem dunklen und farbigen Kanten.
-   Anwendungen sollten keinen Text zeichnen, indem Sie die Zeichen einzeln zeichnen, wenn Sie sich im nicht transparenten Modus befinden, da der Rand eines Zeichens durch das folgende Zeichen abgeschnitten werden kann. Dies liegt daran, dass ein mit ClearType geglättes Zeichen möglicherweise eine negative Breite von a oder c aufweist, wobei das reguläre Zeichen eine positive a-oder c-Breite hat. Nur die B-Breite des Zeichens ist garantiert identisch. Ebenso sollten Anwendungen vorsichtig sein, wenn geglättter Text neben nicht gepuffertem Text steht.
-   Wenn eine Anwendung Text rendert und dann die Bitmap manipuliert, sollte die Schriftart Glättung deaktiviert werden, indem der **lfquality** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf die nicht-Antialiasing-Qualität festgelegt wird \_ . Beispielsweise kann ein Spiel einen Bitmap-Schatteneffekt hinzufügen, oder Text, der in eine Bitmap gerendert wird, kann skaliert werden, um eine thumbview zu erhalten.
-   Wenn der Benutzer im Hochformat ausgeführt wird (d. h., das Monitor-Striping ist horizontal), sollte das ClearType-Antialiasing deaktiviert werden.

Der *fdwquality* -Parameter in " [**kreatefont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) " und der **lfquality** -Member von " [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) " akzeptieren das ClearType \_ Quality-Flag. Bei der rasterisierung von mit diesem Flag erstellten Schriftarten wird der ClearType-Rasterizer verwendet. Dieses Flag hat keine Auswirkung auf frühere Versionen des Betriebssystems.

 

 
