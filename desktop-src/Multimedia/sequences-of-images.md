---
title: Sequenzen von Bildern
description: Sequenzen von Bildern
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- Drawdib, Bildsequenzen
- Drawdib, Sequenz von Bitmaps
- Drawdibdraw-Funktion
- Drawdibbegin-Funktion
- Drawdibend-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337843"
---
# <a name="sequences-of-images"></a>Sequenzen von Bildern

Sie können eine Sequenz von Bitmaps mit denselben Dimensionen und Formaten anzeigen, indem Sie die [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktion mit der [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) -Funktion verwenden. **Drawdibbegin** erhöht die Effizienz von **drawdibdraw** , indem der drawdib-DC für das Zeichnen vorbereitet wird.

> [!Note]  
> Wenn die Anwendung [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)nicht verwendet, führt [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) Sie implizit vor dem Zeichnen aus. Wenn Ihre Anwendung **drawdibbegin** vor **drawdibdraw** verwendet, muss **drawdibdraw** die Funktion nicht verarbeiten und warten, bis der Vorgang beendet ist.

 

Die [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) -Funktion stellt [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) mit dem drawdib-DC, dem DC-handle, der Adresse der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur und den Quell-und Ziel Rechteck Abmessungen bereit. Wenn Sie eine Sequenz von Bitmaps anzeigen, überprüft **drawdibdraw** die Werte dieser Elemente für jedes Bild in der Sequenz. Wenn **drawdibdraw** Änderungen an einem dieser Elemente erkennt, wird **drawdibbegin** implizit aufgerufen, um die drawdib-DC-Einstellungen anzupassen.

Nachdem Sie [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)verwendet haben, können Sie die Bildsequenz mithilfe von [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) zeichnen und ein oder mehrere Flags entsprechend angeben. Geben Sie das **gleiche DDF \_ \_** -Flag an, solange das DC-Handle nicht geändert wurde. Geben Sie das gleiche DDF \_ \_ -Draw-Flag an, wenn die folgenden Parameter für **drawdibdraw** nicht geändert wurden: die Adresse der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur und die Quell-und Ziel Rechteck Abmessungen.

Sie können die Flags, die mit [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) festgelegt wurden, mithilfe der [**drawdibend**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) -Funktion aktualisieren, gefolgt von einem anderen **drawdibbegin**-aufrufungs Vorgang. Verwenden Sie dann **drawdibend** , um den drawdib-DC der aktuellen Flags und Einstellungen zu löschen. Der nachfolgende aufrufungsvorgang von **drawdibbegin** initialisiert den drawdib-DC mit den entsprechenden Flags und Einstellungen erneut. Alternativ können Sie die Flags für einen drawdib-DC mithilfe von **drawdibbegin** ohne **drawdibend** aktualisieren. Zu diesem Zweck müssen Sie mindestens eine der folgenden Einstellungen gleichzeitig mit den Flags ändern: der Adresse der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur oder der Quell-oder Ziel Rechteck Abmessungen.

Sie können die Effizienz von [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) für datenstreamingvorgänge erhöhen, die komprimierte Bilder verwenden, wie z. b. das Abspielen eines Videoclips mithilfe der Funktionen [**drawdibstart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) und [**drawdibend**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) . Die **drawdibstart** -Funktion bereitet den drawdib-DC auf den Empfang eines Datenstroms vor, indem er eine Nachricht an den Videokomprimierungs-Manager (VCM) sendet. Wenn das Streaming beendet wurde, sendet **drawdibend** eine Nachricht an VCM, um anzugeben, dass es Ressourcen freigeben kann, die für den datenstreamingvorgang reserviert wurden. Weitere Informationen zu VCM finden Sie im [Video Komprimierungs-Manager](video-compression-manager.md).

> [!Note]  
> Sie müssen die Breite und Höhe der Quell-und Ziel Rechtecke in der Anwendung angeben. Sie müssen jedoch nicht die Ursprünge der Rechtecke angeben. Die Anwendung kann die Ursprünge in [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) neu definieren, um unterschiedliche Teile des Bilds zu verwenden oder verschiedene Teile der Anzeige zu aktualisieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bild Rendering](image-rendering.md)
</dt> </dl>

 

 