---
title: Bildrendering
description: Bildrendering
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, Bildrendering
- DrawDib, Zeichnen von DIBs
- DrawDibDraw-Funktion
- DrawDibGetBuffer-Funktion
- DrawDibUpdate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7be73fbe37a28ab44116d2fb2e68acb6a9a3a385603af23dca0e14aa2de4d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690750"
---
# <a name="image-rendering"></a>Bildrendering

Nachdem Sie [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) aufgerufen haben, um einen DrawDib-DC zu erstellen (siehe [DrawDib-Vorgänge),](drawdib-operations.md)können Sie ein DIB mithilfe der [**DrawDibDraw-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) auf den Bildschirm zeichnen. **DrawDibDraw** dithert True-Color-Bitmaps, wenn sie mit 8-Bit-Anzeigeadaptern angezeigt werden.

[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) unterstützt auch Videografiken transparent, wenn komprimierte Bitmaps angezeigt werden. Sie können mithilfe der [**DrawDibGetBuffer-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) auf den Puffer zugreifen, der das dekomprimierte Bild enthält. **DrawDibGetBuffer** gibt **NULL** zurück, wenn eine nicht komprimierte Bitmap gezeichnet wird. Sie sollten Ihre Anwendung für die Verarbeitung komprimierter und nicht komprimierter Bitmaps vorbereiten.

Sie können ein Bild oder einen Teil eines Bilds, das von Ihrer Anwendung angezeigt wird, mithilfe des [**DrawDibUpdate-Makros**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) aktualisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DrawDib-Funktionen](about-the-drawdib-functions.md)
</dt> </dl>

 

 




