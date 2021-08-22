---
title: Informationen zu DrawDib-Funktionen
description: Informationen zu DrawDib-Funktionen
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Video für Windows (VFW), DrawDib
- VFW (Video für Windows),DrawDib
- DrawDib, About
- DrawDib, Farbtabellen
- DrawDib, Übertragungsmodus
- DrawDib, Anzeigeadapter
- DrawDib, Bildstreckung
- DrawDib, komprimierte Bilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e03b41d5af776c39f7d100e9478bd408011d61d8e3d661cb80bd9ab52f08c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942088"
---
# <a name="about-the-drawdib-functions"></a>Informationen zu DrawDib-Funktionen

Zusammen ähneln die DrawDib-Funktionen der [**StretchDIBits-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) da sie Bildstreckungs- und Ditheringfunktionen bereitstellen. Die DrawDib-Funktionen unterstützen jedoch die Dekomprimierung von Bildern, das Datenstreaming und eine größere Anzahl von Anzeigeadaptern.

Unter bestimmten Umständen ist es vorteilhaft, die DrawDib-Funktionen zu verwenden. [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ist jedoch vielfältiger als die DrawDib-Funktionen und sollte verwendet werden, wenn die DrawDib-Funktionen nicht die gewünschte Funktionalität bereitstellen können. Die folgende Liste beschreibt Faktoren, die bei der Entscheidung berücksichtigt werden müssen, ob die DrawDib-Funktionen oder **StretchDIBits** verwendet werden sollen.

-   Farbtabelleninformationsformat. DrawDib-Funktionen zeigen Bilder an, die das **DIB \_ RGB \_ COLORS-Format** für ihre Farbtabelle verwenden. Wenn Bilder in Ihrer Anwendung Farbtabelleninformationen mit dem **DIB \_ PAL \_ COLORS-** oder **DIB \_ PAL \_ INDICES-Format** speichern, müssen Sie [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) verwenden, um sie anzuzeigen.
-   Übertragungsmodus. DrawDib-Funktionen erfordern, dass Ihre Anwendung den **SRCCOPY-Übertragungsmodus** verwendet. Wenn Ihre Anwendung [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) mit einem anderen Übertragungsmodus als **SRCCOPY** verwendet, sollten Sie **weiterhin StretchDIBits** verwenden. Wenn Sie andere Rastervorgänge in Ihrer Anwendung verwenden müssen, z. B. einen XOR, verwenden Sie **stretchDIBits.**
-   Qualität der Video- und Animationswiedergabe. Sie können die DrawDib-Funktionen für Datenstreaminganwendungen verwenden, z. B. für Anwendungen, die Videoclips und animierte Sequenzen wiedergeben. Die DrawDib-Funktionen bieten eine bessere Leistung als [**StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) da sie Bilder höherer Qualität bereitstellen und die Bewegung während der Wiedergabe verbessern.
-   Anzeigeadapter. DrawDib-Funktionen unterstützen eine größere Anzahl von Anzeigeadaptern als [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) unterstützt. Die DrawDib-Funktionen unterstützen VGA-Farbadapter, die 16-Farbpaletten mit 4-Bit-Bildtiefe bereitstellen, SVGA-Adapter, die 256-Farbpaletten mit 8-Bit-Bildtiefe bereitstellen, und echte Farbanzeigeadapter, die Tausende von Farben mit 16-Bit-, 24-Bit- und 32-Bit-Bildtiefe bereitstellen.

    Die DrawDib-Funktionen verbessern auch die Geschwindigkeit und Qualität der Anzeige von Bildern auf Anzeigeadaptern mit eingeschränkteren Funktionen. Wenn Sie z. B. einen 8-Bit-Anzeigeadapter verwenden, werden mit den DrawDib-Funktionen bilder in echten Farben effizient auf 256 Farben erweitert. Außerdem werden bei Verwendung von 4-Bit-Anzeigeadaptern 8-Bit-Bilder angezeigt.

-   Bildstreckung. Wie [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)verwenden die DrawDib-Funktionen Quell- und Zielrechtecke, um den Teil eines angezeigten Bilds zu steuern. Sie können unerwünschte Teile eines Bilds zuschneiden oder ein Bild strecken, indem Sie die Position und Größe der Quell- und Zielrechtecke variieren. Wenn ein Anzeigetreiber das Strecken von Bildern nicht unterstützt, bieten die DrawDib-Funktionen effizientere Stretchingfunktionen als **StretchDIBits.**
-   Komprimierte Bilder. Die DrawDib-Funktionen zeichnen jedes Format, für das Sie über einen Dekomprimierer verfügen, einschließlich RLE (Run-Length Encoding), Mobile und 411 YUV. Windows enthält RLE- und Mobile-Dekomprimierer, die optional installiert werden können.
-   Der Indeo-Codec wird in Windows nicht mehr unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 