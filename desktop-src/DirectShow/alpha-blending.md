---
description: Alpha Blending
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Alpha Blending (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125209"
---
# <a name="alpha-blending-directshow"></a>Alpha Blending (DirectShow)

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Artikel wird die Alpha Mischung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) beschrieben.

Alpha misst die Transparenz eines Pixels oder Bilds. Bei einem nicht komprimierten RGB-Video mit 32-Bit definieren vier Komponenten die einzelnen Pixel: einen Alphakanal (A) und drei Farbkomponenten (RGB). Ein Pixel mit einem Alphawert von 0 (null) ist vollständig transparent. Ein Pixel mit einem Alphawert von 255 ist nicht transparent. Zwischen diesen Werten hat das Pixel verschiedene Transparenz Grade.

DirectShow definiert zwei Medientypen für 32-Bit-RGB-Video:

-   **Mediasubtype \_ ARGB32**: das Video ist 32-Bit-RGB mit einem gültigen Alphakanal.
-   **Mediasubtype \_ RGB32**: Pixel sind 32 Bits, aber der Alphakanal ist nicht unbedingt gültig.

Legen Sie zum Durchführen einer Alpha Mischung in des den unkomprimierten Medientyp der Videogruppe auf mediasubtype \_ ARGB32 fest. Aufrufen Sie in C++ die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode. Im XTL-Format wird dies auch durch Festlegen des [**Bittiefen**](bitdepth-attribute.md) Attributs des [**Group**](group-element.md) -Elements auf 32 erreicht.

Als nächstes benötigen Sie Videodaten, die einen Alphakanal enthalten. Es gibt mehrere Optionen:

-   Sie können eine AVI-Datei verwenden, die bereits über ein 32-Bit-RGB-Video mit Alpha Daten verfügt. Derzeit wird Alpha nicht für MPEG-oder Microsoft Windows Media Format-Quelldateien (WMF) unterstützt.
-   DES unterstützt 32-Bit-Bitmap-Dateien (BMP) und Targa-Dateien (. TGA) mit Alpha-Daten.
-   Sie können einen benutzerdefinierten Quell Filter schreiben, mit dem 32-Bit-RGB-Daten mit Alpha erstellt werden. Der Typ des Ausgabe Mediums muss **mediasubtype \_ ARGB32** sein. Verwenden Sie den Filter als untergeordnetes Objekt in einem Zeitachsen-Quell Objekt.

Wenn die Videoquelle nicht alpha ist, können Sie einen Effekt verwenden, mit dem Alpha Daten erstellt werden. Der [Alpha Setter-Effekt](alpha-setter-effect.md) legt den Alphakanal für das gesamte Bild auf einen konstanten Wert fest. Um das Alpha im zeitlichen Verlauf zu verändern, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle mit dem Alpha Setter-Effekt. Die ursprüngliche Quelle muss nicht 32 Bit betragen, solange der nicht komprimierte Medientyp der Gruppe **mediasubtype \_ ARGB32** ist.

Übergeben Sie schließlich das Video an einen Effekt oder Übergang, der Alpha Blending durchführt. Der [compositorübergang](compositor-transition.md) führt Alpha Blending aus, und der [Schlüssel Übergang](key-transition.md) kann durch einen Alpha-Wert Schlüsseln.

Im folgenden XTL-Beispiel Projekt wird Alpha Blending durchführt:


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



