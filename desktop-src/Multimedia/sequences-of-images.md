---
title: Sequenzen von Bildern
description: Sequenzen von Bildern
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, Bildsequenzen
- DrawDib, Sequenz von Bitmaps
- DrawDibDraw-Funktion
- DrawDibBegin-Funktion
- DrawDibEnd-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac063cb2e9697b3b95045b95c9cc759a562197b56f10ff86a076ddcfa9a72cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688791"
---
# <a name="sequences-of-images"></a>Sequenzen von Bildern

Sie können eine Sequenz von Bitmaps mit den gleichen Dimensionen und Formaten anzeigen, indem Sie die [**DrawDibDraw-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) mit der [**DrawDibBegin-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) verwenden. **DrawDibBegin verbessert** die Effizienz von **DrawDibDraw,** indem der DrawDib-DC für das Zeichnen vorbereitet wird.

> [!Note]  
> Wenn Ihre Anwendung [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)nicht verwendet, führt [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) diese implizit vor dem Zeichnen aus. Wenn Ihre Anwendung **DrawDibBegin** vor **DrawDibDraw** verwendet, muss **DrawDibDraw** die Funktion nicht verarbeiten und warten, bis sie abgeschlossen ist.

 

Die [**DrawDibBegin-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) stellt [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) mit dem DrawDib-DC, dem DC-Handle, der Adresse der [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) sowie den Quell- und Zielrechteckdimensionen zur Auswahl. Wenn Sie eine Sequenz von Bitmaps anzeigen, überprüft **DrawDibDraw** die Werte dieser Elemente für jedes Bild in der Sequenz. Wenn **DrawDibDraw** Änderungen an einem dieser Elemente erkennt, ruft es **implizit DrawDibBegin** erneut auf, um die DrawDib DC-Einstellungen anzupassen.

Nach der [**Verwendung von DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)können Sie die Bildsequenz zeichnen, indem Sie [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) verwenden und ein oder mehrere Flags entsprechend angeben. Geben Sie das **DDF \_ SAME \_ HDC-Flag** an, solange sich das DC-Handle nicht geändert hat. Geben Sie das DDF SAME DRAW-Flag an, wenn sich die folgenden Parameter für DrawDibDraw nicht geändert haben: die Adresse der \_ \_  [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) und die Quell- und Zielrechteckdimensionen.

Sie können die mit [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) festgelegten Flags aktualisieren, indem Sie die [**DrawDibEnd-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) gefolgt von einem weiteren Aufruf von **DrawDibBegin verwenden.** Verwenden Sie **dann DrawDibEnd,** um den DrawDib-DC seiner aktuellen Flags und Einstellungen zu löschen. Beim nachfolgenden Aufruf **von DrawDibBegin** wird der DrawDib-DC mit den entsprechenden Flags und Einstellungen erneut initialisiert. Alternativ können Sie die Flags für einen DrawDib-DC aktualisieren, indem Sie **DrawDibBegin** ohne **DrawDibEnd verwenden.** Dazu müssen Sie mindestens eine der folgenden Einstellungen gleichzeitig mit den Flags ändern: die Adresse der [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) oder die Quell- oder Zielrechteckdimensionen.

Mithilfe der [**Funktionen DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) und [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) können Sie die Effizienz von [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) für Datenstreamingvorgänge erhöhen, die komprimierte Bilder verwenden, z. B. die Wiedergabe eines Videoclips. Die **DrawDibStart-Funktion** bereitet den DrawDib-DC auf den Empfang eines Datenstroms von Bildern vor, indem eine Nachricht an den Videokomprimierungs-Manager (VCM) gesendet wird. Wenn das Streaming beendet ist, **sendet DrawDibStop** eine Nachricht an den VCM, die angibt, dass ressourcen frei werden können, die dem Datenstreamingvorgang zugeordnet sind. Weitere Informationen zu VCM finden Sie unter [Video Compression Manager](video-compression-manager.md).

> [!Note]  
> Sie müssen die Breite und Höhe der Quell- und Zielrechtecke in Ihrer Anwendung angeben. Sie müssen jedoch nicht die Ursprünge der Rechtecke angeben. Ihre Anwendung kann die Ursprünge in [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) neu definieren, um verschiedene Teile des Bilds zu verwenden oder verschiedene Teile der Anzeige zu aktualisieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von Bildern](image-rendering.md)
</dt> </dl>

 

 