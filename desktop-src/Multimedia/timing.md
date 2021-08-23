---
title: Timing (Windows Multimedia)
description: Zeitliche Steuerung
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, timing
- DrawDibTime-Funktion
- DrawDib, Debuggen
- Debuggen von DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688080"
---
# <a name="timing-windows-multimedia"></a>Timing (Windows Multimedia)

Im Rahmen des Debuggens einer Anwendung können Sie Informationen zur Zeit abrufen, die zum Ausführen von wiederkehrenden DrawDib-Vorgängen erforderlich ist. Die [**DrawDibTime-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) gibt Zeitsteuerungsinformationen für die folgenden Vorgänge zurück:

-   Zeichnen einer Bitmap
-   Dekomprimieren einer Bitmap
-   Dithering einer Bitmap
-   Strecken einer Bitmap
-   Übertragen einer Bitmap mithilfe der [**BitBlt-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Übertragen einer Bitmap mithilfe der [**StretchDIBits-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Nach dem Abrufen eines Satzes von Werten setzt [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) die Anzahl und den Wert für jeden Vorgang zurück.

Die [**DrawDibTime-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) ist nur in der Debugversion der DrawDib-Funktionen verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von Bildern](image-rendering.md)
</dt> </dl>

 

 
