---
description: Die Farbfunktionen von Geräten, z. B. Displays und Druckern, können von monofarbig bis zu Tausenden von Farben reichen.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Farbgrundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29bcae40ee6771a9c46b892af6e6a8bceb4dcbc6498fb863353d39f92d4c2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105749"
---
# <a name="color-basics"></a>Farbgrundlagen

Die Farbfunktionen von Geräten, z. B. Displays und Druckern, können von monofarbig bis zu Tausenden von Farben reichen. Da eine Anwendung möglicherweise ausgaben für Geräte in diesem Bereich generieren muss, sollte sie darauf vorbereitet sein, unterschiedliche Farbfunktionen zu verarbeiten.

Eine Anwendung kann die Anzahl der für ein bestimmtes Gerät verfügbaren Farben mithilfe der [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) zum Abrufen des NUMCOLORS-Werts feststellen. Dieser Wert gibt die Anzahl der Farben an, die für die Verwendung durch die Anwendung verfügbar sind. In der Regel entspricht diese Anzahl einer physischen Eigenschaft des Ausgabegeräts, z. B. der Anzahl der Druckfarben oder der Anzahl unterschiedlicher Farbsignale, die der Adapter an den Monitor übertragen kann.

Obwohl der NUMCOLORS-Wert die Anzahl der Farben angibt, werden die verfügbaren Farben nicht identifiziert. Eine Anwendung kann feststellen, welche Farben verfügbar sind, indem sie alle Stifte mit dem PS \_ SOLID-Typ aufzählt. Da der Gerätetreiber, der ein bestimmtes Gerät unterstützt, in der Regel über einen vollständigen Bereich von Solid Pens verfügt und das System erfordert, dass vollfarbige Stifte nur Farben haben, die das Gerät generieren kann, entspricht das Aufzählen dieser Stifte häufig dem Aufzählen der Farben. Eine Anwendung kann die Stifte mithilfe der [**EnumObjects-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) aufzählen. Ein Codebeispiel finden Sie unter [Aufzählen von Farben.](enumerating-colors.md)

Weitere Informationen finden Sie in den folgenden Themen:

-   [Farbwerte](color-values.md)
-   [Farbannäherungen und -dithering](color-approximations-and-dithering.md)
-   [Farbe in Bitmaps](color-in-bitmaps.md)
-   [Farbmischung](color-mixing.md)

 

 



