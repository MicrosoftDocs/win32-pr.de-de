---
description: Die Farbfunktionen von Geräten, wie z. b. anzeigen und Druckern, können zwischen Monochrom und Tausenden von Farben reichen.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Farbgrundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215211"
---
# <a name="color-basics"></a>Farbgrundlagen

Die Farbfunktionen von Geräten, wie z. b. anzeigen und Druckern, können zwischen Monochrom und Tausenden von Farben reichen. Da eine Anwendung möglicherweise in diesem Bereich eine Ausgabe für Geräte generieren muss, sollte Sie darauf vorbereitet sein, unterschiedliche Farbfunktionen zu verarbeiten.

Eine Anwendung kann die Anzahl der für ein bestimmtes Gerät verfügbaren Farben ermitteln, indem Sie die [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion zum Abrufen des numcolors-Werts verwendet. Dieser Wert gibt die Anzahl der Farben an, die für die Verwendung durch die Anwendung verfügbar sind. In der Regel entspricht diese Anzahl einer physischen Eigenschaft des Ausgabegeräts, z. b. der Anzahl der Farben im Drucker oder der Anzahl der unterschiedlichen Farbsignale, die der Anzeige Adapter an den Monitor übertragen kann.

Obwohl der numcolors-Wert die Anzahl von Farben angibt, identifiziert er nicht die verfügbaren Farben. Eine Anwendung kann ermitteln, welche Farben verfügbar sind, indem alle Stifte aufgelistet werden, die den Typ "PS Solid" aufweisen \_ . Da der Gerätetreiber, der ein bestimmtes Gerät unterstützt, in der Regel über einen vollständigen Bereich von ausgefülltem Stifte verfügt, und da das System erfordert, dass solide Stifte nur Farben enthalten, die vom Gerät generiert werden können, ist die Enumeration dieser Stifte häufig Äquivalent zum Auflisten der Farben. Eine Anwendung kann die Stifte mithilfe der [**enumubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) -Funktion auflisten. Ein Codebeispiel finden Sie unter Auflisten von [Farben](enumerating-colors.md).

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Farbwerte](color-values.md)
-   [Farb Näherungen und Dithering](color-approximations-and-dithering.md)
-   [Farbe in Bitmaps](color-in-bitmaps.md)
-   [Farbmischung](color-mixing.md)

 

 



