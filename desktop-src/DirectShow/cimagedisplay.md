---
description: Die cimagedisplay-Klasse ist eine Hilfsklasse für GDI-Videorenderer, um das Anzeige Format zu verwalten.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Cimagedisplay-Klasse (winutil. h)
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
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373965"
---
# <a name="cimagedisplay-class"></a>Cimagedisplay-Klasse

![cimagedisplayclasshierarchy](images/wutil06.png)

Die- `CImageDisplay` Klasse ist eine Hilfsklasse für GDI-Videorenderer, um das Anzeige Format zu verwalten. Das-Objekt speichert eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur, die den aktuellen Anzeigemodus beschreibt, der in der Konstruktormethode des-Objekts initialisiert wird. Die **checkmediatype** -Methode des Objekts überprüft, ob ein vorgeschlagene Medientyp mithilfe von GDI effizient gerendert werden kann.



| Geschützte Member-Variablen                                       | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m- \_ Anzeige**](cimagedisplay-m-display.md)                    | **Videoinfo** -Struktur, die das aktuelle Anzeige Format beschreibt.                     |
| Geschützte Methoden                                                | BESCHREIBUNG                                                                            |
| [**Checkbitfields**](cimagedisplay-checkbitfields.md)           | Überprüft die Farb Masken in einer **videoinfo** -Struktur.                                |
| [**"Count prefixbits"**](cimagedisplay-countprefixbits.md)         | Berechnet die Anzahl der Bits (0) am Anfang eines angegebenen Bitfelds.              |
| [**Count-setbits**](cimagedisplay-countsetbits.md)               | Gibt die Anzahl der Bits zurück, die in einem angegebenen Bitfeld auf 1 festgelegt sind.                          |
| Öffentliche Methoden                                                   | BESCHREIBUNG                                                                            |
| [**Checkheadergültigkeit**](cimagedisplay-checkheadervalidity.md) | Überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.                    |
| [**Checkmediatype**](cimagedisplay-checkmediatype.md)           | Bestimmt, ob ein vorgeschlagene Medientyp mit dem Anzeige Format kompatibel ist.        |
| [**Checkpaletteheader**](cimagedisplay-checkpaletteheader.md)   | Überprüft die Paletteneinträge in einer **videoinfo** -Struktur.                            |
| [**Checkvideotype**](cimagedisplay-checkvideotype.md)           | Überprüft, ob ein angegebenes **videoinfo** -Format mit dem Anzeige Format kompatibel ist. |
| [**Cimagedisplay**](cimagedisplay-cimagedisplay.md)             | Konstruktormethode.                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | Ruft die Farb Masken für ein angegebenes **videoinfo** -Format ab.                        |
| [**GetColorMask**](cimagedisplay-getcolourmask.md)             | Ruft die Farb Masken für das aktuelle Anzeige Format ab.                              |
| [**Getdisplaytiefe**](cimagedisplay-getdisplaydepth.md)         | Ruft die Bittiefe des aktuellen Anzeigemodus ab.                                   |
| [**Getdisplayformat**](cimagedisplay-getdisplayformat.md)       | Ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.                      |
| [**Ispalettisiert**](cimagedisplay-ispalettised.md)               | Gibt an, ob das aktuelle Anzeige Format palettisiert ist.                           |
| [**Erfrischendes Display Type**](cimagedisplay-refreshdisplaytype.md)   | Aktualisiert das Videoformat des Objekts entsprechend der angegebenen Anzeige.                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




