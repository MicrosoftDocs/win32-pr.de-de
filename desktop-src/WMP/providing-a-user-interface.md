---
title: Bereitstellen einer Benutzeroberfläche
description: Bereitstellen einer Benutzeroberfläche
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Windows Media Player-Plug-ins, Eigenschaften Seiten
- Plug-ins, Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Eigenschaften Seiten
- DSP-Plug-ins, Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Benutzeroberfläche
- DSP-Plug-ins, Benutzeroberfläche
- Eigenschaftenseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207167"
---
# <a name="providing-a-user-interface"></a>Bereitstellen einer Benutzeroberfläche

DSP-Plug-Ins können eine Eigenschaften Seite zum Erstellen einer Benutzeroberfläche bereitstellen. Zu diesem Zweck muss das Plug-in ein Eigenschaften Seiten Objekt enthalten, das eine Implementierung einer **IPropertyPage** -Schnittstelle bereitstellt. Das DSP-Plug-in-Objekt muss **ISpecifyPropertyPages:: GetPages** implementieren, das es Windows Media Player ermöglicht, die richtige Eigenschaften Seite für das Plug-in zu finden und zu identifizieren.

**Anzeigen einer Status Grafik**

DSP-Plug-Ins können im Bereich Windows-Media Player Status eine kleine Grafik oder eine Reihe von Grafiken anzeigen, um den Benutzer darüber zu benachrichtigen, dass ein Plug-in aktiv ist. Um diese Funktion zu unterstützen, muss das Plug-in die **IPropertyBag** -Schnittstelle implementieren. Windows Media Player ruft **IPropertyBag:: Read** auf und stellt einen Zeiger auf den angeforderten Eigenschaftsnamen "IconStreams" bereit, bei dem die Groß-/Kleinschreibung beachtet wird, und ein Zeiger auf eine **Variant** -Struktur, die die Daten für die Grafik empfängt. Das Plug-in erstellt ein **IStream** -Objekt (oder ein SafeArray von **IStream** -Objekten, wenn mehrere Grafiken vorhanden sind), lädt dann die Grafikdaten, einschließlich Header Informationen, in den Stream und gibt einen Zeiger auf das **IStream** -Objekt mit dem **punkVal** -Member der **Variant** -Struktur zurück. Wenn das Plug-in nur eine Grafik liefert, wird das **VT** -Element der **Variant** -Struktur als VT \_ Unknown angegeben. Wenn das Plug-in mehrere Grafik- **IStream** -Objekte mithilfe von SAFEARRAY bereitstellt, gibt es das **VT** -Element der **Variant** -Struktur als VT- \_ Array an.

Grafiken können in einer Vielzahl von Dateiformaten gespeichert werden, einschließlich:

**BMP**

Microsoft Windows-Bitmapbilder sind nicht komprimiert.

**JPEG**

Komprimiertes Bildformat, das häufig für Webseiten verwendet wird. JPEG-Format Dateien haben in der Regel JPG-Dateinamen Erweiterungen.

**GIF**

Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.

**PNG**

Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.

Die maximalen Dimensionen für die DSP-Plug-in-Grafiken sind 38 Pixel breit und 14 Pixel hoch.

Der **IStream** -Bytestream, der die Status Grafik enthält, muss Header Informationen enthalten. Ohne Header Informationen kann Windows Media Player den Typ der Grafik nicht ordnungsgemäß identifizieren und das Bild daher nicht laden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




