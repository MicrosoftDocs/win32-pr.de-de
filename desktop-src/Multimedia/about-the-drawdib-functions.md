---
title: Informationen über die drawdib-Funktionen
description: Informationen über die drawdib-Funktionen
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Video für Windows (Vfw), drawdib
- VFW (Video für Windows), drawdib
- Drawdib, Info
- Drawdib, Farbtabellen
- Drawdib, Übertragungsmodus
- Drawdib, Anzeige Adapter
- Drawdib, Bild Streckung
- Drawdib, komprimierte Bilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f3e9ba822e16a7568775378b24f69bbca12de
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726305"
---
# <a name="about-the-drawdib-functions"></a>Informationen über die drawdib-Funktionen

Zusammen ähneln die drawdib-Funktionen der [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) -Funktion darin, dass Sie Bild-und Auszieh Funktionen bereitstellen. Die drawdib-Funktionen unterstützen jedoch Bild Dekomprimierung, Datenstreaming und eine größere Anzahl von Anzeige Adaptern.

In einigen Fällen ist es vorteilhaft, die drawdib-Funktionen zu verwenden. Dennoch ist [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) vielfältiger als die drawdib-Funktionen und sollte verwendet werden, wenn die drawdib-Funktionen nicht die gewünschte Funktionalität bereitstellen können. In der folgenden Liste werden Faktoren beschrieben, die bei der Entscheidung berücksichtigt werden sollten, ob die drawdib-Funktionen oder die **StretchDIBits** verwendet werden sollen

-   Format der Farbtabellen Informationen. Die drawdib-Funktionen zeigen Bilder an, die das **DIB- \_ RGB \_** -Farb Format für ihre Farbtabelle verwenden. Wenn Bilder in Ihrer Anwendung Farb Tabelleninformationen mit dem Format **DIB- \_ PAL \_ Farben** oder **DIB-PAL- \_ \_ Indizes** speichern, müssen Sie für die Anzeige von [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) verwendet werden.
-   Übertragungsmodus. Für drawdib-Funktionen muss Ihre Anwendung den **srccopy** -Übertragungsmodus verwenden. Wenn Ihre Anwendung [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) mit einem anderen Übertragungsmodus als **srccopy** verwendet, sollten Sie weiterhin **StretchDIBits** verwenden. Wenn Sie andere Raster Vorgänge in Ihrer Anwendung verwenden müssen, z. b. ein XOR, verwenden Sie auch **StretchDIBits**.
-   Qualität der Video-und Animations Wiedergabe. Sie können die drawdib-Funktionen für datenstreaminganwendungen verwenden, z. b. solche, die Videoclips und animierte Sequenzen abspielen. Die drawdib-Funktionen geben in der Ausführung von [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ein, dass Sie qualitativ hochwertige Bilder bereitstellen und Bewegung während der Wiedergabe verbessern.
-   Anzeigen von Adaptern. Die drawdib-Funktionen unterstützen eine größere Anzahl von Anzeige Adaptern als von [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) unterstützt werden. Die drawdib-Funktionen unterstützen VGA-Farb Adapter, die 16-farbige Paletten mit 4-Bit-Bildtiefe bereitstellen, SVGA-Adapter, die 256-farbige Paletten mit 8-Bit-Bildtiefe bereitstellen, und echte Farbanzeige Adapter, die Tausende von Farben mithilfe von 16-Bit-, 24-Bit-und 32-Bit-Bild tiefen bereitstellen.

    Die drawdib-Funktionen verbessern außerdem die Geschwindigkeit und Qualität der Anzeige von Bildern auf Anzeige Adaptern mit eingeschränkteren Funktionen. Wenn Sie z. b. einen 8-Bit-Anzeige Adapter verwenden, ist die drawdib-Funktion für die Echt Zeit Farbbilder effizient auf 256 Farben. Außerdem werden 8-Bit-Images bei Verwendung von 4-Bit-Anzeige Adaptern unterschieden.

-   Bild-Streckung. Wie bei [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)verwenden die drawdib-Funktionen Quell-und Ziel Rechtecke, um den Teil eines Bilds zu steuern, der angezeigt wird. Sie können unerwünschte Teile eines Bilds Zuschneiden oder ein Bildstrecken, indem Sie die Position und Größe der Quell-und Ziel Rechtecke verändern. Wenn ein Anzeigetreiber keine Bild Streckung unterstützt, bieten die drawdib-Funktionen effizientere streckungs Funktionen als **StretchDIBits**.
-   Komprimierte Bilder. Die drawdib-Funktionen zeichnen jedes Format, für das Sie einen Dekompressor haben, einschließlich der Codierung (Run-Length Encoding, RLE), Cinepak und 411 YUV. In Windows sind die-und-scrollpak-Dekompressoren enthalten, die optional installiert werden können.
-   Der Indeo-Codec wird in Windows nicht mehr unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Drawdib](drawdib.md)
</dt> </dl>

 

 