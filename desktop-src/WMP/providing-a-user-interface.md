---
title: Bereitstellen eines Benutzeroberfläche
description: Bereitstellen eines Benutzeroberfläche
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Windows Media Player-Plug-Ins, Eigenschaftenseiten
- Plug-Ins, Eigenschaftenseiten
- Plug-Ins für die digitale Signalverarbeitung, Eigenschaftenseiten
- DSP-Plug-Ins, Eigenschaftenseiten
- Plug-Ins für die digitale Signalverarbeitung, Benutzeroberfläche
- DSP-Plug-Ins, Benutzeroberfläche
- Eigenschaftenseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb80525fa4b32845608eebb32752871a038aa6e01088baeebce5bc5f8c84b4bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746738"
---
# <a name="providing-a-user-interface"></a>Bereitstellen eines Benutzeroberfläche

DSP-Plug-Ins können eine Eigenschaftenseite bereitstellen, um eine Benutzeroberfläche zu erstellen. Dazu muss das Plug-In ein Eigenschaftenseitenobjekt enthalten, das eine Implementierung einer **IPropertyPage-Schnittstelle** bietet. Das DSP-Plug-In-Objekt muss **ISpecifyPropertyPages::GetPages** implementieren, wodurch Windows Media Player die richtige Eigenschaftenseite für das Plug-In suchen und identifizieren kann.

**Anzeigen einer Statusgrafik**

DSP-Plug-Ins können eine kleine Grafik oder eine Reihe von Grafiken im Windows Media Player-Statusbereich anzeigen, um den Benutzer zu benachrichtigen, dass ein Plug-In aktiv ist. Um dieses Feature zu unterstützen, muss das Plug-In die **IPropertyBag-Schnittstelle** implementieren. Windows Media Player ruft **IPropertyBag::Read** auf und stellt einen Zeiger auf den angeforderten Eigenschaftsnamen "IconStreams" zur Verfügung, bei dem die Kleinschreibung beachtet wird, und einen Zeiger auf eine **VARIANT-Struktur,** die die Daten für die Grafik empfängt. Das Plug-In erstellt ein **IStream-Objekt** (oder ein SAFEARRAY von **IStream-Objekten,** wenn mehrere Grafiken verfügbar sind), lädt dann die Grafikdaten, einschließlich Headerinformationen, in den Stream und gibt dann einen Zeiger auf das **IStream-Objekt** zurück, indem das **memberval-Member der** **VARIANT-Struktur verwendet** wird. Wenn das Plug-In nur eine Grafik liefert, wird der **vt-Member** der **VARIANT-Struktur** als VT \_ UNKNOWN angegeben. Wenn das Plug-In mehrere grafische **IStream-Objekte** mit safearray angibt, wird der **vt-Member** der **VARIANT-Struktur** als VT \_ ARRAY angegeben.

Grafiken können in einer Vielzahl von Dateiformaten gespeichert werden, darunter:

**Bmp**

Microsoft Windows Bitmapbilder werden nicht komprimiert.

**Jpeg**

Komprimiertes Bildformat, das häufig für Webseiten verwendet wird. JPEG-Formatdateien verfügen in der Regel .jpg Dateierweiterungen.

**Gif**

Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.

**Png**

Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.

Die maximalen Abmessungen für DSP-Plug-In-Grafiken sind 38 Pixel breit und 14 Pixel hoch.

Der **IStream-Bytestream,** der die Statusgrafik enthält, muss Headerinformationen enthalten. Ohne Headerinformationen kann Windows Media Player grafiktyp nicht richtig identifizieren und wird daher das Bild nicht laden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




