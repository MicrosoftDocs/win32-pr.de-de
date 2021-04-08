---
title: Bild Rendering
description: Bild Rendering
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- Drawdib, Bild Rendering
- Drawdib, Zeichnen von DIBs
- Drawdibdraw-Funktion
- Drawdibgetbuffer-Funktion
- Drawdibupdate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037532"
---
# <a name="image-rendering"></a>Bild Rendering

Nachdem Sie [**drawdibopen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) aufgerufen haben, um einen drawdib-DC zu erstellen (siehe [drawdib-Vorgänge](drawdib-operations.md)), können Sie mithilfe der [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktion ein DIB auf den Bildschirm ziehen. **Drawdibdraw** Dithers True-Color-Bitmaps, wenn Sie mit 8-Bit-Anzeige Adaptern angezeigt werden.

[**Drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) unterstützt auch Video-Kompressoren transparent, wenn komprimierte Bitmaps angezeigt werden. Mithilfe der [**drawdibgetbuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) -Funktion können Sie auf den Puffer zugreifen, der das entkomprimierte Image enthält. **Drawdibgetbuffer** gibt **null** zurück, wenn eine nicht komprimierte Bitmap gezeichnet wird. Sie sollten die Anwendung für die Verarbeitung von komprimierten und unkomprimierten Bitmaps vorbereiten.

Sie können ein Bild oder einen Teil eines Bilds aktualisieren, das von der Anwendung angezeigt wird, indem Sie das [**drawdibupdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) -Makro verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über die drawdib-Funktionen](about-the-drawdib-functions.md)
</dt> </dl>

 

 




