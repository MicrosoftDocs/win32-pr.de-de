---
description: Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, ein Grafik Objekt oder Textobjekt so nah wie möglich an die ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled Bitmap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863639"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled Bitmap-Funktionen

Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, ein Grafik Objekt oder Textobjekt so nah wie möglich an die ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten. Unabhängig davon, ob Sie ein Bild oder eine andere Grafik auf einem Farbscanner Scannen, es über das Internet herunterladen, auf dem Bildschirm anzeigen oder bearbeiten oder es auf Papier-, Film-oder anderen Medien drucken, unterstützt Sie ICM 2,0 dabei, Farben konsistent und genau zu halten. Weitere Informationen zu ICM finden Sie unter [Windows Color System](/previous-versions//dd372446(v=vs.85)).

Es gibt verschiedene Funktionen in der Graphics Device Interface (GDI), die Farbdaten verwenden oder verwenden. Die folgenden bitmapfunktionen sind für die Verwendung mit ICM aktiviert:

-   [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**"Kreatedibitmap"**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**"Kreatedibsection"**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**Setdibcolortable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
