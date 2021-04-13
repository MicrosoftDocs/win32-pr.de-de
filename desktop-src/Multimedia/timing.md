---
title: Zeitliche Steuerung (Windows Multimedia)
description: Zeitliche Steuerung
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- Drawdib, zeitliche Steuerung
- Drawdibtime-Funktion
- Drawdib, Debuggen
- Debuggen von drawdib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474862"
---
# <a name="timing-windows-multimedia"></a>Zeitliche Steuerung (Windows Multimedia)

Beim Debuggen einer Anwendung können Sie Informationen über die Zeit abrufen, die zum Durchführen von wiederkehrenden drawdib-Vorgängen erforderlich ist. Die [**drawdibtime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) -Funktion gibt Zeit Steuerungsinformationen für die folgenden Vorgänge zurück:

-   Zeichnen einer Bitmap
-   Das Komprimieren einer Bitmap wird deaktiviert.
-   Dithering einer Bitmap
-   Strecken einer Bitmap
-   Übertragen einer Bitmap mithilfe der [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion
-   Übertragen einer Bitmap mithilfe der [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) -Funktion

Nach dem Abrufen eines Satzes von Werten setzt [**drawdibtime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) die Anzahl und den Wert für jeden Vorgang zurück.

Die [**drawdibtime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) -Funktion ist nur in der Debugversion der drawdib-Funktionen verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bild Rendering](image-rendering.md)
</dt> </dl>

 

 
