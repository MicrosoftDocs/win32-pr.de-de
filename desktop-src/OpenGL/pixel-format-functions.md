---
title: Pixel Format Funktionen
description: Die folgenden Windows-Funktionen verwalten Pixel Formate.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- WGL-Funktionen, Pixel Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856884"
---
# <a name="pixel-format-functions"></a>Pixel Format Funktionen

Die folgenden Windows-Funktionen verwalten Pixel Formate.



| Windows-Funktion                                               | BESCHREIBUNG                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Auswahl Pixel Format**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Ruft das Pixel Format des Geräte Kontexts ab, das dem angegebenen Pixel Format am ehesten entspricht.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Legt das aktuelle Pixel Format eines Geräte Kontexts auf das durch einen Pixel Format Index angegebene Pixel Format fest.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Ruft den Pixel Format Index des aktuellen Pixel Formats eines Geräte Kontexts ab.                                                                                            |
| [**Describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Wenn ein Gerätekontext und ein Pixel Format Index vorliegen, füllt eine [**Pixel formatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur mit den Eigenschaften des Pixel Formats. |
| [**Getenhmetafilepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Ruft Informationen zum Pixel Format für eine erweiterte Metadatei ab.                                                                                                          |



 

Die [**chootarformat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) -Funktion gibt einen 1-basierten Pixel Format Index zurück, der die beste Entsprechung aus den unterstützten Pixel Formaten des Geräte Kontexts identifiziert.

Die Funktion [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifiziert das gewünschte Format mit einem 1-basierten Pixel Format Index. In der Regel wird " **choosepixelformat** " aufgerufen, um ein Pixel Format mit der besten Entsprechung zu finden, und dann " **SetPixelFormat** " mit dem Ergebnis von " **choosepixelformat**" aufgerufen.

Wenn Sie **SetPixelFormat** für einen Gerätekontext aufrufen, der auf ein Fenster verweist, ändert **SetPixelFormat** auch das Pixel Format des Fensters. Wenn das Pixel Format eines Fensters mehrmals festgelegt wird, kann dies zu erheblichen Komplikationen für den Fenster Manager und für Multithreadanwendungen führen, sodass es nicht zulässig ist. Das Pixel Format eines Fensters kann nur ein Mal festgelegt werden. Danach kann das Pixel Format des Fensters nicht mehr geändert werden.

Die [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) -Funktion gibt einen 1-basierten Pixel Format Index zurück.

Die [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) -Funktion nimmt folgende Parameter als Parameter an:

-   Ein Handle für einen Gerätekontext
-   Ein Pixel Format Index
-   Ein Zeiger auf eine [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur.

Die [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) -Funktion gibt zurück, wobei die Member von **pixelformatdescriptor** entsprechend festgelegt sind.

Die **getenhmetafilepixelformat** -Funktion gibt die Größe des Pixel Formats einer Metadatei zurück und ruft die Pixel Formatinformationen der Metadatei ab.

 

 




