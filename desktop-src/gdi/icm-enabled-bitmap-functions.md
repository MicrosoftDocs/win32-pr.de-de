---
description: Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, grafikspezifisches Objekt oder Textobjekt so nah wie möglich an der ursprünglichen Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede in den Bildverarbeitungstechnologien und Farbfunktionen zwischen Geräten.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled Bitmapfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38341851eb9ba2aed25cc93afbf7b869909430a30ecb626bf3a452883fdea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831970"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled Bitmapfunktionen

Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, grafikspezifisches Objekt oder Textobjekt so nah wie möglich an der ursprünglichen Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede in den Bildverarbeitungstechnologien und Farbfunktionen zwischen Geräten. Unabhängig davon, ob Sie ein Bild oder eine andere Grafik auf einem Farbscanner scannen, über das Internet herunterladen, auf dem Bildschirm anzeigen oder bearbeiten oder auf Papier, Film oder anderen Medien drucken, ICM 2.0 hilft Ihnen, Farben konsistent und präzise zu halten. Weitere Informationen zu ICM finden Sie unter [Windows Color System](/previous-versions//dd372446(v=vs.85)).

Es gibt verschiedene Funktionen in der Grafikgeräteschnittstelle (GDI), die Farbdaten verwenden oder verarbeiten. Die folgenden Bitmapfunktionen sind für die Verwendung mit ICM:

-   [**Bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
