---
description: Die CImageDisplay-Klasse ist eine Hilfsklasse für GDI-Videorenderer zum Verwalten des Anzeigeformats.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: CImageDisplay-Klasse (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 551650e7c8b6b0f830a84aee37bf671bbc300224c9e300a3f6f841ef503a504d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428944"
---
# <a name="cimagedisplay-class"></a>CImageDisplay-Klasse

![cimagedisplayclasshierarchy](images/wutil06.png)

Die `CImageDisplay` -Klasse ist eine Hilfsklasse für GDI-Videorenderer zum Verwalten des Anzeigeformats. Das -Objekt speichert eine [**VIDEOINFO-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) die den aktuellen Anzeigemodus beschreibt, der in der Konstruktormethode des Objekts initialisiert wird. Die **CheckMediaType-Methode** des Objekts überprüft, ob ein vorgeschlagener Medientyp effizient mithilfe von GDI gerendert werden kann.



| Geschützte Membervariablen                                       | Beschreibung                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ Display**](cimagedisplay-m-display.md)                    | **VIDEOINFO-Struktur,** die das aktuelle Anzeigeformat beschreibt.                     |
| Geschützte Methoden                                                | Beschreibung                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Überprüft die Farbmasken in einer **VIDEOINFO-Struktur.**                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Berechnet die Anzahl der Nullbits am Anfang eines angegebenen Bitfelds.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Gibt die Anzahl der Bits zurück, die in einem angegebenen Bitfeld auf 1 festgelegt sind.                          |
| Öffentliche Methoden                                                   | Beschreibung                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Überprüft eine [**BITMAPINFOHEADER-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Bestimmt, ob ein vorgeschlagener Medientyp mit dem Anzeigeformat kompatibel ist.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Überprüft die Paletteneinträge in einer **VIDEOINFO-Struktur.**                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Überprüft, ob ein **angegebenes VIDEOINFO-Format** mit dem Anzeigeformat kompatibel ist. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Konstruktormethode.                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | Ruft die Farbmasken für ein angegebenes **VIDEOINFO-Format** ab.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Ruft die Farbmasken für das aktuelle Anzeigeformat ab.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Ruft die Bittiefe des aktuellen Anzeigemodus ab.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Bestimmt, ob das aktuelle Anzeigeformat palettiert ist.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Aktualisiert das Videoformat des Objekts so, dass es mit der angegebenen Anzeige übereinstimmen kann.                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




